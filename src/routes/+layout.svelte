<script>
	import '../app.postcss';

	// We will use a `writable` Svelte store to trigger our modal
	import { writable } from 'svelte/store';

	// We have a custom close button for consistent styling, but this is NOT a requirement.
	import ModalCloseButton from '$lib/components/ModalCloseButton.svelte';

	import Modal from 'svelte-simple-modal';

	const modal = writable(null);

	// @ts-ignore
	// const handleError = (err) => {
	// 	if (err.message !== 'ResizeObserver loop limit exceeded') {
	// 		console.log('here is the handleError err', err);
	// 		errorMessage.set(err.error.body.message);
	// 	}
	// };
</script>

<Modal show={$modal} closeButton={ModalCloseButton} classContent="rounded bg-base-100"
	><slot /></Modal
>
