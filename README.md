SnowJs
======

Small Javascript snippet under a kilobyte that adds snow to your website

How to snow:

Add this piece of code right after the begining of your &lt;body&gt; tag

&lt;div id="snow"&gt;&lt;canvas id="snowCanvas"&gt;&lt;/canvas&gt;&lt;/div&gt;
        &lt;script&gt;var a=document.getElementById("snow"),d=a.getContext("2d"),e=[];a.style.position="fixed";a.style.width="100vw";a.style.height="100vh";a.height=a.offsetHeight;a.width=a.offsetWidth;window.onresize=function(){a.height=a.offsetHeight;a.width=a.offsetWidth}; setInterval(function(){d.clearRect(0,0,a.width,a.height);d.beginPath();if(.6<Math.random()){var b=Math.random(),f=.2+.8*b,c={};c.x=1.5*a.width*Math.random()-.5*a.width;c.y=-20;c.d=2*f*(Math.random()/2+.5);c.e=5*f;c.b=10*b;c.c=function(){this.x+=this.d;this.y+=this.e;this.a()};c.a=function(){d.beginPath();d.arc(this.x,this.y,this.b,0,2*Math.PI,!1);d.fillStyle="#FFF";d.fill()};e.push(c)}for(b=0;b<e.length;b++)e[b].y>a.height?e.splice(b,1):e[b].c()},16);&lt;/script&gt;
