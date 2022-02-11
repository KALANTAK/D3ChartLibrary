# D3ChartLibrary
# D3 Chart Library
I have created this chart Libarary so that one can easily create and access the chart.
#
In this library I have included Bar chart , SunBurst Chart ,Line chart.
# 
In Bar Chart it includes:-

                        1.singleData Bar Chart.
                            1.1 Vertical BarChart
                            1.2 Horizontal BarChart
                        2.MultiData Bar Chart.
                            2.1 Vertical multibarchart stack and group
                            2.2 horizontal multibarchart stack and group
#

In Line Chart it includes:-

                        1.SingleData Line Chart.
                        2.MultiData Line Chart. 

#
To access any of the chart one have to call class name "KalantakChart".
```JavaScript
let abc = new KalantakChart();
```
## Access SingleData Bar Chart & MultiData Bar Chart
#
## SingleData Bar Chart
#### Vertical Bar Chart
1. we have to create one DOMElement and assign id to it.

    After one has call KalantakChart class , we have to add parameters to create this chart.

2. Parameter we will add in our class instance are :-
* id which we assign to DOMElement.
* We will pass `type:"vertical bar chart"` to give the orientation of the chart
* We will pass `data:[{...}]` , Here array of objects contains all the data which we will pass for creating chart .
* We can pass color name of our choice in any format like String , Hexadecimanl etc. we Should pass our color in Array.
    
    ` color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"]`

* We can give width and height of our  choice like `width:1000` and `height:700` .
* We have to give label name of our data like `label1:"country"` and `label2:"value"`.
3. we have to call the method `makeBarChart()`.
4. In this `type` value is not case-sensitive.
5. If type doesnot include `"vertical bar chart"` or `"VERTICAL BAR CHART"` it will give alert message `"This is not your chart which you are looking for!"`.

Let's Take Example :
``` Javascript
  let id = document.getElementById("demo");
        let chart = new KalantakChart(id,
            {
                type: "vertical bar chart",
                data: [
                    { country: "United States", value: "6500" },
                    { country: "Russia", value: "6148" },
                    { country: "Germany (FRG)", value: "1653" },
                    { country: "France", value: "2162" },
                    { country: "United Kingdom", value: "1000" },
                    { country: "China", value: "12000" },
                    { country: "Spain", value: "7500" },
                    { country: "Netherlands", value: "1167" },
                    { country: "Italy", value: "6606" },
                    { country: "Israel", value: "1263" },
                    { country: "india", value: "8000" },
                ],
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                width: 1000,
                height: 700,
                label1: "country",
                label2: "value"
            });
        chart.makeBarChart()
```
#### Horizontal Bar Chart

In this we only have to change `type:"horizontal bar chart"` or `type:" HORIZONTAL BAR CHART"`,rest all paramters are same for like Vertical Bar Chart.

Let's Take Example :
``` Javascript
 let id = document.getElementById("demo");
        let chart = new KalantakChart(id,
            {
                type: "horizontal bar chart",
                data: [
                    { country: "United States", value: "6500" },
                    { country: "Russia", value: "6148" },
                    { country: "Germany (FRG)", value: "1653" },
                    { country: "France", value: "2162" },
                    { country: "United Kingdom", value: "1000" },
                    { country: "China", value: "12000" },
                    { country: "Spain", value: "7500" },
                    { country: "Netherlands", value: "1167" },
                    { country: "Italy", value: "6606" },
                    { country: "Israel", value: "1263" },
                    { country: "india", value: "8000" },
                ],
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                width: 1000,
                height: 700,
                label1: "country",
                label2: "value"
            });
        chart.makeBarChart()
```

## MultiData Bar Chart
#### Vertical multibarchart stack and group
#### Stack
1. we have to create one DOMElement and assign id to it.

    After one has call KalantakChart class , we have to add parameters to create this chart.

2. Parameter we will add in our class instance are :-
* id which we assign to DOMElement.
* We will pass `type:"vertical multibarchart stack"` to give the orientation of the chart
* We will pass `data:[{...}]` , Here array of objects contains all the data which we will pass for creating chart .
* We can give width and height of our  choice like `width:1000` and `height:500`.
* We have to give label name of our data like `label1:"group"`.
* We can pass color name of our choice in any format like String , Hexadecimanl etc. we Should pass our color in Array.
    
    ` color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"]`
* we will pass keys which are included in our data like:

    `columns: ['group', 'nitrogen', 'normal', 'stress']`
* If one want tooltip in chart then He/She can pass 

    `tooltip: true`

  Else

  `tooltip: false`
3. we have to call the method `makeMultiBarChart()`.
4. In this `type` value is not case-sensitive.
5. If type doesnot include `"vertical multibarchart stack"` or `"VERTICAL MULTIBARCHART STACK"` it will give alert message `"This is not your chart which you are looking for!"`.

Let's Take Example :
``` Javascript
 
        let id5 = document.getElementById("demo4");
        let multidatabar = new KalantakChart(
            id5,
            {
                type: "horizontal MULTIBARCHART STACK",
                data: [
                    { group: 'banana', nitrogen: 12, normal: 1, stress: 13, },
                    { group: 'poacee', nitrogen: 6, normal: 6, stress: 33, },
                    { group: 'sorgho', nitrogen: 11, normal: 28, stress: 12, },
                    { group: 'triticum', nitrogen: 19, normal: 6, stress: 1, },

                ],
                width: 1050,
                height: 850,
                label1: "group",
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                columns: ['group', 'nitrogen', 'normal', 'stress'],
                tooltip: true,
            });
        multidatabar.makeMultiBarChart();
```
#### Group
In this we only have to change `type:"vertical multibarchart unstack"` or `type:"VERTICAL MULTIBARCHART UNSTACK"`,rest all paramters are same  like vertical multibarchart stack.
Let's Take Example :
``` Javascript
 
        let id5 = document.getElementById("demo4");
        let multidatabar = new KalantakChart(
            id5,
            {
                type: "vertical multibarchart unstack",
                data: [
                    { group: 'banana', nitrogen: 12, normal: 1, stress: 13, },
                    { group: 'poacee', nitrogen: 6, normal: 6, stress: 33, },
                    { group: 'sorgho', nitrogen: 11, normal: 28, stress: 12, },
                    { group: 'triticum', nitrogen: 19, normal: 6, stress: 1, },
                ],
                width: 1050,
                height: 850,
                label1: "group",
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                columns: ['group', 'nitrogen', 'normal', 'stress'],
                tooltip: true,
            });
        multidatabar.makeMultiBarChart();
```
#### Horizontal multibarchart stack and group
#### Stack
In this we only have to change `type:"horizontal multibarchart stack"` or `type:"HORIZONTAL MULTIBARCHART STACK"`,rest all paramters are same  like vertical multibarchart stack.
Let's Take Example :
``` Javascript
 
        let id5 = document.getElementById("demo4");
        let multidatabar = new KalantakChart(
            id5,
            {
                type: "horizontal multibarchart stack",
                data: [
                    { group: 'banana', nitrogen: 12, normal: 1, stress: 13, },
                    { group: 'poacee', nitrogen: 6, normal: 6, stress: 33, },
                    { group: 'sorgho', nitrogen: 11, normal: 28, stress: 12, },
                    { group: 'triticum', nitrogen: 19, normal: 6, stress: 1, },

                ],
                width: 1050,
                height: 850,
                label1: "group",
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                columns: ['group', 'nitrogen', 'normal', 'stress'],
                tooltip: true,
            });
        multidatabar.makeMultiBarChart();
```
#### Group
In this we only have to change `type:"horizontal multibarchart unstack"` or `type:"HORIZONTAL MULTIBARCHART UNSTACK"`,rest all paramters are same  like vertical multibarchart stack.
Let's Take Example :
``` Javascript
 
        let id5 = document.getElementById("demo4");
        let multidatabar = new KalantakChart(
            id5,
            {
                type: "horizontal multibarchart unstack",
                data: [
                    { group: 'banana', nitrogen: 12, normal: 1, stress: 13, },
                    { group: 'poacee', nitrogen: 6, normal: 6, stress: 33, },
                    { group: 'sorgho', nitrogen: 11, normal: 28, stress: 12, },
                    { group: 'triticum', nitrogen: 19, normal: 6, stress: 1, },

                ],
                width: 1050,
                height: 850,
                label1: "group",
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                columns: ['group', 'nitrogen', 'normal', 'stress'],
                tooltip: true,
            });
        multidatabar.makeMultiBarChart();
```

## Access SunBurst Chart
#
1. we have to create one DOMElement and assign id to it.

    After one has call KalantakChart class , we have to add parameters to create this chart.
2. Parameter we will add in our class instance are :-
* id which we assign to DOMElement.
* We will pass `type:"sunburst"` to identify the type of the chart
* We will pass `data:{[{...}]}` , Here object of array of objects contains all the data which we pass for making chart.
* We can give width and height of our  choice like `width:1500` and `height:750` .
* We can pass color name of our choice in any format like String , Hexadecimanl etc. we Should pass our color in Array.
    
    ` color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"]`
* If one want hover effect on chart then He/She can pass 
    `hover: true`

  Else

  `hover: false`
* If one want clickable and zoomable  effect on chart then He/She can pass 

    `click: true`

  Else

  `click: false`
3. we have to call the method `makeSunChart()`.
4. In this `type` value is not case-sensitive.
5. If type doesnot include `"sunbusrt"` or `"SUNBURST"` it will give alert message `"This is not your chart which you are looking for!"`.

Let's Take Example :
``` Javascript
 let id2 = document.getElementById("demo1");
        let sunburst = new KalantakChart(id2,
            {
                type: "sunburst",
                data: {
                    "name": "TOPICS", "children": [{
                        "name": "Topic A",
                        "children": [{ "name": "Sub A1", "size": 4 }, { "name": "Sub A2", "size": 4 }]
                    }, {
                        "name": "Topic B",
                        "children": [{ "name": "Sub B1", "size": 3 }, { "name": "Sub B2", "size": 3 }, {
                            "name": "Sub B3", "size": 3
                        }]
                    }, {
                        "name": "Topic C",
                        "children": [{ "name": "Sub A1", "size": 4 }, { "name": "Sub A2", "size": 4 }]
                    }]
                },
                width: 1500,
                height: 750,
                color: ["pink", "#a05d56", "#d0743c", "#ff8c00"],
                hover: true,
                click: true,
            });
        sunburst.makeSunChart()
```
## Access SingleData Line Chart & MultiData Line Chart
#
### SingleData Line Chart
1. we have to create one DOMElement and assign id to it.

    After one has called KalantakChart class , we have to add parameters to create this chart.

2. Parameter we will add in our class instance are :-
* id which we assign to DOMElement.
* We will pass `type:"linechart"` to identify the type of the chart.
* We will pass `data:[{...}]` , Here array of objects contains all the data which we will pass for creating chart.
* We can give width and height of our  choice like `width:1000` and `height:550` .
* We have to give label name of our data like `label1:"date"` and `label2:"close"`.
* If one want animation effect on chart then He/She can pass 

    `animation: true`

  Else

  `animation: false`
* we will ask for animation if one wants animation , we can pass argument like `animation:true`
* As we have given gradient to our line chart so we can change two colors by `startcolor:"yellow"` and `endcolor:"red"`.
* If one want hover effect on chart then He/She can pass 

    `hover: true`

  Else

  `hover: false`
3. we have to call the method `makeLineChart()`.
4. In this `type` value is not case-sensitive.
5. If type doesnot include `"linechart"` or `"LINECHART"` it will give alert message `"This is not your chart which you are looking for!"`.

Let's Take Example :
``` Javascript
     let id3 = document.getElementById("demo2");
        let linechart = new KalantakChart(id3,
            {
                type: "linechart",
                data: [
                    { date: "9-Apr-12", close: "53.98" },
                    { date: "10-Apr-12", close: " 77.98" },
                    { date: "11-Apr-12", close: "67.00" },
                    { date: "12-Apr-12", close: "89.70" },
                    { date: "13-Apr-12", close: "99.00" },
                    { date: "14-Apr-12", close: "130.28" },
                    { date: "15-Apr-12", close: "166.70" },
                    { date: "16-Apr-12", close: "234.98" },
                    { date: "17-Apr-12", close: "345.44" },
                    { date: "18-Apr-12", close: "443.34" },
                    { date: "19-Apr-12", close: "543.70" },
                    { date: "20-Apr-12", close: " 580.13" },
                    { date: "21-Apr-12", close: "605.23" },
                    { date: "22-Apr-12", close: "622.77" },
                    { date: "23-Apr-12", close: " 626.20" },
                ],
                width: 1000,
                height: 550,
                label1: "date",
                label2: "close",
                animation: true,
                startcolor: "yellow",
                endcolor: "red",
                hover: true,
            });
        linechart.makeLineChart()
```
### MultiData Line Chart
1. we have to create one DOMElement and assign id to it.

    After one has called KalantakChart class , we have to add parameters to create this chart.
2. Parameter we will add in our class instance are :-
* id which we assign to DOMElement.
* We will pass `type:"multiline"` to identify the type of the chart.
* We will pass `data:[{.[..].}]` , Here array of objects contains all datas which we will pass to create chart.
* We can give width and height of our  choice like `width:1000` and `height:500` .
* We have to give label name of our data like `label1:"date"` and `label2:"price"`.
* We can pass color name of our choice in any format like String , Hexadecimanl etc. we Should pass our color in Array.
    
    ` color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"]`
* If one want animation effect on chart then He/She can pass 

    `animation: true`

  Else

  `animation: false`
* If one want hover effect on chart then He/She can pass 

    `hover: true`

  Else

  `hover: false`

3. we have to call the method `makeMultiLineChart()`.
4. In this `type` value is not case-sensitive.
5. If type doesnot include `"multiline"` or `"MULTILINE"` it will give alert message `"This is not your chart which you are looking for!"`.

Let's Take Example :
```JavaScript
        let id4 = document.getElementById("demo3");
        let multilinechart = new KalantakChart(id4,
            {
                type: "multilinechart",
                data: [
                    {
                        name: "USA",
                        values: [
                            { date: "2000", price: "100" },
                            { date: "2001", price: "110" },
                            { date: "2002", price: "145" },
                            { date: "2003", price: "241" },
                            { date: "2004", price: "101" },
                            { date: "2005", price: "90" },
                            { date: "2006", price: "10" },
                            { date: "2007", price: "35" },
                            { date: "2008", price: "21" },
                            { date: "2009", price: "201" }
                        ]
                    },
                    {
                        name: "Canada",
                        values: [
                            { date: "2000", price: "200" },
                            { date: "2001", price: "120" },
                            { date: "2002", price: "33" },
                            { date: "2003", price: "21" },
                            { date: "2004", price: "51" },
                            { date: "2005", price: "190" },
                            { date: "2006", price: "120" },
                            { date: "2007", price: "85" },
                            { date: "2008", price: "221" },
                            { date: "2009", price: "101" }
                        ]
                    },
                    {
                        name: "Maxico",
                        values: [
                            { date: "2000", price: "50" },
                            { date: "2001", price: "10" },
                            { date: "2002", price: "5" },
                            { date: "2003", price: "71" },
                            { date: "2004", price: "20" },
                            { date: "2005", price: "9" },
                            { date: "2006", price: "220" },
                            { date: "2007", price: "235" },
                            { date: "2008", price: "61" },
                            { date: "2009", price: "10" }
                        ]
                    }
                ],
                width: 1000,
                height: 550,
                label1: "date",
                label2: "price",
                color: ["#6b486b", "#a05d56", "#d0743c", "#ff8c00"],
                animation: true,
                hover: true,
            });
        multilinechart.makeMultiLineChart()
```
