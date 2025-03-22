<script>
    let { name, href } = $props();
</script>

<a target="_blank" rel="noopener noreferrer" href={href} class="text-center [word-spacing:-6px] text-sky-500 hover:bg-sky-500 hover:text-white text-nowrap">
    [ {name} ]
</a>