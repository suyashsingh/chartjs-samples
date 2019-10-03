# Chart.js Chart Samples
Data visualization using Chart.js.

## Contents
1. `hello-world-chart.html`: Maiden voyage to charting using chartjs.
2. `responsive-chart.html`: Integrating Chart.js with Bootstrap 4.
3. `multiple-charts.html`: Multiple responsive charts in a page.
4. `chart-with-animation-customization.html`: Changing the default animation type
5. `chart-with-title-customization.html`: Enabling / Customizing chart title.
6. `chart-with-dynamic-data.html`: Bar chart with dynamic data

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

4. Animation can be customized as follows:

```javascript
var myChart = new Chart(ctx, {
    type: 'bar',
    data: chartData,
    options: {
        animation: {
           
            duration: 500,  // Change the animation durarion, 0 for no animation
            easing: "easeInQuad" // Change the animation type a.k.a easing function
        }
    }
});
```

5. Title Customizations:

```javascript
var myChart = new Chart(ctx, {
    type: 'bar',
    data: chartData,
    options: {
        title: {
            display: true, // defaults to false
            text: "Chart with Title Customization",
            fontSize: 45,
            fontFamily: 'Helvetica',
            fontColor: '#212529',
            fontStyle: 'bold',
            position: 'bottom' // position of the chart title
        }
    }
});
```
6. Bar Width Customization: 

```javascript
var customizationOptions = {
    scales: {
        xAxes: [{
        barThickness: 700
        }]
    }
};
```
