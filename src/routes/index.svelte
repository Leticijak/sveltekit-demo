<script>
	let title = 'Welcome to Svelte Bane';
	const updateTitle = () => {
		title = 'Something completely new';
	};
</script>

<div class="index">
	<h2>{title}</h2>
	<p>
		Lorem ipsum, dolor sit amet consectetur adipisicing elit. Saepe vel doloremque asperiores
		eligendi reiciendis magnam nihil! Quos nam possimus adipisci placeat quibusdam corporis natus
		nisi voluptatem, dolor dicta optio, distinctio assumenda odit nostrum beatae omnis mollitia
		quaerat repudiandae dolorem est!
	</p>
	<button on:click={updateTitle}>Change the title</button>
	<br />
	<!-- <input type="text" bind:value={title} /> -->
	<br />
	<a href="/about">Go to about page</a>
</div>

<style>
	.index {
		text-align: center;
		display: block;
		margin: 20px auto;
	}
</style>
