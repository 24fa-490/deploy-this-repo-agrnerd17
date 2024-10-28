<script>
	import ContainerSummaryRow from './ContainerSummaryRow.svelte';
	export let containers = [];
	export let onContainerClicked = () => {};
</script>

<h3>A PseudoTable Component</h3>

<p>
	This is an example of Svelte containers, NOT the best way to create a simple table. It probably
	should be done in the ContainerTable component so that it is easy to add callbacks for people
	clicking the shipname or id or...
</p>

<p>Notice that tab order is set correctly with the index into the container object.</p>

<table>
	<thead>
		<tr>
			<th>Container Number</th>
			<th>Name of Ship</th>
			<th>Container Size</th>
			<th>Date Container Shipped</th>
		</tr>
	</thead>
	<tbody>
		{#each containers as container, ix}
			<tr
				tabindex={ix + 1}
				on:keydown={(e) => e.key === 'Enter' && onContainerClicked(container, e)}
				on:click={(e) => onContainerClicked(container, e)}
			>
				<ContainerSummaryRow {container} />
			</tr>
		{/each}
	</tbody>
</table>

<p>Last container clicked: none</p>

<style>
	table {
		width: 100%;
		border-collapse: collapse;
	}

	th,
	td {
		padding: 8px;
		text-align: left;
		border-bottom: 1px solid black;
	}

	tr:hover {
		background-color: #f5f5f5;
		cursor: pointer;
	}

	tr:focus {
		outline: 2px solid blue;
	}
</style>
