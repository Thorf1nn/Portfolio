<script lang="ts">
    export let resumelink : string
    export let langage : string
</script>

<li class="hover:text-gray-400 transition-colors cursor-pointer">
    <a class="font-bold" href={resumelink} target="_blank">{langage} resume</a>
</li>

