# D3 Snippets

## Overview

This document show the main D3 components. You can copy-paste them in order to accelerate your projects.

## Variables

```javascript
let width = 500
let height = 1000
let margin = 20
```

## Containers

Main SVG Container
```javascript
let svg = d3.select("body").append("svg")
svg.attr("width",width)
svg.attr("height",height)
```
Group Container
```javascript
let g = svg.append("g")
```

## Shapes

### Rectange
```javascript
let rect = svg.append("rect")
              .attr("id","r")
              .attr("class","rectu")
              .attr("x",0)
              .attr("y",10)
              .attr("width",40)
              .attr("height",50)
              .style("fill","red")
```

### Circle
```javascript
let circle = svg.append("circle")
              .attr("id","r")
              .attr("class","circu")
              .attr("cx",10)
              .attr("cy",80)
              .attr("r",10)
              .style("fill","blue")
```

### Line
```javascript
let line = svg.append("line")
              .attr("id","r")
              .attr("class","lineu")
              .attr("x1",30)
              .attr("y1",100)
              .attr("x2",40)
              .attr("y2",200)
              .style("stroke","red")
```

### Path
```javascript
let path = svg.append("path")
              .attr("id","r")
              .attr("class","pathu")
              .attr("d","M213.1,6.7c-32.4-14.4-73.7,0-88.1,30.6")
              .style("fill","red")
```

### Text
```javascript
let text = svg.append("text")
              .attr("id","r")
              .attr("class","textu")
              .attr("x",0)
              .attr("y",180)
              .html("text")
              .style("fill","blue")
```

## Transform Attribute
```javascript
let g2 = svg.append("g")
let text2 = g2.append("text")
              .attr("id","r")
              .attr("class","textu")
              .attr("x",0)
              .attr("y",180)
              .html("translated text")
              .style("fill","blue")
g2.attr("transform","translate(50,70)")
```

## Data in Json Format
```javascript
const data = [{value:10},
              {value:20},
              {value:40},
              {value:30},
              {value:60},
              {value:10},
              {value:70},
              {value:80},
             ]
```

## Joined Shapes with data

### Rect
```javascript
g3.selectAll(".game")
  .data(data)
  .enter()
  .append("rect")
  .attr("class","game")
  .attr("x",(d,i)=>i*10)
  .attr("y",(d,i)=>50 )
  .attr("width",5)
  .attr("height",20)
  .style("fill",(d,i)=>d.value)
```

### Circle
```javascript
g4.selectAll(".gamec")
  .data(data)
  .enter()
  .append("circle")
  .attr("class","gamec")
  .attr("cx",(d,i)=>i*10)
  .attr("cy",(d,i)=>50 )
  .attr("r",5)
  .style("fill",(d,i)=>d.value)
```

### Line
```javascript
g5.selectAll(".gamel")
  .data(data)
  .enter()
  .append("line")
  .attr("class","gamel")
  .attr("x1",(d,i)=>i*10)
  .attr("y1",(d,i)=>50 )
  .attr("x2",(d,i)=>i*10)
  .attr("y2",(d,i)=>60 )
  .style("stroke","black")
```


```javascript

```
