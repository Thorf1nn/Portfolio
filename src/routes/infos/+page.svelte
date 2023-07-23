<script lang="ts">

    import Header from "../../components/Header.svelte";
</script>

<section>
    <div class="flex justify-center items-center h-screen">
        <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
            <Header state="infos"/>
            <div class="absolute text-xs bottom-20 fadeInOutAnimation lg:text-xl lg:right-40">
                <ul class="flex flex-col space-y-2">
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a href="https://github.com/Thorf1nn?tab=repositories" target="_blank">Github &UpperRightArrow;</a>
                    </li>
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a href="https://www.linkedin.com/in/luca-orelli-410b8a231/" target="_blank">Linkedin &UpperRightArrow;</a>
                    </li>
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a href="https://www.malt.fr/profile/lucaorelli" target="_blank">Malte &UpperRightArrow;</a>
                    </li>
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a href="https://comeup.com/en/@lucode" target="_blank">ComeUp &UpperRightArrow;</a>
                    </li>
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a href="https://fr.fiverr.com/thorf1nn?up_rollout=true" target="_blank">Fiverr &UpperRightArrow;</a>
                    </li>
                </ul>
                <ul class="mt-8">
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a class="font-bold" href="/resumes/english_resume.pdf" target="_blank">English resume</a>
                    </li>
                    <li class="hover:text-gray-400 transition-colors cursor-pointer">
                        <a class="font-bold" href="/resumes/french_resume.pdf" target="_blank">French resume</a>
                    </li>
                </ul>
            </div>
        </div>
      </div>
</section>