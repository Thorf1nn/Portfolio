<script lang="ts">

    import Header from "../../components/Header.svelte";

</script>

<section>
    <div class="flex justify-center items-center h-screen">
        <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
            <Header state="contact"/>
            <div class="lg:flex lg:justify-center items-center">
                <form class="flex flex-col mt-10 w-full max-w-sm fadeInOutAnimation" action="?/writemessage" method="POST">
                    <h2 class="NeueMontreal-Regular mb-4">&dArr; Contact me</h2>
                    <label class="space-y-4">
                        <input class="outline-0	border border-black bg-transparent w-full p-2 placeholder:text-black" name="name" type="name" placeholder="Enter your name">
                        <input class="outline-0	border border-black bg-transparent w-full p-2 placeholder:text-black" name="email" type="email" placeholder="Enter your email">
                        <textarea class="outline-0	border border-black bg-transparent w-full p-2 resize-none h-[200px] placeholder:text-black" name="message" placeholder="Enter message"></textarea>
                        <button class="text-black py-2 rounded hover:text-gray-400 transition-colors cursor-pointer">
                            <input type="submit" value="Submit" class="cursor-pointer">
                            &UpperRightArrow;
                        </button>
                    </label>
                </form>
            </div>
        </div>
      </div>
</section>