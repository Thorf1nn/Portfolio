<script lang="ts">
	import { stringify } from "postcss";


    import Header from "../../components/Header.svelte";
    import Link from "../../components/Links/Link.svelte";
    import Resume from "../../components/Links/Resume.svelte";

    interface PlatformLink {
        [platform: string]: string;
    }

    const links: PlatformLink = {
        Github: "https://github.com/Thorf1nn?tab=repositories",
        Malt: "https://www.linkedin.com/in/luca-orelli-410b8a231/",
        ComeUp: "https://example.comup.com",
        Fiverr: "https://www.fiverr.com/your_username",
        Linkedin: "https://www.linkedin.com/in/your_username",
    };

    interface LangageResume {
        [langage: string]: string;
    }

    const resumes : LangageResume = {
        English : "/resumes/english_resume.pdf",
        French : "/resumes/french_resume.pdf"
    }

</script>

<section>
    <div class="flex justify-center items-center h-screen">
        <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
            <Header state="infos"/>
            <div class="absolute text-xs bottom-20 fadeInOutAnimation lg:text-xl lg:right-40">
                <ul class="flex flex-col space-y-2">
                    {#each Object.keys(links) as platform}
                        <Link link={links[platform]} platform={platform}/>
                    {/each}
                </ul>
                <ul class="mt-8">
                  {#each Object.keys(resumes) as langageResume}
                    <Resume resumelink={resumes[langageResume]} langage={langageResume}/>
                  {/each}
                </ul>
            </div>
        </div>
      </div>
</section>