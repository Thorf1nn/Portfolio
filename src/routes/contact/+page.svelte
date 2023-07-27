<script>
    import Header from "../../components/Header.svelte";
    import ContactButton from "../../components/ContactButton.svelte";
</script>

<div class="flex justify-center items-center h-screen">
    <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
        <Header state="contact"/>
        <div class="md:flex md:justify-center items-center">
            <div class="flex flex-col space-y-4 fadeInOutAnimation mt-10">
                <p class="text-2xl md:text-3xl lg:text-5xl NeueMontreal-Regular">Want to discuss for a new project?</p>
                <p class="text-xl md:text-2xl lg:text-3xl NeueMontreal-Light">I'm available for freelance work</p>
                <ContactButton></ContactButton>
            </div>
       </div>
    </div>
</div>
