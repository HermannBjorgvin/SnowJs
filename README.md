SnowJs
======

Small Javascript snippet under a kilobyte that adds snow to your website

How to snow:

Add this piece of code right after the begining of your <body> tag

<div id="snow"><canvas id="snowCanvas"></canvas></div>
        <script>var a=document.getElementById("snow"),b=document.getElementById("snowCanvas"),d=b.getContext("2d"),e=[];a.style.position="fixed";a.style.width="100vw";a.style.height="100vh";b.height=a.offsetHeight;b.width=a.offsetWidth;window.onresize=function(){b.height=a.offsetHeight;b.width=a.offsetWidth}; function f(){var c=2*(.5+.5*Math.random()),g=5*(.5+.5*Math.random()),h=10*Math.random();this.x=b.width*Math.random()*1.5-.25*b.width;this.y=0;this.b=c;this.c=g;this.s=h;this.u=function(){this.x+=this.b;this.y+=this.c;this.a()};this.a=function(){d.beginPath();d.arc(this.x,this.y,this.s,0,2*Math.PI,!1);d.fillStyle="#FFF";d.fill()}} setInterval(function(){d.clearRect(0,0,b.width,b.height);d.beginPath();.6<Math.random()&&e.push(new f);for(var c=0;c<e.length;c++)e[c].y>a.offsetHeight?e.splice(c,1):e[c].u()},16);</script>
