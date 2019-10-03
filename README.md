# chartjs-samples
Chart.js visualization samples

## Contents
1. `hello-world-chart.html` Maiden voyage to charting using chartjs.

## Notes
1. At bare minimum, a chart can be created using (chart customization options 
can be ommited as well.):

```javascript
var myChart = new Chart(ctx, {
    type: 'bar',
    data: chartData,
    options: customizationOptions
});
```