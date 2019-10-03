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

2. Disabling user selection in the canvas would be needed as clicking legends on
the canvas will select some text on the webpage. Refer this [link](https://www.w3schools.com/cssref/css3_pr_user-select.asp)
for more information.

```css
<style>
    /*
        Disable text selection in the canvas, else when you click the
        legend some text on the page might get selected, which is not 
        desirable.
    */
    canvas {
        -moz-user-select: none;
        -webkit-user-select: none;
        -ms-user-select: none;
        user-select: none; /* Standard syntax */
    }
</style>
```
3. There is no default type of the chart. You will have to explicitely specify 
the chart type else you will get an error.