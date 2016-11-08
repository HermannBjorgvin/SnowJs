SnowJs
###A seasonal repository
======

Small Javascript snippet under a kilobyte that adds snow to your website

How to snow:

Add this piece of code right after the begining of your &lt;body&gt; tag

```
<canvas id="snow"></canvas><script>(function(){var a=document.getElementById("snow"),c=a.getContext("2d"),e=[];a.style.pointerEvents="none";a.style.position="fixed";a.style.top=0;a.style.left=0;a.style.width="100vw";a.style.height="100vh";a.height=a.offsetHeight;a.width=a.offsetWidth;window.onresize=function(){a.height=a.offsetHeight;a.width=a.offsetWidth};var d=Math;setInterval(function(){c.clearRect(0,0,a.width,a.height);c.beginPath();var f=d.random(),g=.05+.95*f;flake={};flake.x=1.5*a.width*d.random()-.5*a.width;flake.y=-9;flake.b=2*g*(d.random()/2+.5);flake.c=(4+2*d.random())*g;flake.a=d.pow(5*f,2)/5;flake.update=function(){this.x+=this.b;this.y+=this.c;c.beginPath();c.arc(this.x,this.y,this.a,0,2*d.PI,!1);c.fillStyle="#FFF";c.fill()};e.push(flake);for(b=0;b<e.length;b++)e[b].y>a.height?e.splice(b,1):e[b].update()},16)})();</script>
```
