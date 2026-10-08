<script lang="ts">
    import './layout.css';
    import favicon from '#lib/assets/favicon.svg';
    import type {LayoutProps} from './$types';
    import {iq} from '#lib/app.store.ts';

    let {children}: LayoutProps = $props();
</script>

<svelte:head>
    <title>IQ: {$iq}</title>
    <link href={favicon} rel="icon"/>
</svelte:head>

{@render children()}
