SnowJs
======

Small Javascript snippet under a kilobyte that adds snow to your website

How to snow:

Add this piece of code right after the begining of your &lt;body&gt; tag

&lt;div id="snow"&gt;&lt;canvas id="snowCanvas"&gt;&lt;/canvas&gt;&lt;/div&gt;
        &lt;script&gt;var b=document.getElementById("snow"),c=document.getElementById("snowCanvas"),d=c.getContext("2d"),e=[];b.style.position="fixed";b.style.width="100vw";b.style.height="100vh";c.height=b.offsetHeight;c.width=b.offsetWidth;window.onresize=function(){c.height=b.offsetHeight;c.width=b.offsetWidth}; function f(a,g,h){this.x=c.width*Math.random()*1.5-.25*c.width;this.y=0;this.b=a;this.c=g;this.s=h;this.update=function(){this.x+=this.b;this.y+=this.c;this.a()};this.a=function(){d.beginPath();d.arc(this.x,this.y,this.s,0,2*Math.PI,!1);d.fillStyle="#FFF";d.fill()}} setInterval(function(){d.clearRect(0,0,c.width,c.height);d.beginPath();if(.6<Math.random()){var a=Math.random();e.push(new f(2*(.2+.8*a),5*(.2+.8*a),10*a))}for(a=0;a<e.length;a++)e[a].y>b.offsetHeight?e.splice(a,1):e[a].update()},16);&lt;/script&gt;
