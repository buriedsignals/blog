---
layout: default
title: About
permalink: /about/
---

<div id="d3-header">
   <script type="text/javascript">
   const bounds = document.getElementById("d3-header");
   var svg = d3.select(bounds).append('svg');
   var width = bounds.getBoundingClientRect().width;
   var height = 250;

    svg.attr('width', width);
    svg.attr('height', height);

    var angles = d3.range(0, 2 * Math.PI, Math.PI / 400);

    var path = svg.append("g")
        .attr("transform", "translate(" + width / 2 + "," + height / 2 + ")")
        .attr("fill", "none")
        .attr("stroke-width", 3)
        .attr("stroke-linejoin", "round")
      .selectAll("path")
      .data(["cyan", "magenta", "yellow"])
      .enter().append("path")
        .attr("stroke", function(d) { return d; })
        .style("mix-blend-mode", "darken")
        .datum(function(d, i) {
          return d3.radialLine()
              .curve(d3.curveLinearClosed)
              .angle(function(a) { return a; })
              .radius(function(a) {
                var t = d3.now() / 1000;
                return width / 8 + Math.cos(a * 8 - i * 2 * Math.PI / 3 + t) * Math.pow((1 + Math.cos(a - t)) / 2, 3) * width / 50;
              });
        });

    d3.timer(function() {
      path.attr("d", function(d) {
        return d(angles);
      });
    });
   </script>
</div>

# About

## This blog
Buried Signals is an outlet for technical and creative experiments in visual storytelling. It's a great reason to play around with new ideas while justifying frequent exploration of literature and science. I write about anything orbiting my cognitive space: inquiries into geopolitics, philosophy, physics or fiction. 

## Who, me?
I’m a creative producer and aspiring visual journalist. Accasionally I do consulting work for companies and non-profits, you can read more about that [here](/consulting). As a co-founder of the non-profit [Wallrunners](wallrunners.org) I spend time building parkour academies where they're most needed. 

Past gigs have found me working as an integrated producer or content creator with Red Bull, Immersive Garden and North Kingdom. I started out by making [documentaries](redbull.com/wallrunners) and [films](https://vimeo.com/145770250). 

Feel free to start a conversation anytime, I'm on Telegram (@buriedsignals) and [Twitter](twitter.com/buriedsignals).

## Opinions on journalism
Advocating [Gonzo journalism](en.wikipedia.org/wiki/Gonzo_journalism) as a framework to abstain from false claims of objectivity. 
Also trying to [keep my identity small](www.paulgraham.com/identity.html) (inspired by [Kevin Simler’s](meltingasphalt.com/about/) manifesto). 

I am committed to working within the tenets of Jim Lehrer’s 
[journalism principles](www.pbs.org/newshour/politics/jim-lehrer-in-his-own-words). My personal opinions are clearly labeled, 
fiction and philosophy essays obviously reflect my own views.

Someday perhaps these essays will contribute in the struggle against disinformation, in the meantime I take great pleasure in 
the daily pursuit of truth and progress in the craft.

A self-imposed manifesto for these essays :
- Communicate in a clear and concise manner
- Seek to understand the opposing viewpoint and give readers access to both perspectives
- Fight stereotypes, fear-mongering and bipartisan polarisation
- Controversy for it’s own sake is entertainment
- My writing should and can be challenged
- Collaborate with experts, identify uncertainty when it exists
- Curate theoretical or operational solutions to the problem
- Sources are verified and always accessible
- Privacy matters, analytics and cookies on this site are non-invasive

<div class="pro-truth-logo">
    <a href="http://ProTruthPledge.org"><img style="width: 100px; height: 100px;" src="https://www.protruthpledge.org/hotlink-ok/ptpBacked.gif"></a><br>
    I signed the <a href="http://ProTruthPledge.org">Pro-Truth Pledge:</a><br>please hold me accountable.
</div>