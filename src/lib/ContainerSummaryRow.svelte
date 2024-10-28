<script>
	export let container;
</script>

<div class="row">
	<div class="id">{container.containerNumber}</div>
	<div class="shipname">{container.nameOfShip}</div>
	<div class="date">{container.dateContainerShipped}</div>
	<div class="size">{container.containerSize}</div>
</div>

<tr>
	<td>{container.containerNumber}</td>
	<td>{container.nameOfShip}</td>
	<td>{container.containerSize}</td>
	<td>{container.dateContainerShipped}</td>
</tr>

<style>
	.row {
		display: flex;
		background-color: #f9f9f9;
		border: 1px solid #ddd;
		padding: 5px;
		margin-bottom: 5px;
	}
	.id,
	.shipname,
	.size,
	.date {
		margin: 0 10px;
	}
	.id {
		font-weight: bold;
		flex: 1;
	}
	.size {
		text-align: right;
		flex: 0 0 50px;
	}
	.date {
		flex: 0 0 100px;
		text-align: center;
	}
	.shipname {
		flex: 2;
		color: #555;
	}
</style>
