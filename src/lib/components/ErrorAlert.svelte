<!--
@component

The `ErrorAlert.svelte` component displays when an error has been detected. It
is displayed in the form of a (optionally) dismissable alert within the greater
structure of the page layout. The errors are caught and handled in
`/src/routes/+layout.svelte`.

 -->

<script>
	import { XCircleIcon } from 'svelte-feather-icons';

	import { errorMessage } from '$lib/stores/alertsStore';

	export let dismissable = true;
</script>

{#if $errorMessage}
	<div class="alert alert-error dark:prose-invert">
		<XCircleIcon />
		<span>Error: {$errorMessage}</span>
		{#if dismissable}
			<button class="btn-neutral btn-sm" on:click={() => errorMessage.set('')}>Dismiss</button>
		{/if}
	</div>
{/if}
