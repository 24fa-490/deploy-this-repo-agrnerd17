<script>
	export let container;
</script>

<div class="row">
	<div class="id">{container.containernumber}</div>
	<div class="shipname">{container.nameofship}</div>
	<div class="date">{container.datecontainershipped}</div>
	<div class="size">{container.containersize}</div>
</div>

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
