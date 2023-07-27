<script>
    import "../layout/app.css";
    import "../layout/animation.css";
    import "../layout/fonts.css"

    import Scene from "../components/three/Scene.svelte";


    import EntranceAnimation from "../components/animation/EntranceAnimation.svelte";
</script>

<EntranceAnimation />
<Scene/>

<style>
    .is-visible {
        animation-duration: 1s;
        animation-name: is-visible;
        animation-delay: 1s;
        animation-fill-mode: backwards;
    }

    @keyframes is-visible {
        0% { visibility: hidden; }
        100% { visibility: visible; }
    }
</style>

<svelte:head>
	<title>Luca Orelli - Portfolio</title>
</svelte:head>

<slot />