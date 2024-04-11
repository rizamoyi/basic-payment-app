<!--
@component

The `TransferHistory` component will display a listing of details concerning any
transfers the user has initiated with an anchor.
-->

<script>
	import { page } from '$app/stores';
	import { transfers } from '$lib/stores/transfersStore';
	import { webAuthStore } from '$lib/stores/webAuthStore';

	import { queryTransfers24 } from '$lib/stellar/sep24';
	import { queryTransfers6 } from '$lib/stellar/sep6';

	let expiredToken = false;
	const protocolBadgeClasses = {
		sep6: 'badge badge-secondary',
		sep24: 'badge badge-accent'
	};
</script>
