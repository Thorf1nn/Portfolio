<script>
	import { Canvas, InteractiveObject, OrbitControls, T } from '@threlte/core'
	import { spring } from 'svelte/motion'
	import { degToRad } from 'three/src/math/MathUtils'
    import { Fog } from '@threlte/core'


	const scale = spring(0.5)
</script>

<div class="cube absolute">
    <Canvas>
        <Fog color={'#2958B2'} />

		<T.DirectionalLight castShadow position={[2, 20, 10]} />
		<T.DirectionalLight position={[-3, 10, -10]} intensity={0.2} />
		<T.AmbientLight intensity={0.2} />

		<!-- Cube -->
		<T.Group scale={$scale}>
			<T.Mesh position.y={0.5} castShadow let:ref>
				<!-- Add interaction -->
				<InteractiveObject
					object={ref}
					interactive
					on:pointerenter={() => ($scale = 2)}
					on:pointerleave={() => ($scale = 1)}
				/>

				<T.BoxGeometry />
				<T.MeshStandardMaterial color={'#333333'} />
			</T.Mesh>
		</T.Group>

		<!-- Floor -->
		<T.Mesh receiveShadow rotation.x={degToRad(-90)}>
			<T.CircleGeometry args={[1, 72]} />
			<T.MeshStandardMaterial color={"white"} />
		</T.Mesh>
	</Canvas>
</div>

<style>
	.cube {
		height: 100%;
		width: 100%;
	}
</style>