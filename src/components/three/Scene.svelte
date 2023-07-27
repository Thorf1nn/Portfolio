<script lang="ts">
    import { onMount, onDestroy } from 'svelte';
    import { browser } from '$app/environment';
    import * as THREE from 'three';

    if (browser) {
      let cam, scene, renderer, clock, smokeMaterial;
      let w, h;
      let smokeParticles = [];

      const animate = () => {
        let delta = clock.getDelta();

        requestAnimationFrame(animate);

        smokeParticles.forEach(sp => {
          sp.rotation.z += delta * 0.2;
        });

        renderer.render(scene, cam);
      };

      const resize = () => {
        w = window.innerWidth;
        h = window.innerHeight;
        renderer.setSize(w, h);
      };

      const lights = () => {
        const light = new THREE.DirectionalLight(0xffffff, 0.5);

        clock = new THREE.Clock();

        renderer = new THREE.WebGLRenderer();
        renderer.setClearColor(0xffffff, 1);
        renderer.setSize(w, h);

        scene = new THREE.Scene();

        light.position.set(-1, 0, 1);
        scene.add(light);
      };

      const camera = () => {
        cam = new THREE.PerspectiveCamera(75, w / h, 1, 10000);

        cam.position.z = 1000;

        scene.add(cam);
      };

      const action = () => {
        const loader = new THREE.TextureLoader();

        loader.crossOrigin = '';

        loader.load(
          '/assets/pink-smoke.png',
          function onLoad(texture) {
            const smokeGeo = new THREE.PlaneGeometry(300, 300);

            smokeMaterial = new THREE.MeshLambertMaterial({
              map: texture,
              transparent: true
            });

            for (let p = 0, l = 350; p < l; p++) {
              let particle = new THREE.Mesh(smokeGeo, smokeMaterial);

              particle.position.set(
                Math.random() * 500 - 250,
                Math.random() * 500 - 250,
                Math.random() * 1000 - 100
              );

              particle.rotation.z = Math.random() * 360;
              scene.add(particle);
              smokeParticles.push(particle);
            }

            animate();
          }
        );
      };

      const onWindowResize = () => {
        w = window.innerWidth;
        h = window.innerHeight;
        cam.aspect = w / h;
        cam.updateProjectionMatrix();
        renderer.setSize(w, h);
      };

      const mediaQuery = window.matchMedia('(max-width: 768px)');


      const init = () => {
        w = window.innerWidth;
        h = window.innerHeight;

        lights(); //💡
        camera(); // 🎥
        action(); // 🎬

        // Wrap the renderer.domElement in a container div
        const container = document.createElement('div');
        container.style.position = 'fixed'; // Set position to fixed
        container.style.top = '0';
        container.style.left = '0';
        container.style.backgroundSize = 'cover'; // Set background-size to cover
        container.style.backgroundRepeat = 'no-repeat'; // Set background-repeat to no-repeat
        container.style.backgroundPosition = 'center'; // Set background-position to center
        container.style.zIndex = '-2';
        container.appendChild(renderer.domElement);
        document.body.appendChild(container);

        window.addEventListener('resize', resize);
      };

      onMount(() => {
        init();
      });

      onDestroy(() => {
        window.removeEventListener('resize', resize);
      });
    }
  </script>
