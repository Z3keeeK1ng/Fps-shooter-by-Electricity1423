<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, viewport-fit=cover">
<title>Arena Strike - 3D FPS</title>
<style>
  html,body{margin:0;height:100%;overflow:hidden;background:#000;font-family:"Segoe UI",Arial,sans-serif;color:#fff;user-select:none}
  canvas{display:block;width:100vw;height:100vh}
  #hud{position:fixed;inset:0;pointer-events:none}
  #cross{position:absolute;left:50%;top:50%;width:26px;height:26px;transform:translate(-50%,-50%)}
  #cross i{position:absolute;background:#fff;box-shadow:0 0 2px #000}
  #cross i:nth-child(1){left:12px;top:0;width:2px;height:8px}
  #cross i:nth-child(2){left:12px;bottom:0;width:2px;height:8px}
  #cross i:nth-child(3){top:12px;left:0;height:2px;width:8px}
  #cross i:nth-child(4){top:12px;right:0;height:2px;width:8px}
  #cross.hit i{background:#f33}
  #hp{position:absolute;left:24px;bottom:24px;width:260px}
  #hp .bar{height:18px;background:rgba(0,0,0,.5);border:2px solid #fff;border-radius:3px;overflow:hidden}
  #hp .fill{height:100%;width:100%;background:linear-gradient(90deg,#d22,#4e4);transition:width .15s}
  #hp span{font-size:13px;letter-spacing:2px;text-shadow:0 0 4px #000}
  #ammo{position:absolute;right:28px;bottom:20px;text-align:right;text-shadow:0 0 6px #000}
  #ammo b{font-size:48px}
  #ammo small{font-size:22px;opacity:.8}
  #ammo div{font-size:13px;letter-spacing:2px;opacity:.8;height:16px}
  #top{position:absolute;top:16px;left:0;right:0;text-align:center;text-shadow:0 0 6px #000;font-size:18px;letter-spacing:2px}
  #top b{font-size:26px}
  #banner{position:absolute;top:22%;left:0;right:0;text-align:center;font-size:44px;font-weight:700;letter-spacing:6px;opacity:0;transition:opacity .4s;text-shadow:0 0 12px #000}
  #dmg{position:absolute;inset:0;background:radial-gradient(ellipse at center,transparent 40%,rgba(255,0,0,.75));opacity:0;transition:opacity .25s}
  #overlay{position:fixed;inset:0;background:rgba(0,0,0,.78);display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;z-index:10;cursor:pointer}
  #overlay h1{font-size:64px;margin:0 0 6px;letter-spacing:8px;color:#ff5a3c;text-shadow:0 0 20px #f30}
  #overlay p{margin:6px;font-size:18px;opacity:.9}
  #overlay .keys{margin-top:18px;font-size:15px;line-height:1.8;opacity:.8}
  #overlay .btn{margin-top:26px;padding:14px 44px;font-size:22px;letter-spacing:4px;border:2px solid #ff5a3c;border-radius:4px;background:rgba(255,90,60,.15)}
  html,body{touch-action:none;-webkit-touch-callout:none;-webkit-user-select:none;-webkit-tap-highlight-color:transparent;overscroll-behavior:none}
  #touch{display:none;position:fixed;inset:0;z-index:5;pointer-events:none}
  .touch #touch{display:block}
  #stick{position:absolute;left:max(28px,env(safe-area-inset-left));bottom:max(28px,env(safe-area-inset-bottom));width:140px;height:140px;border-radius:50%;background:rgba(255,255,255,.1);border:2px solid rgba(255,255,255,.35);pointer-events:auto}
  #knob{position:absolute;left:50%;top:50%;width:64px;height:64px;margin:-32px 0 0 -32px;border-radius:50%;background:rgba(255,255,255,.35);border:2px solid rgba(255,255,255,.6)}
  .tb{position:absolute;display:flex;align-items:center;justify-content:center;border-radius:50%;background:rgba(255,255,255,.14);border:2px solid rgba(255,255,255,.45);font-weight:700;letter-spacing:1px;font-size:14px;pointer-events:auto;text-shadow:0 0 4px #000}
  .tb.down{background:rgba(255,90,60,.55)}
  .tb.on{background:rgba(90,200,255,.45)}
  #bFire{right:max(30px,env(safe-area-inset-right));bottom:max(36px,env(safe-area-inset-bottom));width:100px;height:100px;font-size:18px;background:rgba(255,70,50,.28);border-color:rgba(255,120,100,.8)}
  #bJump{right:150px;bottom:max(60px,env(safe-area-inset-bottom));width:66px;height:66px}
  #bRel{right:44px;bottom:160px;width:58px;height:58px}
  #bRun{right:116px;bottom:140px;width:58px;height:58px}
  #bPause{position:absolute;top:12px;right:14px;width:42px;height:42px;font-size:15px}
  .touch #hp{top:14px;bottom:auto;left:14px;width:150px}
  .touch #ammo{top:62px;bottom:auto;right:14px}
  .touch #ammo b{font-size:30px}
  .touch #top{font-size:13px;top:8px}
  .touch #top b{font-size:18px}
  #wname{font-size:15px;letter-spacing:3px;font-weight:700;opacity:.95;height:auto!important;margin-bottom:2px}
  #wlist{position:absolute;bottom:14px;left:50%;transform:translateX(-50%);display:flex;gap:6px;font-size:12px;letter-spacing:1px;text-shadow:0 0 4px #000}
  #wlist span{padding:4px 8px;background:rgba(0,0,0,.45);border:1px solid rgba(255,255,255,.3);border-radius:3px;opacity:.7}
  #wlist span.on{opacity:1;border-color:#ff5a3c;background:rgba(255,90,60,.3)}
  .touch #wlist{bottom:auto;top:40px;gap:4px;font-size:10px;pointer-events:auto}
  .touch #wlist span{padding:5px 6px}
  #scope{display:none;position:absolute;inset:0;background:radial-gradient(circle at center,transparent 0,transparent 28vmin,#000 28.4vmin)}
  #scope:before,#scope:after{content:"";position:absolute;background:#000}
  #scope:before{left:0;right:0;top:50%;height:2px}
  #scope:after{top:0;bottom:0;left:50%;width:2px}
  #bSwap{right:44px;bottom:232px;width:58px;height:58px}
  #bZoom{display:none;right:116px;bottom:212px;width:58px;height:58px}
  body.nocursor,body.nocursor *{cursor:none!important}
  .tkeys{display:none}
  .touch .tkeys{display:block}
  .touch .pcl{display:none}
  @media (max-height:520px){
    #overlay h1{font-size:34px;letter-spacing:4px}
    #overlay p{font-size:14px}
    #overlay .keys{font-size:12px;margin-top:8px;line-height:1.5}
    #overlay .btn{margin-top:12px;padding:10px 30px;font-size:18px}
    #banner{font-size:28px}
  }
  #err{display:none;position:fixed;inset:0;z-index:99;background:#200;color:#fdd;padding:30px;font:16px/1.6 monospace;white-space:pre-wrap;overflow:auto}
</style>
</head>
<body>
<canvas id="gl"></canvas>
<div id="hud">
  <div id="top">WAVE <b id="wave">1</b> &nbsp;|&nbsp; KILLS <b id="kills">0</b> &nbsp;|&nbsp; SCORE <b id="score">0</b></div>
  <div id="banner"></div>
  <div id="cross"><i></i><i></i><i></i><i></i></div>
  <div id="hp"><span>HEALTH</span><div class="bar"><div class="fill" id="hpfill"></div></div></div>
  <div id="ammo"><div id="wname"></div><div id="reloadmsg"></div><b id="mag">30</b> <small>/ <span id="res">120</span></small></div>
  <div id="dmg"></div>
  <div id="scope"></div>
  <div id="wlist"></div>
</div>
<div id="overlay">
  <h1>ARENA STRIKE</h1>
  <p id="ovmsg">Survive endless waves of hostile bots.</p>
  <div class="keys tkeys">
    <b>Left stick</b> move &nbsp; <b>Drag right side</b> aim<br>
    <b>FIRE</b> shoot (hold) &nbsp; <b>JUMP</b> &nbsp; <b>R</b> reload &nbsp; <b>RUN</b> sprint &nbsp; <b>SWAP</b> / tap list = weapon<br>
    Headshots deal double damage. Landscape works best.
  </div>
  <div class="keys pcl">
    <b>WASD</b> move &nbsp; <b>MOUSE</b> aim &nbsp; <b>CLICK</b> shoot (hold for auto)<br>
    <b>SHIFT</b> sprint &nbsp; <b>SPACE</b> jump &nbsp; <b>R</b> reload &nbsp; <b>ESC</b> pause<br>
    <b>1-7 / WHEEL / Q</b> switch weapon &nbsp; <b>RIGHT CLICK</b> scope (AWM)<br>
    Headshots deal double damage.
  </div>
  <div class="btn" id="btn">CLICK TO PLAY</div>
</div>
<div id="touch">
  <div id="stick"><div id="knob"></div></div>
  <div class="tb" id="bFire">FIRE</div>
  <div class="tb" id="bJump">JUMP</div>
  <div class="tb" id="bRel">R</div>
  <div class="tb" id="bRun">RUN</div>
  <div class="tb" id="bSwap">SWAP</div>
  <div class="tb" id="bZoom">ZOOM</div>
  <div class="tb" id="bPause">❚❚</div>
</div>
<div id="err"></div>

<script>
// No external libraries: pure WebGL, works offline.
function showErr(m){var d=document.getElementById("err");d.style.display="block";d.textContent+=m+"\n\n";}
window.addEventListener("error",function(e){showErr("Error: "+(e.message||"unknown")+(e.filename?"\n at "+e.filename+":"+e.lineno:""));});

function startGame(){
"use strict";
const canvas = document.getElementById("gl");
const gl = canvas.getContext("webgl",{antialias:true}) || canvas.getContext("experimental-webgl");
if(!gl) throw new Error("WebGL is not available. Enable hardware acceleration in your browser settings.");

// ---------- Matrix helpers (column-major) ----------
const m4 = {
  ident(){return new Float32Array([1,0,0,0,0,1,0,0,0,0,1,0,0,0,0,1]);},
  mul(a,b){const o=new Float32Array(16);
    for(let c=0;c<4;c++)for(let r=0;r<4;r++){let s=0;for(let k=0;k<4;k++)s+=a[k*4+r]*b[c*4+k];o[c*4+r]=s;}return o;},
  persp(fov,asp,n,f){const t=1/Math.tan(fov/2),o=new Float32Array(16);
    o[0]=t/asp;o[5]=t;o[10]=(f+n)/(n-f);o[11]=-1;o[14]=2*f*n/(n-f);return o;},
  trans(x,y,z){const o=m4.ident();o[12]=x;o[13]=y;o[14]=z;return o;},
  scale(x,y,z){const o=m4.ident();o[0]=x;o[5]=y;o[10]=z;return o;},
  rotY(a){const c=Math.cos(a),s=Math.sin(a);return new Float32Array([c,0,-s,0, 0,1,0,0, s,0,c,0, 0,0,0,1]);},
  rotX(a){const c=Math.cos(a),s=Math.sin(a);return new Float32Array([1,0,0,0, 0,c,s,0, 0,-s,c,0, 0,0,0,1]);}
};
function chain(){let r=arguments[0];for(let i=1;i<arguments.length;i++)r=m4.mul(r,arguments[i]);return r;}

// ---------- Shader ----------
function mkShader(type,src){const s=gl.createShader(type);gl.shaderSource(s,src);gl.compileShader(s);
  if(!gl.getShaderParameter(s,gl.COMPILE_STATUS))throw new Error("Shader error: "+gl.getShaderInfoLog(s));return s;}
const prog = gl.createProgram();
gl.attachShader(prog,mkShader(gl.VERTEX_SHADER,`
attribute vec3 aPos; attribute vec3 aNor;
uniform mat4 uVP; uniform mat4 uModel;
varying vec3 vW; varying vec3 vN;
void main(){
  vec4 w = uModel*vec4(aPos,1.0);
  vW = w.xyz;
  vN = normalize(mat3(uModel)*aNor);
  gl_Position = uVP*w;
}`));
gl.attachShader(prog,mkShader(gl.FRAGMENT_SHADER,`
precision mediump float;
varying vec3 vW; varying vec3 vN;
uniform vec3 uColor; uniform float uEmis; uniform float uChk; uniform float uFog;
uniform vec3 uCam; uniform vec3 uFogCol;
void main(){
  vec3 n = normalize(vN);
  vec3 L = normalize(vec3(0.5,1.0,0.35));
  float d = max(dot(n,L),0.0);
  float hemi = 0.5+0.5*n.y;
  float light = 0.28 + 0.45*hemi*0.6 + 0.6*d;
  vec3 col = uColor;
  if(uChk>0.5){
    float t = mod(floor(vW.x/2.0)+floor(vW.z/2.0),2.0);
    col *= 0.8+0.25*t;
    vec2 g = abs(fract(vW.xz/2.0)-0.5);
    float line = step(0.47,max(g.x,g.y));
    col = mix(col,vec3(0.32,0.36,0.46),line*0.6);
  } else if(uEmis<0.5){
    float band = step(0.93,fract(vW.y*0.9));
    col *= 1.0-0.18*band;
  }
  vec3 c = mix(col*light, col, uEmis);
  float dist = length(vW-uCam);
  float f = clamp((dist-14.0)/56.0,0.0,1.0)*uFog;
  c = mix(c,uFogCol,f);
  gl_FragColor = vec4(c,1.0);
}`));
gl.linkProgram(prog);
if(!gl.getProgramParameter(prog,gl.LINK_STATUS))throw new Error("Link error: "+gl.getProgramInfoLog(prog));
gl.useProgram(prog);
const U={}; ["uVP","uModel","uColor","uEmis","uChk","uFog","uCam","uFogCol"].forEach(n=>U[n]=gl.getUniformLocation(prog,n));
const aPos=gl.getAttribLocation(prog,"aPos"), aNor=gl.getAttribLocation(prog,"aNor");

// ---------- Unit cube (centered, size 1) ----------
(function(){
  const f=[ // normal, 4 corners
    [[0,0,1],[-.5,-.5,.5],[.5,-.5,.5],[.5,.5,.5],[-.5,.5,.5]],
    [[0,0,-1],[.5,-.5,-.5],[-.5,-.5,-.5],[-.5,.5,-.5],[.5,.5,-.5]],
    [[1,0,0],[.5,-.5,.5],[.5,-.5,-.5],[.5,.5,-.5],[.5,.5,.5]],
    [[-1,0,0],[-.5,-.5,-.5],[-.5,-.5,.5],[-.5,.5,.5],[-.5,.5,-.5]],
    [[0,1,0],[-.5,.5,.5],[.5,.5,.5],[.5,.5,-.5],[-.5,.5,-.5]],
    [[0,-1,0],[-.5,-.5,-.5],[.5,-.5,-.5],[.5,-.5,.5],[-.5,-.5,.5]]
  ], d=[];
  f.forEach(q=>{const n=q[0],c=q.slice(1);[0,1,2,0,2,3].forEach(i=>d.push(...c[i],...n));});
  const buf=gl.createBuffer(); gl.bindBuffer(gl.ARRAY_BUFFER,buf);
  gl.bufferData(gl.ARRAY_BUFFER,new Float32Array(d),gl.STATIC_DRAW);
  gl.enableVertexAttribArray(aPos); gl.vertexAttribPointer(aPos,3,gl.FLOAT,false,24,0);
  gl.enableVertexAttribArray(aNor); gl.vertexAttribPointer(aNor,3,gl.FLOAT,false,24,12);
})();
gl.enable(gl.DEPTH_TEST); gl.enable(gl.CULL_FACE);
const FOG=[0.04,0.06,0.12];
gl.clearColor(FOG[0],FOG[1],FOG[2],1);
function hex(h){return [(h>>16&255)/255,(h>>8&255)/255,(h&255)/255];}
function drawBox(model,col,emis,chk){
  gl.uniformMatrix4fv(U.uModel,false,model);
  gl.uniform3fv(U.uColor,col);
  gl.uniform1f(U.uEmis,emis||0);
  gl.uniform1f(U.uChk,chk||0);
  gl.drawArrays(gl.TRIANGLES,0,36);
}

// ---------- World ----------
const ARENA=32;
const obstacles=[]; // {minx,maxx,minz,maxz,maxy,col}
function addBox(x,z,w,h,d,col){
  obstacles.push({x,z,w,h,d,minx:x-w/2,maxx:x+w/2,minz:z-d/2,maxz:z+d/2,maxy:h,col:hex(col)});
}
const T=1,H=6;
addBox(0,-ARENA-T/2,ARENA*2+T*2,H,T,0x6b5a52);
addBox(0, ARENA+T/2,ARENA*2+T*2,H,T,0x6b5a52);
addBox(-ARENA-T/2,0,T,H,ARENA*2,0x6b5a52);
addBox( ARENA+T/2,0,T,H,ARENA*2,0x6b5a52);
let seed=7; const rnd=()=>(seed=(seed*16807)%2147483647)/2147483647;
for(let i=0;i<18;i++){
  let x,z; do{x=(rnd()-.5)*(ARENA*2-8);z=(rnd()-.5)*(ARENA*2-8);}while(Math.hypot(x,z)<7);
  const s=1.6+rnd()*1.8; addBox(x,z,s,s*(1+rnd()*.6),s,0x9a7440);
}
for(let i=0;i<6;i++){
  let x,z; do{x=(rnd()-.5)*(ARENA*2-8);z=(rnd()-.5)*(ARENA*2-8);}while(Math.hypot(x,z)<9);
  addBox(x,z,1.4,5,1.4,0x56607a);
}

// ---------- Player ----------
const player={x:0,y:0,z:0,vx:0,vy:0,vz:0,yaw:0,pitch:0,onGround:true,hp:100,r:.45,eye:1.7};
const keys={};
let locked=false, soft=false, playing=false, paused=false, mouseDown=false;

const cD=hex(0x2a2d33),cM=hex(0x4a505a),cW=hex(0x7a4a28),cS=hex(0x9aa1ab),cO=hex(0x3d4a2e),cG=hex(0x16181b);
const weapons=[
 {name:"M1911 .45",short:"1911",auto:false,magSize:7,reserve:42,rate:.16,dmg:22,reloadTime:1.3,spread:.004,off:[.18,-.19,-.4],muzzle:-.33,
  snd(){noise(.1,.5,2500);tone(170,.09,.25,"sawtooth",-100);},
  model:[[0,.02,-.15,.05,.06,.3,cS],[0,-.02,-.12,.045,.04,.26,cD],[0,-.1,0,.05,.14,.07,cW],[0,.065,-.28,.012,.02,.012,cD]]},
 {name:"GLOCK 17",short:"G17",auto:false,magSize:17,reserve:85,rate:.1,dmg:14,reloadTime:1.2,spread:.006,off:[.18,-.19,-.4],muzzle:-.33,
  snd(){noise(.08,.4,3000);tone(210,.06,.2,"square",-120);},
  model:[[0,.02,-.15,.045,.055,.32,cG],[0,-.025,-.12,.045,.04,.26,cM],[0,-.11,-.01,.045,.15,.06,cG],[0,.055,-.29,.012,.02,.012,cM]]},
 {name:"UZI",short:"UZI",auto:true,magSize:32,reserve:128,rate:.055,dmg:9,reloadTime:1.5,spread:.018,off:[.2,-.2,-.42],muzzle:-.42,
  snd(){noise(.07,.35,3500);tone(240,.05,.18,"sawtooth",-120);},
  model:[[0,0,-.12,.06,.09,.34,cD],[0,.055,-.12,.04,.02,.3,cM],[0,-.12,0,.05,.16,.06,cD],[0,-.15,-.12,.04,.2,.05,cM],[0,.02,-.35,.025,.025,.12,cM]]},
 {name:"MP-40",short:"MP40",auto:true,magSize:32,reserve:128,rate:.1,dmg:12,reloadTime:1.7,spread:.012,off:[.2,-.2,-.42],muzzle:-.55,
  snd(){noise(.1,.5,2800);tone(150,.09,.25,"sawtooth",-80);},
  model:[[0,0,-.15,.05,.07,.4,cG],[0,-.18,-.14,.035,.22,.04,cM],[0,-.09,.02,.045,.13,.06,cG],[0,.015,-.42,.03,.03,.2,cM],[0,.05,-.5,.012,.03,.012,cM]]},
 {name:"UMP",short:"UMP",auto:true,magSize:25,reserve:100,rate:.09,dmg:14,reloadTime:1.6,spread:.008,off:[.2,-.2,-.42],muzzle:-.56,
  snd(){noise(.08,.4,3200);tone(190,.07,.22,"sawtooth",-100);},
  model:[[0,0,-.15,.06,.1,.42,cD],[0,-.16,-.1,.04,.2,.05,cM],[0,-.1,.03,.05,.14,.06,cD],[0,.02,-.46,.03,.03,.18,cM],[0,.075,-.1,.02,.03,.12,cM],[0,.0,.25,.05,.08,.22,cD]]},
 {name:"AKM",short:"AKM",auto:true,magSize:30,reserve:120,rate:.1,dmg:20,reloadTime:2.0,spread:.01,off:[.22,-.22,-.45],muzzle:-.85,
  snd(){noise(.15,.6,2200);tone(110,.12,.3,"sawtooth",-70);},
  model:[[0,0,-.2,.06,.09,.5,cD],[0,-.005,-.52,.065,.075,.25,cW],[0,.02,-.76,.025,.025,.22,cS],[0,-.17,-.25,.04,.22,.07,cM],[0,-.11,.02,.05,.15,.06,cW],[0,-.015,.27,.05,.1,.3,cW],[0,.065,-.5,.012,.05,.012,cM]]},
 {name:"AWM",short:"AWM",auto:false,pierce:true,zoom:true,zoomFov:22,magSize:5,reserve:25,rate:1.1,dmg:100,reloadTime:2.6,spread:.0005,off:[.22,-.23,-.45],muzzle:-1.05,
  snd(){noise(.3,.8,1500);tone(70,.3,.4,"sawtooth",-40);},
  model:[[0,0,-.2,.06,.09,.6,cO],[0,.015,-.78,.03,.03,.5,cG],[0,.095,-.25,.045,.045,.3,cG],[0,.095,-.42,.06,.06,.04,cM],[0,.095,-.08,.06,.06,.04,cM],[0,-.01,.28,.055,.11,.32,cO],[0,-.09,-.2,.04,.07,.1,cM],[0,-.1,.03,.05,.13,.06,cO]]}
];
for(const w of weapons){w.mag=w.magSize;w.startReserve=w.reserve;w.reloading=false;w.reloadT=0;w.cd=0;w.recoil=0;w.flashT=0;}
let cur=0,W=weapons[0],swapT=0,zoomed=false,fov=75,trigReady=true;

// ---------- Audio ----------
let actx=null;
function audio(){if(!actx)actx=new(window.AudioContext||window.webkitAudioContext)();return actx;}
function noise(dur,vol,freq){try{
  const a=audio(),n=Math.floor(a.sampleRate*dur),b=a.createBuffer(1,n,a.sampleRate),d=b.getChannelData(0);
  for(let i=0;i<n;i++)d[i]=(Math.random()*2-1)*Math.pow(1-i/n,2);
  const s=a.createBufferSource();s.buffer=b;
  const f=a.createBiquadFilter();f.type="lowpass";f.frequency.value=freq;
  const g=a.createGain();g.gain.value=vol;
  s.connect(f);f.connect(g);g.connect(a.destination);s.start();}catch(e){}}
function tone(freq,dur,vol,type,slide){try{
  type=type||"square";
  const a=audio(),o=a.createOscillator(),g=a.createGain();
  o.type=type;o.frequency.setValueAtTime(freq,a.currentTime);
  if(slide)o.frequency.exponentialRampToValueAtTime(Math.max(20,freq+slide),a.currentTime+dur);
  g.gain.setValueAtTime(vol,a.currentTime);g.gain.exponentialRampToValueAtTime(.001,a.currentTime+dur);
  o.connect(g);g.connect(a.destination);o.start();o.stop(a.currentTime+dur);}catch(e){}}
const sfx={
  shot(){noise(.12,.5,3000);tone(140,.1,.25,"sawtooth",-90);},
  hit(){tone(900,.05,.15,"square");},
  head(){tone(1400,.09,.2,"square");},
  kill(){tone(300,.25,.25,"sawtooth",-200);},
  hurt(){noise(.2,.5,800);tone(90,.2,.3,"sine",-40);},
  reload(){tone(400,.05,.15);setTimeout(()=>tone(600,.05,.15),700);},
  empty(){tone(200,.04,.15);},
  wave(){tone(440,.2,.2,"triangle");setTimeout(()=>tone(660,.3,.2,"triangle"),180);}
};

// ---------- Enemies ----------
const enemies=[];
const C_SKIN=hex(0x8f2a2a), C_DARK=hex(0x3a3a44), C_EYE=hex(0xffee33), C_WHITE=[1,1,1];
function spawnEnemy(x,z,wave){
  enemies.push({x,z,yaw:0,hp:40+Math.floor(wave/3)*10,speed:Math.min(2.2+wave*.25+Math.random()*.8,5.5),
    r:.5,cd:0,dead:false,deadT:0,phase:Math.random()*6,flashT:0});
}
function enemyBoxes(e){ // axis-aligned hit volumes: [minx,maxx,miny,maxy,minz,maxz,head]
  const x=e.x,z=e.z;
  return [
    [x-.22,x+.22,1.63,2.07,z-.22,z+.22,true],
    [x-.4,x+.4,.7,1.6,z-.28,z+.28,false],
    [x-.32,x+.32,0,.7,z-.25,z+.25,false]
  ];
}

// ---------- Particles ----------
const particles=[];
function burst(x,y,z,col,n,speed){
  for(let i=0;i<n;i++)particles.push({x,y,z,vx:(Math.random()-.5)*speed,vy:Math.random()*.8*speed,vz:(Math.random()-.5)*speed,life:.5+Math.random()*.3,col});
}

// ---------- Collision ----------
function collideCircle(p,r,feetY,headY){
  for(const b of obstacles){
    if(feetY>=b.maxy||headY<=0)continue;
    const cx=Math.max(b.minx,Math.min(p.x,b.maxx)),cz=Math.max(b.minz,Math.min(p.z,b.maxz));
    const dx=p.x-cx,dz=p.z-cz,d2=dx*dx+dz*dz;
    if(d2<r*r){
      if(d2>1e-8){const d=Math.sqrt(d2),push=r-d;p.x+=dx/d*push;p.z+=dz/d*push;}
      else{
        const l=p.x-b.minx,rr=b.maxx-p.x,t=p.z-b.minz,bo=b.maxz-p.z,m=Math.min(l,rr,t,bo);
        if(m===l)p.x=b.minx-r;else if(m===rr)p.x=b.maxx+r;else if(m===t)p.z=b.minz-r;else p.z=b.maxz+r;
      }
    }
  }
}
function rayBox(ox,oy,oz,dx,dy,dz,x0,x1,y0,y1,z0,z1){
  let tmin=0,tmax=1e9;
  const o=[ox,oy,oz],d=[dx,dy,dz],lo=[x0,y0,z0],hi=[x1,y1,z1];
  for(let i=0;i<3;i++){
    if(Math.abs(d[i])<1e-9){if(o[i]<lo[i]||o[i]>hi[i])return -1;}
    else{
      let t1=(lo[i]-o[i])/d[i],t2=(hi[i]-o[i])/d[i];
      if(t1>t2){const t=t1;t1=t2;t2=t;}
      tmin=Math.max(tmin,t1);tmax=Math.min(tmax,t2);
      if(tmin>tmax)return -1;
    }
  }
  return tmin;
}

// ---------- Game state ----------
const S={wave:0,kills:0,score:0,toSpawn:0,spawnT:0,between:2,over:false};
const $=id=>document.getElementById(id);
const el={wave:$("wave"),kills:$("kills"),score:$("score"),hpfill:$("hpfill"),mag:$("mag"),res:$("res"),
  banner:$("banner"),scope:$("scope"),wname:$("wname"),wlist:$("wlist"),dmg:$("dmg"),cross:$("cross"),reloadmsg:$("reloadmsg"),overlay:$("overlay"),ovmsg:$("ovmsg"),btn:$("btn")};
let bannerT=0;
function banner(text,ms){
  el.banner.textContent=text;el.banner.style.opacity=1;
  clearTimeout(bannerT);bannerT=setTimeout(()=>el.banner.style.opacity=0,ms||1800);
}
function updateHUD(){
  el.wave.textContent=S.wave;el.kills.textContent=S.kills;el.score.textContent=S.score;
  el.hpfill.style.width=Math.max(0,player.hp)+"%";
  el.mag.textContent=W.mag;el.res.textContent=W.reserve;el.wname.textContent=W.name;
  el.reloadmsg.textContent=W.reloading?"RELOADING...":(W.mag===0&&W.reserve>0?"PRESS R":(W.mag===0?"NO AMMO":""));
}
function startWave(){S.wave++;S.toSpawn=4+S.wave*2;S.spawnT=0;banner("WAVE "+S.wave);sfx.wave();updateHUD();}
function resetGame(){
  enemies.length=0;particles.length=0;
  Object.assign(player,{x:0,y:0,z:0,vx:0,vy:0,vz:0,hp:100,yaw:0,pitch:0});
  for(const w of weapons){w.mag=w.magSize;w.reserve=w.startReserve;w.reloading=false;w.cd=0;w.flashT=0;w.recoil=0;}
  cur=0;W=weapons[0];swapT=0;zoomed=false;fov=75;
  if(el.scope)el.scope.style.display='none';el.cross.style.display='block';updateWlist();
  Object.assign(S,{wave:0,kills:0,score:0,toSpawn:0,spawnT:0,between:1.5,over:false});
  updateHUD();
}

// ---------- Shooting ----------
function damageEnemy(e,head,x,y,z){
  e.hp-=W.dmg*(head?2:1);e.flashT=.1;
  burst(x,y,z,[1,.2,.1],8,3);
  el.cross.classList.add("hit");setTimeout(()=>el.cross.classList.remove("hit"),90);
  if(e.hp<=0&&!e.dead){
    e.dead=true;e.deadT=0;S.kills++;S.score+=head?150:100;sfx.kill();
    if(Math.random()<.35)W.reserve+=Math.ceil(W.magSize/2);
    burst(e.x,1.2,e.z,[1,.55,0],22,5);
  }else(head?sfx.head:sfx.hit)();
}
function shoot(){
  if(W.reloading||W.cd>0||swapT>0)return false;
  if(W.mag<=0){sfx.empty();W.cd=.25;if(W.reserve>0)reload();return false;}
  W.mag--;W.cd=W.rate;W.recoil=1;W.flashT=.05;
  W.snd();
  const moving=Math.hypot(player.vx,player.vz)>1;
  const spread=W.spread*(moving?2.2:1)*(zoomed?.25:1)+(W.zoom&&!zoomed?.03:0)+(player.onGround?0:.015);
  const cy=Math.cos(player.yaw),sy=Math.sin(player.yaw),cp=Math.cos(player.pitch),sp=Math.sin(player.pitch);
  const fx=-sy*cp,fy=sp,fz=-cy*cp;
  const rx=cy,rz=-sy;
  const up=ry_(rx,0,rz,fx,fy,fz);
  const a=(Math.random()-.5)*spread*2,b=(Math.random()-.5)*spread*2;
  let dx=fx+rx*a+up[0]*b,dy=fy+up[1]*b,dz=fz+rz*a+up[2]*b;
  const l=Math.hypot(dx,dy,dz);dx/=l;dy/=l;dz/=l;
  const ox=player.x,oy=player.y+player.eye,oz=player.z;
  let wall=120;
  for(const o of obstacles){
    const t=rayBox(ox,oy,oz,dx,dy,dz,o.minx,o.maxx,0,o.maxy,o.minz,o.maxz);
    if(t>=0&&t<wall)wall=t;
  }
  const hits=[];
  for(const e of enemies){
    if(e.dead)continue;
    let bt=1e9,bh=false;
    for(const bx of enemyBoxes(e)){
      const t=rayBox(ox,oy,oz,dx,dy,dz,bx[0],bx[1],bx[2],bx[3],bx[4],bx[5]);
      if(t>=0&&t<bt){bt=t;bh=bx[6];}
    }
    if(bt<wall)hits.push({e,t:bt,head:bh});
  }
  hits.sort((p,q)=>p.t-q.t);
  const take=W.pierce?hits:hits.slice(0,1);
  for(const h of take)damageEnemy(h.e,h.head,ox+dx*h.t,oy+dy*h.t,oz+dz*h.t);
  if(!take.length&&wall<120)burst(ox+dx*wall,oy+dy*wall,oz+dz*wall,[1,.85,.5],5,2.5);
  if(W.mag===0&&W.reserve>0)setTimeout(()=>{if(W.mag===0)reload();},250);
  updateHUD();
  return true;
}
function ry_(ax,ay,az,bx,by,bz){return [ay*bz-az*by,az*bx-ax*bz,ax*by-ay*bx];}
function reload(){
  if(W.reloading||W.mag===W.magSize||W.reserve<=0)return;
  W.reloading=true;W.reloadT=W.reloadTime;setZoom(false);sfx.reload();updateHUD();
}

// ---------- Input ----------
const isTouch=(window.matchMedia&&matchMedia("(pointer:coarse)").matches)||("ontouchstart" in window)||navigator.maxTouchPoints>0;
function active(){return playing&&!paused&&(locked||soft);}
function setZoom(on){
  zoomed=!!(on&&W.zoom&&!W.reloading);
  el.scope.style.display=zoomed?"block":"none";
  el.cross.style.display=zoomed?"none":"block";
}
function updateWlist(){
  el.wlist.innerHTML=weapons.map((w,i)=>'<span data-i="'+i+'" class="'+(i===cur?"on":"")+'">'+(i+1)+" "+w.short+"</span>").join("");
  const bz=document.getElementById("bZoom");if(bz)bz.style.display=W.zoom?"flex":"none";
}
function selectWeapon(n){
  n=(n+weapons.length)%weapons.length;
  if(n===cur)return;
  W.reloading=false;setZoom(false);
  cur=n;W=weapons[n];swapT=.3;tone(500,.05,.12,"square");
  updateWlist();updateHUD();
}
addEventListener("keydown",e=>{
  keys[e.code]=true;
  if(e.code==="KeyR"&&active())reload();
  if(e.code==="Space")e.preventDefault();
  if(active()){
    if(e.code.startsWith("Digit")){const n=+e.code.slice(5)-1;if(n>=0&&n<weapons.length)selectWeapon(n);}
    if(e.code==="KeyQ")selectWeapon(cur+1);
  }
  if(e.code==="Escape"&&soft&&playing&&!S.over){pause();}
});
addEventListener("keyup",e=>keys[e.code]=false);
addEventListener("mousedown",e=>{if(!active())return;if(e.button===0)mouseDown=true;if(e.button===2)setZoom(true);});
addEventListener("contextmenu",e=>e.preventDefault());
addEventListener("wheel",e=>{if(active())selectWeapon(cur+(e.deltaY>0?1:-1));},{passive:true});
addEventListener("mouseup",e=>{if(e.button===0)mouseDown=false;if(e.button===2)setZoom(false);});
addEventListener("mousemove",e=>{
  if(!active())return;
  player.yaw-=e.movementX*.0022*(fov/75);
  player.pitch-=e.movementY*.0022*(fov/75);
  player.pitch=Math.max(-1.5,Math.min(1.5,player.pitch));
});
function pause(){
  paused=true;mouseDown=false;
  el.overlay.style.display="flex";el.ovmsg.textContent="Paused";el.btn.textContent="CLICK TO RESUME";
}
document.addEventListener("pointerlockchange",()=>{
  locked=document.pointerLockElement===canvas;
  if(!locked&&playing&&!S.over&&!soft)pause();
});
document.addEventListener("pointerlockerror",()=>{soft=true;}); // fallback for sandboxed previews
el.overlay.addEventListener("click",()=>{
  try{audio().resume();}catch(e){}
  if(S.over||!playing)resetGame();
  playing=true;paused=false;
  el.overlay.style.display="none";
  if(isTouch){
    try{const d=document.documentElement,f=d.requestFullscreen||d.webkitRequestFullscreen;
      if(f){const p=f.call(d);if(p&&p.catch)p.catch(()=>{});}}catch(e){}
    try{const p=screen.orientation&&screen.orientation.lock&&screen.orientation.lock("landscape");if(p&&p.catch)p.catch(()=>{});}catch(e){}
    return;
  }
  try{
    const p=canvas.requestPointerLock();
    if(p&&p.catch)p.catch(()=>{soft=true;});
  }catch(e){soft=true;}
  setTimeout(()=>{if(!locked)soft=true;},400);
});

// ---------- Touch controls ----------
const joy={on:false,x:0,y:0,id:null}; let runOn=false, lookId=null, lookX=0, lookY=0;
if(isTouch){
  document.body.classList.add("touch");
  soft=true;
  const stick=$("stick"),knob=$("knob"),R=55;
  const joyMove=t=>{
    const r=stick.getBoundingClientRect(),cx=r.left+r.width/2,cy=r.top+r.height/2;
    let dx=t.clientX-cx,dy=t.clientY-cy;const l=Math.hypot(dx,dy);
    if(l>R){dx=dx/l*R;dy=dy/l*R;}
    joy.x=dx/R;joy.y=dy/R;
    knob.style.transform="translate("+dx+"px,"+dy+"px)";
  };
  const joyEnd=()=>{joy.on=false;joy.id=null;joy.x=joy.y=0;knob.style.transform="";};
  stick.addEventListener("touchstart",e=>{e.preventDefault();const t=e.changedTouches[0];joy.id=t.identifier;joy.on=true;joyMove(t);},{passive:false});
  canvas.addEventListener("touchstart",e=>{
    e.preventDefault();
    if(!active())return;
    for(const t of e.changedTouches)if(lookId===null){lookId=t.identifier;lookX=t.clientX;lookY=t.clientY;}
  },{passive:false});
  window.addEventListener("touchmove",e=>{
    e.preventDefault();
    for(const t of e.changedTouches){
      if(t.identifier===joy.id)joyMove(t);
      else if(t.identifier===lookId&&active()){
        player.yaw-=(t.clientX-lookX)*.006*(fov/75);
        player.pitch-=(t.clientY-lookY)*.006*(fov/75);
        player.pitch=Math.max(-1.5,Math.min(1.5,player.pitch));
        lookX=t.clientX;lookY=t.clientY;
      }
    }
  },{passive:false});
  const endT=e=>{for(const t of e.changedTouches){if(t.identifier===joy.id)joyEnd();if(t.identifier===lookId)lookId=null;}};
  window.addEventListener("touchend",endT);
  window.addEventListener("touchcancel",endT);
  const hold=(id,on,off)=>{
    const b=$(id);
    b.addEventListener("touchstart",e=>{e.preventDefault();b.classList.add("down");on();},{passive:false});
    ["touchend","touchcancel"].forEach(ev=>b.addEventListener(ev,e=>{e.preventDefault();b.classList.remove("down");if(off)off();},{passive:false}));
  };
  hold("bFire",()=>{if(active())mouseDown=true;},()=>{mouseDown=false;});
  hold("bJump",()=>{keys.Space=true;},()=>{keys.Space=false;});
  hold("bRel",()=>{if(active())reload();});
  hold("bRun",()=>{runOn=!runOn;$("bRun").classList.toggle("on",runOn);});
  hold("bPause",()=>{if(playing&&!S.over&&!paused)pause();});
  hold("bSwap",()=>{if(active())selectWeapon(cur+1);});
  hold("bZoom",()=>{if(active())setZoom(!zoomed);});
  el.wlist.addEventListener("touchstart",e=>{
    e.preventDefault();const t=e.target.closest("span");
    if(t&&active())selectWeapon(+t.dataset.i);
  },{passive:false});
}

// ---------- Update ----------
const clockStart=performance.now();let last=performance.now(),bobT=0;
function hurtPlayer(n){
  player.hp-=n;sfx.hurt();
  el.dmg.style.opacity=1;clearTimeout(hurtPlayer.t);hurtPlayer.t=setTimeout(()=>el.dmg.style.opacity=0,150);
  updateHUD();
  if(player.hp<=0&&!S.over){
    S.over=true;mouseDown=false;
    try{document.exitPointerLock();}catch(e){}
    el.overlay.style.display="flex";
    el.ovmsg.innerHTML="YOU DIED<br>Wave "+S.wave+" &nbsp;•&nbsp; "+S.kills+" kills &nbsp;•&nbsp; "+S.score+" points";
    el.btn.textContent="PLAY AGAIN";
  }
}
function update(dt){
  const sprint=keys.ShiftLeft||keys.ShiftRight||runOn, speed=sprint?9:5.5;
  const fx=-Math.sin(player.yaw),fz=-Math.cos(player.yaw),rx=Math.cos(player.yaw),rz=-Math.sin(player.yaw);
  let wx=0,wz=0;
  if(keys.KeyW){wx+=fx;wz+=fz;} if(keys.KeyS){wx-=fx;wz-=fz;}
  if(keys.KeyD){wx+=rx;wz+=rz;} if(keys.KeyA){wx-=rx;wz-=rz;}
  let mag=1;
  if(joy.on){
    const jm=Math.min(1,Math.hypot(joy.x,joy.y)),jx=joy.x,jy=-joy.y;
    wx+=fx*jy+rx*jx;wz+=fz*jy+rz*jx;mag=jm;
  }
  const wl=Math.hypot(wx,wz); if(wl>0){wx=wx/wl*speed*mag;wz=wz/wl*speed*mag;}
  const accel=player.onGround?14:3;
  player.vx+=(wx-player.vx)*Math.min(1,accel*dt);
  player.vz+=(wz-player.vz)*Math.min(1,accel*dt);
  if(keys.Space&&player.onGround){player.vy=7.5;player.onGround=false;}
  player.vy-=22*dt;
  player.x+=player.vx*dt;player.z+=player.vz*dt;player.y+=player.vy*dt;
  if(player.y<=0){player.y=0;player.vy=0;player.onGround=true;}
  collideCircle(player,player.r,player.y,player.y+1.8);
  const lim=ARENA-player.r;
  player.x=Math.max(-lim,Math.min(lim,player.x));
  player.z=Math.max(-lim,Math.min(lim,player.z));
  const hv=Math.hypot(player.vx,player.vz);
  if(player.onGround)bobT+=dt*hv*1.7;

  W.cd=Math.max(0,W.cd-dt);W.recoil=Math.max(0,W.recoil-dt*9);W.flashT=Math.max(0,W.flashT-dt);swapT=Math.max(0,swapT-dt);
  if(W.reloading){
    W.reloadT-=dt;
    if(W.reloadT<=0){const take=Math.min(W.magSize-W.mag,W.reserve);W.mag+=take;W.reserve-=take;W.reloading=false;updateHUD();}
  }
  if(mouseDown){if((W.auto||trigReady)&&shoot()&&!W.auto)trigReady=false;}else trigReady=true;

  const alive=enemies.filter(e=>!e.dead).length;
  if(S.toSpawn>0){
    S.spawnT-=dt;
    if(S.spawnT<=0&&alive<14){
      S.spawnT=Math.max(.35,1.2-S.wave*.06);
      let x,z,tries=0;
      do{
        const a=Math.random()*Math.PI*2,rr=ARENA-3;
        x=Math.max(-rr,Math.min(rr,Math.cos(a)*rr*1.3));
        z=Math.max(-rr,Math.min(rr,Math.sin(a)*rr*1.3));tries++;
      }while(tries<20&&Math.hypot(x-player.x,z-player.z)<18);
      spawnEnemy(x,z,S.wave);S.toSpawn--;
    }
  }else if(alive===0&&!S.over){
    S.between-=dt;
    if(S.between<=0){
      if(S.wave>0){player.hp=Math.min(100,player.hp+25);for(const w of weapons)w.reserve+=w.magSize;banner("WAVE CLEARED",1200);}
      S.between=S.wave>0?3:.5;startWave();
    }
  }

  for(let i=enemies.length-1;i>=0;i--){
    const e=enemies[i];
    if(e.dead){e.deadT+=dt;if(e.deadT>3)enemies.splice(i,1);continue;}
    let dx=player.x-e.x,dz=player.z-e.z;const dist=Math.hypot(dx,dz)||1;dx/=dist;dz/=dist;
    e.yaw=Math.atan2(dx,dz);
    if(dist>1.4){e.x+=dx*e.speed*dt;e.z+=dz*e.speed*dt;e.phase+=dt*e.speed*2.2;}
    for(const o of enemies){
      if(o===e||o.dead)continue;
      const ex=e.x-o.x,ez=e.z-o.z,d=Math.hypot(ex,ez);
      if(d<.9&&d>1e-4){e.x+=ex/d*.9*dt*3;e.z+=ez/d*.9*dt*3;}
    }
    collideCircle(e,e.r,0,2.2);
    e.x=Math.max(-ARENA+.5,Math.min(ARENA-.5,e.x));
    e.z=Math.max(-ARENA+.5,Math.min(ARENA-.5,e.z));
    e.cd-=dt;
    if(dist<1.6&&e.cd<=0&&!S.over){e.cd=.9;hurtPlayer(8);}
    if(e.flashT>0)e.flashT-=dt;
  }
  for(let i=particles.length-1;i>=0;i--){
    const p=particles[i];p.life-=dt;p.vy-=9*dt;p.x+=p.vx*dt;p.y+=p.vy*dt;p.z+=p.vz*dt;
    if(p.life<=0)particles.splice(i,1);
  }
}

// ---------- Render ----------
function limb(base,hx,hy,hz,ang,w,h,d,col,emis){ // pivot at top of limb
  drawBox(chain(base,m4.trans(hx,hy,hz),m4.rotX(ang),m4.trans(0,-h/2,0),m4.scale(w,h,d)),col,emis||0,0);
}
function render(){
  const dpr=Math.min(devicePixelRatio||1,isTouch?1.5:2);
  const w=Math.floor(canvas.clientWidth*dpr),h=Math.floor(canvas.clientHeight*dpr);
  if(canvas.width!==w||canvas.height!==h){canvas.width=w;canvas.height=h;}
  gl.viewport(0,0,canvas.width,canvas.height);
  gl.clear(gl.COLOR_BUFFER_BIT|gl.DEPTH_BUFFER_BIT);

  let cx,cy,cz,yaw,pitch;
  if(playing){
    const hv=Math.hypot(player.vx,player.vz);
    cx=player.x;cz=player.z;cy=player.y+player.eye+Math.sin(bobT)*.045*Math.min(1,hv/5);
    yaw=player.yaw;pitch=player.pitch;
  }else{
    const t=(performance.now()-clockStart)*.0002;
    cx=Math.cos(t)*14;cz=Math.sin(t)*14;cy=4;yaw=Math.atan2(cx,cz);pitch=-.2;
  }
  fov+=((zoomed&&playing?W.zoomFov:75)-fov)*.3;
  const proj=m4.persp(fov*Math.PI/180,canvas.width/canvas.height,.05,200);
  const view=chain(m4.rotX(-pitch),m4.rotY(-yaw),m4.trans(-cx,-cy,-cz));
  const vp=m4.mul(proj,view);
  gl.useProgram(prog);
  gl.uniformMatrix4fv(U.uVP,false,vp);
  gl.uniform3f(U.uCam,cx,cy,cz);
  gl.uniform3fv(U.uFogCol,FOG);
  gl.uniform1f(U.uFog,1);

  // floor
  drawBox(chain(m4.trans(0,-.5,0),m4.scale(ARENA*2,1,ARENA*2)),hex(0x3a404e),0,1);
  // obstacles
  for(const o of obstacles)drawBox(chain(m4.trans(o.x,o.maxy/2,o.z),m4.scale(o.w,o.maxy,o.d)),o.col,0,0);
  // enemies
  for(const e of enemies){
    const fall=e.dead?Math.min(Math.PI/2,e.deadT*4):0;
    const sink=e.dead&&e.deadT>2?-(e.deadT-2)*1.5:0;
    const base=chain(m4.trans(e.x,sink,e.z),m4.rotY(e.yaw),m4.rotX(-fall));
    const fl=e.flashT>0;
    const cs=fl?C_WHITE:C_SKIN, cd=fl?C_WHITE:C_DARK;
    const sw=Math.sin(e.phase)*.8;
    drawBox(chain(base,m4.trans(0,1.15,0),m4.scale(.7,.9,.4)),cs,fl?1:0,0);
    drawBox(chain(base,m4.trans(0,1.85,0),m4.scale(.4,.4,.4)),cd,fl?1:0,0);
    drawBox(chain(base,m4.trans(0,1.88,.21),m4.scale(.3,.07,.05)),C_EYE,1,0);
    limb(base,-.18,.7,0, sw,.25,.7,.28,cd,fl?1:0);
    limb(base, .18,.7,0,-sw,.25,.7,.28,cd,fl?1:0);
    limb(base,-.47,1.55,0,-sw*.6-.8,.2,.7,.22,cs,fl?1:0);
    limb(base, .47,1.55,0, sw*.6-.8,.2,.7,.22,cs,fl?1:0);
  }
  // particles
  for(const p of particles){
    const s=.09*Math.min(1,p.life*2.5);
    drawBox(chain(m4.trans(p.x,p.y,p.z),m4.scale(s,s,s)),p.col,1,0);
  }
  // gun (camera space, drawn over everything)
  if(playing&&fov>40){
    gl.clear(gl.DEPTH_BUFFER_BIT);
    gl.uniformMatrix4fv(U.uVP,false,proj);
    gl.uniform1f(U.uFog,0);
    const hv=Math.hypot(player.vx,player.vz),k=Math.min(1,hv/5);
    let ang=W.recoil*.08;
    if(W.reloading)ang=-.6*Math.sin(Math.min(1,(W.reloadTime-W.reloadT)/W.reloadTime)*Math.PI);
    const sw=swapT>0?swapT/.3:0;
    const g=chain(m4.trans(W.off[0]+Math.cos(bobT*.5)*.012*k,W.off[1]+Math.abs(Math.sin(bobT))*.012*k-sw*.35,W.off[2]+W.recoil*.06),m4.rotX(ang-sw*.5));
    for(const b of W.model)drawBox(chain(g,m4.trans(b[0],b[1],b[2]),m4.scale(b[3],b[4],b[5])),b[6],0,0);
    if(W.flashT>0)drawBox(chain(g,m4.trans(0,.02,W.muzzle),m4.scale(.12,.12,.1)),hex(0xffcc55),1,0);
  }
}

function loop(now){
  requestAnimationFrame(loop);
  const dt=Math.min((now-last)/1000||0,.05);last=now;
  document.body.classList.toggle("nocursor",active()&&!S.over);
  if(active()&&!S.over)update(dt);
  render();
}
resetGame();
requestAnimationFrame(loop);
}

try{startGame();}catch(e){showErr("Startup failed: "+(e&&e.stack||e));}
</script>
</body>
</html>
