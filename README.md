[Sasc.html](https://github.com/user-attachments/files/33598925/Sasc.html)
<!DOCTYPE html>
<html lang="pt-BR"><head><meta charset="utf-8"><title>Sasc</title>
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<style>
:root{--bg:#fff;--fg:#111;--card:#f2f2f5;--mut:#777;--ac:#d6249f;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme=light]){--bg:#0d0d10;--fg:#f4f4f6;--card:#1c1c22;--mut:#9a9aa5}}
*{box-sizing:border-box}html,body{height:100%;margin:0}
body{background:var(--bg);color:var(--fg);font:15px system-ui,sans-serif}
button,input,select{font:inherit;color:inherit}
.btn{background:var(--ac);color:#fff;border:0;border-radius:10px;padding:11px 16px;width:100%;font-weight:600;margin:3px 0}
.btn.s{background:var(--card);color:var(--fg)}.btn.r{background:#d92d20}.btn.m{width:auto;padding:7px 12px}
input[type=text],input[type=password],select{width:100%;padding:12px;border-radius:10px;border:1px solid var(--mut);background:var(--card);margin:4px 0}
#auth{max-width:340px;margin:0 auto;padding:40px 20px;text-align:center}
#auth h1{font-size:34px;background:linear-gradient(45deg,#f09433,#dc2743,#bc1888);-webkit-background-clip:text;color:transparent}
a{color:var(--ac);font-weight:600;cursor:pointer}
#app{display:none;height:100%;flex-direction:column}
#top{padding:8px 12px;display:flex;justify-content:space-between;align-items:center;min-height:50px}
#top b{font-size:20px}#clock{display:block;font-size:11px;color:var(--mut);text-align:center}
.ib{background:none;border:0;font-size:22px;position:relative;min-width:40px}
.bd{position:absolute;top:-2px;right:0;background:#e0245e;color:#fff;border-radius:9px;font-size:11px;font-style:normal;padding:1px 5px}
#main{flex:1;overflow-y:auto;scroll-snap-type:y mandatory}#main.feed{scroll-snap-type:none}
nav{display:flex;border-top:1px solid var(--card)}
nav button{flex:1;background:none;border:0;padding:13px 0;color:var(--mut);font-weight:600}nav button.on{color:var(--fg)}
#fab{position:fixed;right:16px;bottom:calc(70px + env(safe-area-inset-bottom,0px));width:54px;height:54px;border-radius:50%;border:0;background:var(--ac);color:#fff;font-size:30px;z-index:5}
.reel{position:relative;height:100%;scroll-snap-align:start;overflow:hidden;color:#fff;display:flex;align-items:flex-end}
.feed .reel{height:460px;margin:0 12px 14px;border-radius:16px}
.reel video,.reel .art{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}
.art{display:flex;align-items:center;justify-content:center;font-size:90px}
.info{position:relative;padding:14px;width:100%;background:linear-gradient(transparent,#000a)}
.tag{font-size:12px;opacity:.85}.ia{background:#fff3;border-radius:6px;padding:1px 6px;font-size:11px;margin-left:4px}
.av{width:30px;height:30px;border-radius:50%;object-fit:cover;vertical-align:middle;margin-right:6px;background:#888;display:inline-block}
.who{cursor:pointer;font-weight:700}
.dots{position:absolute;right:10px;top:10px;z-index:2;background:#0006;color:#fff;border:0;border-radius:50%;width:36px;height:36px;font-size:20px}
.menu{position:absolute;right:10px;top:50px;z-index:3;background:var(--bg);color:var(--fg);border-radius:12px;box-shadow:0 4px 18px #0006;overflow:hidden}
.menu button{display:block;width:100%;background:none;border:0;padding:12px 16px;text-align:left;white-space:nowrap}
.ov{position:fixed;inset:0;background:#000c;z-index:20;display:flex;align-items:center;justify-content:center;padding:20px}
.box{background:var(--bg);border-radius:16px;padding:20px;width:100%;max-width:360px;max-height:90%;overflow:auto}
.box h3{margin-top:0}label.l{display:block;margin:8px 0 2px;font-size:13px;color:var(--mut)}
#toast{position:fixed;left:12px;right:12px;bottom:calc(76px + env(safe-area-inset-bottom,0px));background:var(--card);border-radius:14px;padding:12px;z-index:30;display:none;box-shadow:0 4px 18px #0005}
#toast div{display:flex;gap:8px;margin-top:8px}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:3px;padding:3px}
.grid div{aspect-ratio:9/14;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center;font-size:36px;color:#fff;cursor:pointer}
.grid video{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}.grid span{position:absolute;bottom:3px;left:4px;font-size:10px}
.pad{padding:16px}.c{text-align:center}.prof .av{width:84px;height:84px;margin:0}
.err{color:#e0245e;font-size:13px;min-height:18px}
.row{display:flex;align-items:center;gap:10px;padding:10px 0;border-bottom:1px solid var(--card);cursor:pointer}.row>div{flex:1}
.mut{color:var(--mut);font-size:13px}
.tabs{display:flex;gap:8px;margin-bottom:12px}
.msg{max-width:78%;padding:8px 12px;border-radius:14px;margin:4px 0;background:var(--card);word-wrap:break-word}.msg.me{background:var(--ac);color:#fff;margin-left:auto}
.acts button{background:#0006;color:#fff;border:0;border-radius:14px;padding:6px 12px;margin:6px 6px 0 0;font-size:14px}.ofc{background:#1d9bf0;color:#fff;border-radius:8px;padding:1px 6px;font-size:11px;font-weight:700;white-space:nowrap}
.chip{display:inline-block;background:var(--card);border-radius:8px;padding:4px 10px;margin:3px;font-size:13px}
</style></head><body>
<div id="auth"></div>
<div id="app"><div id="top"></div><div id="main"></div>
<button id="fab" aria-label="Postar">+</button>
<nav><button data-t="home">Início</button><button data-t="reels">Reels</button><button data-t="prof">Perfil</button></nav></div>
<div id="toast"></div><div id="modal"></div>
<script>
const $=s=>document.querySelector(s),esc=s=>String(s??'').replace(/[&<>"]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
let S;try{S=JSON.parse(localStorage.getItem('sasc')||'')}catch(e){}
S=S||{};S.users=S.users||{};S.follow=S.follow||{};S.fr=S.fr||{};S.chats=S.chats||{};S.notes=S.notes||{};S.likes=S.likes||{};S.cm=S.cm||{};S.hidden=S.hidden||[];S.rep=S.rep||{};S.vw=S.vw||{};S.keep=S.keep||{};S.mods=S.mods||[];S.dreq=S.dreq||[];
for(const[k,u]of Object.entries(S.users))if(!u.uid){u.uid=k;u.handle=k;u.name=k}
S.users.sasc={uid:'sasc',sys:true,handle:'sasc.protecao',name:'Sasc Proteção',pw:Math.random()+'x',photo:'data:image/svg+xml,'+encodeURIComponent('<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64"><rect width="64" height="64" fill="#1d9bf0"/><text x="32" y="44" font-size="34" text-anchor="middle">🛡️</text></svg>'),usage:0,blockedUntil:0,prefs:{},link:{}};
let raw='';try{raw=localStorage.getItem('sasc')||''}catch(e){}
const save=()=>{try{const s=JSON.stringify(S);localStorage.setItem('sasc',s);raw=s;sessionStorage.setItem('ss',S.session||'')}catch(e){}};
try{const ss=sessionStorage.getItem('ss');if(ss!==null)S.session=ss||null}catch(e){}
addEventListener('pagehide',save);document.addEventListener('visibilitychange',save);
/* vídeos no IndexedDB */
let db,mine=[];
const idb=()=>new Promise(r=>{try{const q=indexedDB.open('sasc',1);q.onupgradeneeded=()=>q.result.createObjectStore('r',{keyPath:'id'});q.onsuccess=()=>{db=q.result;const g=db.transaction('r').objectStore('r').getAll();g.onsuccess=()=>{mine=g.result.map(x=>({...x,src:URL.createObjectURL(x.blob)})).sort((a,b)=>b.id-a.id);r()};g.onerror=()=>r()};q.onerror=()=>r()}catch(e){r()}});
const put=r=>{try{const{src,...x}=r;db.transaction('r','readwrite').objectStore('r').put(x)}catch(e){}S.rv=Date.now();save()};
const del=id=>{try{db.transaction('r','readwrite').objectStore('r').delete(id)}catch(e){}S.rv=Date.now();save()};
function loadMine(cb){try{const g=db.transaction('r').objectStore('r').getAll();g.onsuccess=()=>{const old=mine.map(x=>x.id).join(),m=new Map(mine.map(x=>[x.id,x]));mine=g.result.map(x=>({...x,src:m.has(x.id)?m.get(x.id).src:URL.createObjectURL(x.blob)})).sort((a,b)=>b.id-a.id);if(cb)cb(old!==mine.map(x=>x.id).join())}}catch(e){}}
const demo=[{id:1,by:'ana.viaja',name:'Pôr do sol na praia',theme:'Viagem',ai:false,e:'🌅'},{id:2,by:'chef_leo',name:'Brigadeiro em 5 minutos',theme:'Culinária',ai:false,e:'🍫'},{id:3,by:'gamer.zi',name:'Melhor jogada da semana',theme:'Games',ai:false,e:'🎮'},{id:4,by:'ia.arte',name:'Cidade do futuro',theme:'Arte',ai:true,e:'🏙️'},{id:5,by:'bola_na_rede',name:'Golaço de bicicleta',theme:'Esportes',ai:false,e:'⚽'},{id:6,by:'riso.facil',name:'Gato vs. pepino',theme:'Humor',ai:false,e:'😹'}];
const G=['linear-gradient(135deg,#f09433,#dc2743)','linear-gradient(135deg,#4facfe,#00f2fe)','linear-gradient(135deg,#43e97b,#38f9d7)','linear-gradient(135deg,#a18cd1,#fbc2eb)','linear-gradient(135deg,#fa709a,#fee140)','linear-gradient(135deg,#667eea,#764ba2)'];
const all=()=>mine.concat(demo).filter(r=>!S.hidden.includes(r.id)&&(!r.hold||r.by===S.session||adm())),me=()=>S.session,U=()=>S.users[S.session],hd=id=>S.users[id]?S.users[id].handle:id,byH=h=>Object.values(S.users).find(u=>u.handle===h);
let first=null,tab='home',mult=1,views=0,ctr=0,vw=null,thr=null,setTab='c',pend=null,asked={};
const ck=(a,b)=>[a,b].sort().join('|');
const fol=(a,b)=>(S.follow[a]||[]).includes(b),mutual=(a,b)=>fol(a,b)&&fol(b,a);
const friends=(a,b)=>mutual(a,b)&&(S.fr[a]||[]).includes(b)&&(S.fr[b]||[]).includes(a);
const pendN=()=>Object.values(S.chats).filter(c=>!c.acc&&c.to===me()).length;
const note=(to,type,txt,ref)=>{S.notes[to]=[{type,txt,ref,ts:Date.now(),r:0}].concat(S.notes[to]||[]).slice(0,60)};
const unread=()=>(S.notes[me()]||[]).filter(n=>!n.r).length;
const ADMPW='!123@CA@321!';
const adm=()=>{const u=U();return !!(u&&u.owner&&u.admin)};
const isOwn=()=>{const u=U();return !!(u&&(u.owner||u.handle==='callebe'))};
const ofc=id=>S.users[id]&&S.users[id].owner?' <span class="ofc">✔ Oficial</span>':'';
const pres=(u,k)=>{const p=(u.pres||{})[k];return p&&((u.vis||{})[k]||u.uid===me())?' · '+esc(p):''};
const link=id=>'https://claude.ai/artifact/Bji8Wwed714toV7XRDufEz#reel='+id;
function cp2(t){const a=document.createElement('textarea');a.value=t;document.body.appendChild(a);a.select();try{document.execCommand('copy');toast('Link copiado!')}catch(e){toast(t)}a.remove()}
function copy(t){try{navigator.clipboard.writeText(t).then(()=>toast('Link copiado!'),()=>cp2(t))}catch(e){cp2(t)}}
const lk=id=>(S.likes[id]||[]).length;
const isMod=()=>S.mods.includes(me());
const DCLINK='https://discord.com/oauth2/authorize?client_id=1560981826644869181&response_type=code&redirect_uri=https%3A%2F%2Fclaude.ai%2Fartifact%2FBji8Wwed714toV7XRDufEz&scope=identify+openid';
let gOff=false,gdb=null;
const dcOff=()=>!!(S.dcOff||gOff);
(async()=>{try{if(!window.claude)return;gdb=await claude.use('db');if(!gdb)return;gdb.doc('flags/discord').onSnapshot(s=>{const o=!!(s.exists&&s.data()&&s.data().off);if(o!==gOff){gOff=o;if(me()&&tab==='set'&&setTab==='a'&&!$('#modal').innerHTML&&!$('#bk2'))sets()}},()=>{})}catch(e){}})();
async function setDc(v){S.dcOff=v;save();modal('');let msg=v?'Vinculação com o Discord parada.':'Vinculação com o Discord reativada.';
 if(gdb){try{await gdb.doc('flags/discord').set({off:v,t:Date.now()});gOff=v}catch(e){msg+=' Mas não consegui avisar os outros aparelhos ('+(e&&e.code||'erro')+').'}}
 else msg+=' Vale só neste aparelho: o aviso para os outros não está disponível.';
 toast(msg);if(tab==='set')adminV()}
const prot=(to,x)=>{if(!S.users[to])return;const k=ck('sasc',to),c=S.chats[k]=S.chats[k]||{from:'sasc',to,acc:true,m:[]};c.m.push({f:'sasc',x,t:Date.now()});note(to,'sys',x.slice(0,70),k)};
const flagged=r=>{if(S.keep[r.id])return false;const v=(S.vw[r.id]||[]).length,n=(S.rep[r.id]||[]).length;return v>=2&&n/v>=.3};
function view1(r){const a=S.vw[r.id]=S.vw[r.id]||[];if(!a.includes(me())){a.push(me());save()}}
const lnk=x=>esc(x).replace(/https?:\/\/\S*?reel=(\d+)/g,(m,i)=>`<a data-rl="${i}">abrir reel</a>`);
function openReel(id){if(!all().find(r=>r.id==id))return toast('Esse reel não existe mais');show('reels',id)}
function frames(f){return new Promise(res=>{const v=document.createElement('video'),u=URL.createObjectURL(f),out=[];v.muted=true;v.playsInline=true;v.preload='auto';v.src=u;const end=()=>{URL.revokeObjectURL(u);res(out)};setTimeout(end,15000);v.onerror=end;
 v.onloadedmetadata=async()=>{const d=v.duration||1;try{for(const p of [.15,.4,.65,.9]){await new Promise(r=>{v.onseeked=r;v.currentTime=Math.min(p*d,Math.max(d-.05,0))});const c=document.createElement('canvas');c.width=320;c.height=Math.round(320*(v.videoHeight/v.videoWidth))||180;c.getContext('2d').drawImage(v,0,0,c.width,c.height);out.push(await new Promise(r=>c.toBlob(r,'image/jpeg',.7)))}}catch(e){}end()}})}
async function review(f,nm,th){try{const s=window.claude&&await claude.use('sample');if(!s)return 'na';const im=await frames(f);if(!im.length)return 'na';
 const r=await s(`Você é revisor de segurança de uma rede social. Título do vídeo: "${nm}". Tema: "${th}". Veja os quadros anexados. Marque flag=true SOMENTE se mostrarem claramente: conteúdo sexual envolvendo menores ou menores em contexto sexualizado, nudez explícita ou atos sexuais, ou violência gráfica extrema. NÃO exagere: crianças brincando, praia, família, esportes e conteúdo comum são OK. Responda só JSON: {"flag":true,"why":"motivo curto"} ou {"flag":false}`,{images:im,modelTier:'quick',cache:false});
 const j=JSON.parse((r.text.match(/\{[\s\S]*\}/)||['{}'])[0]);return j.flag?'flag':'ok'}catch(e){return 'na'}}
function reportF(r){if(r.by===me())return toast('Você não pode denunciar o próprio reel');if((S.rep[r.id]||[]).some(x=>x.u===me()))return toast('Você já denunciou este reel');
 modal(`<h3>Denunciar reel</h3><label class="l">Motivo</label><select id="rs"><option>Conteúdo sexual</option><option>Conteúdo envolvendo menores</option><option>Violência</option><option>Assédio ou ódio</option><option>Spam ou golpe</option><option>Outro</option></select><label class="l">Mensagem (opcional)</label><input id="rx" type="text" placeholder="Conte o que aconteceu"><button class="btn" id="ok">Enviar denúncia</button><button class="btn s" id="cc">Cancelar</button>`);
 $('#cc').onclick=()=>modal('');
 $('#ok').onclick=()=>{(S.rep[r.id]=S.rep[r.id]||[]).push({u:me(),w:$('#rs').value,x:$('#rx').value.trim(),t:Date.now()});view1(r);Object.keys(S.users).forEach(k=>{if(S.users[k].owner)note(k,'rp',(flagged(r)?'Reel muito denunciado: ':'Nova denúncia: ')+r.name,r.id)});save();modal('');toast('Denúncia enviada. Obrigado por ajudar o Sasc a ser seguro.')}}
function dreqF(r){modal(`<h3>Pedir exclusão</h3><p>Deseja enviar uma mensagem ao administrador?</p><div id="qa"><button class="btn" id="y1">Sim, escrever</button><button class="btn s" id="n1">Não, só pedir</button></div><div id="qb" style="display:none"><input id="qx" type="text" placeholder="Mensagem ao administrador"><button class="btn" id="go2">Enviar pedido</button></div><button class="btn s" id="cc">Cancelar</button>`);
 const send=x=>{S.dreq.push({id:Date.now(),rid:r.id,rn:r.name,by:me(),x,t:Date.now()});Object.keys(S.users).forEach(k=>{if(S.users[k].owner)note(k,'dq','@'+U().handle+' pediu para excluir: '+r.name,r.id)});save();modal('');toast('Pedido enviado ao administrador')};
 $('#cc').onclick=()=>modal('');$('#y1').onclick=()=>{$('#qa').style.display='none';$('#qb').style.display=''};$('#n1').onclick=()=>send('');$('#go2').onclick=()=>send($('#qx').value.trim())}
function like(r){const a=S.likes[r.id]=S.likes[r.id]||[],i=a.indexOf(me());if(i>=0)a.splice(i,1);else{a.push(me());if(r.by!==me())note(r.by,'lk','@'+U().handle+' curtiu seu reel: '+r.name,r.id)}save()}
function rdel(r,why){const i=mine.indexOf(r);if(i>=0){mine.splice(i,1);del(r.id)}else S.hidden.push(r.id);prot(r.by,'Seu reel "'+r.name+'" ('+link(r.id)+') foi deletado '+(why==='rep'?'por denúncias':'por um administrador')+'.');S.dreq=S.dreq.filter(q=>q.rid!==r.id);delete S.likes[r.id];delete S.cm[r.id];save()}
const stat=(u,k)=>{const o=k==='roblox'?['Offline','Jogando Roblox']:['Offline','Online','Ausente','Não perturbe'],p=(u.pres||{})[k]||'Offline';return `<div style="padding:6px 0 12px"><select data-ps="${k}">${o.map(x=>`<option ${x===p?'selected':''}>${x}</option>`).join('')}</select><label class="mut"><input type="checkbox" data-pv="${k}" ${(u.vis||{})[k]?'checked':''}> Mostrar meu status para amigos</label></div>`};
const ago=t=>{const m=Math.floor((Date.now()-t)/6e4);return m<1?'agora':m<60?m+' min atrás':m<1440?Math.floor(m/60)+' h atrás':Math.floor(m/1440)+' d atrás'};
const nz=s=>String(s||'').normalize('NFD').replace(/[\u0300-\u036f]/g,'').toLowerCase();
/* auth */
function authView(su){
 $('#auth').style.display='block';$('#app').style.display='none';
 $('#auth').innerHTML=`<h1>Sasc</h1><p class="mut">${su?'Crie sua conta':'Entre na sua conta'}</p>
 ${su?`<div style="margin:10px 0"><img id="pv" class="av" style="width:84px;height:84px;margin:0" alt=""><br><label class="btn s m" style="display:inline-block;margin-top:8px">Escolher foto de perfil<input id="ph" type="file" accept="image/*" hidden></label></div>`:''}
 <input id="h" type="text" placeholder="@ localizador" autocapitalize="none"><input id="p" type="password" placeholder="Senha"><input id="ap" type="password" placeholder="Senha de administrador" style="display:none">
 <div class="err" id="er"></div><button class="btn" id="go">${su?'Cadastrar':'Entrar'}</button>
 <p>${su?'Já tem conta? <a id="sw">Entrar</a>':'Você não tem uma conta? <a id="sw">Clique aqui!</a>'}</p>`;
 let photo='';$('#sw').onclick=()=>authView(!su);
 if(su)$('#ph').onchange=e=>resize(e.target.files[0],d=>{photo=d;$('#pv').src=d});
 $('#go').onclick=()=>{const h=$('#h').value.trim().replace(/^@/,'').toLowerCase(),p=$('#p').value,er=$('#er');
  if(!/^[a-z0-9_.]{3,20}$/.test(h))return er.textContent='O @ deve ter 3 a 20 letras, números, _ ou .';
  if(su){if(h==='callebe'&&(p!==ADMPW||byH(h)))return er.textContent='Não foi possível criar a conta.';if(p.length<4)return er.textContent='A senha precisa de 4+ caracteres';
   if(byH(h)||demo.some(r=>r.by===h))return er.textContent='Esse @ já existe';
   
   if(!photo)return er.textContent='Coloque uma foto de perfil';
   const id='u'+Date.now();Object.keys(S.users).forEach(k=>note(k,'acc','@'+h+' criou uma conta no Sasc',id));S.users[id]={uid:id,handle:h,name:h,pw:p,photo,usage:0,blockedUntil:0,prefs:{},rested:false,phone:'',link:{},owner:h==='callebe',admin:h==='callebe'};S.session=id}
  else{const u=byH(h);if(!u||u.pw!==p)return er.textContent='@ ou senha incorretos';S.session=u.uid}
  save();enter()}}
function resize(f,cb){if(!f)return;const r=new FileReader();r.onload=()=>{const i=new Image();i.onload=()=>{const c=document.createElement('canvas');c.width=c.height=128;const m=Math.min(i.width,i.height);c.getContext('2d').drawImage(i,(i.width-m)/2,(i.height-m)/2,m,m,0,0,128,128);cb(c.toDataURL('image/jpeg',.8))};i.src=r.result};r.readAsDataURL(f)}
function enter(){const u=U();if(u.blockedUntil&&Date.now()<u.blockedUntil)return blockView();
 if(u.blockedUntil){u.blockedUntil=0;u.usage=0;u.rested=false;save()}
 $('#auth').style.display='none';$('#app').style.display='flex';show('home');{const hm=(location.hash+location.search+document.referrer).match(/reel=(\d+)/);if(hm)setTimeout(()=>openReel(hm[1]),50)}if(unread())toast('Você tem '+unread()+' notificação(ões) nova(s) 🔔')}
function blockView(){const l=U().blockedUntil-Date.now();
 $('#app').style.display='none';$('#auth').style.display='block';
 $('#auth').innerHTML=`<h1>Pausa</h1><p>Você está no limite de uso. Volte em <b>${Math.floor(l/36e5)}h ${Math.ceil(l%36e5/6e4)}min</b>.</p><button class="btn s" id="lo">Sair</button>`;
 $('#lo').onclick=logout}
function logout(){save();S.session=null;save();authView(false)}
/* tempo de uso */
setInterval(()=>{if(!me()||$('#app').style.display!=='flex'||document.hidden)return;
 const u=U();u.usage+=mult;const c=$('#clock');if(c)c.textContent=`Hoje: ${Math.floor(u.usage/60)} de 180 min`;
 if(u.usage>=10800){u.blockedUntil=Date.now()+432e5;save();return blockView()}
 if(u.usage>=3600&&!u.rested){u.rested=true;rest()}
 if(++ctr%10===0){save();degr()}},1000);
function degr(){const u=U(),f=u.usage>9000?Math.min(1,(u.usage-9000)/1800):0;document.querySelectorAll('.reel video,.reel .art').forEach(e=>e.style.filter=f?`blur(${(f*6).toFixed(1)}px) grayscale(${f}) contrast(${1-f*.4})`:'')}
function rest(){modal(`<h3>Hora de dar um tempo 🌿</h3><p>Você já está há 1 hora no app. Que tal descansar os olhos?</p><button class="btn" id="br">Pausa de 5 minutos</button><button class="btn s" id="ct">Continuar</button>`);
 $('#br').onclick=()=>{U().blockedUntil=Date.now()+3e5;save();modal('');blockView()};$('#ct').onclick=()=>modal('')}
/* cabeçalho e telas */
function hdr(){const u=unread(),sb='<button class="ib" id="sb">🔍</button>',nb=`<button class="ib" id="nb">🔔${u?`<i class="bd">${u}</i>`:''}</button>`,n=pendN(),g='<button class="ib" id="gb">⚙️</button>',c=`<button class="ib" id="cb">💬${n?`<i class="bd">${n}</i>`:''}</button>`;
 const back=['set','thread','user','search','notes'].includes(tab);
 $('#top').innerHTML=`${back?'<button class="ib" id="bk">←</button>':tab==='prof'?'<b>Sasc</b>':g}<span><b>${tab==='prof'?'Conta':'Sasc'}</b><span id="clock"></span></span>${back?'<span style="min-width:40px"></span>':'<span>'+sb+nb+(tab==='prof'?g:c)+'</span>'}`;
 const q=s=>$(s);if(q('#sb'))q('#sb').onclick=()=>show('search');if(q('#nb'))q('#nb').onclick=()=>show('notes');if(q('#gb'))q('#gb').onclick=()=>show('set');if(q('#cb'))q('#cb').onclick=()=>show('chat');if(q('#bk'))q('#bk').onclick=()=>show(tab==='thread'?'chat':'home')}
function show(t,a){tab=t;if(t==='user')vw=a;if(t==='thread')thr=a;if(t==='reels')first=a;
 document.querySelectorAll('nav button').forEach(b=>b.classList.toggle('on',b.dataset.t===t));
 $('#fab').style.display=['home','reels','prof'].includes(t)?'':'none';
 const m=$('#main');m.className=t==='reels'?'':'feed';m.scrollTop=0;hdr();
 ({home:feed,reels:feed,prof:()=>prof(me()),user:()=>prof(vw),chat:chat,thread:thread,set:sets,search:srch,notes:notesV})[t]()}
function feed(){const p=U().prefs,sc=r=>(p[r.theme]||0)-(flagged(r)?100:0),l=all().sort((a,b)=>sc(b)-sc(a));if(tab==='reels'&&first){const i=l.findIndex(r=>r.id==first);if(i>0)l.unshift(l.splice(i,1)[0])}
 $('#main').innerHTML=l.map(card).join('');
 document.querySelectorAll('.dots').forEach(b=>b.onclick=e=>{e.stopPropagation();menu(b)});
 document.querySelectorAll('.who').forEach(w=>w.onclick=()=>S.users[w.dataset.by]&&show('user',w.dataset.by));
 document.querySelectorAll('[data-lk]').forEach(b=>b.onclick=()=>{const r=all().find(x=>x.id==b.dataset.lk);like(r);b.textContent=((S.likes[r.id]||[]).includes(me())?'❤️ ':'🤍 ')+lk(r.id)});
 document.querySelectorAll('[data-cm]').forEach(b=>b.onclick=()=>viewReel(b.dataset.cm));
 document.querySelectorAll('[data-cp]').forEach(b=>b.onclick=()=>copy(link(b.dataset.cp)));
 const io=new IntersectionObserver(es=>es.forEach(en=>{const v=en.target.querySelector('video');
  if(en.isIntersecting&&en.intersectionRatio>.6){if(v&&tab==='reels')v.play().catch(()=>{});seen(+en.target.dataset.id)}else if(v&&tab==='reels')v.pause()}),{threshold:[.6]});
 document.querySelectorAll('.reel').forEach(r=>io.observe(r));degr()}
function card(r){const u=S.users[r.by];
 return `<div class="reel" data-id="${r.id}" style="background:${G[r.id%6]}">${r.src?`<video src="${r.src}" loop playsinline ${tab==='reels'?'':'controls'}></video>`:`<div class="art">${r.e||'🎬'}</div>`}
 <button class="dots" data-id="${r.id}">⋯</button><div class="info">${u?`<img class="av" src="${u.photo}" alt="">`:'<span class="av"></span>'}<span class="who" data-by="${r.by}">@${esc(hd(r.by))}</span>${ofc(r.by)}<br><b>${esc(r.name)}</b><br><span class="tag">#${esc(r.theme)}${r.ai?'<span class="ia">Feito com IA</span>':''}${r.hold?'<span class="ia">Em revisão</span>':''}</span><div class="acts"><button data-lk="${r.id}">${(S.likes[r.id]||[]).includes(me())?'❤️':'🤍'} ${lk(r.id)}</button><button data-cm="${r.id}">💬 ${(S.cm[r.id]||[]).length}</button><button data-cp="${r.id}">🔗</button></div></div></div>`}
function menu(b){document.querySelectorAll('.menu').forEach(m=>m.remove());
 const r=all().find(x=>x.id==b.dataset.id),m=document.createElement('div');m.className='menu';
 m.innerHTML=`<button data-a="l">👍 Gostei deste reel</button><button data-a="d">👎 Não gostei deste reel</button><button data-a="r">🚩 Denunciar</button>${isMod()&&!adm()?'<button data-a="q">🗑️ Pedir exclusão</button>':''}<button data-a="c">🔗 Copiar link</button>${adm()?'<button data-a="x">🗑️ Apagar (admin)</button>':''}${r.by===me()?'<button data-a="e">✏️ Editar vídeo</button>':''}`;
 b.parentNode.appendChild(m);
 m.onclick=e=>{const a=e.target.dataset.a;if(!a)return;m.remove();if(a==='r')return reportF(r);if(a==='q')return dreqF(r);if(a==='e')return postForm(r);if(a==='c')return copy(link(r.id));if(a==='x'){rdel(r);show(tab,vw);return toast('Vídeo apagado pelo administrador')}
  const p=U().prefs;p[r.theme]=(p[r.theme]||0)+(a==='l'?2:-2);save();toast(a==='l'?'Que bom! Vamos mostrar mais assim.':'Ok, vamos mostrar menos assim.')};
 setTimeout(()=>document.addEventListener('click',()=>m.remove(),{once:true}),0)}
function seen(id){const rr=all().find(x=>x.id===id);if(rr)view1(rr);if(++views%4!==0)return;const r=all().find(x=>x.id===id);if(!r||asked[r.theme]===views)return;asked[r.theme]=views;
 const t=$('#toast');t.style.display='block';
 t.innerHTML=`Você gosta de conteúdo de <b>${esc(r.theme)}</b>?<div><button class="btn" id="y">Sim</button><button class="btn s" id="n">Não</button></div>`;
 const f=v=>{const p=U().prefs;p[r.theme]=(p[r.theme]||0)+v;save();t.style.display='none'};$('#y').onclick=()=>f(3);$('#n').onclick=()=>f(-3)}
function toast(m){const t=$('#toast');t.style.display='block';t.textContent=m;setTimeout(()=>t.style.display='none',2600)}
/* perfil */
function prof(id){const u=S.users[id],own=id===me(),l=all().filter(r=>r.by===id),M=me();
 const fc=Object.values(S.follow).filter(a=>a.includes(id)).length,fg=(S.follow[id]||[]).length,fr=!own&&friends(M,id);
 let act='';
 if(!own){act=`<button class="btn m" id="fl">${fol(M,id)?'Seguindo ✓':'Seguir'}</button> <button class="btn s m" id="ms">Mensagem</button>`;
  if(mutual(M,id)){const mk=(S.fr[M]||[]).includes(id);act+=`<br><select id="fs" style="width:auto"><option value="s">Seguidor</option><option value="a" ${mk?'selected':''}>Amigo</option></select>${mk&&!fr?'<div class="mut">Aguardando a outra pessoa marcar você como amigo</div>':''}`}}
 const info=(fr||own)?`<div>${u.link?.roblox?`<span class="chip">🎮 Roblox: ${esc(u.link.roblox)}${pres(u,'roblox')}</span>`:''}${u.link?.discord?`<span class="chip">💬 Discord: ${esc(u.link.discord)}${pres(u,'discord')}</span>`:''}${u.phone?`<span class="chip">📱 ${esc(u.phone)}</span>`:''}</div>`:'';
 $('#main').innerHTML=`<div class="pad c prof"><img class="av" src="${u.photo}" alt=""><h2 style="margin:8px 0 0">${esc(u.name)}${ofc(id)}</h2><div class="mut">@${esc(u.handle)}${u.owner?' · Dono do App':''}</div>
 <div class="mut">${l.length} reels · ${fc} seguidores · ${fg} seguindo</div>${fr?'<div class="mut">👫 Amigos</div>':''}${info}<div style="margin-top:10px">${act}</div>
 ${own?`<label class="mut" style="display:block;margin:12px 0"><input type="checkbox" id="sp" ${mult>1?'checked':''}> Modo teste (tempo 60× mais rápido)</label><button class="btn s" id="lo">Sair</button>`:''}</div>
 <div class="grid">${l.map(r=>`<div data-id="${r.id}" style="background:${G[r.id%6]}">${r.src?`<video src="${r.src}" muted></video>`:'🎬'}<span>${esc(r.name)}</span></div>`).join('')}</div>`;
 if(own){$('#sp').onchange=e=>mult=e.target.checked?60:1;$('#lo').onclick=logout;
  }
 document.querySelectorAll('.grid div').forEach(d=>d.onclick=()=>viewReel(d.dataset.id));
 if(!own){$('#fl').onclick=()=>{const a=S.follow[M]=S.follow[M]||[];if(fol(M,id)){a.splice(a.indexOf(id),1);[M,id].forEach(x=>{const o=x===M?id:M,f=S.fr[x];if(f&&f.includes(o))f.splice(f.indexOf(o),1)})}else{a.push(id);note(id,'fol','@'+U().handle+' começou a seguir você',M)}save();prof(id)};
  $('#ms').onclick=()=>openChat(id);
  if($('#fs'))$('#fs').onchange=e=>{const a=S.fr[M]=S.fr[M]||[],i=a.indexOf(id);if(e.target.value==='a'&&i<0)a.push(id);if(e.target.value==='s'&&i>=0)a.splice(i,1);save();prof(id)}}}
/* chat */
function openChat(id){const k=ck(me(),id);if(!S.chats[k]){if(friends(me(),id))S.chats[k]={from:me(),to:id,acc:true,m:[]};else S.chats[k]={from:me(),to:id,acc:false,m:[]};}show('thread',k)}
function chat(){const M=me(),cs=Object.entries(S.chats).filter(([k,c])=>c.from===M||c.to===M);
 const row=([k,c])=>{const o=c.from===M?c.to:c.from,u=S.users[o];if(!u)return'';const l=c.m[c.m.length-1];
  return `<div class="row" data-k="${k}"><img class="av" src="${u.photo}" alt=""><div><b>${esc(u.name)}</b> ${friends(M,o)?'👫':''}<div class="mut">${l?esc(l.x).slice(0,40):'Sem mensagens'}</div></div></div>`};
 const rq=cs.filter(([k,c])=>!c.acc&&c.to===M),ok=cs.filter(([k,c])=>c.acc||c.from===M);
 $('#main').innerHTML=`<div class="pad"><input id="sq" type="text" placeholder="Enviar mensagem para @..." autocapitalize="none"><div class="err" id="er"></div>
 ${rq.length?`<h4>Pedidos de mensagem</h4>${rq.map(([k,c])=>{const u=S.users[c.from];return `<div class="row"><img class="av" src="${u.photo}" alt=""><div><b>@${esc(u.handle)}</b><div class="mut">${esc(c.m[0]?.x||'').slice(0,50)}</div></div><button class="btn m" data-a="${k}">Aceitar</button><button class="btn s m" data-i="${k}">Ignorar</button></div>`}).join('')}`:''}
 <h4>Conversas</h4>${ok.map(row).join('')||'<p class="mut">Nenhuma conversa ainda. Procure um @ acima ou fale com amigos.</p>'}</div>`;
 $('#sq').onkeydown=e=>{if(e.key!=='Enter')return;const u=byH(e.target.value.trim().replace(/^@/,'').toLowerCase());
  if(!u||u.sys||u.uid===M)return $('#er').textContent='@ não encontrado';openChat(u.uid)};
 document.querySelectorAll('.row[data-k]').forEach(r=>r.onclick=()=>show('thread',r.dataset.k));
 document.querySelectorAll('[data-a]').forEach(b=>b.onclick=()=>{S.chats[b.dataset.a].acc=true;save();hdr();chat()});
 document.querySelectorAll('[data-i]').forEach(b=>b.onclick=()=>{delete S.chats[b.dataset.i];save();hdr();chat()})}
function thread(){const M=me(),c=S.chats[thr],o=c.from===M?c.to:c.from,u=S.users[o],wait=!c.acc&&c.from===M&&c.m.length>0;
 $('#main').innerHTML=`<div class="pad"><div class="row" style="cursor:default"><img class="av" src="${u.photo}" alt=""><div><b>${esc(u.name)}</b><div class="mut">@${esc(u.handle)}</div></div></div><div id="ms">${c.m.map(m=>`<div class="msg ${m.f===M?'me':''}">${lnk(m.x)}</div>`).join('')}</div>
 ${o==='sasc'?'<p class="mut">Mensagem automática do Sasc Proteção. Não é possível responder.</p>':!c.acc&&c.to===M?'<p class="mut">Aceite o pedido na tela de chat para responder.</p>':wait?'<p class="mut">Aguardando a pessoa aceitar sua mensagem.</p>':`<input id="tx" type="text" placeholder="Mensagem..."><button class="btn" id="sd">Enviar</button>`}</div>`;
 document.querySelectorAll('[data-rl]').forEach(a=>a.onclick=()=>openReel(a.dataset.rl));
 if($('#sd'))$('#sd').onclick=()=>{const x=$('#tx').value.trim();if(!x)return;c.m.push({f:M,x,t:Date.now()});save();thread()};
 if($('#tx'))$('#tx').onkeydown=e=>{if(e.key==='Enter')$('#sd').click()}}
/* pesquisa e notificações */
let sq='',sk='c';
function srch(){
 $('#main').innerHTML=`<div class="pad"><input id="q" type="text" placeholder="Pesquisar contas e reels..." value="${esc(sq)}"><div class="tabs"><button class="btn ${sk==='c'?'':'s'}" id="k1">Conta</button><button class="btn ${sk==='r'?'':'s'}" id="k2">Reel</button></div><div id="res"></div></div>`;
 const run=()=>{const q=nz(sq.replace(/^@/,'').trim()),R=$('#res');
  const pm=sq.match(/https?:\/\/\S*reel=(\d+)/);if(pm)return openReel(pm[1]);
  if(!q){R.innerHTML='<p class="mut">Digite um nome ou cole o link de um reel.</p>';return}
  if(sk==='c'){const l=Object.values(S.users).filter(u=>!u.sys&&(nz(u.handle).includes(q)||nz(u.name).includes(q)));
   R.innerHTML=l.map(u=>`<div class="row" data-u="${u.uid}"><img class="av" src="${u.photo}" alt=""><div><b>${esc(u.name)}</b><div class="mut">@${esc(u.handle)}</div></div></div>`).join('')||'<p class="mut">Nenhuma conta encontrada.</p>';
   R.querySelectorAll('[data-u]').forEach(r=>r.onclick=()=>show('user',r.dataset.u))}
  else{const l=all().filter(r=>nz(r.name).includes(q)||nz(r.theme).includes(q)||nz(hd(r.by)).includes(q));
   R.innerHTML=l.map(r=>`<div class="row" data-r="${r.id}"><span class="av" style="width:44px;height:60px;border-radius:8px;background:${G[r.id%6]};text-align:center;line-height:60px">${r.e||'🎬'}</span><div><b>${esc(r.name)}</b><div class="mut">#${esc(r.theme)} · @${esc(hd(r.by))}</div></div></div>`).join('')||'<p class="mut">Nenhum reel encontrado.</p>';
   R.querySelectorAll('[data-r]').forEach(r=>r.onclick=()=>viewReel(r.dataset.r))}};
 $('#q').oninput=e=>{sq=e.target.value;run()};
 $('#k1').onclick=()=>{sk='c';srch()};$('#k2').onclick=()=>{sk='r';srch()};run()}
function viewReel(id){const r=all().find(x=>x.id==id);if(!r)return toast('Esse reel não existe mais');
 view1(r);const M=me(),mn=r.by===M,cm=S.cm[r.id]||[],lked=(S.likes[r.id]||[]).includes(M);
 modal(`<div class="reel" style="height:42vh;border-radius:12px;background:${G[r.id%6]}">${r.src?`<video src="${r.src}" controls autoplay loop playsinline></video>`:`<div class="art">${r.e||'🎬'}</div>`}</div>
 <p style="margin:8px 0"><b>${esc(r.name)}</b><br><span class="mut">@${esc(hd(r.by))}</span>${ofc(r.by)} <span class="mut">· #${esc(r.theme)}${r.ai?' · Feito com IA':''}</span></p>
 <div class="acts" style="margin-bottom:6px"><button id="vl">${lked?'❤️':'🤍'} ${lk(r.id)}</button>${mn?'':'<button id="vr">🚩 Denunciar</button>'}${isMod()&&!adm()?'<button id="vq">🗑️ Pedir exclusão</button>':''}<button id="vc">🔗 Copiar link</button>${mn?'<button id="ve">Editar</button>':''}${adm()?'<button id="vd">🗑️ Apagar (admin)</button>':''}</div>
 <div>${cm.map(c=>`<div style="margin:6px 0"><b>@${esc(hd(c.u))}</b>${ofc(c.u)} <span class="mut">${ago(c.t)}</span><br>${esc(c.x)}</div>`).join('')||'<p class="mut">Seja o primeiro a comentar.</p>'}</div>
 <input id="ci" type="text" placeholder="Escreva um comentário..."><button class="btn" id="cs">Comentar</button><button class="btn s" id="cc">Fechar</button>`);
 $('#cc').onclick=()=>{modal('');if(['home','reels','prof','user'].includes(tab))show(tab,vw)};
 $('#vl').onclick=()=>{like(r);$('#vl').textContent=((S.likes[r.id]||[]).includes(M)?'❤️ ':'🤍 ')+lk(r.id)};
 $('#vc').onclick=()=>copy(link(r.id));if($('#vr'))$('#vr').onclick=()=>reportF(r);if($('#vq'))$('#vq').onclick=()=>dreqF(r);
 if($('#ve'))$('#ve').onclick=()=>{modal('');postForm(r)};
 if($('#vd'))$('#vd').onclick=()=>{rdel(r);modal('');show(tab,vw);toast('Vídeo apagado pelo administrador')};
 const sc=()=>{const x=$('#ci').value.trim();if(!x)return;(S.cm[r.id]=S.cm[r.id]||[]).push({u:M,x,t:Date.now()});if(r.by!==M)note(r.by,'cm','@'+U().handle+' comentou: '+x.slice(0,40),r.id);save();viewReel(id)};
 $('#cs').onclick=sc;$('#ci').onkeydown=e=>{if(e.key==='Enter')sc()}}
function viewReelOld(id){const r=all().find(x=>x.id==id);if(!r)return toast('Esse reel não existe mais');
 modal(`<div class="reel" style="height:60vh;border-radius:12px;background:${G[r.id%6]}">${r.src?`<video src="${r.src}" controls autoplay loop playsinline></video>`:`<div class="art">${r.e||'🎬'}</div>`}<div class="info"><b>@${esc(hd(r.by))}</b> · ${esc(r.name)}<br><span class="tag">#${esc(r.theme)}${r.ai?'<span class="ia">Feito com IA</span>':''}</span></div></div><button class="btn s" id="cc">Fechar</button>`);$('#cc').onclick=()=>modal('')}
function notesV(){const l=S.notes[me()]||[],ic={sys:'🛡️',rp:'🚩',dq:'🛡️',lk:'❤️',cm:'💬',fol:'👤',reel:'🎬',acc:'🆕'};
 $('#main').innerHTML=`<div class="pad"><h3 style="margin-top:0">Notificações</h3>${l.map((n,i)=>`<div class="row" data-i="${i}" style="${n.r?'opacity:.6':''}"><span style="font-size:22px">${ic[n.type]}</span><div><b>${esc(n.txt)}</b><div class="mut">${ago(n.ts)}</div></div></div>`).join('')||'<p class="mut">Nenhuma notificação.</p>'}</div>`;
 document.querySelectorAll('.row[data-i]').forEach(r=>r.onclick=()=>{const n=l[r.dataset.i];n.type==='sys'?show('thread',n.ref):['dq','rp'].includes(n.type)?(setTab='a',show('set')):['reel','lk','cm'].includes(n.type)?viewReel(n.ref):S.users[n.ref]&&show('user',n.ref)});
 l.forEach(n=>n.r=1);save();hdr()}
/* configurações */
function adetail(rid,ctx){const r=all().find(x=>x.id===rid);if(!r){toast('Esse reel não existe mais');return adminV()}
 const rp=S.rep[rid]||[],rq=S.dreq.filter(q=>q.rid===rid);
 $('#main').innerHTML=`<div class="pad"><button class="btn s m" id="bk2">← Voltar</button>
 <div class="reel" style="height:46vh;border-radius:12px;margin:10px 0;background:${G[rid%6]}">${r.src?`<video src="${r.src}" controls playsinline></video>`:`<div class="art">${r.e||'🎬'}</div>`}</div>
 <b>${esc(r.name)}</b><div class="mut">@${esc(hd(r.by))} · #${esc(r.theme)}${r.ai?' · Feito com IA':''}${r.hold?' · Em revisão pela IA':''}</div>
 <h4>Mensagens das denúncias (${rp.length})</h4>${rp.map(x=>`<div style="margin:6px 0"><b>@${esc(hd(x.u))}</b> <span class="mut">${esc(x.w)} · ${ago(x.t)}</span><br>${esc(x.x||'(sem mensagem)')}</div>`).join('')||'<p class="mut">Nenhuma denúncia.</p>'}
 ${rq.length?`<h4>Pedidos de exclusão</h4>${rq.map(q=>`<div style="margin:6px 0"><b>@${esc(hd(q.by))}</b> <span class="mut">${ago(q.t)}</span><br>${esc(q.x||'(sem mensagem)')}</div>`).join('')}`:''}</div>
 <div style="position:sticky;bottom:0;display:flex;justify-content:space-between;gap:10px;padding:10px 16px;background:var(--bg)"><button class="btn s" id="kp" style="width:48%">✔ Deixar no ar</button><button class="btn r" id="dd" style="width:48%">🗑️ Deletar</button></div>`;
 $('#bk2').onclick=()=>show('set');
 $('#kp').onclick=()=>{rq.forEach(q=>prot(q.by,'Seu pedido sobre "'+r.name+'" foi analisado: o reel continua no ar.'));const wh=r.hold;delete r.hold;if(mine.includes(r))put(r);if(ctx==='rep')S.keep[rid]=Date.now();S.dreq=S.dreq.filter(q=>q.rid!==rid);if(wh)prot(r.by,'Seu reel "'+r.name+'" foi aprovado e já está no ar.');save();toast('Reel mantido no ar');adminV()};
 $('#dd').onclick=()=>{rq.forEach(q=>prot(q.by,'Seu pedido foi aprovado: o reel "'+r.name+'" foi deletado.'));rdel(r,ctx==='rep'?'rep':'adm');toast('Reel deletado');adminV()}}
function adminV(){const u=U();if(!u.owner)return adminOld();
 const yr=new Date().getFullYear(),cnt=(r,y)=>(S.rep[r.id]||[]).filter(x=>!y||new Date(x.t).getFullYear()===yr).length,
 top=y=>all().filter(r=>cnt(r,y)).sort((a,b)=>cnt(b,y)-cnt(a,y)).slice(0,10),
 li=(r,y,c)=>`<div class="row" data-r="${r.id}" data-c="${c}"><div><b>${esc(r.name)}</b>${S.keep[r.id]?' ✔ mantido':''}<div class="mut">@${esc(hd(r.by))} · ${c==='hold'?'em revisão pela IA':cnt(r,y)+' denúncia(s)'+(flagged(r)?' · menos recomendado':'')}</div></div></div>`,
 em=t=>`<p class="mut">${t}</p>`;
 $('#main').innerHTML=`<div class="pad"><div class="tabs"><button class="btn s" id="t1">Conta</button><button class="btn s" id="t2">Vincular</button><button class="btn" id="t3">Admin</button></div>
 <p><span class="ofc">✔ Oficial</span> <b>Dono do App</b><br><span class="mut">Seu selo fica mesmo se você mudar o @. Modo administrador: <b>${u.admin?'ATIVO':'desativado'}</b></span></p>
 ${u.admin?'<button class="btn r" id="ad">Desativar modo administrador</button>':'<input id="ap" type="password" placeholder="Senha de administrador"><button class="btn" id="aa">Ativar modo administrador</button>'}<div class="err" id="er"></div>
 ${u.admin?`<h4>🚨 Emergência</h4><p class="mut">Vinculação com o Discord: <b>${dcOff()?'PARADA':'ativa'}</b></p>${dcOff()?'<button class="btn" id="dr">Reativar vinculação com o Discord</button>':'<button class="btn r" id="de">🚨 Parar vinculação com o Discord</button>'}<h4>Em revisão pela IA</h4>${all().filter(r=>r.hold).map(r=>li(r,0,'hold')).join('')||em('Nada em revisão.')}
 <h4>Pedidos de exclusão</h4>${S.dreq.map(q=>`<div class="row" data-r="${q.rid}" data-c="req"><div><b>${esc(q.rn)}</b><div class="mut">@${esc(hd(q.by))}: ${esc(q.x||'(sem mensagem)')}</div></div></div>`).join('')||em('Nenhum pedido.')}
 <h4>Mais denunciados em ${yr}</h4>${top(1).map(r=>li(r,1,'rep')).join('')||em('Nenhuma denúncia neste ano.')}
 <h4>Mais denunciados de todos os tempos</h4>${top(0).map(r=>li(r,0,'rep')).join('')||em('Nenhuma denúncia ainda.')}
 <h4>Moderadores (podem pedir exclusão)</h4><input id="mh" type="text" placeholder="@ da pessoa" autocapitalize="none"><button class="btn" id="mg">Dar permissão</button>${S.mods.map(id=>`<div class="row" style="cursor:default"><div>@${esc(hd(id))}</div><button class="btn r m" data-rm="${id}">Remover permissão</button></div>`).join('')}`:''}</div>`;
 $('#t1').onclick=()=>{setTab='c';sets()};$('#t2').onclick=()=>{setTab='v';sets()};
 if($('#ad'))$('#ad').onclick=()=>{u.admin=false;save();toast('Modo administrador desativado');adminV()};
 if($('#aa'))$('#aa').onclick=()=>{if($('#ap').value!==ADMPW)return $('#er').textContent='Senha incorreta';u.admin=true;save();toast('Modo administrador ativado');adminV()};
 document.querySelectorAll('[data-r]').forEach(e=>e.onclick=()=>adetail(+e.dataset.r,e.dataset.c));
 if($('#de'))$('#de').onclick=()=>{modal(`<h3>Parar vinculação com o Discord?</h3><p>Tem certeza? Ninguém será mais enviado ao Discord para vincular a conta até você reativar.</p><button class="btn r" id="y2">Sim, parar agora</button><button class="btn s" id="cc">Cancelar</button>`);$('#cc').onclick=()=>modal('');$('#y2').onclick=()=>setDc(true)};
 if($('#dr'))$('#dr').onclick=()=>setDc(false);
 if($('#mg'))$('#mg').onclick=()=>{const t=byH($('#mh').value.trim().replace(/^@/,'').toLowerCase());if(!t||t.sys)return $('#er').textContent='@ não encontrado';if(t.owner)return $('#er').textContent='Você já é o dono';if(!S.mods.includes(t.uid)){S.mods.push(t.uid);prot(t.uid,'O administrador deu a você permissão para pedir a exclusão de vídeos. Use ⋯ > Pedir exclusão.')}save();toast('Permissão concedida a @'+t.handle);adminV()};
 document.querySelectorAll('[data-rm]').forEach(b=>b.onclick=()=>{S.mods=S.mods.filter(x=>x!==b.dataset.rm);prot(b.dataset.rm,'Sua permissão de moderador foi removida.');save();toast('Permissão removida');adminV()})}
async function bkExport(){const o={...S,users:{...S.users}};delete o.session;delete o.rv;delete o.dcOff;delete o.users.sasc;const d=JSON.stringify(o);
 try{const dl=window.claude&&await claude.use('downloads');if(!dl)throw 0;await dl.save({filename:'sasc-backup.json',data:d});toast('Backup pronto')}
 catch(e){if(e&&e.code==='declined')return;try{await navigator.clipboard.writeText(d);toast('Não consegui baixar o arquivo. O backup foi copiado: cole num arquivo .json')}catch(x){toast('Não foi possível exportar o backup')}}}
function merge(b){let nu=0,sk=0;const un=(a,c,k)=>{a=a||[];const s=new Set(a.map(k));(c||[]).forEach(x=>{if(!s.has(k(x))){a.push(x);s.add(k(x))}});return a},id=x=>x;
 for(const[k,u]of Object.entries(b.users||{})){if(u.sys)continue;const l=S.users[k];if(l){l.usage=Math.max(l.usage||0,u.usage||0);l.blockedUntil=Math.max(l.blockedUntil||0,u.blockedUntil||0)}else if(byH(u.handle))sk++;else{S.users[k]=u;nu++}}
 for(const k in b.follow||{})S.follow[k]=un(S.follow[k],b.follow[k],id);
 for(const k in b.fr||{})S.fr[k]=un(S.fr[k],b.fr[k],id);
 for(const k in b.likes||{})S.likes[k]=un(S.likes[k],b.likes[k],id);
 for(const k in b.vw||{})S.vw[k]=un(S.vw[k],b.vw[k],id);
 for(const k in b.cm||{})S.cm[k]=un(S.cm[k],b.cm[k],c=>c.u+'|'+c.t);
 for(const k in b.rep||{})S.rep[k]=un(S.rep[k],b.rep[k],c=>c.u+'|'+c.t);
 for(const k in b.notes||{})S.notes[k]=un(S.notes[k],b.notes[k],n=>n.ts+n.txt).sort((a,c)=>c.ts-a.ts).slice(0,60);
 for(const k in b.chats||{}){const l=S.chats[k],c=b.chats[k];if(!l)S.chats[k]=c;else{l.acc=l.acc||c.acc;l.m=un(l.m,c.m,m=>m.t+m.f+m.x).sort((a,d)=>a.t-d.t)}}
 S.hidden=un(S.hidden,b.hidden,id);S.mods=un(S.mods,b.mods,id);S.dreq=un(S.dreq,b.dreq,q=>q.id);Object.assign(S.keep,b.keep||{});save();return{nu,sk}}
function bkImport(f){if(!f)return;const r=new FileReader();r.onload=()=>{let b;try{b=JSON.parse(r.result)}catch(e){return toast('Arquivo inválido')}if(!b||!b.users)return toast('Arquivo inválido');const m=merge(b);sets();toast(m.nu+' conta(s) importada(s)'+(m.sk?'; '+m.sk+' com @ repetido foi ignorada':'')+'. Vídeos não vão no backup.')};r.readAsText(f)}
function adminOld(){const u=U();
 $('#main').innerHTML=`<div class="pad"><div class="tabs"><button class="btn s" id="t1">Conta</button><button class="btn s" id="t2">Vincular</button><button class="btn" id="t3">Admin</button></div>
 ${u.owner?`<p><span class="ofc">✔ Oficial</span> <b>Dono do App</b><br><span class="mut">Seu selo fica mesmo se você mudar o @. Modo administrador: <b>${u.admin?'ATIVO':'desativado'}</b></span></p>${u.admin?'<button class="btn r" id="ad">Desativar modo administrador</button>':'<input id="ap" type="password" placeholder="Senha de administrador"><button class="btn" id="aa">Ativar modo administrador</button>'}`:`<p class="mut">Este @ é reservado. Digite a senha para assumir o app como dono.</p><input id="ap" type="password" placeholder="Senha de administrador"><button class="btn" id="aa">Assumir como dono</button>`}<div class="err" id="er"></div></div>`;
 $('#t1').onclick=()=>{setTab='c';sets()};$('#t2').onclick=()=>{setTab='v';sets()};
 if($('#ad'))$('#ad').onclick=()=>{u.admin=false;save();toast('Modo administrador desativado');adminV()};
 if($('#aa'))$('#aa').onclick=()=>{if($('#ap').value!==ADMPW)return $('#er').textContent='Senha incorreta';u.owner=true;u.admin=true;save();toast('Modo administrador ativado');adminV()}}
function sets(){const u=U();if(setTab==='a'&&isOwn())return adminV();
 $('#main').innerHTML=`<div class="pad"><div class="tabs"><button class="btn ${setTab==='c'?'':'s'}" id="t1">Conta</button><button class="btn ${setTab==='v'?'':'s'}" id="t2">Vincular</button>${isOwn()?`<button class="btn s" id="t3">Admin</button>`:''}</div>${setTab==='c'?`
 <div class="c"><img class="av" id="pp" src="${u.photo}" style="width:84px;height:84px;margin:0" alt=""><br><label class="btn s m" style="display:inline-block;margin-top:6px">Mudar foto<input id="ph" type="file" accept="image/*" hidden></label></div>
 <label class="l">Nome</label><input id="nm" type="text" value="${esc(u.name)}"><label class="l">Localizador (@)</label><input id="hh" type="text" value="${esc(u.handle)}" autocapitalize="none">
 <label class="l">Nova senha (deixe vazio para manter)</label><input id="pw" type="password"><div class="err" id="er"></div><button class="btn" id="sv">Salvar</button>
 <label class="l">Número de telefone ${u.phone?'(confirmado)':''}</label><input id="ph2" type="text" placeholder="+55 11 99999-9999" value="${esc(u.phone)}"><button class="btn s" id="sm">Confirmar número por SMS</button><h4>Backup entre aparelhos</h4><p class="mut">Exporte neste aparelho e importe no outro para juntar as contas. Vídeos não vão no backup. O arquivo contém as senhas das contas: guarde com cuidado.</p><button class="btn s" id="bx">Exportar backup</button><label class="btn s" style="display:block;text-align:center">Importar backup<input id="bi" type="file" accept=".json,application/json" hidden></label>`:`
 <p class="mut">Amigos veem as contas vinculadas no seu perfil. O Sasc não consegue ler seu status direto do Roblox ou do Discord, então você escolhe o status abaixo e decide se amigos podem vê-lo.</p>
 ${['roblox','discord'].map(k=>`<div class="row" style="cursor:default"><div><b>${k==='roblox'?'🎮 Roblox':'💬 Discord'}</b><div class="mut">${u.link?.[k]?'Usuário informado: '+esc(u.link[k])+' (não verificado)':'Não vinculado'}</div></div><button class="btn m" data-l="${k}">Vincular</button></div>${u.link?.[k]?stat(u,k):''}`).join('')}`}</div>`;
 $('#t1').onclick=()=>{setTab='c';sets()};$('#t2').onclick=()=>{setTab='v';sets()};if($('#t3'))$('#t3').onclick=()=>{setTab='a';sets()};
 if(setTab==='v'){document.querySelectorAll('[data-l]').forEach(b=>b.onclick=()=>linkF(b.dataset.l));document.querySelectorAll('[data-ps]').forEach(s=>s.onchange=()=>{u.pres=u.pres||{};u.pres[s.dataset.ps]=s.value;save()});document.querySelectorAll('[data-pv]').forEach(c=>c.onchange=()=>{u.vis=u.vis||{};u.vis[c.dataset.pv]=c.checked;save()});return}
 $('#ph').onchange=e=>resize(e.target.files[0],d=>{u.photo=d;save();sets()});
 $('#bx').onclick=bkExport;$('#bi').onchange=e=>bkImport(e.target.files[0]);
 $('#sv').onclick=()=>{const h=$('#hh').value.trim().replace(/^@/,'').toLowerCase(),n=$('#nm').value.trim(),p=$('#pw').value;
  if(!n)return $('#er').textContent='Digite um nome';if(!/^[a-z0-9_.]{3,20}$/.test(h))return $('#er').textContent='@ inválido (3 a 20 letras, números, _ ou .)';
  if(h==='callebe'&&!u.owner)return $('#er').textContent='Não foi possível alterar o @.';const o=byH(h);if((o&&o.uid!==u.uid)||demo.some(r=>r.by===h))return $('#er').textContent='Esse @ já existe';
  if(p&&p.length<4)return $('#er').textContent='Senha com 4+ caracteres';
  u.name=n;u.handle=h;if(p)u.pw=p;save();toast('Conta atualizada')};
 $('#sm').onclick=()=>{const n=$('#ph2').value.trim();if(!/^\+?[0-9 ()-]{8,18}$/.test(n))return $('#er').textContent='Número inválido';
  pend={n,c:String(Math.floor(1e5+Math.random()*9e5))};
  modal(`<h3>Confirmar número</h3><p>Enviamos um SMS para <b>${esc(n)}</b>.</p><p class="mut">Simulação: sem servidor de SMS, o código aparece aqui: <b>${pend.c}</b></p><input id="cd" type="text" placeholder="Código de 6 dígitos"><div class="err" id="e2"></div><button class="btn" id="ok">Confirmar</button><button class="btn s" id="cc">Cancelar</button>`);
  $('#cc').onclick=()=>modal('');$('#ok').onclick=()=>{if($('#cd').value.trim()!==pend.c)return $('#e2').textContent='Código incorreto';u.phone=pend.n;save();modal('');sets();toast('Número confirmado')}}}
function linkF(k){if(k==='discord'&&dcOff()){modal('<h3>Vinculação indisponível</h3><p>A vinculação com o Discord está temporariamente desativada. Tente de novo mais tarde.</p><button class="btn s" id="cc">Ok</button>');$('#cc').onclick=()=>modal('');return}const nm=k==='roblox'?'Roblox':'Discord',url=k==='roblox'?'https://www.roblox.com':DCLINK;
 modal(`<h3>Vincular ${nm}</h3><p class="mut">Informe seu usuário do ${nm}. O Sasc ainda não consegue confirmar que a conta é sua (isso exige login oficial do ${nm} e um servidor), então ela aparece como não verificada. O site abrirá em outra aba.</p><input id="lu" type="text" placeholder="Usuário no ${nm}"><button class="btn" id="ok">Vincular</button><button class="btn s" id="cc">Cancelar</button>`);
 $('#cc').onclick=()=>modal('');$('#ok').onclick=()=>{const v=$('#lu').value.trim();if(!v)return;const u=U();u.link=u.link||{};u.link[k]=v;save();window.open(url,'_blank','noopener');modal('');sets()}}
/* postar / editar / excluir */
function modal(h){$('#modal').innerHTML=h?`<div class="ov"><div class="box">${h}</div></div>`:''}
function postForm(r){const ed=!!r;
 modal(`<h3>${ed?'Editar vídeo':'Novo reel'}</h3>${ed?'':`<label class="l">Vídeo (celular ou computador)</label><input id="f" type="file" accept="video/*">`}
 <label class="l">Nome do vídeo</label><input id="nm" type="text" value="${ed?esc(r.name):''}"><label class="l">Tema</label><input id="th" type="text" placeholder="Ex.: Humor, Música..." value="${ed?esc(r.theme):''}">
 <label class="l">Foi feito com IA?</label><select id="ai"><option value="n">Não</option><option value="s" ${ed&&r.ai?'selected':''}>Sim</option></select><div class="err" id="er"></div>
 <button class="btn" id="ok">${ed?'Salvar':'Publicar'}</button>${ed?'<button class="btn r" id="dl">🗑️ Excluir vídeo</button>':''}<button class="btn s" id="cc">Cancelar</button>`);
 $('#cc').onclick=()=>modal('');
 if(ed)$('#dl').onclick=()=>{if($('#dl').dataset.c){const i=mine.indexOf(r);if(i>=0)mine.splice(i,1);del(r.id);modal('');show(tab);return toast('Vídeo excluído')}$('#dl').dataset.c=1;$('#dl').textContent='Toque de novo para confirmar a exclusão'};
 $('#ok').onclick=async()=>{const nm=$('#nm').value.trim(),th=$('#th').value.trim(),f=ed?null:$('#f').files[0];
  if(!ed&&!f)return $('#er').textContent='Escolha um vídeo';if(!nm||!th)return $('#er').textContent='Preencha nome e tema';
  const ai=$('#ai').value==='s';let rv='';if(!ed){$('#ok').disabled=true;$('#ok').textContent='Analisando o vídeo...';rv=await review(f,nm,th)}
  if(ed){Object.assign(r,{name:nm,theme:th,ai});put(r)}else{const n={id:Date.now(),by:me(),name:nm,theme:th,ai,blob:f,src:URL.createObjectURL(f),hold:rv==='flag'};mine.unshift(n);put(n);if(n.hold){prot(me(),'Seu reel "'+nm+'" está em revisão por um administrador antes de ir ao ar.');Object.keys(S.users).forEach(k=>{if(S.users[k].owner)note(k,'dq','Reel em revisão pela IA: '+nm,n.id)})}else Object.keys(S.users).forEach(k=>{if(k!==me()&&fol(k,me()))note(k,'reel','@'+U().handle+' postou um novo reel: '+nm,n.id)});save()}
  modal('');show(tab);toast(ed?'Alterações salvas':rv==='flag'?'Seu reel foi enviado para revisão antes de ir ao ar':'Reel publicado!')}}
addEventListener('hashchange',()=>{const m=location.hash.match(/reel=(\d+)/);if(m&&me())openReel(m[1])});
function sync(){const r=localStorage.getItem('sasc');if(!r||r===raw)return;let n;try{n=JSON.parse(r)}catch(e){return}raw=r;
 const k=S.session,rv=S.rv,ok=k&&S.users[k],u0=ok?unread():0,p0=ok?pendN():0;
 for(const x in S)delete S[x];Object.assign(S,n);S.session=k;
 const live=k&&S.users[k]&&$('#app').style.display==='flex';
 if(S.rv!==rv)setTimeout(()=>loadMine(ch=>{if(ch&&live&&['home','reels'].includes(tab)&&!$('#modal').innerHTML)feed()}),800);
 if(!live)return;
 const u1=unread(),p1=pendN();hdr();
 if(u1>u0)toast('🔔 Nova notificação');else if(p1>p0)toast('💬 Novo pedido de mensagem');
 const a=document.activeElement,typing=a&&a.matches&&a.matches('input,select,textarea')&&a.id!=='tx'&&$('#main').contains(a);
 if(typing||$('#modal').innerHTML)return;
 const t=$('#tx'),tv=t?t.value:null,fc=a&&a.id==='tx';
 if(tab==='chat')chat();else if(tab==='thread'){if(S.chats[thr])thread()}else if(tab==='notes')notesV();else if(tab==='user'||tab==='prof')prof(tab==='prof'?me():vw);else if(tab==='set'&&setTab==='a'&&!$('#bk2'))sets();
 if(tv!==null&&$('#tx')){$('#tx').value=tv;if(fc)$('#tx').focus()}}
addEventListener('storage',e=>{if(e.key==='sasc')sync()});setInterval(sync,1500);
$('#fab').onclick=()=>postForm();
document.querySelectorAll('nav button').forEach(b=>b.onclick=()=>show(b.dataset.t));
idb().then(()=>{if(S.session&&S.users[S.session])enter();else authView(false)});
</script></body></html>
