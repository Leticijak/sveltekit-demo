<script context="module">
	export async function load({ params, fetch, session, stuff }) {
		const url = `https://jsonplaceholder.typicode.com/posts/${params.id}`;
		const res = await fetch(url);

		if (res.ok) {
			return {
				props: {
					guide: guide
				}
			};
		}
		return {
			status: res.status,
			error: new Error(`Could not get the thing you're looking for`)
		};
	}
</script>

<script>
	export let guide;
</script>

<div class="guide" />

<style>
	.guide {
		margin-top: 40px;
		padding: 10px;
		border: 1px dotted gray;
	}
</style>
