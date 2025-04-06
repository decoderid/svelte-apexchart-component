<script lang="ts" module>
  import type { ApexOptions } from 'apexcharts'
  import type { HTMLAttributes } from 'svelte/elements'
  import { onMount } from 'svelte'
</script>

<script lang="ts">
  const props = $props<{ options: ApexOptions } & HTMLAttributes<HTMLDivElement>>()

  let chartContainer: HTMLDivElement

  onMount(async () => {
    const ApexCharts = (await import('apexcharts')).default
    const chart = new ApexCharts(chartContainer!, props.options)
    chart.render()
  })
</script>

<div bind:this={chartContainer} {...props}></div>
