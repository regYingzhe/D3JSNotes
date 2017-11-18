# D3JSNotes
1.D3 scale: d3.scale.linear().domain([0, 400]).range([0, 400])
for y direction matters because svg coordinate x, y is different with ordinary x, y,
coordinate system. 

2.# D3JSNotes
1.dataSet = [{"name":"Shanghai"        , "population":18, "rank": 1},
           {"name":"Guangzhou"       , "population":11, "rank":10},
           {"name":"Dongguan"        , "population": 8, "rank":20},
           {"name":"Cairo"           , "population": 7, "rank":30},
           {"name":"Saint Petersburg", "population": 5, "rank":40},
           {"name":"New Taipei"      , "population": 4, "rank":50}];
2. create svg viewport:
var svgContainer = d3.select("body").append("svg").attr("width", 200).attr("height", 200)

3. svgContainer.selectAll("circle").data(dataSet).enter().append("circle")

4. the date is 0 indexed.

5. d3 axis: d3.select("body").append("svg")
           .attr("width", 200).attr("height", 200)
           .append("g")
           .call(d3.svg.axis())
6. d3.svg.axis().orient([orientation])
7. 
