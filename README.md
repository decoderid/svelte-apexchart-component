## Preview
![image](https://github.com/user-attachments/assets/ed69dae4-ede7-4780-84fe-b6937501873a)


### install
```bash
$ npm install apexcharts --save
```

### usage
```svelte
<script lang="ts" module">
  import Apexchart from '~/components/wrapper/apexchart.svelte'
  const chartOneOptions: any = {
    series: [
      {
        name: 'Sales',
        data: [168, 385, 201, 298, 187, 195, 291, 110, 215, 390, 280, 112],
      },
    ],
    colors: ['#465fff'],
    chart: {
      fontFamily: 'Outfit, sans-serif',
      type: 'bar',
      height: 180,
      toolbar: {
        show: false,
      },
    },
    plotOptions: {
      bar: {
        horizontal: false,
        columnWidth: '39%',
        borderRadius: 5,
        borderRadiusApplication: 'end',
      },
    },
    dataLabels: {
      enabled: false,
    },
    stroke: {
      show: true,
      width: 4,
      colors: ['transparent'],
    },
    xaxis: {
      categories: [
        'Jan',
        'Feb',
        'Mar',
        'Apr',
        'May',
        'Jun',
        'Jul',
        'Aug',
        'Sep',
        'Oct',
        'Nov',
        'Dec',
      ],
      axisBorder: {
        show: false,
      },
      axisTicks: {
        show: false,
      },
    },
    legend: {
      show: true,
      position: 'top',
      horizontalAlign: 'left',
      fontFamily: 'Outfit',
      markers: {
        radius: 99,
      },
    },
    yaxis: {
      title: false,
    },
    grid: {
      yaxis: {
        lines: {
          show: true,
        },
      },
    },
    fill: {
      opacity: 1,
    },

    tooltip: {
      x: {
        show: false,
      },
      y: {
        formatter: function (val) {
          return val
        },
      },
    },
  }
</script>

<Apexchart options={chartOneOptions} />
```
