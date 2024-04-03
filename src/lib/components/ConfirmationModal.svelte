<!---
 @component
 
 The `ConfirmationModal.svelte` component implements a reusable "popup dialog"
 that will prompt the user tp enter their chosen 6-digit pincode to confirm their
 intent for a particular action to take place. This confirmation flow takes place on the following occasions:
 
  1. On signup, when the user has entered their desired pincode (and **before** the keypair is encrypted with the pincode), 
    we ask them to confirm the same pincode to make sure they know what they entered the first time.

  2. Before any Stellar transaction (payment, changeTrust, etc.) is signed and submitted to the network, we propmt for this 
    pincode, which will allow the app to decrypt the keypair in order to sign the transaction.

  3. When authenticating with an anchor server, the SEP-10 challenge transaction is shown to the user
     in this modal for them to approve and sign, before it is sent back to the authenticaion server.
-->

<script>
	import { copy } from 'svelte-copy';
	import { CopyIcon } from 'svelte-feather-icons';
	import {} from '$lib/stores/alertsStore';
	import ErrorAlert from './ErrorAlert.svelte';
</script>

<div class="prose p-3">
	<!-- <h1>{title}</h1>
	<p>{body}</p> -->
</div>
