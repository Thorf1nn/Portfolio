<script>
    import "../layout/app.css";
    import "../layout/animation.css";
    import "../layout/fonts.css"

    import Cloud from "../components/three/Cloud.svelte";
    import EntranceAnimation from "../components/animation/EntranceAnimation.svelte";
</script>

<EntranceAnimation />

<Cloud/>

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


<slot />