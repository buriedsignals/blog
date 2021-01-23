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
                return width / 10 + Math.cos(a * 8 - i * 2 * Math.PI / 3 + t) * Math.pow((1 + Math.cos(a - t)) / 2, 3) * width / 50;
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

## Who am I?
I’m a creative producer and aspiring visual journalist, I do consulting work for companies and non-profits. Read more about that here.
I’m a co-founder of the non-profit parkour academies [Wallrunners](wallrunners.org).
I’ve also made [documentaries](redbull.com/wallrunners) and [films](vimeo.com/buriedsignals/between). 
Past gigs have found me working with Red Bull, Immersive Garden, North Kingdom and a number of [consulting](teresamonroe.com) [projects](life.seedstars.com). 
Challenge me anytime, I'm on Telegram (@buriedsignals) and [Twitter](twitter.com/buriedsignals).

## Manifesto
I’m an advocate of [Gonzo journalism](en.wikipedia.org/wiki/Gonzo_journalism) as a framework to abstain from false claims of objectivity, 
complemented with an intent to [keep my identity small](www.paulgraham.com/identity.html) 
(inspired by [Kevin Simler’s](meltingasphalt.com/about/) manifesto). 
I’ve taken the [pro-truth pledge](www.protruthpledge.org/) and I vow to work under the tenets of Jim Lehrer’s 
[journalism principles](www.pbs.org/newshour/politics/jim-lehrer-in-his-own-words). My personal opinions are clearly labeled, 
fiction and philosophy essays reflect my own views.

Someday perhaps these essays will contribute in the struggle against disinformation and hold the powerful accountable, in the meantime I take great pleasure in the daily pursuit of truth and progress in the craft.

As a creed for these essays :
- Communicate in a clear and concise manner
- Use the medium best suited to the task
- Challenge myself to understand and give readers access to different views
- Fight stereotypes, fear-mongering and bipartisan polarisation
- Controversy for it’s own sake is entertainment
- My writing should and can be challenged
- Collaborate with experts, identify uncertainty when it exists
- Curate theoretical or operational solutions to the problem
- Sources are verified and always accessible
- Privacy matters, analytics and cookies on this site are non-invasive