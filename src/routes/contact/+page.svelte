<script>
    import Header from "../../components/Header.svelte";
    import ContactButton from "../../components/ContactButton.svelte";
</script>

<div class="flex justify-center items-center h-screen">
    <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
        <Header state="contact"/>
        <div class="lg:flex lg:justify-center items-center">
            <div class="flex flex-col ">
                <p>Want to discuss a new project?</p>
                <p>I'm available for freelance work</p>
            </div>
            <ContactButton></ContactButton>
       </div>
    </div>
</div>