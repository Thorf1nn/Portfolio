
<script lang="ts">

    export let link : string
    export let projectTitle : string
    export let projectInformations : string

</script>

<a href={link} target="_blank">
    <div class="flex flex-col space-between">
        <div class="hover:text-gray-400 transition-colors cursor-pointer">
            <h1 class="NeueMontreal-Light text-2xl lg:text-4xl">{projectTitle}</h1>
            <span class="font-bold">{projectInformations}</span>
        </div>
    </div>
</a>