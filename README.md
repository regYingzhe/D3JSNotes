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
7. scale: d3.scale.linear().domain([]).range([])
d3.time.scale()
8. DOM Level 0 Event listener:
<a href="#" onclick="alert("clicked")">Click Me </a>
9. DOM Level 1 Event listener:
<a href="#" id="myLink">Click Me </a>
<script>
document.getElementById("myLink").onclick = function(){alert("clicked")}
document.getElementById("myLink").onclick = function(){alert("clicked1")}
</script>
drawback is that overwrite the previous listener.
10. <a href="#" id="myLink">Click Me </a>
<script>
var el = docuent.getElementById("myLink");
function sayCupcake() {alert("cupcake");}
el.addEventListener("click", sayCupcake, false)
</script>

11. el.addEventListener("click", sayCupcake, false) which is
target.addEventListener(type, listener[, useCapture])

12. One - Event Listeners from the Capture Phase are executed before Event Listeners from the Bubbling Phase

Two - Event Listeners are executed in order of definition

Three - Capture Phase overrides definition order if there are Bubbling Phase Event Listeners defined earlier than the Capture Phase event listeners.
13. var force = d3.layout.force() // construcate new force layout
.nodes(nodes) // sets nodes for layout
.links(links) // sets links for associate array
.size([w, h]) // can be dynamic size with jquery
.linkStrength(0.1) // rigidity of the link
.linkDistance(20) // target distance between nodes
.charge(-30) // how hard they repel them together
.gravity(0.1) // sets the how hard they attrack with each together
.start() ;; start the simulation


