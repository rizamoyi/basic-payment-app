<script>
	/**
	 * Below, we are importing a few different Svelte components that will be
	 * placed into the page. This makes keeping our codebase organized a bit
	 * easier.
	 */

	// `AssetStats` will display an overview of the users's account balances
	// import AssetStats from './components/AssetStats.svelte';
	// `RecentPayments` will show a brief history of payments to/from the user
	// import RecentPayments from './components/RecentPayments.svelte';
	// `FavoriteContacts` will display all favorited contacts
	import FavoriteContacts from './components/FavouriteContacts.svelte';
	// `TransferHistory` will display anchor transfer status information
	// import TransferHistory from './components/TransferHistory.svelte';
</script>

<!-- <AssetStats /> -->

<!-- `RecentPayments` and `FavoriteContacts` displayed as two columns on larger screens -->
<div class="grid grid-cols-1 gap-10 lg:grid-cols-2">
	<div class="overflow-x-auto">
		<!-- <RecentPayments /> -->
	</div>
	<div class="overflow-x-auto">
		<FavoriteContacts />
	</div>
</div>

<!-- `TransferHistory` displayed at the bottom of the dashboard -->
<div class="overflow-x-auto">
	<!-- <TransferHistory /> -->
</div>
