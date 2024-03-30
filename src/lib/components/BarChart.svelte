<script>
	import { Chart } from 'svelte-echarts';

	export let xAxisData = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'];
	export let yAxisData = [820, 932, 901, 934, 1290, 1330, 1320];

	const options = {
		tooltip: {
			trigger: 'axis',
			axisPointer: {
				type: 'shadow'
			}
		},
		xAxis: {
			data: xAxisData,
			type: 'category'
		},
		yAxis: {
			type: 'value'
		},
		series: [
			{
				data: yAxisData,
				type: 'bar'
			}
		]
	};
</script>

<div class="app">
	<Chart {options} />
</div>

<style>
	.app {
		width: 600px;
		height: 400px;
	}
</style>
