<script lang="ts">
    import '../app.css';
    import favicon from '$lib/assets/favicon.svg';
    import {AppBar} from '@skeletonlabs/skeleton-svelte';
	import {ListCheck, Presentation, User} from "lucide-svelte";

    let {children} = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon}/>
</svelte:head>

<AppBar>
    <div class="flex justify-center">
        <a type="button" class="btn preset-gradient-one mx-4" href="/presentation">
            <span>Who am I ?</span>
            <User size={18}/>
        </a>
        <button type="button" class="btn preset-gradient-one mx-4">
            <span>My skills</span>
            <ListCheck size={18}/>
        </button>
		<button type="button" class="btn preset-gradient-one mx-4">
			<span>My projects</span>
			<Presentation size={18}/>
		</button>
    </div>
</AppBar>

{@render children?.()}
