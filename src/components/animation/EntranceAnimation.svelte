<style>
    .animation-container {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 9999;
        animation: animate-fade 1.2s 1.2s forwards;
        background: #000;
    }

    @keyframes animate-fade {
        0% {
            opacity: 1;
        }
        100% {
            opacity: 0;
            pointer-events: none;
        }
    }
</style>

<div class="animation-container">
    <div class="flex justify-center items-center h-full w-full space-x-2">
        <h1 class="text-white NeueMontreal-Regular text-2xl fadeOutInAnimation">Luca ORELLI</h1>
        <p class="text-white NeueMontreal-Light text-xl fadeOutInAnimation2">Portfolio</p>
    </div>
</div>
