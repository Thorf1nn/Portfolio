<script lang="ts">

    import Header from "../../components/Header.svelte";
    import Projects from "../../components/Projects.svelte";
</script>

<section>
    <div class="flex justify-center items-center h-screen z-0">
        <div class="border-2 border-black w-[90%] h-[90%] p-4 m-4">
            <Header state="projects"/>
            <div class="absolute mt-10 md:mt-0 md:right-20 lg:right-40 fadeInOutAnimation">
                <h2 class="NeueMontreal-Regular mb-4">&dArr; Front end projects</h2>
                <div class="flex flex-col space-y-4">
                    <Projects link={"https://valodle.eu/"} projectTitle={"VALODLE"} projectInformations={"2023 / Personnal / Game"}/>
                    <Projects link={"https://el-sys.fr/#home"}  projectTitle={"ELSYS SOLUTIONS"}  projectInformations={"2022 / Internship / Showcase"}/>
                </div>
                <h2 class="NeueMontreal-Regular my-4">&dArr; Software projects</h2>
                <Projects link={"https://github.com/Thorf1nn/42sh"} projectTitle={"42SH"} projectInformations={"2022 / School / Software"}/>
            </div>
        </div>
      </div>
</section>