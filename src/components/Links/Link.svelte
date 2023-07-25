
<script lang="ts">
    export let link : string
    export let platform : string
</script>

<li class="hover:text-gray-400 transition-colors cursor-pointer">
    <a href={link} target="_blank">{platform} &UpperRightArrow;</a>
</li>