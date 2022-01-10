<script context="module">
	export async function load({ params, fetch, session, stuff }) {
		const id = params.id;
		const res = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`);
		const guide = await res.json();

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

<div class="guide">
	<h2>{guide.title}</h2>
	<p>{guide.body}</p>
</div>

<style>
	.guide {
		margin-top: 40px;
		padding: 10px;
		border: 1px dotted gray;
	}
</style>
