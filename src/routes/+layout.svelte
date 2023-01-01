<main class="scroll">
	<slot />
</main>

<style lang="scss">
	@import 'https://cdn.jsdelivr.net/gh/verdulife/utility-classes/dist/reset.css';
	@import 'https://cdn.jsdelivr.net/gh/verdulife/utility-classes/dist/utility-classes.css';

	:root {
		--color-pri: rgb(234, 48, 160);
		--font-title: 'TheBoldFont';
		--font-text: 'Adelle Sans';

		font-family: var(--font-text);
	}
</style>
