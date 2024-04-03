<script>
	// Import svelte components
	import TruncatedKey from '$lib/components/TruncatedKey.svelte';
</script>

<div class="hero min-h-screen bg-base-200">
	<div class="hero-content flex-col gap-7 lg:flex-row-reverse">
		<div class="text-center lg:text-left">
			<h1 class="text-5xl font-bold">Sign Up</h1>
			<p class="py-6">
				Please provide a 6-digit pincode to sign up. This pincode will be used to encrypt the secret
				key for your stellat address, before it it stored in your browser's local storage. Your
				secret key to this address willbe stored on your device. You willbe the only one to ever
				have custody over this key
			</p>
		</div>
		<div class="flex-col">
			<div class="card w-full max-w-sm flex-shrink-0 bg-base-100 shadow-2xl">
				<div class="card-body">
					<form>
						<div class="form-control my-1">
							<label for="publicKey" class="label">
								<span class="label-text">Public Key</span>
							</label>
							<div class="input-bordered input flex">
								<TruncatedKey keyText="" />
							</div>
						</div>
					</form>
				</div>
			</div>
		</div>
	</div>
</div>
