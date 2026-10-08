<script>
    import Apple from "../components/Apple.svelte";
    import {iq} from '#lib/app.store.ts';
    import Github from "#lib/assets/github_logo.svg"
</script>

<div class="flex flex-col items-center justify-center size-full">
    <div class="flex items-center justify-center size-150">
        <Apple/>
    </div>
    <p class="text-white text-2xl" style="font-family: Consolas">IQ: {$iq}</p>
</div>
<a class="fixed bottom-5 left-5 text-white flex items-center justify-center gap-2 select-none"
   href="https://github.com/XenonPPG/AppleIQ">
    <img class="size-5" src={Github}/>
    Github
</a>