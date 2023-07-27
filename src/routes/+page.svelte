<script lang="ts">
	import Header from "../components/Header.svelte";
</script>

<main>
    <div class="flex justify-center items-center h-screen">
        <div class="relative border-2 border-black w-[90%] h-[90%] p-4 m-4">
            <Header state="home"/>
            <div class="absolute bottom-10 right-10 fadeInOutAnimation">
                <p class="flex flex-col space-between justify-center lg:text-2xl">
                    <span>Full-Stack developer</span>
                    <span>specialized</span>
                    <span>in Svelte, React,</span>
                    <span>NodeJS, Express</span>
                    <span>With my strong</span>
                    <span>background in</span>
                    <span>web development,</span>
                    <span>I create beautiful and</span>
                    <span>functional</span>
                    <span>applications</span>
                </p>
            </div>
        </div>
    </div>
</main>
