<script>
    import Link from "$lib/Link.svelte";
    import { base } from '$app/paths';

    let projects = [
	    {
		    "name": "launcher-cli",
		    "href": "https://github.com/garfxld/launcher-cli",
		    "description": "No description, website, or topics provided."
	    },
	    {
		    "name": "website",
		    "href": "https://github.com/garfxld/website",
		    "description": "My personal website"
	    },
	    {
		    "name": "rpx (Archived)",
		    "href": "https://github.com/garfxld/rpx",
		    "description": "A resource pack manager for Minecraft: Java Edition"
	    },
    ]
</script>

<head>
    <title>Garfxld's Website</title>
</head>

<div id="content" class="w-screen h-screen flex justify-center dark:bg-neutral-950">
    <div class="w-full max-w-6xl h-full px-10 pt-24 font-mono dark:text-white">
        <div class="flex items-center gap-2">
            <img src="{base}/profile.png" alt="Garfxld" class="size-9 rounded-full" />
            <h1 class="text-4xl">Garfxld</h1>
        </div>

        <div class="flex gap-2 mt-2">
            <Link name="Github" href="https://github.com/garfxld" />
            <Link name="Discord" href="https://discord.com/users/743060709465784409" />
            <Link name="Spotify" href="https://open.spotify.com/user/9z6vambozryoo2jskc8d0l8ip" />
        </div>

        <h2 class="text-lg mt-16">Projects / Work</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-2 mt-2">
            {#each projects as { name, href, description }}
                <a target="_blank" rel="noopener noreferrer" href={href} class="block p-2 border rounded-sm border-neutral-500 hover:border-neutral-200 cursor-pointer select-none group">
                    <div class="flex items-center gap-1">
                        <p class="font-bold">{name}</p>
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 invisible group-hover:visible text-neutral-300" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                            <path stroke="none" d="M0 0h24v24H0z"></path>
                            <line x1="17" y1="7" x2="7" y2="17"></line>
                            <polyline points="8 7 17 7 17 16"></polyline>
                        </svg>
                    </div>
                    <p class="text-sm italic text-neutral-300">{description}</p>
                </a>
            {/each}
        </div>
    </div>
</div>
