<script>
    import AppleGif from '#lib/assets/apple.gif';
    import Apple from "./Apple.svelte";
    import {iq} from '#lib/app.store.ts';

    let open = $state(false)

    function OnClick() {
        open = true;
        iq.set($iq + 3);
    }
</script>

<div class={{ 'size-full items-center justify-center':true, 'grid grid-cols-2':open, 'flex':!open }}>
    {#if !open}
        <img on:click={OnClick} src="{AppleGif}" class="select-none" draggable="false">
    {:else}
        {#each {length: 4}}
            <Apple/>
        {/each}
    {/if}
</div>