<script lang="ts">
    export let state : string

</script>

<header>
    <h1 class="text-2xl NeueMontreal-Light">Luca ORELLI</h1>
    <p class="NeueMontreal-Regular">Full-Stack Developer</p>
        <ul class="mt-10 space-y-4 ">
            <li>
                {#if state === 'home'}
                <p>
                    ●
                </p>
                {:else}
                <a class="hover:text-gray-500 transition-colors cursor-pointer" href="/">
                    Home
                </a>
                {/if}
            </li>
            <li>
            {#if state === 'projects'}
            <p>
                ●
            </p>
            {:else}
            <a class="hover:text-gray-500 transition-colors cursor-pointer" href="/projects">
                Projects
            </a>
            {/if}
            </li>
            <li>
            {#if state === 'infos'}
                <p>
                    ●
                </p>
            {:else}
                <a class="hover:text-gray-500 transition-colors cursor-pointer" href="/infos">
                    Infos
                </a>
            {/if}
            </li>
            <li>
            {#if state === 'contact'}
                <p>
                    ●
                </p>
            {:else}
            <a class="hover:text-gray-500 transition-colors cursor-pointer" href="/contact">
                Contact
            </a>
            {/if}
            </li>
        </ul>
</header>