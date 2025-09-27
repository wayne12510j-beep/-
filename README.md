[Uploading 飞机.html…]()
{\rtf1\ansi\ansicpg936\cocoartf2709
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww25400\viewh12940\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 <!DOCTYPE html>\
<html lang="zh-CN">\
<head>\
<meta charset="UTF-8">\
<title>\uc0\u26216 \u27979 \u36215 \u39134 \u27036 </title>\
<meta name="viewport" content="width=device-width,initial-scale=1">\
<style>\
:root\{--radius:16px;--pad-gray:#616161;--runway:#ffeb3b\}\
*\{box-sizing:border-box;font-family:-apple-system,BlinkMacSystemFont,"PingFang SC","Helvetica Neue",Arial,sans-serif\}\
body\{margin:0;height:100vh;display:flex;flex-direction:column;background:#f5f5f5\}\
\
/* ===== \uc0\u31461 \u36259 \u24425 \u34425 \u39030 \u37096 \u65288 \u26080 \u20113 \u26421 \u65289  ===== */\
header\{\
  background:linear-gradient(90deg,#ff9a9e,#fecfef,#a8e6cf,#74b9ff,#a29bfe);\
  padding:18px 0 22px;\
  text-align:center;\
\}\
header h1\{\
  margin:0;font-size:28px;\
  color:#fff;text-shadow:0 2px 4px rgba(0,0,0,.2);\
  letter-spacing:1px;\
\}\
nav\{margin-top:10px\}\
nav button\{\
  margin:0 6px;padding:8px 16px;\
  border:none;border-radius:var(--radius);\
  font-size:14px;color:#fff;cursor:pointer;\
  box-shadow:0 2px 4px rgba(0,0,0,.2);\
  transition:transform .2s;\
\}\
nav button:hover\{transform:translateY(-2px)\}\
.btn-yellow\{background:#ffeb3b;color:#333\}\
.btn-pink\{background:#ff9a9e\}\
.btn-blue\{background:#74b9ff\}\
\
main\{flex:1;display:flex;overflow:hidden;padding:15px;gap:15px\}\
.area\{flex:1;border-radius:var(--radius);padding:15px;overflow-y:auto;position:relative\}\
#pad\{background:var(--pad-gray);background-image:repeating-linear-gradient(45deg,transparent,transparent 35px,rgba(255,255,255,.1) 35px,rgba(255,255,255,.1) 70px)\}\
#sky\{background:linear-gradient(180deg,#74b9ff,#a8e6cf)\}\
.cloud\{position:absolute;background:#fff;border-radius:50%;opacity:.7;animation:float 20s infinite ease-in-out\}\
.cloud1\{width:100px;height:40px;top:20%;left:10%;animation-duration:25s\}\
.cloud2\{width:80px;height:30px;top:40%;right:20%;animation-duration:30s\}\
@keyframes float\{0%,100%\{transform:translateX(0)\}50%\{transform:translateX(40px)\}\}\
.area h2\{margin:0 0 12px;font-size:20px;color:#fff;text-shadow:0 1px 3px rgba(0,0,0,.3)\}\
.group\{margin-bottom:15px\}\
.groupTitle\{font-size:16px;font-weight:600;margin-bottom:8px;color:#fff;text-shadow:0 1px 2px rgba(0,0,0,.3)\}\
.stuGrid\{display:grid;grid-template-columns:repeat(auto-fill,minmax(80px,1fr));gap:12px\}\
.student\{display:flex;flex-direction:column;align-items:center;cursor:pointer;user-select:none\}\
.student .plane\{font-size:42px;text-shadow:0 2px 4px rgba(0,0,0,.2);transition:transform .2s\}\
.student:hover .plane\{transform:scale(1.15) rotate(5deg)\}\
.nameBox\{margin-top:6px;background:#fff;border-radius:var(--radius);padding:4px 10px;font-size:13px;font-weight:500;box-shadow:0 2px 4px rgba(0,0,0,.1)\}\
footer\{text-align:center;font-size:12px;color:#666;padding:8px 0\}\
</style>\
</head>\
<body>\
<header>\
  <h1>\uc0\u26216 \u27979 \u36215 \u39134 \u27036 </h1>\
  <nav>\
    <button class="btn-yellow" onclick="randomCall()">\uc0\u38543 \u26426 \u28857 \u21517 </button>\
    <button class="btn-pink" onclick="clearAll()">\uc0\u19968 \u38190 \u36820 \u33322 </button>\
  </nav>\
</header>\
\
<main>\
  <section id="pad" class="area">\
    <h2>\uc0\u55357 \u57067  \u20572 \u26426 \u22378 \u65288 \u24453 \u39134 \u65289 </h2>\
    <div id="padContent"></div>\
  </section>\
  <section id="sky" class="area">\
    <div class="cloud cloud1"></div>\
    <div class="cloud cloud2"></div>\
    <h2>\uc0\u9729 \u65039  \u34013 \u22825 \u65288 \u24050 \u36215 \u39134 \u65289 </h2>\
    <div id="skyContent"></div>\
  </section>\
</main>\
\
<footer>\uc0\u25968 \u25454 \u27599  5 \u20998 \u38047 \u33258 \u21160 \u20445 \u23384 \u21040 \u26412 \u22320 \u27983 \u35272 \u22120 </footer>\
\
<script>\
const teams=[\{id:1,name:"\uc0\u31532 \u19968 \u32452 ",students:["\u21016 \u23567 \u29788 ","\u21009 \u22825 ","\u21556 \u20064 \u36828 ","\u21556 \u20043 \u28085 ","\u32993 \u26031 \u35821 ","\u36213 \u24311 \u24681 "]\},\{id:2,name:"\u31532 \u20108 \u32452 ",students:["\u37073 \u20048 \u29002 ","\u28504 \u33509 \u22925 ","\u21513 \u33521 \u30643 ","\u37073 \u20197 \u27819 ","\u24464 \u23431 \u21338 ","\u38047 \u37995 "]\},\{id:3,name:"\u31532 \u19977 \u32452 ",students:["\u27784 \u20896 \u26093 ","\u26446 \u26133 \u39056 ","\u33891 \u31859 \u22810 ","\u29579 \u23376 \u29788 ","\u21521 \u20026 \u29614 ","\u29579 \u21338 \u36828 "]\},\{id:4,name:"\u31532 \u22235 \u32452 ",students:["\u32918 \u28070 \u38738 ","\u34081 \u21807 \u35782 ","\u37073 \u33298 \u38597 ","\u23004 \u24605 \u23431 ","\u24352 \u39336 \u28982 ","\u21608 \u26970 \u25215 "]\},\{id:5,name:"\u31532 \u20116 \u32452 ",students:["\u26446 \u26223 \u29764 ","\u23002 \u32764 ","\u20005 \u23433 ","\u38498 \u20852 \u27721 ","\u38065 \u22025 \u23452 ","\u26446 \u38632 \u22025 "]\},\{id:6,name:"\u31532 \u20845 \u32452 ",students:["\u29579 \u26771 \u30651 ","\u21016 \u24681 \u38026 ","\u20505 \u20381 \u24420 ","\u37041 \u24609 \u21487 ","\u21608 \u38079 \u38632 ","\u27611 \u23376 \u38064 "]\},\{id:7,name:"\u31532 \u19971 \u32452 ",students:["\u20309 \u26771 \u40784 ","\u36830 \u36920 \u27954 ","\u20319 \u24605 \u40784 ","\u38470 \u36828 \u33322 ","\u26361 \u33853 \u22025 ","\u33406 \u40527 \u38660 "]\},\{id:8,name:"\u31532 \u20843 \u32452 ",students:["\u23731 \u40527 \u28059 ","\u26417 \u36920 \u25196 ","\u29579 \u23376 \u28904 ","\u23004 \u21016 \u19996 ","\u26417 \u24681 \u33841 ","\u32834 \u26199 \u34174 "]\}];\
let state=JSON.parse(localStorage.getItem("morningFly"))||\{\};\
\
function save()\{localStorage.setItem("morningFly",JSON.stringify(state))\}\
function randomCall()\{const all=teams.flatMap(t=>t.students);alert("\uc0\u24184 \u36816 \u21516 \u23398 \u65306 "+all[Math.floor(Math.random()*all.length)])\}\
function clearAll()\{if(!confirm("\uc0\u30830 \u23450 \u35753 \u25152 \u26377 \u39134 \u26426 \u36820 \u33322 \u65311 "))return;teams.forEach(t=>t.students.forEach(s=>state[s]="pad"));save();render()\}\
\
function toggleStu(name)\{\
  state[name]=state[name]==="sky"?"pad":"sky";\
  save();render();\
\}\
function createStu(name)\{\
  const d=document.createElement('div');d.className='student';\
  d.innerHTML=`<div class="plane">\uc0\u55357 \u57065 \u65039 </div><div class="nameBox">$\{name\}</div>`;\
  d.onclick=()=>toggleStu(name);\
  return d;\
\}\
function render()\{\
  const padBox=document.getElementById('padContent');\
  const skyBox=document.getElementById('skyContent');\
  padBox.innerHTML='';skyBox.innerHTML='';\
  teams.forEach(t=>\{\
    const [padStu,skyStu]=[[],[]];\
    t.students.forEach(s=>\{(state[s]==="sky"?skyStu:padStu).push(s)\});\
    if(padStu.length)\{const g=createGroup(t.name,padStu);padBox.appendChild(g)\}\
    if(skyStu.length)\{const g=createGroup(t.name,skyStu);skyBox.appendChild(g)\}\
  \});\
\}\
function createGroup(name,stus)\{\
  const g=document.createElement('div');g.className='group';\
  g.innerHTML=`<div class="groupTitle">$\{name\}</div><div class="stuGrid"></div>`;\
  const grid=g.querySelector('.stuGrid');\
  stus.forEach(n=>grid.appendChild(createStu(n)));\
  return g;\
\}\
\
/* \uc0\u21021 \u22987 \u21270  & \u23450 \u26102 \u20445 \u23384  */\
teams.forEach(t=>t.students.forEach(s=>\{if(!state[s])state[s]="pad"\}));\
save();render();\
setInterval(save,5*60*1000);\
</script>\
</body>\
</html>}
