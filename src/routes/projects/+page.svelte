<script lang="ts">

    import Header from "../../components/Header.svelte";
    import Projects from "../../components/Projects.svelte";

    interface Project {
        link : string,
        title: string,
        date : string
    }

    const projects: { [key: string]: Project } = {
        valodle: {
            link: "https://valodle.eu/",
            title: "VALODLE",
            date: "2023 / Personal / Game",
        },
        elsys: {
            link: "https://el-sys.fr/#home",
            title: "ELSYS SOLUTIONS",
            date: "2022 / Internship / Showcase",
        },
    };

    const softwareProjects: { [key: string]: Project } = {
        arcade: {
            link: "https://github.com/Thorf1nn/Arcade-Epitech",
            title: "ARCADE",
            date: "2023 / School / Game Software",
        },
        raytracer: {
            link: "https://github.com/Thorf1nn/Raytracer-Epitech",
            title: "RAYTRACER",
            date: "2023 / School / Software",
        },
        zappy: {
            link: "https://github.com/Thorf1nn/Zappy-Epitech",
            title: "ZAPPY",
            date: "2023 / School / AI Game Software",
        },
    };

</script>

<style>
    .hidden-scrollbar::-webkit-scrollbar {
        display: none;
    }
</style>

<section>
    <div class="flex justify-center items-center h-screen">
        <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
            <Header state="projects"/>
            <div class="hidden-scrollbar text-xl absolute overflow-y-auto h-[30%] lg:h-[35%] mt-10 md:mt-0 md:right-20 lg:right-40 fadeInOutAnimation lg:text-3xl">
                <h2 class="NeueMontreal-Regular mb-4">&dArr; Front end projects</h2>
                <div class="flex flex-col space-y-4">
                    {#each Object.keys(projects) as projectKey}
                        <Projects
                        link={projects[projectKey].link}
                        projectTitle={projects[projectKey].title}
                        projectInformations={projects[projectKey].date}
                    />
                    {/each}
                </div>
                <h2 class="NeueMontreal-Regular my-8">&dArr; Software projects</h2>
                <div class="flex flex-col space-y-4">
                    {#each Object.keys(softwareProjects) as projectKey}
                        <Projects
                        link={softwareProjects[projectKey].link}
                        projectTitle={softwareProjects[projectKey].title}
                        projectInformations={softwareProjects[projectKey].date}
                    />
                    {/each}
                </div>
            </div>
        </div>
      </div>
</section>