<script lang="ts">
	export let value = '';
	export let placeholder = '';
	export let isLoading = false;
	export let onInput = () => {};
	export let handleSubmit = () => {};

	function handleKeyPress(event: { key: string }) {
		if (event.key === 'Enter') {
			handleSubmit();
		}
	}
</script>

<textarea
	maxlength="9000"
	class="w-[20rem] md:w-[45rem] h-[15rem] md:h-[20rem] border rounded p-4 bg-slate-50 shadow-md mb-4"
	disabled={isLoading}
	bind:value
	{placeholder}
	on:input={onInput}
	on:keypress={handleKeyPress}
/>
