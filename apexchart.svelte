<script lang="ts">
  import type { ApexOptions } from 'apexcharts'
  import { onMount } from 'svelte'
  let { options } = $props<{ options: ApexOptions }>()
  let chartContainer: HTMLDivElement

  onMount(async () => {
    const ApexCharts = (await import('apexcharts')).default
    const chart = new ApexCharts(chartContainer!, options)
    chart.render()
  })
</script>

<div bind:this={chartContainer}></div>
