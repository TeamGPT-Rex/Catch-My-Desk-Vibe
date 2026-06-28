import { createContext, useContext, useState, useEffect, useRef } from "react";

// ─── CONSTANTS ────────────────────────────────────────────────────────────────

const BODY_COLORS = [
  { id:"green",  hex:"#4CAF50", dark:"#2E7D32", grad:["#81C784","#4CAF50"] },
  { id:"coral",  hex:"#FF6B6B", dark:"#C62828", grad:["#FF8A65","#FF6B6B"] },
  { id:"sky",    hex:"#42A5F5", dark:"#1565C0", grad:["#64B5F6","#42A5F5"] },
  { id:"sand",   hex:"#F9A825", dark:"#E65100", grad:["#FFB300","#F9A825"] },
  { id:"violet", hex:"#AB47BC", dark:"#6A1B9A", grad:["#BA68C8","#AB47BC"] },
];

const HOBBIES = [
  {id:"gaming",   icon:"🎮", label:"Gaming"},
  {id:"coding",   icon:"💻", label:"Coding"},
  {id:"reading",  icon:"📚", label:"Reading"},
  {id:"gym",      icon:"🏋️", label:"Gym"},
  {id:"cooking",  icon:"🍳", label:"Cooking"},
  {id:"art",      icon:"🎨", label:"Art"},
  {id:"travel",   icon:"✈️", label:"Travel"},
  {id:"music",    icon:"🎸", label:"Playing music"},
];

const MUSIC_GENRES = [
  {id:"lofi",    icon:"☕", label:"Lo-fi"},
  {id:"techno",  icon:"🔊", label:"Techno/Electronic"},
  {id:"rock",    icon:"🎸", label:"Rock"},
  {id:"pop",     icon:"✨", label:"Pop"},
  {id:"jazz",    icon:"🎷", label:"Jazz"},
  {id:"ambient", icon:"🌿", label:"Ambient"},
  {id:"hiphop",  icon:"🎤", label:"Hip-hop"},
  {id:"classical",icon:"🎻",label:"Classical"},
];

const MOVIE_GENRES = [
  {id:"anime",       icon:"🌸", label:"Anime"},
  {id:"scifi",       icon:"🚀", label:"Sci-Fi"},
  {id:"mystery",     icon:"🔍", label:"Mystery/Thriller"},
  {id:"fantasy",     icon:"🧙", label:"Fantasy"},
  {id:"comedy",      icon:"😂", label:"Comedy"},
  {id:"documentary", icon:"🎥", label:"Documentary"},
  {id:"drama",       icon:"🎭", label:"Drama"},
  {id:"action",      icon:"💥", label:"Action"},
];

const DESK_STYLES = [
  {id:"minimal",  icon:"◻️", label:"Minimal & Clean"},
  {id:"cozy",     icon:"🧸", label:"Cozy & Warm"},
  {id:"techy",    icon:"⚡", label:"Tech & Futuristic"},
  {id:"nature",   icon:"🌿", label:"Nature & Organic"},
  {id:"artistic", icon:"🎨", label:"Artistic & Eclectic"},
  {id:"retro",    icon:"📼", label:"Retro & Vintage"},
];

const STREAMING = {
  netflix:    {name:"Netflix",    color:"#E50914", bg:"#141414", url:"https://www.netflix.com/search?q="},
  prime:      {name:"Prime Video",color:"#00A8E1", bg:"#0F1111", url:"https://www.amazon.com/s?k="},
  disney:     {name:"Disney+",   color:"#113CCF", bg:"#040714", url:"https://www.disneyplus.com/search/"},
  apple:      {name:"Apple TV+", color:"#A2AAAD", bg:"#000000", url:"https://tv.apple.com/search/"},
  hbo:        {name:"Max",       color:"#9B59B6", bg:"#002BE7", url:"https://www.max.com/search/"},
  crunchyroll:{name:"Crunchyroll",color:"#F47521", bg:"#1a1a1a", url:"https://www.crunchyroll.com/search?q="},
};

// Colour palette for album art cards — cycles per track
const TRACK_COLORS = [
  ["#1a1a2e","#4a0e8f"],["#0d2137","#1565C0"],["#1a0d00","#b5451b"],
  ["#0a1628","#1DB954"],["#1a001a","#7B61FF"],["#001a1a","#00897B"],
  ["#1a1000","#F9A825"],["#1a0a0f","#C62828"],
];

// Playlist pools per genre
const PLAYLISTS = {
  lofi:    [["Rainy Window Study","ChillHop Collective"],["Late Night Pages","Lo-fi Kitten"],["Warm Blanket","Cozy Tones"],["Café Candle","Soft Static"],["3am Desk Glow","NuJazz Pilot"],["Quiet Hours","Bear & Co."]],
  techno:  [["Neural Pulse","SYNC404"],["Grid Collapse","Binary Swell"],["404 Dance","Voltage Rush"],["Bassline Protocol","XeroWave"],["Subcarrier","NoiseGrid"],["Overclock","Freqshift"]],
  rock:    [["Midnight Amp","Stone Cabin"],["Fuzzbox Highway","The Relics"],["Unplugged Fog","Ember Arc"],["Three Chords","Sunday Moot"],["Static Echo","Redline Co"],["Rooftop Howl","Glass Jaw"]],
  pop:     [["Pink Saturday","Starlette"],["Glow Up","Neon Peach"],["Main Character","Solo Kay"],["Bubblegum Phase","The Mints"],["Sunroof Girl","Daisy Fox"],["Mood Ring","Pastel Pack"]],
  jazz:    [["Midnight Lounge","The Quartet"],["Rain On Glass","Solo Sax"],["Blue Tuesday","Mellow Trio"],["Last Round","Brass & Smoke"],["11pm","The Quartet"],["Corner Booth","Reed Station"]],
  ambient: [["Forest Layer","Drift Moss"],["Deep Canopy","Stillwater"],["Morning Fog","Pale Shore"],["Breath Cycle","Opal Grid"],["Creek Bed","Fernlight"],["Open Field","Hush Basin"]],
  hiphop:  [["Street Cipher","Block Poet"],["Night Frequency","MC Dusk"],["Rooftop Session","The Collective"],["Sample Flip","Vinyl Digger"],["Flow State","Pavement Art"],["Golden Era","The MCs"]],
  classical:[["Moonlight Reverie","Chamber Orch."],["String Interlude","Quartet No.4"],["Allegro Morning","Solo Piano"],["Nocturne in Blue","Evening Trio"],["Adagio Study","Orchestra Min."],["Fugue at Dusk","Baroque Ens."]],
};

// Watchlist pools per genre
const WATCHLISTS = {
  anime:       [["Spirited Seasons","crunchyroll","🌸","Coming-of-age in a world of spirits"],["Paper Village","netflix","🌸","Hand-drawn magic meets small-town summer"],["Sky Garden","crunchyroll","🌸","Two friends rebuild a floating city"],["Clockwork Moth","netflix","🌸","A mechanic girl and her impossible machine"]],
  scifi:       [["The Quiet Probe","netflix","🚀","A lone robot on a nameless planet"],["Last Orbit","prime","🚀","Survival comedy in a broken space station"],["Signal Delay","apple","🚀","A message arrives 200 years too late"],["Coldside","hbo","🚀","Scientists find something under Europa's ice"]],
  mystery:     [["The Third Umbrella","netflix","🔍","A detective, a rainy village, a locked library"],["Station 9","hbo","🔍","Cold case on a silent night train"],["Glass Afternoon","prime","🔍","Everyone lied. But why?"],["Moth & Mirror","apple","🔍","Amateur sleuth vs. a con artist collective"]],
  fantasy:     [["The Root Kingdom","netflix","🧙","Underground elves and above-ground rebels"],["A Map of Clouds","prime","🧙","Magic costs a memory — can you pay?"],["Seven Lanterns","disney","🧙","A quest no one expected to survive"],["The Cartographer","hbo","🧙","Maps that change the world they describe"]],
  comedy:      [["Office Poltergeist","netflix","😂","Ghost haunts a corporate team. Legally."],["Bad Timing","prime","😂","A romance with a 5-minute delay in everything"],["The Swap","hbo","😂","Two rivals accidentally swap careers for a week"],["42 Notifications","apple","😂","Social media addiction as a thriller-comedy"]],
  documentary: [["Beneath the Kelp","netflix","🎥","The secret lives of underwater forests"],["Night Shift Earth","prime","🎥","A year of nocturnal animals"],["The Ink Trade","apple","🎥","A disappearing craft in 5 cities"],["Salt Flat","disney","🎥","Documenting the world's flattest place"]],
  drama:       [["The Last Draft","netflix","🎭","A novelist races against her own silence"],["Platform 7","hbo","🎭","Every commuter has a secret"],["Quiet Hours","prime","🎭","A family reunion that unravels slowly"],["The Weight of Light","apple","🎭","A photographer loses her sight, finds her vision"]],
  action:      [["Iron Quarter","netflix","💥","A city divided by neon and violence"],["Breakout","prime","💥","One heist, six people, zero trust"],["Chrome Falls","hbo","💥","A courier knows too much"],["The Relay","apple","💥","Pass the package. Don't ask why."]],
};

// Reward objects — canvas-based, properly scaled, grounded with shadow
const REWARDS = {
  default:  { name:"Productivity Cactus", why:"Every creative desk needs something alive that thrives on neglect.", emoji:"🌵",
    drawCtx:(ctx,x,y,s)=>{
      ctx.save();ctx.globalAlpha=0.15;ctx.fillStyle="#000";ctx.beginPath();ctx.ellipse(x,y+2,s*.18,s*.05,0,0,Math.PI*2);ctx.fill();ctx.restore();
      ctx.fillStyle="#8D6E63";ctx.beginPath();ctx.roundRect(x-s*.13,y-s*.12,s*.26,s*.13,s*.03);ctx.fill();
      ctx.fillStyle="#A1887F";ctx.beginPath();ctx.roundRect(x-s*.11,y-s*.14,s*.22,s*.04,s*.02);ctx.fill();
      ctx.fillStyle="#4CAF50";ctx.beginPath();ctx.roundRect(x-s*.05,y-s*.56,s*.10,s*.44,s*.05);ctx.fill();
      ctx.fillStyle="#66BB6A";ctx.beginPath();ctx.roundRect(x-s*.03,y-s*.54,s*.06,s*.40,s*.03);ctx.fill();
      ctx.fillStyle="#4CAF50";ctx.beginPath();ctx.roundRect(x-s*.17,y-s*.40,s*.12,s*.06,s*.03);ctx.fill();
      ctx.beginPath();ctx.roundRect(x+s*.05,y-s*.29,s*.12,s*.06,s*.03);ctx.fill();
      ctx.fillStyle="#FF6B6B";ctx.beginPath();ctx.arc(x,y-s*.57,s*.07,0,Math.PI*2);ctx.fill();
      ctx.fillStyle="#FF8A65";ctx.beginPath();ctx.arc(x,y-s*.57,s*.04,0,Math.PI*2);ctx.fill();
    }},
  chaotic:  { name:"Chaos Trophy", why:"You thrive in the storm. This golden award belongs on your battlefield.", emoji:"🏆",
    drawCtx:(ctx,x,y,s)=>{
      ctx.save();ctx.globalAlpha=0.15;ctx.fillStyle="#000";ctx.beginPath();ctx.ellipse(x,y+2,s*.18,s*.05,0,0,Math.PI*2);ctx.fill();ctx.restore();
      ctx.fillStyle="#8D6E63";ctx.beginPath();ctx.roundRect(x-s*.13,y-s*.1,s*.26,s*.1,s*.02);ctx.fill();
      ctx.fillStyle="#A1887F";ctx.beginPath();ctx.roundRect(x-s*.09,y-s*.18,s*.18,s*.09,s*.02);ctx.fill();
      const g=ctx.createLinearGradient(x-s*.18,y-s*.7,x+s*.18,y-s*.18);g.addColorStop(0,"#FFE566");g.addColorStop(.5,"#FFD700");g.addColorStop(1,"#F9A825");ctx.fillStyle=g;
      ctx.beginPath();ctx.moveTo(x-s*.18,y-s*.18);ctx.quadraticCurveTo(x-s*.22,y-s*.44,x-s*.14,y-s*.62);ctx.quadraticCurveTo(x,y-s*.72,x+s*.14,y-s*.62);ctx.quadraticCurveTo(x+s*.22,y-s*.44,x+s*.18,y-s*.18);ctx.closePath();ctx.fill();
      ctx.fillStyle="rgba(255,255,255,0.22)";ctx.beginPath();ctx.moveTo(x-s*.14,y-s*.2);ctx.quadraticCurveTo(x-s*.18,y-s*.42,x-s*.1,y-s*.58);ctx.quadraticCurveTo(x-s*.04,y-s*.3,x-s*.06,y-s*.2);ctx.closePath();ctx.fill();
      ctx.strokeStyle="#FFD700";ctx.lineWidth=s*.06;ctx.lineCap="round";
      ctx.beginPath();ctx.arc(x-s*.22,y-s*.38,s*.08,Math.PI*.4,Math.PI*1.6);ctx.stroke();
      ctx.beginPath();ctx.arc(x+s*.22,y-s*.38,s*.08,-Math.PI*.6,Math.PI*.6);ctx.stroke();
    }},
  focused:  { name:"Focus Hourglass", why:"Your flow state deserves a timer you'll actually respect.", emoji:"⏳",
    drawCtx:(ctx,x,y,s)=>{
      ctx.save();ctx.globalAlpha=0.15;ctx.fillStyle="#000";ctx.beginPath();ctx.ellipse(x,y+2,s*.13,s*.04,0,0,Math.PI*2);ctx.fill();ctx.restore();
      ctx.fillStyle="#42A5F5";ctx.beginPath();ctx.roundRect(x-s*.14,y-s*.72,s*.28,s*.07,s*.03);ctx.fill();
      ctx.beginPath();ctx.roundRect(x-s*.14,y-s*.1,s*.28,s*.07,s*.03);ctx.fill();
      ctx.fillStyle="rgba(144,202,249,0.8)";ctx.beginPath();ctx.moveTo(x-s*.13,y-s*.65);ctx.quadraticCurveTo(x-s*.12,y-s*.42,x,y-s*.38);ctx.quadraticCurveTo(x+s*.12,y-s*.42,x+s*.13,y-s*.65);ctx.closePath();ctx.fill();
      ctx.fillStyle="rgba(66,165,245,0.9)";ctx.beginPath();ctx.moveTo(x-s*.13,y-s*.1);ctx.quadraticCurveTo(x-s*.12,y-s*.3,x,y-s*.38);ctx.quadraticCurveTo(x+s*.12,y-s*.3,x+s*.13,y-s*.1);ctx.closePath();ctx.fill();
      ctx.fillStyle="#1565C0";ctx.beginPath();ctx.arc(x,y-s*.38,s*.03,0,Math.PI*2);ctx.fill();
    }},
  cozy:     { name:"Eternal Cosy Mug", why:"Your aura is warm drinks and soft light. This mug never goes cold.", emoji:"☕",
    drawCtx:(ctx,x,y,s)=>{
      ctx.save();ctx.globalAlpha=0.15;ctx.fillStyle="#000";ctx.beginPath();ctx.ellipse(x,y+2,s*.2,s*.055,0,0,Math.PI*2);ctx.fill();ctx.restore();
      const g=ctx.createLinearGradient(x-s*.18,0,x+s*.18,0);g.addColorStop(0,"#FF8A65");g.addColorStop(1,"#FFA07A");ctx.fillStyle=g;
      ctx.beginPath();ctx.roundRect(x-s*.18,y-s*.55,s*.36,s*.55,s*.06);ctx.fill();
      ctx.fillStyle="#FFCCBC";ctx.beginPath();ctx.ellipse(x,y-s*.55,s*.18,s*.05,0,0,Math.PI*2);ctx.fill();
      ctx.fillStyle="#5D4037";ctx.beginPath();ctx.ellipse(x,y-s*.54,s*.14,s*.04,0,0,Math.PI*2);ctx.fill();
      ctx.strokeStyle="#FF7043";ctx.lineWidth=s*.07;ctx.lineCap="round";ctx.beginPath();ctx.arc(x+s*.22,y-s*.33,s*.1,Math.PI*.7,-Math.PI*.7);ctx.stroke();
      ctx.fillStyle="rgba(255,255,255,0.2)";ctx.beginPath();ctx.roundRect(x-s*.14,y-s*.52,s*.06,s*.28,s*.03);ctx.fill();
      ctx.strokeStyle="rgba(255,255,255,0.45)";ctx.lineWidth=s*.022;ctx.lineCap="round";
      [-.06,0,.06].forEach(dx=>{ctx.beginPath();ctx.moveTo(x+dx*s,y-s*.58);ctx.quadraticCurveTo(x+dx*s-s*.04,y-s*.72,x+dx*s,y-s*.80);ctx.stroke();});
    }},
  zen:      { name:"Mini Zen Garden", why:"A tiny sandbox for your calmest thoughts. Rake included.", emoji:"🪨",
    drawCtx:(ctx,x,y,s)=>{
      ctx.save();ctx.globalAlpha=0.12;ctx.fillStyle="#000";ctx.beginPath();ctx.ellipse(x,y+2,s*.28,s*.07,0,0,Math.PI*2);ctx.fill();ctx.restore();
      ctx.fillStyle="#D7CCC8";ctx.beginPath();ctx.roundRect(x-s*.26,y-s*.32,s*.52,s*.32,s*.04);ctx.fill();
      ctx.fillStyle="#EFEBE9";ctx.beginPath();ctx.roundRect(x-s*.23,y-s*.29,s*.46,s*.26,s*.03);ctx.fill();
      ctx.strokeStyle="#BCAAA4";ctx.lineWidth=s*.01;ctx.setLineDash([s*.02,s*.02]);
      [-.22,-.16,-.10,-.04].forEach(dy=>{ctx.beginPath();ctx.moveTo(x-s*.2,y+dy*s);ctx.lineTo(x+s*.2,y+dy*s);ctx.stroke();});ctx.setLineDash([]);
      const r1=ctx.createRadialGradient(x-s*.1,y-s*.2,0,x-s*.1,y-s*.2,s*.1);r1.addColorStop(0,"#BDBDBD");r1.addColorStop(1,"#9E9E9E");ctx.fillStyle=r1;ctx.beginPath();ctx.ellipse(x-s*.1,y-s*.2,s*.1,s*.07,-.3,0,Math.PI*2);ctx.fill();
      const r2=ctx.createRadialGradient(x+s*.1,y-s*.16,0,x+s*.1,y-s*.16,s*.07);r2.addColorStop(0,"#9E9E9E");r2.addColorStop(1,"#757575");ctx.fillStyle=r2;ctx.beginPath();ctx.ellipse(x+s*.1,y-s*.16,s*.07,s*.05,.2,0,Math.PI*2);ctx.fill();
    }},
  creative: { name:"Magic Idea Lamp", why:"Your desk sparks ideas constantly. This lamp keeps them glowing.", emoji:"💡",
    drawCtx:(ctx,x,y,s)=>{
      ctx.save();ctx.globalAlpha=0.12;ctx.fillStyle="#000";ctx.beginPath();ctx.ellipse(x,y+2,s*.1,s*.03,0,0,Math.PI*2);ctx.fill();ctx.restore();
      ctx.fillStyle="#A1887F";ctx.beginPath();ctx.roundRect(x-s*.09,y-s*.1,s*.18,s*.1,s*.04);ctx.fill();
      ctx.fillStyle="#8D6E63";ctx.beginPath();ctx.roundRect(x-s*.03,y-s*.55,s*.06,s*.46,s*.03);ctx.fill();
      ctx.fillStyle="#A1887F";ctx.beginPath();ctx.roundRect(x-s*.07,y-s*.58,s*.14,s*.06,s*.03);ctx.fill();
      const gl=ctx.createRadialGradient(x,y-s*.78,0,x,y-s*.78,s*.22);gl.addColorStop(0,"rgba(255,253,120,0.55)");gl.addColorStop(1,"rgba(255,253,120,0)");ctx.fillStyle=gl;ctx.beginPath();ctx.arc(x,y-s*.78,s*.28,0,Math.PI*2);ctx.fill();
      const bg=ctx.createRadialGradient(x-s*.04,y-s*.82,0,x,y-s*.76,s*.17);bg.addColorStop(0,"#FFF9C4");bg.addColorStop(.6,"#FFD700");bg.addColorStop(1,"#F9A825");ctx.fillStyle=bg;ctx.beginPath();ctx.arc(x,y-s*.76,s*.17,0,Math.PI*2);ctx.fill();
      ctx.fillStyle="rgba(255,255,255,0.4)";ctx.beginPath();ctx.ellipse(x-s*.05,y-s*.84,s*.06,s*.04,-.5,0,Math.PI*2);ctx.fill();
    }},
};

// ─── DESK WITH REWARD ─────────────────────────────────────────────────────────
// Each reward is a detailed SVG illustration designed to look placed on a desk surface

const REWARD_SVG = {
  default: () => `
    <!-- Productivity Cactus — detailed potted plant -->
    <!-- pot shadow -->
    <ellipse cx="50" cy="162" rx="30" ry="7" fill="rgba(0,0,0,0.22)"/>
    <!-- terracotta pot body -->
    <path d="M24,130 Q22,162 50,162 Q78,162 76,130 Z" fill="#C1440E"/>
    <path d="M24,130 Q22,156 50,156 Q78,156 76,130 Z" fill="#D4520F"/>
    <!-- pot rim -->
    <rect x="20" y="122" width="60" height="12" rx="6" fill="#D4520F"/>
    <rect x="20" y="122" width="60" height="6" rx="3" fill="#E8641A"/>
    <!-- soil -->
    <ellipse cx="50" cy="128" rx="28" ry="8" fill="#4a2c0a"/>
    <ellipse cx="50" cy="126" rx="24" ry="6" fill="#5a3510"/>
    <!-- main stem -->
    <rect x="44" y="40" width="12" height="88" rx="6" fill="#2E7D32"/>
    <rect x="46" y="44" width="8" height="80" rx="4" fill="#43A047"/>
    <!-- spines detail -->
    <line x1="38" y1="65" x2="44" y2="60" stroke="#81C784" stroke-width="1.5"/>
    <line x1="38" y1="75" x2="44" y2="70" stroke="#81C784" stroke-width="1.5"/>
    <line x1="56" y1="62" x2="62" y2="57" stroke="#81C784" stroke-width="1.5"/>
    <line x1="56" y1="72" x2="62" y2="67" stroke="#81C784" stroke-width="1.5"/>
    <!-- left arm -->
    <path d="M44,75 Q28,72 26,58 Q24,48 32,46" fill="none" stroke="#2E7D32" stroke-width="10" stroke-linecap="round"/>
    <path d="M44,75 Q30,72 28,60 Q26,50 33,48" fill="none" stroke="#43A047" stroke-width="6" stroke-linecap="round"/>
    <!-- right arm -->
    <path d="M56,85 Q72,82 74,66 Q76,54 68,52" fill="none" stroke="#2E7D32" stroke-width="10" stroke-linecap="round"/>
    <path d="M56,85 Q70,82 72,68 Q74,56 67,54" fill="none" stroke="#43A047" stroke-width="6" stroke-linecap="round"/>
    <!-- flower bud -->
    <circle cx="50" cy="36" r="14" fill="#E91E63"/>
    <circle cx="43" cy="30" r="8" fill="#F06292"/>
    <circle cx="57" cy="30" r="8" fill="#F06292"/>
    <circle cx="50" cy="28" r="8" fill="#F48FB1"/>
    <circle cx="50" cy="36" r="8" fill="#FFD700"/>
    <circle cx="50" cy="36" r="4" fill="#F9A825"/>`,

  cozy: () => `
    <!-- Cosy Mug — ceramic mug with steam and latte art -->
    <!-- mug shadow -->
    <ellipse cx="52" cy="162" rx="36" ry="8" fill="rgba(0,0,0,0.22)"/>
    <!-- mug body -->
    <path d="M16,80 Q14,162 52,162 Q90,162 88,80 Z" fill="#F4F0EC"/>
    <path d="M18,80 Q16,158 52,158 Q88,158 86,80 Z" fill="#FAFAFA"/>
    <!-- mug color band -->
    <path d="M16,80 Q16,110 52,110 Q88,110 88,80 Z" fill="#FF7043"/>
    <path d="M18,80 Q18,107 52,107 Q86,107 86,80 Z" fill="#FF8A65"/>
    <!-- rim -->
    <ellipse cx="52" cy="80" rx="36" ry="11" fill="#F5F5F5"/>
    <ellipse cx="52" cy="80" rx="32" ry="9" fill="#FFFFFF"/>
    <!-- coffee surface -->
    <ellipse cx="52" cy="80" rx="28" ry="7" fill="#6D4C41"/>
    <ellipse cx="52" cy="79" rx="24" ry="5" fill="#795548"/>
    <!-- latte art heart -->
    <path d="M44,78 Q44,74 48,76 Q52,72 56,76 Q60,74 60,78 Q60,82 52,86 Q44,82 44,78Z" fill="rgba(255,255,255,0.35)"/>
    <!-- handle -->
    <path d="M88,95 Q115,95 115,120 Q115,145 88,145" fill="none" stroke="#E8E0D8" stroke-width="18" stroke-linecap="round"/>
    <path d="M88,95 Q110,95 110,120 Q110,145 88,145" fill="none" stroke="#FAFAFA" stroke-width="10" stroke-linecap="round"/>
    <!-- steam wisps -->
    <path d="M38,68 Q32,52 40,36 Q46,24 38,10" fill="none" stroke="rgba(255,255,255,0.6)" stroke-width="4" stroke-linecap="round"/>
    <path d="M52,64 Q46,48 54,32 Q60,18 52,4" fill="none" stroke="rgba(255,255,255,0.5)" stroke-width="3.5" stroke-linecap="round"/>
    <path d="M66,68 Q72,52 64,36 Q58,22 66,8" fill="none" stroke="rgba(255,255,255,0.45)" stroke-width="3" stroke-linecap="round"/>`,

  zen: () => `
    <!-- Mini Zen Garden — wooden tray with sand, rocks and rake -->
    <!-- tray shadow -->
    <ellipse cx="50" cy="162" rx="46" ry="8" fill="rgba(0,0,0,0.22)"/>
    <!-- wooden tray sides -->
    <rect x="4" y="100" width="92" height="62" rx="6" fill="#8D6E63"/>
    <!-- tray interior -->
    <rect x="8" y="104" width="84" height="54" rx="4" fill="#D7CCC8"/>
    <!-- sand texture -->
    <rect x="10" y="106" width="80" height="50" rx="3" fill="#EFEBE9"/>
    <!-- sand rake lines (curved, realistic) -->
    <path d="M14,116 Q50,112 86,116" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <path d="M14,122 Q50,118 86,122" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <path d="M14,128 Q50,124 86,128" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <path d="M14,134 Q50,130 86,134" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <path d="M14,140 Q50,136 86,140" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <path d="M14,146 Q50,142 86,146" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <path d="M14,152 Q50,148 86,152" fill="none" stroke="#D7CCC8" stroke-width="1.5"/>
    <!-- large rock 1 -->
    <ellipse cx="28" cy="128" rx="16" ry="12" fill="#9E9E9E"/>
    <ellipse cx="26" cy="124" rx="12" ry="8" fill="#BDBDBD"/>
    <ellipse cx="24" cy="122" rx="6" ry="4" fill="#E0E0E0"/>
    <!-- large rock 2 -->
    <ellipse cx="66" cy="138" rx="14" ry="10" fill="#757575"/>
    <ellipse cx="64" cy="134" rx="10" ry="7" fill="#9E9E9E"/>
    <ellipse cx="62" cy="132" rx="5" ry="3" fill="#BDBDBD"/>
    <!-- small pebble -->
    <ellipse cx="82" cy="120" rx="6" ry="4" fill="#8D8D8D"/>
    <!-- rake handle (leaning against side) -->
    <rect x="82" y="40" width="5" height="68" rx="2.5" fill="#A1887F" transform="rotate(8 84 74)"/>
    <rect x="74" y="42" width="3" height="14" rx="1.5" fill="#8D6E63" transform="rotate(8 75 49)"/>
    <line x1="74" y1="44" x2="86" y2="46" stroke="#795548" stroke-width="2.5"/>
    <line x1="74" y1="50" x2="86" y2="52" stroke="#795548" stroke-width="2.5"/>
    <line x1="74" y1="56" x2="86" y2="58" stroke="#795548" stroke-width="2.5"/>
    <!-- tray wood grain detail -->
    <line x1="4" y1="115" x2="8" y2="115" stroke="rgba(0,0,0,0.08)" stroke-width="1"/>
    <line x1="4" y1="130" x2="8" y2="130" stroke="rgba(0,0,0,0.08)" stroke-width="1"/>`,

  focused: () => `
    <!-- Focus Hourglass — premium glass hourglass with wood frame -->
    <!-- shadow -->
    <ellipse cx="50" cy="162" rx="24" ry="6" fill="rgba(0,0,0,0.22)"/>
    <!-- wood base -->
    <rect x="26" y="148" width="48" height="14" rx="5" fill="#8D6E63"/>
    <rect x="28" y="148" width="44" height="8" rx="3" fill="#A1887F"/>
    <!-- wood top cap -->
    <rect x="26" y="18" width="48" height="14" rx="5" fill="#8D6E63"/>
    <rect x="28" y="22" width="44" height="6" rx="3" fill="#A1887F"/>
    <!-- vertical pillars -->
    <rect x="28" y="30" width="6" height="120" rx="3" fill="#795548"/>
    <rect x="66" y="30" width="6" height="120" rx="3" fill="#795548"/>
    <!-- glass upper chamber -->
    <path d="M34,32 Q34,85 50,92 Q66,85 66,32 Z" fill="rgba(200,232,255,0.7)"/>
    <path d="M36,34 Q36,82 50,88 Q64,82 64,34 Z" fill="rgba(180,220,255,0.5)"/>
    <!-- upper sand (partially emptied) -->
    <path d="M34,70 Q34,85 50,92 Q66,85 66,70 Z" fill="#F9A825" opacity="0.9"/>
    <path d="M36,72 Q36,83 50,89 Q64,83 64,72 Z" fill="#FFB300" opacity="0.8"/>
    <!-- glass lower chamber -->
    <path d="M34,148 Q34,95 50,92 Q66,95 66,148 Z" fill="rgba(200,232,255,0.7)"/>
    <path d="M36,146 Q36,97 50,92 Q64,97 64,146 Z" fill="rgba(180,220,255,0.5)"/>
    <!-- lower sand (accumulated) -->
    <path d="M34,125 Q34,148 50,148 Q66,148 66,125 Q58,118 50,116 Q42,118 34,125Z" fill="#F9A825" opacity="0.9"/>
    <path d="M36,130 Q36,146 50,146 Q64,146 64,130 Q57,124 50,122 Q43,124 36,130Z" fill="#FFB300" opacity="0.85"/>
    <!-- sand stream (falling) -->
    <line x1="50" y1="92" x2="50" y2="116" stroke="#FFD54F" stroke-width="2" opacity="0.8"/>
    <!-- glass shine -->
    <path d="M38,36 Q36,70 38,88" fill="none" stroke="rgba(255,255,255,0.5)" stroke-width="3" stroke-linecap="round"/>`,

  chaotic: () => `
    <!-- Chaos Trophy — golden winner's cup with engraving -->
    <!-- shadow -->
    <ellipse cx="50" cy="162" rx="28" ry="7" fill="rgba(0,0,0,0.22)"/>
    <!-- base plate -->
    <rect x="26" y="148" width="48" height="14" rx="3" fill="#8D6E63"/>
    <rect x="24" y="144" width="52" height="8" rx="3" fill="#795548"/>
    <!-- stem -->
    <rect x="44" y="118" width="12" height="30" rx="4" fill="#B8860B"/>
    <rect x="42" y="114" width="16" height="8" rx="3" fill="#DAA520"/>
    <!-- cup body -->
    <path d="M16,40 Q12,95 20,112 Q32,126 50,126 Q68,126 80,112 Q88,95 84,40 Z" fill="#B8860B"/>
    <path d="M18,42 Q14,95 22,110 Q34,124 50,124 Q66,124 78,110 Q86,95 82,42 Z" fill="#DAA520"/>
    <path d="M20,44 Q16,92 24,108 Q36,120 50,120 Q64,120 76,108 Q84,92 80,44 Z" fill="#FFD700"/>
    <!-- cup shine/highlight -->
    <path d="M24,48 Q20,90 26,106 Q32,88 28,48 Z" fill="rgba(255,255,255,0.28)"/>
    <!-- rim -->
    <ellipse cx="50" cy="40" rx="34" ry="10" fill="#B8860B"/>
    <ellipse cx="50" cy="40" rx="30" ry="8" fill="#FFD700"/>
    <ellipse cx="50" cy="38" rx="26" ry="6" fill="#FFE566"/>
    <!-- handles -->
    <path d="M16,58 Q-4,65 -4,90 Q-4,115 16,108" fill="none" stroke="#B8860B" stroke-width="14" stroke-linecap="round"/>
    <path d="M16,60 Q0,67 0,90 Q0,112 16,106" fill="none" stroke="#FFD700" stroke-width="8" stroke-linecap="round"/>
    <path d="M84,58 Q104,65 104,90 Q104,115 84,108" fill="none" stroke="#B8860B" stroke-width="14" stroke-linecap="round"/>
    <path d="M84,60 Q100,67 100,90 Q100,112 84,106" fill="none" stroke="#FFD700" stroke-width="8" stroke-linecap="round"/>
    <!-- engraving text -->
    <text x="50" y="88" text-anchor="middle" font-size="11" fill="rgba(120,80,0,0.6)" font-weight="bold">★ #1 ★</text>
    <!-- star on top -->
    <text x="50" y="32" text-anchor="middle" font-size="18" fill="#FFF176">★</text>`,

  creative: () => `
    <!-- Magic Idea Lamp — sleek modern desk lamp with warm glow -->
    <!-- shadow -->
    <ellipse cx="50" cy="162" rx="28" ry="7" fill="rgba(0,0,0,0.22)"/>
    <!-- base (circular weighted) -->
    <ellipse cx="50" cy="152" rx="30" ry="10" fill="#37474F"/>
    <ellipse cx="50" cy="150" rx="26" ry="7" fill="#455A64"/>
    <ellipse cx="50" cy="149" rx="20" ry="5" fill="#546E7A"/>
    <!-- arm joint at base -->
    <circle cx="50" cy="144" r="8" fill="#37474F"/>
    <circle cx="50" cy="144" r="5" fill="#546E7A"/>
    <!-- vertical arm -->
    <rect x="46" y="68" width="8" height="80" rx="4" fill="#455A64"/>
    <rect x="47" y="70" width="5" height="76" rx="2.5" fill="#546E7A"/>
    <!-- arm joint at top -->
    <circle cx="50" cy="68" r="7" fill="#37474F"/>
    <!-- horizontal arm -->
    <rect x="50" y="64" width="52" height="7" rx="3.5" fill="#455A64" transform="rotate(-20 50 68)"/>
    <!-- lamp head -->
    <path d="M72,28 Q60,18 48,24 Q36,30 38,46 Q40,60 56,64 Q72,68 80,56 Q88,44 80,34 Q78,30 72,28Z" fill="#37474F"/>
    <path d="M70,30 Q60,22 50,28 Q40,34 42,48 Q44,60 58,63 Q72,66 78,56 Q84,46 77,36 Q74,30 70,30Z" fill="#546E7A"/>
    <!-- bulb inner glow -->
    <circle cx="62" cy="46" r="18" fill="rgba(255,253,120,0.18)"/>
    <circle cx="62" cy="46" r="13" fill="rgba(255,248,80,0.25)"/>
    <circle cx="62" cy="46" r="9" fill="rgba(255,244,40,0.4)"/>
    <circle cx="62" cy="46" r="5" fill="rgba(255,244,40,0.7)"/>
    <!-- outer glow rays -->
    <circle cx="62" cy="46" r="28" fill="rgba(255,248,120,0.08)"/>
    <circle cx="62" cy="46" r="38" fill="rgba(255,248,120,0.04)"/>
    <!-- power cord -->
    <path d="M50,148 Q45,155 42,162" fill="none" stroke="#263238" stroke-width="3" stroke-linecap="round"/>
    <!-- sparkle effects -->
    <text x="34" y="22" font-size="12" fill="rgba(255,244,40,0.8)">✦</text>
    <text x="82" y="18" font-size="9" fill="rgba(255,244,40,0.6)">✦</text>
    <text x="92" y="36" font-size="10" fill="rgba(255,244,40,0.5)">✦</text>`,
};
function DeskWithReward({photoUrl, archetype}) {
  const reward = REWARDS[archetype] || REWARDS.default;
  const svgContent = REWARD_SVG[archetype] || REWARD_SVG.default;

  return (
    <div style={{width:"100%",position:"relative",borderRadius:20,overflow:"hidden",
      border:"3px solid white",boxShadow:"0 8px 32px rgba(0,0,0,0.18)"}}>
      {/* tape strips */}
      <div style={{position:"absolute",top:-7,left:"18%",width:56,height:13,background:"rgba(255,255,200,0.85)",borderRadius:3,transform:"rotate(-2deg)",zIndex:10,boxShadow:"0 1px 3px rgba(0,0,0,0.1)"}}/>
      <div style={{position:"absolute",top:-7,right:"18%",width:56,height:13,background:"rgba(255,255,200,0.85)",borderRadius:3,transform:"rotate(2deg)",zIndex:10,boxShadow:"0 1px 3px rgba(0,0,0,0.1)"}}/>

      {/* photo */}
      <div style={{position:"relative",aspectRatio:"16/7"}}>
        {photoUrl
          ? <img src={photoUrl} alt="desk" style={{width:"100%",height:"100%",objectFit:"cover",display:"block"}}/>
          : <div style={{width:"100%",height:"100%",background:"linear-gradient(135deg,#a7f3d0,#bae6fd)"}}/>}

        {/* bottom vignette to ground the reward */}
        <div style={{position:"absolute",inset:0,background:"linear-gradient(to bottom, transparent 50%, rgba(0,0,0,0.25) 100%)"}}/>

        {/* SVG reward — bottom-left corner, fixed size, looks placed on desk */}
        <svg
          viewBox="0 0 100 165"
          style={{
            position:"absolute",
            bottom:0,
            left:"4%",
            width:"16%",
            height:"auto",
            filter:"drop-shadow(2px 4px 6px rgba(0,0,0,0.35))",
            zIndex:5,
          }}
          dangerouslySetInnerHTML={{__html: svgContent()}}
        />

        {/* reward name badge */}
        <div style={{position:"absolute",bottom:10,right:10,background:"rgba(0,0,0,0.7)",backdropFilter:"blur(10px)",borderRadius:12,padding:"5px 11px",display:"flex",alignItems:"center",gap:6,zIndex:6}}>
          <span style={{fontSize:14}}>{reward.emoji}</span>
          <span style={{fontSize:10,fontWeight:900,color:"white",letterSpacing:.5}}>{reward.name}</span>
        </div>

        {/* new addition badge */}
        <div style={{position:"absolute",bottom:10,left:"22%",background:"rgba(255,220,50,0.92)",borderRadius:8,padding:"3px 8px",fontSize:9,fontWeight:900,color:"#7a5c00",letterSpacing:1,textTransform:"uppercase",zIndex:6,boxShadow:"0 2px 6px rgba(0,0,0,0.15)"}}>
          ✦ New addition
        </div>
      </div>
    </div>
  );
}

// ─── STATE ────────────────────────────────────────────────────────────────────

const BODY_COLORS_MAP = [
  { id:"green",  hex:"#4CAF50", dark:"#2E7D32", grad:["#81C784","#4CAF50"] },
  { id:"coral",  hex:"#FF6B6B", dark:"#C62828", grad:["#FF8A65","#FF6B6B"] },
  { id:"sky",    hex:"#42A5F5", dark:"#1565C0", grad:["#64B5F6","#42A5F5"] },
  { id:"sand",   hex:"#F9A825", dark:"#E65100", grad:["#FFB300","#F9A825"] },
  { id:"violet", hex:"#AB47BC", dark:"#6A1B9A", grad:["#BA68C8","#AB47BC"] },
];

const defaultState = {
  step: 1,
  photoUrl: null,
  persona: null,
  selectedHobbies: [],
  selectedMusic: [],
  selectedMovies: [],
  selectedStyle: null,
  step2Update: null,
  step3Update: null,
};

const Ctx = createContext(null);

function Provider({children}) {
  const [state, setState] = useState(defaultState);
  const update = f => setState(p => ({...p,...(typeof f === "function" ? f(p) : f)}));
  const reset  = () => setState(defaultState);
  return <Ctx.Provider value={{state, update, reset}}>{children}</Ctx.Provider>;
}

function useGame() { return useContext(Ctx); }

// ─── HELPERS ─────────────────────────────────────────────────────────────────

const bc = id => BODY_COLORS_MAP.find(c=>c.id===id) || BODY_COLORS_MAP[0];

function toggleMax(arr, val, max) {
  if (arr.includes(val)) return arr.filter(x=>x!==val);
  if (arr.length >= max) return arr;
  return [...arr, val];
}

function buildPlaylist(musicIds) {
  const tracks = [];
  musicIds.forEach(id => {
    (PLAYLISTS[id]||[]).slice(0,3).forEach(([title,artist]) => tracks.push({title, artist, genreId:id}));
  });
  return tracks.slice(0,8);
}

function buildWatchlist(movieIds) {
  const films = [];
  movieIds.forEach(id => {
    (WATCHLISTS[id]||[]).slice(0,2).forEach(([title,platform,icon,reason]) => films.push({title,platform,icon,reason}));
  });
  return films.slice(0,6);
}

// Single source of truth for reward selection — used by Step4 AND Step5
function getRewardArchetype(state) {
  const { selectedStyle:style, selectedHobbies:hobbies, selectedMusic:music,
          selectedMovies:movies, persona } = state;
  const deskObjects = (persona?.deskObjects || []).map(o => o.toLowerCase());

  const REWARD_KEYWORDS = {
    creative: ["lamp","light","bulb","lantern"],
    cozy:     ["mug","cup","coffee","tea","drink","thermos","bottle","candle"],
    zen:      ["plant","cactus","succulent","garden","rock","stone","pebble","terrarium","bonsai"],
    chaotic:  ["trophy","award","medal"],
    focused:  ["hourglass","timer","clock","sand"],
  };

  const isOnDesk = key => {
    if (!deskObjects.length) return false;
    return (REWARD_KEYWORDS[key]||[]).some(kw => deskObjects.some(o => o.includes(kw)));
  };

  const scores = { creative:0, cozy:0, zen:0, chaotic:0, focused:0 };

  // Style → weight 3
  ({minimal:"zen", techy:"creative", cozy:"cozy", retro:"chaotic", nature:"zen", artistic:"creative"}[style] || null)
    && (scores[{minimal:"zen", techy:"creative", cozy:"cozy", retro:"chaotic", nature:"zen", artistic:"creative"}[style]] += 3);

  // Hobbies → weight 2 each
  const hobbyMap = { coding:"creative", gym:"chaotic", reading:"cozy", cooking:"cozy",
                     art:"creative", music:"cozy", travel:"chaotic", gaming:"chaotic" };
  (hobbies||[]).forEach(h => hobbyMap[h] && (scores[hobbyMap[h]] += 2));

  // Music → weight 2 each (strong lifestyle signal)
  const musicMap = { lofi:"cozy", ambient:"zen", jazz:"zen", classical:"zen",
                     techno:"chaotic", rock:"chaotic", pop:"creative", hiphop:"chaotic" };
  (music||[]).forEach(m => musicMap[m] && (scores[musicMap[m]] += 2));

  // Movies → weight 1 each
  const movieMap = { documentary:"zen", mystery:"cozy", drama:"cozy", comedy:"chaotic",
                     fantasy:"creative", anime:"creative", scifi:"creative", action:"chaotic" };
  (movies||[]).forEach(m => movieMap[m] && (scores[movieMap[m]] += 1));

  // Pick winner: highest score, not already on desk
  const ranked = Object.entries(scores).sort((a,b) => b[1]-a[1]);
  for (const [key] of ranked) if (!isOnDesk(key)) return key;
  // Fallback: anything not on desk
  for (const key of ["creative","chaotic","zen","cozy","focused"]) if (!isOnDesk(key)) return key;
  return "creative";
}

// ─── AI CALLS ────────────────────────────────────────────────────────────────

async function analyzeDesk(photoUrl) {
  const compressImage = url => new Promise(res => {
    const img = new Image();
    img.onload = () => {
      const MAX=800, scale=img.width>MAX?MAX/img.width:1;
      const c=document.createElement("canvas");
      c.width=Math.round(img.width*scale); c.height=Math.round(img.height*scale);
      c.getContext("2d").drawImage(img,0,0,c.width,c.height);
      res(c.toDataURL("image/jpeg",0.82));
    };
    img.src=url;
  });
  const b64=(await compressImage(photoUrl)).split(",")[1];
  const prompt=`You are a witty desk personality analyser. Study this desk photo carefully.
Return ONLY a JSON object — start with { end with } — no other text.
{"archetype":"cozy","tagline":"Zen Tea Sorcerer","colorId":"green","description":"2 punchy sentences about THIS desk with humour.","deskTraits":["trait1","trait2","trait3"],"deskObjects":["mug","plant","keyboard","monitor","notebook"]}
archetype: chaotic|focused|cozy|zen|creative|default. colorId: green|coral|sky|sand|violet. tagline: 2-4 words. deskTraits: exactly 3 strings. deskObjects: list of 5-8 physical objects you can actually see on the desk (use simple lowercase English nouns like "mug", "plant", "lamp", "hourglass", "cactus", "notebook", "trophy", "candle").`;
  const res=await fetch("/api/analyze",{method:"POST",headers:{"Content-Type":"application/json"},body:JSON.stringify({model:"claude-sonnet-4-6",max_tokens:350,messages:[{role:"user",content:[{type:"image",source:{type:"base64",media_type:"image/jpeg",data:b64}},{type:"text",text:prompt}]}]})});
  const data=await res.json();
  if(data.error) throw new Error(data.error.message);
  const raw=data.content?.find(b=>b.type==="text")?.text||"";
  const m=raw.match(/\{[\s\S]*\}/);
  if(!m) throw new Error("No JSON: "+raw.slice(0,200));
  const p=JSON.parse(m[0]);
  if(!p.description||!p.tagline) throw new Error("Missing fields");
  return p;
}

async function updatePersonaStep2(persona, hobbies, music) {
  const hL=hobbies.map(id=>HOBBIES.find(h=>h.id===id)?.label||id).join(", ");
  const mL=music.map(id=>MUSIC_GENRES.find(m=>m.id===id)?.label||id).join(", ");
  const prompt=`Desk persona: archetype="${persona.archetype}", tagline="${persona.tagline}", description="${persona.description}".
New: hobbies=${hL}, music=${mL}. Evolve incorporating these. Return ONLY JSON:
{"tagline":"2-4 words","description":"2 punchy sentences blending desk+hobbies+music","deskTraits":["t1","t2","t3"]}
Start with {`;
  const res=await fetch("/api/analyze",{method:"POST",headers:{"Content-Type":"application/json"},body:JSON.stringify({model:"claude-sonnet-4-6",max_tokens:250,messages:[{role:"user",content:[{type:"text",text:prompt}]}]})});
  const data=await res.json();
  if(data.error) throw new Error(data.error.message);
  const raw=data.content?.find(b=>b.type==="text")?.text||"";
  const m=raw.match(/\{[\s\S]*\}/); if(!m) throw new Error("No JSON");
  return JSON.parse(m[0]);
}

async function updatePersonaStep3(persona, step2Update, movies, style) {
  const mL=movies.map(id=>MOVIE_GENRES.find(m=>m.id===id)?.label||id).join(", ");
  const sL=DESK_STYLES.find(s=>s.id===style)?.label||style;
  const cur=step2Update||persona;
  const prompt=`Persona so far: tagline="${cur.tagline}", description="${cur.description}".
New: films=${mL}, desk style=${sL}. Final evolution. Return ONLY JSON:
{"tagline":"2-4 words final","description":"2 punchy final sentences","deskTraits":["t1","t2","t3"]}
Start with {`;
  const res=await fetch("/api/analyze",{method:"POST",headers:{"Content-Type":"application/json"},body:JSON.stringify({model:"claude-sonnet-4-6",max_tokens:250,messages:[{role:"user",content:[{type:"text",text:prompt}]}]})});
  const data=await res.json();
  if(data.error) throw new Error(data.error.message);
  const raw=data.content?.find(b=>b.type==="text")?.text||"";
  const m=raw.match(/\{[\s\S]*\}/); if(!m) throw new Error("No JSON");
  return JSON.parse(m[0]);
}

// ─── AVATAR ───────────────────────────────────────────────────────────────────

// Animated hobby accessories — each returns SVG elements with CSS animations
const HOBBY_ARMS = {
  gym: (g2, uid) => ({
    // Right arm flexing with dumbbell going up/down
    right: `
      <g style="transform-origin:90px 85px;animation:armFlexR_${uid} 1.2s ease-in-out infinite">
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- dumbbell -->
        <rect x="91" y="78" width="18" height="5" rx="2.5" fill="#555"/>
        <rect x="91" y="74" width="5" height="13" rx="2" fill="#777"/>
        <rect x="104" y="74" width="5" height="13" rx="2" fill="#777"/>
      </g>`,
    // Left arm also curling
    left: `
      <g style="transform-origin:10px 85px;animation:armFlexL_${uid} 1.2s ease-in-out infinite 0.6s">
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- dumbbell left -->
        <rect x="-9" y="78" width="18" height="5" rx="2.5" fill="#555"/>
        <rect x="-9" y="74" width="5" height="13" rx="2" fill="#777"/>
        <rect x="4" y="74" width="5" height="13" rx="2" fill="#777"/>
      </g>`,
    anim: `
      @keyframes armFlexR_${uid} { 0%,100%{transform:rotate(-15deg) translateY(0)} 50%{transform:rotate(15deg) translateY(-6px)} }
      @keyframes armFlexL_${uid} { 0%,100%{transform:rotate(15deg) translateY(0)} 50%{transform:rotate(-15deg) translateY(-6px)} }`,
  }),
  cooking: (g2, uid) => ({
    right: `
      <g style="transform-origin:90px 85px;animation:panWave_${uid} 0.9s ease-in-out infinite">
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- frying pan -->
        <ellipse cx="104" cy="82" rx="10" ry="9" fill="#444"/>
        <ellipse cx="104" cy="81" rx="8" ry="7" fill="#666"/>
        <rect x="93" y="80" width="10" height="4" rx="2" fill="#333"/>
        <!-- sizzle dots -->
        <circle cx="101" cy="79" r="1.5" fill="#FF8C00" style="animation:sizzle_${uid} 0.5s ease-in-out infinite"/>
        <circle cx="106" cy="76" r="1" fill="#FF8C00" style="animation:sizzle_${uid} 0.5s ease-in-out infinite 0.2s"/>
        <circle cx="110" cy="80" r="1.2" fill="#FF8C00" style="animation:sizzle_${uid} 0.5s ease-in-out infinite 0.1s"/>
      </g>`,
    left: `
      <g>
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- spatula -->
        <rect x="-6" y="72" width="4" height="22" rx="2" fill="#888"/>
        <rect x="-8" y="68" width="8" height="6" rx="1" fill="#aaa"/>
      </g>`,
    anim: `
      @keyframes panWave_${uid} { 0%,100%{transform:rotate(-8deg)} 50%{transform:rotate(8deg) translateY(-4px)} }
      @keyframes sizzle_${uid}  { 0%,100%{opacity:0.3;transform:translateY(0)} 50%{opacity:1;transform:translateY(-3px)} }`,
  }),
  gaming: (g2, uid) => ({
    right: `
      <g style="animation:ctrlBob_${uid} 0.8s ease-in-out infinite">
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- controller body -->
        <rect x="88" y="78" width="22" height="14" rx="5" fill="#222"/>
        <rect x="90" y="80" width="6" height="6" rx="1" fill="#444"/>
        <circle cx="105" cy="82" r="2" fill="#E53935"/>
        <circle cx="109" cy="84" r="2" fill="#43A047"/>
        <circle cx="107" cy="80" r="2" fill="#1E88E5"/>
      </g>`,
    left: `
      <g style="animation:ctrlBob_${uid} 0.8s ease-in-out infinite 0.4s">
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- left side of controller -->
        <rect x="-10" y="78" width="14" height="10" rx="4" fill="#222"/>
        <circle cx="-3" cy="82" r="3" fill="#333"/>
        <circle cx="-3" cy="82" r="1.5" fill="#555"/>
      </g>`,
    anim: `@keyframes ctrlBob_${uid} { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-5px)} }`,
  }),
  coding: (g2, uid) => ({
    right: `
      <g>
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- mini laptop -->
        <rect x="88" y="76" width="22" height="15" rx="3" fill="#333"/>
        <rect x="89" y="77" width="20" height="12" rx="2" fill="#1a1a2e"/>
        <!-- code lines with typing animation -->
        <rect x="91" y="79" width="8" height="1.5" rx="1" fill="#4ade80" style="animation:codeLine_${uid} 1.5s steps(1) infinite"/>
        <rect x="91" y="82" width="12" height="1.5" rx="1" fill="#60a5fa" style="animation:codeLine_${uid} 1.5s steps(1) infinite 0.5s"/>
        <rect x="91" y="85" width="6" height="1.5" rx="1" fill="#f472b6" style="animation:codeLine_${uid} 1.5s steps(1) infinite 1s"/>
        <!-- cursor blink -->
        <rect x="99" y="79" width="1.5" height="6" rx="0.5" fill="white" style="animation:blink_${uid} 0.8s step-start infinite"/>
        <rect x="88" y="90" width="22" height="4" rx="1" fill="#444"/>
      </g>`,
    left: `
      <g>
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- coffee cup for coder -->
        <rect x="-8" y="80" width="10" height="12" rx="3" fill="#FF8A65"/>
        <ellipse cx="-3" cy="80" rx="5" ry="2" fill="#FFCCBC"/>
        <path d="M2,83 Q8,86 2,90" fill="none" stroke="#FF8A65" stroke-width="2" stroke-linecap="round"/>
      </g>`,
    anim: `
      @keyframes codeLine_${uid} { 0%,49%{opacity:1} 50%,100%{opacity:0.3} }
      @keyframes blink_${uid}    { 0%,49%{opacity:1} 50%,100%{opacity:0} }`,
  }),
  reading: (g2, uid) => ({
    right: `
      <g style="animation:bookTilt_${uid} 2s ease-in-out infinite">
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- open book -->
        <path d="M88,73 L88,92 L100,89 L100,73 Z" fill="#E3F2FD"/>
        <path d="M100,73 L100,89 L112,92 L112,73 Z" fill="#fff"/>
        <rect x="99" y="73" width="2" height="17" rx="1" fill="#90CAF9"/>
        <!-- page lines -->
        <line x1="91" y1="77" x2="98" y2="76" stroke="#90CAF9" stroke-width="1"/>
        <line x1="91" y1="80" x2="98" y2="79" stroke="#90CAF9" stroke-width="1"/>
        <line x1="91" y1="83" x2="98" y2="82" stroke="#90CAF9" stroke-width="1"/>
        <line x1="102" y1="77" x2="109" y2="78" stroke="#BDBDBD" stroke-width="1"/>
        <line x1="102" y1="80" x2="109" y2="81" stroke="#BDBDBD" stroke-width="1"/>
        <line x1="102" y1="83" x2="109" y2="84" stroke="#BDBDBD" stroke-width="1"/>
      </g>`,
    left: `
      <g>
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- reading glasses -->
        <path d="M-4,75 Q-1,71 3,75 Q6,79 3,81 Q-1,85 -4,81 Q-7,77 -4,75Z" fill="none" stroke={g2} stroke-width="1.5"/>
        <path d="M3,75 L8,75" stroke={g2} stroke-width="1.5"/>
      </g>`,
    anim: `@keyframes bookTilt_${uid} { 0%,100%{transform:rotate(-5deg)} 50%{transform:rotate(5deg)} }`,
  }),
  art: (g2, uid) => ({
    right: `
      <g style="animation:brushStroke_${uid} 1s ease-in-out infinite">
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- paintbrush -->
        <rect x="94" y="68" width="3" height="22" rx="1.5" fill="#8D6E63"/>
        <path d="M93,68 Q95.5,60 98,68 Z" fill="#FF6B6B"/>
        <!-- paint stroke trail -->
        <path d="M97,74 Q108,66 116,72" fill="none" stroke="#FF6B6B" stroke-width="3" stroke-linecap="round" opacity="0.7" style="animation:fadeStroke_${uid} 1s ease-in-out infinite"/>
        <path d="M97,80 Q110,76 118,82" fill="none" stroke="#FFD700" stroke-width="3" stroke-linecap="round" opacity="0.7" style="animation:fadeStroke_${uid} 1s ease-in-out infinite 0.3s"/>
        <path d="M97,86 Q106,84 114,90" fill="none" stroke="#4FC3F7" stroke-width="3" stroke-linecap="round" opacity="0.7" style="animation:fadeStroke_${uid} 1s ease-in-out infinite 0.6s"/>
      </g>`,
    left: `
      <g>
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- palette -->
        <ellipse cx="-2" cy="82" rx="8" ry="9" fill="#F5F5F5"/>
        <circle cx="-5" cy="78" r="2" fill="#FF6B6B"/><circle cx="-1" cy="76" r="2" fill="#FFD700"/>
        <circle cx="3" cy="78" r="2" fill="#4FC3F7"/><circle cx="4" cy="83" r="2" fill="#4CAF50"/>
        <circle cx="-3" cy="86" r="2" fill="#AB47BC"/>
      </g>`,
    anim: `
      @keyframes brushStroke_${uid} { 0%,100%{transform:rotate(-10deg) translateY(0)} 50%{transform:rotate(5deg) translateY(-5px)} }
      @keyframes fadeStroke_${uid}  { 0%{opacity:0} 30%{opacity:0.7} 100%{opacity:0} }`,
  }),
  music: (g2, uid) => ({
    right: `
      <g>
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- guitar -->
        <rect x="93" y="66" width="4" height="24" rx="2" fill="#8D6E63"/>
        <ellipse cx="95" cy="86" rx="6" ry="8" fill="#D4A05A"/>
        <ellipse cx="95" cy="86" rx="4" ry="6" fill="#C19046"/>
        <circle cx="95" cy="86" r="1.5" fill="#8D6E63"/>
        <line x1="93" y1="70" x2="97" y2="70" stroke="#888" stroke-width="0.7"/>
        <line x1="93" y1="72" x2="97" y2="72" stroke="#888" stroke-width="0.7"/>
        <line x1="93" y1="74" x2="97" y2="74" stroke="#888" stroke-width="0.7"/>
      </g>`,
    left: `
      <g>
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- music notes floating -->
        <text x="-8" y="78" font-size="9" fill={g2} style="animation:noteFloat_${uid} 1.2s ease-in-out infinite">♪</text>
        <text x="-4" y="88" font-size="7" fill={g2} style="animation:noteFloat_${uid} 1.2s ease-in-out infinite 0.4s">♫</text>
      </g>`,
    anim: `@keyframes noteFloat_${uid} { 0%,100%{transform:translateY(0) rotate(-10deg);opacity:0.7} 50%{transform:translateY(-8px) rotate(10deg);opacity:1} }`,
  }),
  travel: (g2, uid) => ({
    right: `
      <g style="animation:bagSwing_${uid} 1.5s ease-in-out infinite">
        <rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- suitcase -->
        <rect x="89" y="76" width="20" height="16" rx="4" fill="#1565C0"/>
        <rect x="89" y="76" width="20" height="16" rx="4" fill="none" stroke="#0D47A1" stroke-width="1"/>
        <rect x="95" y="73" width="8" height="4" rx="2" fill="#0D47A1"/>
        <line x1="89" y1="84" x2="109" y2="84" stroke="#0D47A1" stroke-width="1"/>
        <line x1="99" y1="76" x2="99" y2="92" stroke="#0D47A1" stroke-width="1"/>
        <!-- wheels -->
        <circle cx="92" cy="92" r="2" fill="#333"/><circle cx="106" cy="92" r="2" fill="#333"/>
      </g>`,
    left: `
      <g>
        <rect x="2" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
        <rect x="3" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>
        <!-- map -->
        <rect x="-8" y="76" width="12" height="16" rx="2" fill="#FFF9C4"/>
        <line x1="-6" y1="80" x2="2" y2="80" stroke="#BDBDBD" stroke-width="0.8"/>
        <line x1="-6" y1="83" x2="2" y2="84" stroke="#BDBDBD" stroke-width="0.8"/>
        <line x1="-4" y1="86" x2="1" y2="87" stroke="#BDBDBD" stroke-width="0.8"/>
        <circle cx="-2" cy="82" r="2" fill="#FF6B6B"/>
      </g>`,
    anim: `@keyframes bagSwing_${uid} { 0%,100%{transform:rotate(-5deg)} 50%{transform:rotate(5deg) translateY(-3px)} }`,
  }),
  default: (g2, uid) => ({
    right: `<rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/><rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>`,
    left:  `<rect x="2"  y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/><rect x="3"  y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>`,
    anim:  "",
  }),
};

// ─── MUSIC HEAD ACCESSORIES (step 2+) ────────────────────────────────────────
const MUSIC_HATS = {
  lofi: (uid) => ({
    svg: `
      <rect x="24" y="10" width="52" height="22" rx="14" fill="#5C6BC0"/>
      <rect x="24" y="10" width="52" height="14" rx="10" fill="#7986CB"/>
      <rect x="22" y="20" width="56" height="6" rx="3" fill="#3949AB"/>
      <rect x="16" y="24" width="10" height="14" rx="5" fill="#263238" style="animation:hpBob_${uid} 1.5s ease-in-out infinite"/>
      <rect x="74" y="24" width="10" height="14" rx="5" fill="#263238" style="animation:hpBob_${uid} 1.5s ease-in-out infinite"/>
      <rect x="17" y="25" width="8" height="12" rx="4" fill="#37474F"/>
      <rect x="75" y="25" width="8" height="12" rx="4" fill="#37474F"/>
      <circle cx="21" cy="31" r="3" fill="#4FC3F7"/>
      <circle cx="79" cy="31" r="3" fill="#4FC3F7"/>`,
    anim: `@keyframes hpBob_${uid} { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-2px)} }`,
  }),
  techno: (uid) => ({
    svg: `
      <rect x="20" y="27" width="22" height="12" rx="6" fill="#111"/>
      <rect x="58" y="27" width="22" height="12" rx="6" fill="#111"/>
      <line x1="42" y1="33" x2="58" y2="33" stroke="#333" stroke-width="2.5"/>
      <line x1="16" y1="33" x2="20" y2="33" stroke="#333" stroke-width="2"/>
      <line x1="80" y1="33" x2="84" y2="33" stroke="#333" stroke-width="2"/>
      <rect x="21" y="28" width="20" height="10" rx="5" fill="#00E5FF" opacity="0.25" style="animation:neonPulse_${uid} 0.8s ease-in-out infinite"/>
      <rect x="59" y="28" width="20" height="10" rx="5" fill="#00E5FF" opacity="0.25" style="animation:neonPulse_${uid} 0.8s ease-in-out infinite 0.4s"/>
      <rect x="24" y="30" width="6" height="2" rx="1" fill="rgba(255,255,255,0.4)"/>
      <rect x="62" y="30" width="6" height="2" rx="1" fill="rgba(255,255,255,0.4)"/>`,
    anim: `@keyframes neonPulse_${uid} { 0%,100%{opacity:0.2} 50%{opacity:0.6} }`,
  }),
  rock: (uid) => ({
    svg: `
      <path d="M35,14 Q38,0 42,6 Q44,-4 50,2 Q52,-6 56,4 Q60,0 63,14" fill="#E53935" stroke="#B71C1C" stroke-width="1" style="animation:rockSpike_${uid} 0.6s ease-in-out infinite"/>
      <rect x="30" y="12" width="40" height="6" rx="3" fill="#B71C1C"/>
      <rect x="22" y="17" width="56" height="7" rx="3" fill="#212121"/>
      <circle cx="38" cy="20" r="2" fill="#FFD700"/>
      <circle cx="50" cy="20" r="2" fill="#FFD700"/>
      <circle cx="62" cy="20" r="2" fill="#FFD700"/>`,
    anim: `@keyframes rockSpike_${uid} { 0%,100%{transform:scaleY(1)} 50%{transform:scaleY(1.08)} }`,
  }),
  pop: (uid) => ({
    svg: `
      <ellipse cx="38" cy="31" rx="7" ry="8" fill="#E91E63" style="animation:starGlam_${uid} 1s ease-in-out infinite"/>
      <ellipse cx="62" cy="31" rx="7" ry="8" fill="#E91E63" style="animation:starGlam_${uid} 1s ease-in-out infinite 0.5s"/>
      <text x="38" y="35" text-anchor="middle" font-size="9" fill="white">★</text>
      <text x="62" y="35" text-anchor="middle" font-size="9" fill="white">★</text>
      <line x1="30" y1="33" x2="34" y2="33" stroke="#F8BBD9" stroke-width="2"/>
      <line x1="66" y1="33" x2="70" y2="33" stroke="#F8BBD9" stroke-width="2"/>
      <line x1="45" y1="33" x2="55" y2="33" stroke="#F8BBD9" stroke-width="1.5"/>
      <text x="22" y="22" font-size="8" fill="#FFD700" style="animation:glitter_${uid} 0.7s ease-in-out infinite">✦</text>
      <text x="72" y="20" font-size="7" fill="#FF80AB" style="animation:glitter_${uid} 0.7s ease-in-out infinite 0.35s">✦</text>
      <text x="44" y="12" font-size="6" fill="#E040FB" style="animation:glitter_${uid} 0.7s ease-in-out infinite 0.15s">✦</text>`,
    anim: `@keyframes starGlam_${uid}{0%,100%{transform:scale(1)}50%{transform:scale(1.08)}} @keyframes glitter_${uid}{0%,100%{opacity:0.3;transform:scale(0.8)}50%{opacity:1;transform:scale(1.2)}}`,
  }),
  jazz: (uid) => ({
    svg: `
      <ellipse cx="50" cy="16" rx="32" ry="7" fill="#4E342E"/>
      <ellipse cx="50" cy="16" rx="28" ry="5" fill="#5D4037"/>
      <path d="M22,16 Q28,4 50,4 Q72,4 78,16" fill="#4E342E"/>
      <path d="M24,15 Q30,5 50,5 Q70,5 76,15" fill="#6D4C41"/>
      <path d="M26,16 Q28,13 50,13 Q72,13 74,16" fill="none" stroke="#FFD700" stroke-width="2"/>
      <path d="M68,14 Q78,4 76,18" fill="#F5F5F5" stroke="#E0E0E0" stroke-width="0.5"/>`,
    anim: ``,
  }),
  ambient: (uid) => ({
    svg: `
      <path d="M30,14 Q28,2 40,8 Q42,0 50,6 Q58,0 60,8 Q72,2 70,14" fill="#2E7D32" style="animation:leafSway_${uid} 2s ease-in-out infinite"/>
      <path d="M32,14 Q30,4 40,9 Q50,5 60,9 Q70,4 68,14" fill="#43A047"/>
      <circle cx="38" cy="8" r="2" fill="rgba(100,200,255,0.7)" style="animation:dewDrop_${uid} 2s ease-in-out infinite"/>
      <circle cx="50" cy="5" r="2.5" fill="rgba(100,200,255,0.7)" style="animation:dewDrop_${uid} 2s ease-in-out infinite 0.7s"/>
      <circle cx="62" cy="8" r="2" fill="rgba(100,200,255,0.7)" style="animation:dewDrop_${uid} 2s ease-in-out infinite 1.4s"/>`,
    anim: `@keyframes leafSway_${uid}{0%,100%{transform:rotate(-3deg)}50%{transform:rotate(3deg)}} @keyframes dewDrop_${uid}{0%,100%{opacity:0.5}50%{opacity:1}}`,
  }),
  hiphop: (uid) => ({
    svg: `
      <ellipse cx="50" cy="14" rx="30" ry="6" fill="#111"/>
      <path d="M20,14 Q22,4 50,4 Q78,4 80,14" fill="#1a1a1a"/>
      <path d="M22,13 Q24,5 50,5 Q76,5 78,13" fill="#2a2a2a"/>
      <rect x="36" y="12" width="28" height="5" rx="2.5" fill="#111"/>
      <rect x="44" y="13" width="12" height="3" rx="1.5" fill="#FFD700"/>
      <path d="M20,14 Q14,16 16,20 Q18,22 24,20 Q26,18 26,14" fill="#111"/>`,
    anim: ``,
  }),
  classical: (uid) => ({
    svg: `
      <path d="M18,36 Q16,14 28,8 Q36,4 50,6 Q64,4 72,8 Q84,14 82,36" fill="#F5F5F5" stroke="#E0E0E0" stroke-width="1"/>
      <path d="M20,34 Q18,16 30,10 Q50,6 70,10 Q82,16 80,34" fill="white"/>
      <circle cx="22" cy="28" r="5" fill="#F5F5F5" stroke="#E0E0E0" stroke-width="0.8"/>
      <circle cx="22" cy="36" r="5" fill="#F5F5F5" stroke="#E0E0E0" stroke-width="0.8"/>
      <circle cx="78" cy="28" r="5" fill="#F5F5F5" stroke="#E0E0E0" stroke-width="0.8"/>
      <circle cx="78" cy="36" r="5" fill="#F5F5F5" stroke="#E0E0E0" stroke-width="0.8"/>
      <ellipse cx="50" cy="8" rx="16" ry="6" fill="white" stroke="#E0E0E0" stroke-width="0.8"/>`,
    anim: ``,
  }),
  default: (uid) => ({ svg:``, anim:`` }),
};

// ─── MOVIE FACE ACCESSORIES (step 3+) ────────────────────────────────────────
const MOVIE_FACE = {
  documentary: (uid) => ({
    svg: `
      <path d="M18,20 Q20,8 50,6 Q80,8 82,20" fill="#D4AC0D"/>
      <path d="M20,20 Q22,10 50,8 Q78,10 80,20" fill="#F4D03F"/>
      <ellipse cx="50" cy="20" rx="34" ry="6" fill="#B7950B"/>
      <ellipse cx="50" cy="20" rx="30" ry="4" fill="#D4AC0D"/>
      <path d="M22,22 Q24,44 50,46 Q76,44 78,22" fill="none" stroke="#A0890A" stroke-width="2"/>
      <circle cx="62" cy="33" r="10" fill="none" stroke="#B7950B" stroke-width="2.5"/>
      <circle cx="62" cy="33" r="8" fill="rgba(200,240,255,0.2)"/>
      <line x1="72" y1="33" x2="76" y2="36" stroke="#B7950B" stroke-width="2"/>`,
    anim: ``,
  }),
  mystery: (uid) => ({
    svg: `
      <path d="M24,18 Q26,4 50,4 Q74,4 76,18" fill="#795548"/>
      <path d="M26,17 Q28,6 50,6 Q72,6 74,17" fill="#8D6E63"/>
      <path d="M22,18 Q18,22 22,24 Q30,26 38,20" fill="#6D4C41"/>
      <path d="M78,18 Q82,22 78,24 Q70,26 62,20" fill="#6D4C41"/>
      <rect x="24" y="16" width="52" height="4" rx="2" fill="#4E342E"/>
      <circle cx="63" cy="34" r="11" fill="none" stroke="#5D4037" stroke-width="3"/>
      <circle cx="63" cy="34" r="9" fill="rgba(200,240,200,0.2)"/>
      <path d="M57,28 Q60,26 64,28" fill="none" stroke="rgba(255,255,255,0.6)" stroke-width="1.5" stroke-linecap="round"/>
      <line x1="72" y1="43" x2="80" y2="52" stroke="#5D4037" stroke-width="4" stroke-linecap="round"/>
      <line x1="73" y1="44" x2="80" y2="51" stroke="#8D6E63" stroke-width="2" stroke-linecap="round"/>`,
    anim: ``,
  }),
  fantasy: (uid) => ({
    svg: `
      <path d="M50,0 Q44,20 32,28 Q22,34 26,40 Q74,40 74,40 Q78,34 68,28 Q56,20 50,0Z" fill="#4A148C"/>
      <path d="M50,2 Q44,22 33,29 Q24,34 27,39 Q73,39 73,39 Q76,34 67,29 Q56,22 50,2Z" fill="#6A1B9A"/>
      <ellipse cx="50" cy="40" rx="28" ry="7" fill="#4A148C"/>
      <ellipse cx="50" cy="40" rx="26" ry="5" fill="#7B1FA2"/>
      <text x="46" y="18" font-size="8" fill="#FFD700" style="animation:wizStar_${uid} 1.2s ease-in-out infinite">★</text>
      <text x="36" y="32" font-size="6" fill="#E040FB" style="animation:wizStar_${uid} 1.2s ease-in-out infinite 0.4s">✦</text>
      <text x="57" y="28" font-size="7" fill="#40C4FF" style="animation:wizStar_${uid} 1.2s ease-in-out infinite 0.8s">★</text>`,
    anim: `@keyframes wizStar_${uid}{0%,100%{opacity:0.4;transform:scale(0.8)}50%{opacity:1;transform:scale(1.2)}}`,
  }),
  scifi: (uid) => ({
    svg: `
      <rect x="18" y="24" width="64" height="16" rx="8" fill="rgba(0,0,0,0.85)"/>
      <rect x="19" y="25" width="62" height="14" rx="7" fill="#0D1B2A"/>
      <rect x="22" y="27" width="56" height="1.5" rx="0.5" fill="#00E5FF" opacity="0.7" style="animation:hudScan_${uid} 1.5s linear infinite"/>
      <rect x="22" y="31" width="56" height="1.5" rx="0.5" fill="#00E5FF" opacity="0.4"/>
      <rect x="22" y="35" width="56" height="1.5" rx="0.5" fill="#00E5FF" opacity="0.4"/>
      <circle cx="38" cy="32" r="6" fill="none" stroke="#00E5FF" stroke-width="1" opacity="0.8"/>
      <line x1="32" y1="32" x2="44" y2="32" stroke="#00E5FF" stroke-width="0.8" opacity="0.6"/>
      <line x1="38" y1="26" x2="38" y2="38" stroke="#00E5FF" stroke-width="0.8" opacity="0.6"/>
      <circle cx="62" cy="32" r="6" fill="none" stroke="#76FF03" stroke-width="1" opacity="0.8"/>
      <line x1="56" y1="32" x2="68" y2="32" stroke="#76FF03" stroke-width="0.8" opacity="0.6"/>
      <line x1="62" y1="26" x2="62" y2="38" stroke="#76FF03" stroke-width="0.8" opacity="0.6"/>`,
    anim: `@keyframes hudScan_${uid}{0%{transform:translateY(0);opacity:0.7}50%{transform:translateY(8px);opacity:0.3}100%{transform:translateY(0);opacity:0.7}}`,
  }),
  anime: (uid) => ({
    svg: `
      <ellipse cx="38" cy="33" rx="10" ry="11" fill="white"/>
      <ellipse cx="62" cy="33" rx="10" ry="11" fill="white"/>
      <ellipse cx="38" cy="34" rx="7" ry="8" fill="#E91E63"/>
      <ellipse cx="62" cy="34" rx="7" ry="8" fill="#7B1FA2"/>
      <circle cx="38" cy="35" r="4" fill="#1a1a2e"/>
      <circle cx="62" cy="35" r="4" fill="#1a1a2e"/>
      <ellipse cx="35" cy="29" rx="3" ry="4" fill="white"/>
      <circle cx="42" cy="37" r="1.5" fill="white"/>
      <ellipse cx="59" cy="29" rx="3" ry="4" fill="white"/>
      <circle cx="66" cy="37" r="1.5" fill="white"/>
      <path d="M74,18 Q78,12 76,22 Q74,26 72,22 Q70,16 74,18Z" fill="#64B5F6" style="animation:sweatDrop_${uid} 1.5s ease-in-out infinite"/>`,
    anim: `@keyframes sweatDrop_${uid}{0%,100%{transform:translateY(0)}50%{transform:translateY(4px)}}`,
  }),
  comedy: (uid) => ({
    svg: `
      <path d="M50,0 Q44,16 36,22 Q64,22 56,16 Q50,0 50,0Z" fill="#FF5722"/>
      <path d="M50,1 Q45,16 37,21 Q63,21 55,16 Q50,1 50,1Z" fill="#FF7043"/>
      <ellipse cx="50" cy="22" rx="14" ry="4" fill="#E64A19"/>
      <circle cx="46" cy="10" r="2" fill="#FFD700"/>
      <circle cx="54" cy="14" r="1.5" fill="#4FC3F7"/>
      <circle cx="49" cy="17" r="1.5" fill="white"/>
      <path d="M36,22 Q28,28 26,34" fill="none" stroke="#FF5722" stroke-width="1.5"/>
      <circle cx="50" cy="46" r="7" fill="#FF1744" style="animation:noseHonk_${uid} 0.8s ease-in-out infinite"/>
      <circle cx="48" cy="44" r="2" fill="rgba(255,255,255,0.4)"/>`,
    anim: `@keyframes noseHonk_${uid}{0%,100%{transform:scale(1)}50%{transform:scale(1.15)}}`,
  }),
  drama: (uid) => ({
    svg: `
      <path d="M22,20 Q22,50 50,52 Q78,50 78,20 Q78,12 50,12 Q22,12 22,20Z" fill="rgba(255,248,220,0.85)" stroke="#DAA520" stroke-width="1.5"/>
      <path d="M38,36 Q44,30 50,36" fill="none" stroke="#333" stroke-width="2" stroke-linecap="round"/>
      <path d="M60,36 Q66,30 72,36" fill="none" stroke="#333" stroke-width="2" stroke-linecap="round"/>
      <path d="M30,24 Q38,20 44,24" fill="none" stroke="#333" stroke-width="2" stroke-linecap="round"/>
      <path d="M56,24 Q62,20 70,24" fill="none" stroke="#333" stroke-width="2" stroke-linecap="round"/>
      <path d="M36,38 Q34,44 36,46 Q38,44 36,38Z" fill="#64B5F6"/>`,
    anim: ``,
  }),
  action: (uid) => ({
    svg: `
      <rect x="20" y="14" width="60" height="12" rx="6" fill="#C62828"/>
      <rect x="20" y="14" width="60" height="6" rx="3" fill="#E53935"/>
      <path d="M78,16 Q88,12 86,22 Q84,28 80,24" fill="#C62828"/>
      <path d="M79,17 Q87,14 85,22 Q83,27 80,23" fill="#EF9A9A"/>
      <circle cx="32" cy="20" r="1.5" fill="rgba(255,255,255,0.3)"/>
      <circle cx="42" cy="20" r="1.5" fill="rgba(255,255,255,0.3)"/>
      <circle cx="52" cy="20" r="1.5" fill="rgba(255,255,255,0.3)"/>
      <circle cx="62" cy="20" r="1.5" fill="rgba(255,255,255,0.3)"/>
      <line x1="32" y1="26" x2="42" y2="40" stroke="#B71C1C" stroke-width="2" stroke-linecap="round" opacity="0.7"/>`,
    anim: ``,
  }),
  default: (uid) => ({ svg:``, anim:`` }),
};

function Avatar({ colorId, tagline, step=1, hobbies=[], musicIds=[], movieIds=[], styleId=null, size=100 }) {
  const c = bc(colorId);
  const [g1,g2] = c.grad;
  const uid = "av" + Math.random().toString(36).slice(2,8);
  const hasCrown   = step>=2;
  const hasHobby   = step>=2 && hobbies.length>0;
  const hasMusic   = step>=2 && musicIds.length>0;
  const hasMovie   = step>=3 && movieIds.length>0;
  const hasAura    = step>=3 && styleId!==null;
  const hasSparkle = step>=3;

  const firstMusicId = musicIds[0];
  const firstMovieId = movieIds[0];
  const firstMusic   = MUSIC_GENRES.find(m=>m.id===firstMusicId);
  const firstMovie   = MOVIE_GENRES.find(m=>m.id===firstMovieId);
  const auraClr = ({minimal:"#E3F2FD",cozy:"#FFF9C4",techy:"#E8EAF6",nature:"#E8F5E9",artistic:"#FCE4EC",retro:"#FFF3E0"})[styleId]||"#F3E5F5";

  const hobbyId1 = hobbies[0] || "default";
  const hobbyId2 = hobbies[1];
  const arms1 = HOBBY_ARMS[hobbyId1] || HOBBY_ARMS.default;
  const arms2 = hobbyId2 ? (HOBBY_ARMS[hobbyId2] || HOBBY_ARMS.default) : null;
  const rightArm = arms1(g2, uid).right;
  const leftArm  = arms2 ? arms2(g2, uid).left : arms1(g2, uid).left;

  const musicHat  = hasMusic ? (MUSIC_HATS[firstMusicId]  || MUSIC_HATS.default)(uid)  : { svg:"", anim:"" };
  const movieFace = hasMovie ? (MOVIE_FACE[firstMovieId]  || MOVIE_FACE.default)(uid)  : { svg:"", anim:"" };

  const animations = [
    arms1(g2,uid).anim||"",
    arms2 ? (arms2(g2,uid).anim||"") : "",
    musicHat.anim||"",
    movieFace.anim||"",
  ].join("");

  const hideNormalEyes = firstMovieId === "anime" && hasMovie;

  const svgInner = `
    ${hasAura ? `<ellipse cx="50" cy="115" rx="46" ry="18" fill="${auraClr}" opacity="0.5"/><ellipse cx="50" cy="115" rx="38" ry="12" fill="${auraClr}" opacity="0.3"/>` : ""}
    <ellipse cx="50" cy="149" rx="22" ry="5" fill="rgba(0,0,0,0.12)"/>
    <line x1="38" y1="17" x2="29" y2="10" stroke="${g2}" stroke-width="3" stroke-linecap="round"/>
    <circle cx="29" cy="9" r="4" fill="${g1}" stroke="white" stroke-width="1.5"/>
    <circle cx="29" cy="9" r="1.5" fill="white"/>
    <line x1="62" y1="17" x2="71" y2="10" stroke="${g2}" stroke-width="3" stroke-linecap="round"/>
    <circle cx="71" cy="9" r="4" fill="${g1}" stroke="white" stroke-width="1.5"/>
    <circle cx="71" cy="9" r="1.5" fill="white"/>
    <rect x="22" y="14" width="56" height="44" rx="22" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.08)" stroke-width="1"/>
    <rect x="26" y="16" width="48" height="18" rx="14" fill="url(#sh${uid})"/>
    <ellipse cx="28" cy="44" rx="6" ry="4" fill="rgba(255,255,255,0.22)"/>
    <ellipse cx="72" cy="44" rx="6" ry="4" fill="rgba(255,255,255,0.22)"/>
    ${!hideNormalEyes ? `
      <ellipse cx="38" cy="33" rx="8" ry="9" fill="white" stroke="rgba(0,0,0,0.06)" stroke-width="0.5"/>
      <ellipse cx="62" cy="33" rx="8" ry="9" fill="white" stroke="rgba(0,0,0,0.06)" stroke-width="0.5"/>
      <circle cx="39" cy="34" r="5" fill="${g2}"/><circle cx="63" cy="34" r="5" fill="${g2}"/>
      <circle cx="40" cy="32" r="2" fill="white"/><circle cx="64" cy="32" r="2" fill="white"/>
      <circle cx="42" cy="34" r="1" fill="rgba(255,255,255,0.7)"/><circle cx="66" cy="34" r="1" fill="rgba(255,255,255,0.7)"/>
    ` : ""}
    <path d="M40,50 Q50,56 60,50" fill="none" stroke="rgba(0,0,0,0.18)" stroke-width="2.5" stroke-linecap="round"/>
    <rect x="42" y="58" width="16" height="8" rx="4" fill="url(#bg${uid})"/>
    <rect x="16" y="64" width="68" height="48" rx="20" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.08)" stroke-width="1"/>
    <rect x="20" y="66" width="60" height="20" rx="14" fill="url(#sh${uid})"/>
    <circle cx="36" cy="78" r="2.5" fill="rgba(255,255,255,0.3)"/>
    <circle cx="50" cy="75" r="2.5" fill="rgba(255,255,255,0.3)"/>
    <circle cx="64" cy="78" r="2.5" fill="rgba(255,255,255,0.3)"/>
    ${hasMovie
      ? `<rect x="32" y="78" width="36" height="24" rx="8" fill="${g2}"/>
         <rect x="33" y="79" width="34" height="10" rx="6" fill="rgba(255,255,255,0.15)"/>
         <text x="50" y="93" text-anchor="middle" font-size="13" fill="white">${firstMovie?.icon||"🎬"}</text>`
      : `<rect x="36" y="82" width="28" height="16" rx="6" fill="rgba(0,0,0,0.1)"/>`}
    ${hasHobby ? rightArm : `<rect x="82" y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/><rect x="83" y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>`}
    ${hasHobby ? leftArm  : `<rect x="2"  y="66" width="16" height="38" rx="8" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/><rect x="3"  y="67" width="14" height="14" rx="7" fill="url(#sh${uid})"/>`}
    <rect x="28" y="110" width="18" height="30" rx="9" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
    <rect x="54" y="110" width="18" height="30" rx="9" fill="url(#bg${uid})" stroke="rgba(0,0,0,0.06)" stroke-width="1"/>
    <ellipse cx="37" cy="142" rx="13" ry="6" fill="${g2}"/><ellipse cx="63" cy="142" rx="13" ry="6" fill="${g2}"/>
    <ellipse cx="37" cy="141" rx="10" ry="3" fill="rgba(255,255,255,0.18)"/><ellipse cx="63" cy="141" rx="10" ry="3" fill="rgba(255,255,255,0.18)"/>
    ${hasSparkle ? `<text x="6" y="72" font-size="10">✦</text><text x="86" y="70" font-size="8">✦</text><text x="4" y="98" font-size="7">✦</text><text x="88" y="96" font-size="10">✦</text>` : ""}
    ${hasMusic ? musicHat.svg : (hasCrown ? `
      <rect x="34" y="2" width="32" height="11" rx="3" fill="#7B61FF"/>
      <rect x="30" y="10" width="40" height="4" rx="2" fill="#5B42D4"/>
      <polygon points="34,10 37,2 40,10" fill="#9B81FF"/>
      <polygon points="47,10 50,0 53,10" fill="#9B81FF"/>
      <polygon points="60,10 63,2 66,10" fill="#9B81FF"/>
      <circle cx="37" cy="6" r="2" fill="#FFD700"/>
      <circle cx="50" cy="4" r="2.5" fill="${g1}"/>
      <circle cx="63" cy="6" r="2" fill="#4FC3F7"/>
    ` : "")}
    ${hasMovie ? movieFace.svg : ""}
  `;

  return (
    <div style={{display:"flex",flexDirection:"column",alignItems:"center",gap:8}}>
      {animations && <style>{animations}</style>}
      <svg width={size} height={size*1.55} viewBox="0 0 100 155" style={{overflow:"visible"}}>
        <defs>
          <linearGradient id={`bg${uid}`} x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stopColor={g1}/><stop offset="100%" stopColor={g2}/>
          </linearGradient>
          <linearGradient id={`sh${uid}`} x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stopColor="rgba(255,255,255,0.55)"/><stop offset="100%" stopColor="rgba(255,255,255,0)"/>
          </linearGradient>
        </defs>
        <g dangerouslySetInnerHTML={{__html: svgInner}}/>
      </svg>
      {tagline && (
        <div style={{background:"rgba(0,0,0,0.78)",color:"white",fontSize:11,fontWeight:900,
          padding:"5px 14px",borderRadius:99,letterSpacing:1,textTransform:"uppercase",
          textAlign:"center",maxWidth:180}}>
          {tagline}
        </div>
      )}
    </div>
  );
}

// ─── SHARED UI ────────────────────────────────────────────────────────────────

function Glass({children, style={}}) {
  return (
    <div style={{background:"rgba(255,255,255,0.9)",backdropFilter:"blur(16px)",borderRadius:24,border:"1px solid rgba(255,255,255,0.5)",boxShadow:"0 4px 24px rgba(0,0,0,0.08)",...style}}>
      {children}
    </div>
  );
}

function Btn({onClick, disabled, children, style={}}) {
  return (
    <button onClick={onClick} disabled={disabled} style={{border:"none",cursor:disabled?"not-allowed":"pointer",fontWeight:900,fontFamily:"inherit",transition:"all 0.2s",opacity:disabled?0.45:1,...style}}>
      {children}
    </button>
  );
}

function StepBar({step}) {
  return (
    <div style={{display:"flex",alignItems:"center",gap:6,justifyContent:"center",padding:"4px 0"}}>
      {[1,2,3,4,5].map(n=>(
        <div key={n} style={{display:"flex",alignItems:"center",gap:6}}>
          <div style={{width:26,height:26,borderRadius:"50%",display:"flex",alignItems:"center",justifyContent:"center",
            fontSize:10,fontWeight:900,
            background:n<=step?"#22c55e":"rgba(0,0,0,0.1)",
            color:n<=step?"white":"rgba(0,0,0,0.35)",
            boxShadow:n===step?"0 0 0 3px rgba(34,197,94,0.3)":"none",
            transition:"all 0.3s"}}>
            {n<step?"✓":n}
          </div>
          {n<5 && <div style={{width:18,height:2,borderRadius:99,background:n<step?"#22c55e":"rgba(0,0,0,0.1)",transition:"all 0.3s"}}/>}
        </div>
      ))}
    </div>
  );
}

function MultiSelect({items, selected, onToggle, max, accent}) {
  return (
    <div style={{display:"grid",gridTemplateColumns:"repeat(2,1fr)",gap:7}}>
      {items.map(item=>{
        const sel=selected.includes(item.id), full=!sel&&selected.length>=max;
        return (
          <button key={item.id} onClick={()=>!full&&onToggle(item.id)}
            style={{padding:"10px 8px",borderRadius:16,border:`2px solid ${sel?accent:"#e7e5e4"}`,background:sel?`${accent}15`:"rgba(255,255,255,0.7)",cursor:full?"not-allowed":"pointer",display:"flex",alignItems:"center",gap:8,opacity:full?0.45:1,transform:sel?"scale(1.03)":"scale(1)",transition:"all 0.15s",fontFamily:"inherit"}}>
            <span style={{fontSize:20,flexShrink:0}}>{item.icon}</span>
            <span style={{fontSize:11,fontWeight:900,color:sel?accent:"#57534e",textAlign:"left",lineHeight:1.2}}>{item.label}</span>
            {sel&&<span style={{marginLeft:"auto",fontSize:10,color:accent,fontWeight:900}}>✓</span>}
          </button>
        );
      })}
    </div>
  );
}

function AvatarPersonaRow({ colorId, tagline, step=1, hobbies=[], musicIds=[], movieIds=[], styleId=null, size=80, label, description, traits, dark="#2E7D32" }) {
  return (
    <Glass style={{width:"100%",padding:14,display:"flex",alignItems:"flex-start",gap:14}}>
      <div style={{flexShrink:0,display:"flex",flexDirection:"column",alignItems:"center"}}>
        <Avatar colorId={colorId} tagline={null} step={step} hobbies={hobbies} musicIds={musicIds} movieIds={movieIds} styleId={styleId} size={size}/>
        {tagline&&<div style={{marginTop:5,background:"rgba(0,0,0,0.76)",color:"white",fontSize:9,fontWeight:900,padding:"3px 10px",borderRadius:99,letterSpacing:1,textTransform:"uppercase",textAlign:"center",maxWidth:110,lineHeight:1.3}}>{tagline}</div>}
      </div>
      <div style={{flex:1,minWidth:0,paddingTop:6}}>
        {label&&<div style={{fontSize:10,fontWeight:900,color:dark,textTransform:"uppercase",letterSpacing:2,marginBottom:7}}>{label}</div>}
        {description&&<p style={{fontSize:12,color:"#374151",fontWeight:600,lineHeight:1.6,margin:"0 0 10px"}}>{description}</p>}
        {traits&&traits.length>0&&<div style={{display:"flex",flexWrap:"wrap",gap:4}}>{traits.map((t,i)=><span key={i} style={{fontSize:10,fontWeight:700,padding:"3px 8px",borderRadius:99,background:`${dark}18`,color:dark,border:`1px solid ${dark}33`}}>{t}</span>)}</div>}
      </div>
    </Glass>
  );
}

function TrackCard({track, idx}) {
  const genre=MUSIC_GENRES.find(m=>m.id===track.genreId);
  const [bg1,bg2]=TRACK_COLORS[idx%TRACK_COLORS.length];
  const url=`https://open.spotify.com/search/${encodeURIComponent(track.title+" "+track.artist)}`;
  return (
    <a href={url} target="_blank" rel="noopener noreferrer" style={{textDecoration:"none",display:"flex",alignItems:"center",gap:10,padding:"8px 10px",borderRadius:14,background:"rgba(245,243,255,0.7)",border:"1px solid #ede9fe",cursor:"pointer"}}>
      <div style={{width:50,height:50,borderRadius:10,flexShrink:0,position:"relative",overflow:"hidden",background:`linear-gradient(135deg,${bg1},${bg2})`}}>
        <div style={{position:"absolute",inset:0,display:"flex",flexDirection:"column",alignItems:"center",justifyContent:"center",gap:1}}>
          <span style={{fontSize:16}}>{genre?.icon||"🎵"}</span>
          <div style={{fontSize:7,fontWeight:900,color:"rgba(255,255,255,0.85)",textAlign:"center",padding:"0 4px",lineHeight:1.2}}>{track.title.slice(0,12)}</div>
        </div>
      </div>
      <div style={{flex:1,minWidth:0}}>
        <div style={{fontSize:12,fontWeight:900,color:"#1c1917",overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap"}}>{track.title}</div>
        <div style={{fontSize:10,color:"#a8a29e",fontWeight:600,marginBottom:5}}>{track.artist}</div>
        <div style={{display:"inline-flex",alignItems:"center",gap:4,background:"#1DB954",borderRadius:8,padding:"2px 7px"}}>
          <svg width="9" height="9" viewBox="0 0 24 24" fill="white"><path d="M12 0C5.4 0 0 5.4 0 12s5.4 12 12 12 12-5.4 12-12S18.66 0 12 0zm5.521 17.34c-.24.359-.66.48-1.021.24-2.82-1.74-6.36-2.101-10.561-1.141-.418.122-.779-.179-.899-.539-.12-.421.18-.78.54-.9 4.56-1.021 8.52-.6 11.64 1.32.42.18.479.659.301 1.02zm1.44-3.3c-.301.42-.841.6-1.262.3-3.239-1.98-8.159-2.58-11.939-1.38-.479.12-1.02-.12-1.14-.6-.12-.48.12-1.021.6-1.141C9.6 9.9 15 10.561 18.72 12.84c.361.181.54.78.241 1.2zm.12-3.36C15.24 8.4 8.82 8.16 5.16 9.301c-.6.179-1.2-.181-1.38-.721-.18-.601.18-1.2.72-1.381 4.26-1.26 11.28-1.02 15.721 1.621.539.3.719 1.02.419 1.56-.299.421-1.02.599-1.559.3z"/></svg>
          <span style={{fontSize:9,fontWeight:900,color:"white"}}>Spotify</span>
        </div>
      </div>
      <span style={{fontSize:18,flexShrink:0}}>{genre?.icon}</span>
    </a>
  );
}

function FilmCard({film, idx}) {
  const p=STREAMING[film.platform]||STREAMING.netflix;
  const url=p.url+encodeURIComponent(film.title);
  const [bg1]=TRACK_COLORS[(idx+4)%TRACK_COLORS.length];
  return (
    <a href={url} target="_blank" rel="noopener noreferrer" style={{textDecoration:"none",display:"flex",alignItems:"center",gap:10,padding:"9px 10px",borderRadius:14,background:"rgba(255,241,242,0.7)",border:"1px solid #fecdd3",cursor:"pointer"}}>
      <div style={{width:50,height:50,borderRadius:10,flexShrink:0,overflow:"hidden",background:`linear-gradient(135deg,${bg1},${p.color}99)`}}>
        <div style={{width:"100%",height:"100%",display:"flex",flexDirection:"column",alignItems:"center",justifyContent:"center",gap:1}}>
          <span style={{fontSize:20}}>{film.icon}</span>
          <div style={{fontSize:6,fontWeight:900,color:"rgba(255,255,255,0.85)",textAlign:"center",padding:"0 3px",lineHeight:1.2}}>{film.title.slice(0,14)}</div>
        </div>
      </div>
      <div style={{flex:1,minWidth:0}}>
        <div style={{fontSize:12,fontWeight:900,color:"#1c1917",overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap",marginBottom:2}}>{film.title}</div>
        <div style={{fontSize:10,color:"#a8a29e",fontWeight:600,marginBottom:5,overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap"}}>{film.reason}</div>
        <div style={{display:"inline-flex",alignItems:"center",gap:4,background:p.color,borderRadius:8,padding:"2px 8px"}}>
          <span style={{fontSize:9,fontWeight:900,color:"white"}}>▶ {p.name}</span>
        </div>
      </div>
    </a>
  );
}

// ─── STEP 1: UPLOAD + AI ─────────────────────────────────────────────────────

function Step1() {
  const {state, update} = useGame();
  const [analyzing, setAnalyzing] = useState(false);
  const [dots, setDots] = useState(".");
  const [statusIdx, setStatusIdx] = useState(0);
  const statuses = ["Scanning desk surface...","Reading objects & colours...","Building your persona...","Almost there..."];

  const handleFile = (file) => {
    if (!file) return;
    const reader = new FileReader();
    reader.onload = async (e) => {
      const url = e.target.result;
      update({photoUrl: url});
      setAnalyzing(true);
      // animate status messages
      let si=0;
      const sint = setInterval(()=>{ si=(si+1)%statuses.length; setStatusIdx(si); }, 1200);
      const dint = setInterval(()=>setDots(d=>d.length>=3?".":".."), 500);
      try {
        const persona = await analyzeDesk(url);
        clearInterval(sint); clearInterval(dint);
        update({persona, step:2});  // go directly to step 2 reveal after analysis
        // But first show the result — we need a reveal moment so stay on step 1 with result shown
        update({persona, analyzing:false});
      } catch(err) {
        clearInterval(sint); clearInterval(dint);
        update({
          persona:{ archetype:"creative", tagline:"Mystery Desk Dweller", colorId:"sky",
            description:"Your desk radiates a creative energy — we couldn't auto-analyse the photo but the vibe is unmistakably yours. Every object here tells a story worth discovering.",
            deskTraits:["creative energy","hidden depths","desk with stories"],
            apiError:true, apiErrorMsg:err.message},
          analyzing:false
        });
      }
      setAnalyzing(false);
    };
    reader.readAsDataURL(file);
  };

  const persona = state.persona;
  const color   = persona ? bc(persona.colorId) : null;

  // If we have a persona result, show it
  if (persona && !analyzing) {
    return (
      <div style={{minHeight:"100%",background:"linear-gradient(135deg,#0d1f0e,#0e1a2e,#1a0d28)",
        position:"relative",overflow:"hidden"}}>
        {state.photoUrl && <img src={state.photoUrl} alt="" style={{position:"absolute",inset:0,
          width:"100%",height:"100%",objectFit:"cover",opacity:0.1,filter:"blur(12px)"}}/>}
        <div style={{position:"relative",zIndex:10,display:"flex",flexDirection:"column",
          alignItems:"center",padding:"24px 16px",gap:18,maxWidth:420,margin:"0 auto"}}>
          <StepBar step={1}/>
          <div style={{fontSize:11,fontWeight:900,color:"#4ade80",textTransform:"uppercase",letterSpacing:3}}>✦ Step 1 Complete ✦</div>

          {persona.apiError && (
            <div style={{width:"100%",background:"rgba(251,191,36,0.15)",border:"1px solid rgba(251,191,36,0.4)",
              borderRadius:14,padding:"10px 14px",fontSize:11,color:"#FCD34D",fontWeight:700}}>
              ⚠️ Auto-analysis unavailable — placeholder persona assigned.
              {persona.apiErrorMsg && <div style={{fontSize:9,marginTop:3,opacity:0.7,fontFamily:"monospace"}}>{persona.apiErrorMsg}</div>}
            </div>
          )}

          <AvatarPersonaRow
            colorId={persona.colorId} tagline={persona.tagline} step={1} size={85}
            label="🤖 Your Desk Persona" description={persona.description}
            traits={persona.deskTraits||[]} dark={color?.dark}
          />

          {state.photoUrl && (
            <div style={{width:"100%",borderRadius:16,overflow:"hidden",border:"3px solid rgba(255,255,255,0.15)"}}>
              <img src={state.photoUrl} alt="desk" style={{width:"100%",aspectRatio:"16/7",objectFit:"cover",display:"block"}}/>
              <div style={{background:"rgba(0,0,0,0.7)",padding:"8px 14px",fontSize:11,color:"rgba(255,255,255,0.7)",fontWeight:600}}>
                📍 Your desk — analysed
              </div>
            </div>
          )}

          <Btn onClick={()=>update({step:2})} style={{width:"100%",
            background:`linear-gradient(135deg,${color?.grad[0]},${color?.grad[1]})`,
            color:"white",padding:"16px 0",borderRadius:18,fontSize:13,
            textTransform:"uppercase",letterSpacing:2,boxShadow:`0 4px 20px ${color?.hex}55`}}>
            Continue to Step 2 →
          </Btn>
        </div>
      </div>
    );
  }

  // Upload or analyzing state
  return (
    <div style={{minHeight:"100%",display:"flex",flexDirection:"column",alignItems:"center",
      justifyContent:"center",background: analyzing
        ? "linear-gradient(135deg,#060e08,#060d18)"
        : "linear-gradient(135deg,#ecfdf5,#e0f2fe)",
      padding:24,gap:24,position:"relative",overflow:"hidden"}}>

      {/* Scanning animation overlay */}
      {analyzing && state.photoUrl && <>
        <img src={state.photoUrl} alt="" style={{position:"absolute",inset:0,width:"100%",height:"100%",
          objectFit:"cover",opacity:0.35,filter:"saturate(0.3) brightness(0.5)"}}/>
        <div style={{position:"absolute",inset:0,background:"rgba(0,0,0,0.5)"}}/>
        <div style={{position:"absolute",left:0,right:0,top:"40%",height:3,
          background:"linear-gradient(90deg,transparent,#4ade80,#22d3ee,#4ade80,transparent)",
          boxShadow:"0 0 18px #4ade80",animation:"scanLine 2s linear infinite",zIndex:10}}/>
        {[[8,8],[8,80],[88,8],[88,80]].map(([x,y],i)=>(
          <div key={i} style={{position:"absolute",left:`${x}%`,top:`${y}%`,width:20,height:20,
            borderTop:y<50?"2px solid #4ade80":undefined,borderBottom:y>50?"2px solid #4ade80":undefined,
            borderLeft:x<50?"2px solid #4ade80":undefined,borderRight:x>50?"2px solid #4ade80":undefined,zIndex:11}}/>
        ))}
      </>}

      <div style={{position:"relative",zIndex:20,display:"flex",flexDirection:"column",
        alignItems:"center",gap:20,width:"100%",maxWidth:400}}>
        <StepBar step={1}/>

        {analyzing ? (
          <>
            <div style={{fontSize:48,animation:"pulse 1.5s ease-in-out infinite"}}>🤖</div>
            <div style={{textAlign:"center"}}>
              <div style={{fontSize:16,fontWeight:900,color:"white",letterSpacing:2,textTransform:"uppercase",marginBottom:6}}>
                AI Scanning{dots}
              </div>
              <div style={{fontSize:13,color:"rgba(255,255,255,0.6)",fontWeight:600}}>{statuses[statusIdx]}</div>
            </div>
            <Glass style={{width:"100%",padding:16,background:"rgba(0,0,0,0.6)",border:"1px solid rgba(74,222,128,0.3)"}}>
              {["Desk objects","Colour palette","Chaos level","Personality type","Robot colour"].map((label,i)=>(
                <div key={i} style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:8,fontSize:12}}>
                  <span style={{color:"rgba(255,255,255,0.7)",fontWeight:600}}>{label}</span>
                  <span style={{color:"#4ade80",fontWeight:900,fontSize:11}}>SCANNING...</span>
                </div>
              ))}
            </Glass>
          </>
        ) : (
          <>
            <div style={{textAlign:"center",maxWidth:340}}>
              <div style={{fontSize:60,marginBottom:12,animation:"bounce 1.2s infinite",display:"inline-block"}}>🖥️</div>
              <h1 style={{fontSize:26,fontWeight:900,color:"#14532d",margin:"0 0 8px",letterSpacing:-0.5}}>Catch My Desk Vibe!</h1>
              <p style={{color:"#16a34a",fontWeight:600,fontSize:13,margin:0}}>Upload your desk photo — AI reveals your persona in 4 steps.</p>
            </div>
            <Glass style={{width:"100%",padding:18}}>
              {[["📸","Step 1: AI analyses your desk → persona + avatar"],["🎮","Step 2: Hobbies & music → playlist + evolved avatar"],["🎬","Step 3: Films & style → watchlist + full avatar"],["🎁","Step 4: Final card + desk reward"]].map(([ic,tx])=>(
                <div key={ic} style={{display:"flex",gap:12,alignItems:"flex-start",marginBottom:10}}>
                  <span style={{fontSize:18}}>{ic}</span>
                  <span style={{fontSize:12,color:"#44403c",fontWeight:600}}>{tx}</span>
                </div>
              ))}
            </Glass>
            <div style={{width:"100%",aspectRatio:"16/8",borderRadius:20,
              border:"3px dashed #86efac",overflow:"hidden",position:"relative",background:"rgba(255,255,255,0.6)"}}>
              <label style={{width:"100%",height:"100%",display:"flex",flexDirection:"column",
                alignItems:"center",justifyContent:"center",cursor:"pointer",gap:10}}>
                <span style={{fontSize:44}}>📸</span>
                <span style={{fontSize:11,fontWeight:900,color:"#16a34a",textTransform:"uppercase",letterSpacing:2}}>Upload Desk Photo</span>
                <span style={{fontSize:11,color:"#a8a29e",fontWeight:600}}>AI analyses it automatically</span>
                <input type="file" accept="image/*" style={{display:"none"}} onChange={e=>handleFile(e.target.files?.[0])}/>
              </label>
            </div>
          </>
        )}
      </div>
    </div>
  );
}

// ─── STEP 2: HOBBY + MUSIC ────────────────────────────────────────────────────

function Step2() {
  const {state, update} = useGame();
  const persona  = state.persona;
  const color    = bc(persona?.colorId);
  const [loading, setLoading] = useState(false);
  const [evolved, setEvolved] = useState(state.step2Update || null);

  const canContinue = state.selectedHobbies.length > 0 && state.selectedMusic.length > 0;

  const handleSubmit = async () => {
    if (!canContinue) return;
    setLoading(true);
    try {
      const upd = await updatePersonaStep2(persona, state.selectedHobbies, state.selectedMusic);
      setEvolved(upd);
      update({step2Update: upd}); // persist to global state for Step3 + Step4
    } catch(e) {
      const fallback = { tagline: persona.tagline, description: persona.description, deskTraits: persona.deskTraits };
      setEvolved(fallback);
      update({step2Update: fallback});
    }
    setLoading(false);
  };

  const playlist = buildPlaylist(state.selectedMusic);
  const currentTagline = evolved?.tagline || persona?.tagline;
  const currentDesc    = evolved?.description || persona?.description;
  const currentTraits  = evolved?.deskTraits || persona?.deskTraits || [];

  return (
    <div style={{minHeight:"100%",background:"linear-gradient(135deg,#ecfdf5,#e0f2fe,#f5f3ff)",position:"relative",overflow:"hidden"}}>
      {state.photoUrl && <img src={state.photoUrl} alt="" style={{position:"absolute",inset:0,width:"100%",height:"100%",objectFit:"cover",opacity:0.08,filter:"blur(16px)"}}/>}
      <div style={{position:"relative",zIndex:10,display:"flex",flexDirection:"column",
        alignItems:"center",padding:"20px 14px",gap:14,maxWidth:440,margin:"0 auto"}}>

        <StepBar step={2}/>

        {/* Avatar row — shows description beside avatar only after evolve */}
        {evolved ? (
          <AvatarPersonaRow
            colorId={persona?.colorId} tagline={currentTagline}
            step={2} hobbies={state.selectedHobbies} musicIds={state.selectedMusic} size={80}
            label="🤖 Persona Update" description={currentDesc}
            traits={currentTraits} dark={color.dark}
          />
        ) : (
          <Avatar colorId={persona?.colorId} tagline={currentTagline}
            step={1} hobbies={[]} musicIds={[]} size={90}/>
        )}

        {/* Before submit: show forms. After submit: hide forms, show compact summary + results */}
        {!evolved ? (
          <>
            {/* Hobby selection */}
            <Glass style={{width:"100%",padding:16}}>
              <div style={{fontSize:11,fontWeight:900,color:"#166534",textTransform:"uppercase",letterSpacing:1,marginBottom:10}}>
                🎯 Your Hobbies <span style={{color:"#a8a29e",fontWeight:600,fontSize:10}}>(select up to 2)</span>
              </div>
              <MultiSelect items={HOBBIES} selected={state.selectedHobbies} max={2} accent="#22c55e"
                onToggle={v=>update({selectedHobbies:toggleMax(state.selectedHobbies,v,2)})}/>
            </Glass>

            {/* Music selection */}
            <Glass style={{width:"100%",padding:16}}>
              <div style={{fontSize:11,fontWeight:900,color:"#6d28d9",textTransform:"uppercase",letterSpacing:1,marginBottom:10}}>
                🎵 Music Vibes <span style={{color:"#a8a29e",fontWeight:600,fontSize:10}}>(select up to 2)</span>
              </div>
              <MultiSelect items={MUSIC_GENRES} selected={state.selectedMusic} max={2} accent="#a855f7"
                onToggle={v=>update({selectedMusic:toggleMax(state.selectedMusic,v,2)})}/>
            </Glass>

            <Btn onClick={handleSubmit} disabled={!canContinue||loading} style={{width:"100%",
              background:canContinue?"linear-gradient(135deg,#22c55e,#a855f7)":"#e7e5e4",
              color:canContinue?"white":"#a8a29e",padding:"14px 0",borderRadius:18,
              fontSize:12,textTransform:"uppercase",letterSpacing:2}}>
              {loading?"Evolving your avatar...":"✨ Update My Avatar & Playlist"}
            </Btn>
          </>
        ) : (
          <>
            {/* Compact choice summary (replaces forms) */}
            <Glass style={{width:"100%",padding:"12px 16px"}}>
              <div style={{fontSize:10,fontWeight:900,color:"#a8a29e",textTransform:"uppercase",letterSpacing:1,marginBottom:8}}>Your choices</div>
              <div style={{display:"flex",flexWrap:"wrap",gap:5}}>
                {state.selectedHobbies.map(id=>{const h=HOBBIES.find(x=>x.id===id); return h&&<span key={id} style={{fontSize:11,fontWeight:700,padding:"3px 10px",borderRadius:99,background:"#f0fdf4",color:"#166534",border:"1px solid #bbf7d0"}}>{h.icon} {h.label}</span>;})}
                {state.selectedMusic.map(id=>{const m=MUSIC_GENRES.find(x=>x.id===id); return m&&<span key={id} style={{fontSize:11,fontWeight:700,padding:"3px 10px",borderRadius:99,background:"#faf5ff",color:"#7e22ce",border:"1px solid #e9d5ff"}}>{m.icon} {m.label}</span>;})}
              </div>
            </Glass>

            {/* Playlist */}
            <Glass style={{width:"100%",padding:16}}>
              <div style={{fontSize:11,fontWeight:900,color:"#6d28d9",textTransform:"uppercase",letterSpacing:2,marginBottom:12}}>🎵 Your Playlist</div>
              <div style={{display:"flex",flexDirection:"column",gap:8,maxHeight:280,overflowY:"auto"}}>
                {playlist.map((track,i)=><TrackCard key={i} track={track} idx={i} musicIds={state.selectedMusic}/>)}
              </div>
            </Glass>

            <Btn onClick={()=>update({step:3})} style={{width:"100%",
              background:`linear-gradient(135deg,${color.grad[0]},${color.grad[1]})`,
              color:"white",padding:"16px 0",borderRadius:18,fontSize:12,
              textTransform:"uppercase",letterSpacing:2,boxShadow:`0 4px 20px ${color.hex}55`}}>
              Continue to Step 3 →
            </Btn>
          </>
        )}
      </div>
    </div>
  );
}

// ─── STEP 3: FILM + STYLE ─────────────────────────────────────────────────────

function Step3() {
  const {state, update} = useGame();
  const persona  = state.persona;
  const color    = bc(persona?.colorId);
  const [loading, setLoading] = useState(false);
  const [evolved, setEvolved] = useState(state.step3Update || null);

  const canContinue = state.selectedMovies.length > 0 && state.selectedStyle !== null;

  const handleSubmit = async () => {
    if (!canContinue) return;
    setLoading(true);
    try {
      // Pass step2Update from global state so AI has full context
      const upd = await updatePersonaStep3(persona, state.step2Update, state.selectedMovies, state.selectedStyle);
      setEvolved(upd);
      update({step3Update: upd}); // persist to global state for Step4
    } catch(e) {
      const cur = state.step2Update || persona;
      const fallback = { tagline: cur.tagline, description: cur.description, deskTraits: cur.deskTraits };
      setEvolved(fallback);
      update({step3Update: fallback});
    }
    setLoading(false);
  };

  const watchlist = buildWatchlist(state.selectedMovies);
  // Chain: step3 evolved > step2 update > original persona
  const base = state.step2Update || persona;
  const currentTagline = evolved?.tagline || base?.tagline;
  const currentDesc    = evolved?.description || base?.description;
  const currentTraits  = evolved?.deskTraits || base?.deskTraits || [];

  return (
    <div style={{minHeight:"100%",background:"linear-gradient(135deg,#ecfdf5,#e0f2fe,#f5f3ff)",position:"relative",overflow:"hidden"}}>
      {state.photoUrl && <img src={state.photoUrl} alt="" style={{position:"absolute",inset:0,width:"100%",height:"100%",objectFit:"cover",opacity:0.08,filter:"blur(16px)"}}/>}
      <div style={{position:"relative",zIndex:10,display:"flex",flexDirection:"column",
        alignItems:"center",padding:"20px 14px",gap:14,maxWidth:440,margin:"0 auto"}}>

        <StepBar step={3}/>

        {/* Avatar row — shows description beside avatar only after evolve */}
        {evolved ? (
          <AvatarPersonaRow
            colorId={persona?.colorId} tagline={currentTagline}
            step={3} hobbies={state.selectedHobbies} musicIds={state.selectedMusic}
            movieIds={state.selectedMovies} styleId={state.selectedStyle} size={80}
            label="🤖 Persona Update" description={currentDesc}
            traits={currentTraits} dark={color.dark}
          />
        ) : (
          <Avatar colorId={persona?.colorId} tagline={currentTagline}
            step={2} hobbies={state.selectedHobbies} musicIds={state.selectedMusic}
            movieIds={[]} styleId={null} size={90}/>
        )}

        {/* Before submit: show forms. After submit: hide forms, show compact summary + results */}
        {!evolved ? (
          <>
            {/* Movie genre selection */}
            <Glass style={{width:"100%",padding:16}}>
              <div style={{fontSize:11,fontWeight:900,color:"#9f1239",textTransform:"uppercase",letterSpacing:1,marginBottom:10}}>
                🎬 Film & Series Genre <span style={{color:"#a8a29e",fontWeight:600,fontSize:10}}>(up to 2)</span>
              </div>
              <MultiSelect items={MOVIE_GENRES} selected={state.selectedMovies} max={2} accent="#f43f5e"
                onToggle={v=>update({selectedMovies:toggleMax(state.selectedMovies,v,2)})}/>
            </Glass>

            {/* Desk style selection */}
            <Glass style={{width:"100%",padding:16}}>
              <div style={{fontSize:11,fontWeight:900,color:"#0f766e",textTransform:"uppercase",letterSpacing:1,marginBottom:10}}>
                🎨 Desk Aesthetic Style <span style={{color:"#a8a29e",fontWeight:600,fontSize:10}}>(pick 1)</span>
              </div>
              <div style={{display:"grid",gridTemplateColumns:"repeat(2,1fr)",gap:7}}>
                {DESK_STYLES.map(s=>{
                  const sel = state.selectedStyle===s.id;
                  return (
                    <button key={s.id} onClick={()=>update({selectedStyle:s.id})}
                      style={{padding:"10px 8px",borderRadius:16,
                        border:`2px solid ${sel?"#14b8a6":"#e7e5e4"}`,
                        background:sel?"#f0fdfa":"rgba(255,255,255,0.7)",
                        cursor:"pointer",display:"flex",alignItems:"center",gap:8,
                        transform:sel?"scale(1.03)":"scale(1)",transition:"all 0.15s",fontFamily:"inherit"}}>
                      <span style={{fontSize:20}}>{s.icon}</span>
                      <span style={{fontSize:11,fontWeight:900,color:sel?"#0f766e":"#57534e"}}>{s.label}</span>
                      {sel && <span style={{marginLeft:"auto",fontSize:10,color:"#14b8a6",fontWeight:900}}>✓</span>}
                    </button>
                  );
                })}
              </div>
            </Glass>

            <Btn onClick={handleSubmit} disabled={!canContinue||loading} style={{width:"100%",
              background:canContinue?"linear-gradient(135deg,#f43f5e,#14b8a6)":"#e7e5e4",
              color:canContinue?"white":"#a8a29e",padding:"14px 0",borderRadius:18,
              fontSize:12,textTransform:"uppercase",letterSpacing:2}}>
              {loading?"Evolving your avatar...":"✨ Update My Avatar & Watchlist"}
            </Btn>
          </>
        ) : (
          <>
            {/* Compact choice summary (replaces forms) */}
            <Glass style={{width:"100%",padding:"12px 16px"}}>
              <div style={{fontSize:10,fontWeight:900,color:"#a8a29e",textTransform:"uppercase",letterSpacing:1,marginBottom:8}}>Your choices</div>
              <div style={{display:"flex",flexWrap:"wrap",gap:5}}>
                {state.selectedMovies.map(id=>{const m=MOVIE_GENRES.find(x=>x.id===id); return m&&<span key={id} style={{fontSize:11,fontWeight:700,padding:"3px 10px",borderRadius:99,background:"#fff1f2",color:"#be123c",border:"1px solid #fecdd3"}}>{m.icon} {m.label}</span>;})}
                {state.selectedStyle && (()=>{const s=DESK_STYLES.find(x=>x.id===state.selectedStyle); return s&&<span style={{fontSize:11,fontWeight:700,padding:"3px 10px",borderRadius:99,background:"#f0fdfa",color:"#0f766e",border:"1px solid #99f6e4"}}>{s.icon} {s.label}</span>;})()}
              </div>
            </Glass>

            <Glass style={{width:"100%",padding:16}}>
              <div style={{fontSize:11,fontWeight:900,color:"#9f1239",textTransform:"uppercase",letterSpacing:2,marginBottom:12}}>🎬 Your Watch List</div>
              <div style={{display:"flex",flexDirection:"column",gap:8}}>
                {watchlist.map((film,i)=><FilmCard key={i} film={film} idx={i}/>)}
              </div>
            </Glass>

            <Btn onClick={()=>update({step:4})} style={{width:"100%",
              background:`linear-gradient(135deg,${color.grad[0]},${color.grad[1]})`,
              color:"white",padding:"16px 0",borderRadius:18,fontSize:12,
              textTransform:"uppercase",letterSpacing:2,boxShadow:`0 4px 20px ${color.hex}55`}}>
              See Your Final Vibe Card →
            </Btn>
          </>
        )}
      </div>
    </div>
  );
}

// ─── STEP 4: FINAL CARD ───────────────────────────────────────────────────────

function Step4() {
  const {state, update, reset} = useGame();
  const persona  = state.persona;
  const color    = bc(persona?.colorId);

  // Chain all three layers: step3 > step2 > original AI persona
  const step2 = state.step2Update;
  const step3 = state.step3Update;
  const tagline = step3?.tagline || step2?.tagline || persona?.tagline;
  const desc    = step3?.description || step2?.description || persona?.description;
  const traits  = step3?.deskTraits || step2?.deskTraits || persona?.deskTraits || [];

  const playlist  = buildPlaylist(state.selectedMusic);
  const watchlist = buildWatchlist(state.selectedMovies);

  // ── Reward selection: score-based, desk-aware ─────────────────────────────
  const derivedArchetype = getRewardArchetype(state);
  const reward = REWARDS[derivedArchetype] || REWARDS.default;

  const hobbyItems  = state.selectedHobbies.map(id=>HOBBIES.find(h=>h.id===id)).filter(Boolean);
  const musicItems  = state.selectedMusic.map(id=>MUSIC_GENRES.find(m=>m.id===id)).filter(Boolean);
  const movieItems  = state.selectedMovies.map(id=>MOVIE_GENRES.find(m=>m.id===id)).filter(Boolean);
  const styleItem   = DESK_STYLES.find(s=>s.id===state.selectedStyle);

  return (
    <div style={{minHeight:"100%",background:"linear-gradient(135deg,#ecfdf5,#e0f2fe,#f5f3ff)",position:"relative",overflow:"hidden"}}>
      {state.photoUrl && <img src={state.photoUrl} alt="" style={{position:"absolute",inset:0,width:"100%",height:"100%",objectFit:"cover",opacity:0.08,filter:"blur(18px)"}}/>}
      <div style={{position:"relative",zIndex:10,display:"flex",flexDirection:"column",
        alignItems:"center",padding:"20px 14px",gap:14,maxWidth:440,margin:"0 auto"}}>

        <StepBar step={4}/>

        <Glass style={{width:"100%",padding:"14px 20px",textAlign:"center"}}>
          <div style={{fontSize:20,fontWeight:900,color:"#14532d",textTransform:"uppercase",letterSpacing:2}}>🏆 Your Final Vibe Card</div>
          <div style={{fontSize:10,color:"#16a34a",fontWeight:900,textTransform:"uppercase",letterSpacing:2,marginTop:4}}>Complete desk personality</div>
        </Glass>

        {/* Final avatar + description side by side */}
        <AvatarPersonaRow
          colorId={persona?.colorId} tagline={tagline} step={3}
          hobbies={state.selectedHobbies} musicIds={state.selectedMusic}
          movieIds={state.selectedMovies} styleId={state.selectedStyle} size={85}
          label="🤖 Who You Are" description={desc}
          traits={traits} dark={color.dark}
        />

        {/* Summary choice tags */}
        <Glass style={{width:"100%",padding:"10px 14px"}}>
          <div style={{display:"flex",flexWrap:"wrap",gap:5}}>
            {hobbyItems.map(h=><span key={h.id} style={{fontSize:10,padding:"2px 8px",borderRadius:99,background:"#f0fdf4",color:"#166534",fontWeight:700}}>{h.icon} {h.label}</span>)}
            {musicItems.map(m=><span key={m.id} style={{fontSize:10,padding:"2px 8px",borderRadius:99,background:"#faf5ff",color:"#7e22ce",fontWeight:700}}>{m.icon} {m.label}</span>)}
            {movieItems.map(m=><span key={m.id} style={{fontSize:10,padding:"2px 8px",borderRadius:99,background:"#fff1f2",color:"#be123c",fontWeight:700}}>{m.icon} {m.label}</span>)}
            {styleItem && <span style={{fontSize:10,padding:"2px 8px",borderRadius:99,background:"#f0fdfa",color:"#0f766e",fontWeight:700}}>{styleItem.icon} {styleItem.label}</span>}
          </div>
        </Glass>

        {/* Playlist */}
        <Glass style={{width:"100%",padding:16}}>
          <div style={{fontSize:11,fontWeight:900,color:"#6d28d9",textTransform:"uppercase",letterSpacing:2,marginBottom:12}}>🎵 Your Playlist</div>
          <div style={{display:"flex",flexDirection:"column",gap:8,maxHeight:280,overflowY:"auto"}}>
            {playlist.map((track,i)=><TrackCard key={i} track={track} idx={i} musicIds={state.selectedMusic}/>)}
          </div>
        </Glass>

        {/* Watchlist */}
        <Glass style={{width:"100%",padding:16}}>
          <div style={{fontSize:11,fontWeight:900,color:"#9f1239",textTransform:"uppercase",letterSpacing:2,marginBottom:12}}>🎬 Your Watch List</div>
          <div style={{display:"flex",flexDirection:"column",gap:8}}>
            {watchlist.map((film,i)=><FilmCard key={i} film={film} idx={i}/>)}
          </div>
        </Glass>

        {/* CTA to Step 5 */}
        <div style={{width:"100%",borderRadius:24,overflow:"hidden",position:"relative",
          background:`linear-gradient(135deg,${color.grad[0]},${color.grad[1]})`,
          boxShadow:`0 8px 32px ${color.hex}55`}}>
          {/* faint desk photo behind CTA */}
          {state.photoUrl && <img src={state.photoUrl} alt="" style={{position:"absolute",inset:0,width:"100%",height:"100%",objectFit:"cover",opacity:0.18,mixBlendMode:"overlay"}}/>}
          <div style={{position:"relative",zIndex:1,padding:"22px 20px",textAlign:"center"}}>
            <div style={{fontSize:28,marginBottom:6}}>{reward.emoji}</div>
            <div style={{fontSize:16,fontWeight:900,color:"white",marginBottom:4,letterSpacing:.5}}>
              Elevate Your Desk
            </div>
            <div style={{fontSize:12,color:"rgba(255,255,255,0.82)",fontWeight:600,marginBottom:8,lineHeight:1.5}}>
              See how a <b style={{color:"white"}}>{reward.name}</b> would look on your desk
            </div>
            {/* Debug: show what drove the choice */}
            <div style={{fontSize:9,color:"rgba(255,255,255,0.45)",marginBottom:16,fontFamily:"monospace"}}>
              picked: {derivedArchetype} | desk: [{(persona?.deskObjects||[]).slice(0,4).join(", ")}] | style: {state.selectedStyle||"—"}
            </div>
            <button onClick={()=>update({step:5})}
              style={{background:"white",color:color.dark,fontWeight:900,fontSize:12,
                textTransform:"uppercase",letterSpacing:2,padding:"12px 32px",
                borderRadius:16,border:"none",cursor:"pointer",
                boxShadow:"0 4px 16px rgba(0,0,0,0.15)",fontFamily:"inherit"}}>
              ✦ Show Me →
            </button>
          </div>
        </div>

        <Btn onClick={reset} style={{width:"100%",background:"rgba(0,0,0,0.06)",
          color:"#78716c",padding:"14px 0",borderRadius:18,fontSize:11,
          textTransform:"uppercase",letterSpacing:2,marginBottom:8}}>
          🔄 Start Over
        </Btn>
      </div>
    </div>
  );
}

// ─── STEP 5: ELEVATE YOUR DESK ───────────────────────────────────────────────

function Step5() {
  const {state, update, reset} = useGame();
  const persona = state.persona;
  const color   = bc(persona?.colorId);

  // phase: "scanning" → "placing" → "revealed"
  const [phase, setPhase] = useState("scanning");
  const [scanY, setScanY]   = useState(0);
  const [msgIdx, setMsgIdx] = useState(0);

  const scanMsgs = [
    "📐 Measuring desk surface...",
    "🔍 Finding the perfect spot...",
    "✨ Placing your reward...",
    "🎁 Almost ready!",
  ];

  const derivedArchetype = getRewardArchetype(state);
  const reward = REWARDS[derivedArchetype] || REWARDS.default;

  useEffect(() => {
    // Phase 1: scan line sweeps down
    let sy = 0;
    const scanInt = setInterval(() => {
      sy += 3;
      setScanY(sy);
      if (sy >= 105) {
        clearInterval(scanInt);
        setPhase("placing");
      }
    }, 28);

    // Message cycling during scan
    const msgInt = setInterval(() => setMsgIdx(i => (i+1) % scanMsgs.length), 900);

    return () => { clearInterval(scanInt); clearInterval(msgInt); };
  }, []);

  useEffect(() => {
    if (phase === "placing") {
      const t = setTimeout(() => setPhase("revealed"), 1000);
      return () => clearTimeout(t);
    }
  }, [phase]);

  const revealed = phase === "revealed";
  const scanning = phase === "scanning";

  return (
    <div style={{minHeight:"100%", background:"#0a0f0b", position:"relative", overflow:"hidden"}}>

      {/* Blurred desk photo background */}
      {state.photoUrl && (
        <img src={state.photoUrl} alt="" style={{
          position:"absolute", inset:0, width:"100%", height:"100%",
          objectFit:"cover", opacity:0.22, filter:"blur(24px) saturate(0.5)",
        }}/>
      )}
      <div style={{position:"absolute", inset:0,
        background:"linear-gradient(180deg,rgba(0,0,0,0.6) 0%,rgba(0,0,0,0.15) 50%,rgba(0,0,0,0.75) 100%)"}}/>

      <div style={{position:"relative", zIndex:10, display:"flex", flexDirection:"column",
        alignItems:"center", padding:"20px 14px", gap:16, maxWidth:480, margin:"0 auto"}}>

        <StepBar step={5}/>

        {/* Header */}
        <div style={{textAlign:"center"}}>
          <div style={{fontSize:11,fontWeight:900,color:"rgba(255,255,255,0.5)",
            textTransform:"uppercase",letterSpacing:3,marginBottom:6}}>Step 5</div>
          <div style={{fontSize:22,fontWeight:900,color:"white",letterSpacing:.5,marginBottom:4}}>
            ✦ Elevate Your Desk
          </div>
          <div style={{fontSize:12,color:"rgba(255,255,255,0.65)",fontWeight:600}}>
            {scanning ? scanMsgs[msgIdx] : phase==="placing" ? "🎁 Adding your reward..." : "Here's your upgraded desk!"}
          </div>
        </div>

        {/* Main desk frame */}
        <div style={{
          width:"100%", borderRadius:24, overflow:"hidden",
          border:"3px solid rgba(255,255,255,0.2)",
          boxShadow:"0 20px 60px rgba(0,0,0,0.5)",
          position:"relative",
        }}>
          {/* tape strips */}
          <div style={{position:"absolute",top:-7,left:"16%",width:64,height:14,
            background:"rgba(255,255,220,0.85)",borderRadius:3,transform:"rotate(-2deg)",zIndex:20}}/>
          <div style={{position:"absolute",top:-7,right:"16%",width:64,height:14,
            background:"rgba(255,255,220,0.85)",borderRadius:3,transform:"rotate(2deg)",zIndex:20}}/>

          <div style={{aspectRatio:"4/3", position:"relative"}}>
            {/* desk photo */}
            {state.photoUrl
              ? <img src={state.photoUrl} alt="Your desk"
                  style={{width:"100%", height:"100%", objectFit:"cover", display:"block"}}/>
              : <div style={{width:"100%",height:"100%",background:"linear-gradient(135deg,#a7f3d0,#bae6fd)"}}/>}

            {/* bottom vignette */}
            <div style={{position:"absolute",inset:0,
              background:"linear-gradient(to bottom, transparent 45%, rgba(0,0,0,0.35) 100%)"}}/>

            {/* SCAN LINE — sweeps during scanning phase */}
            {scanning && (
              <>
                <div style={{
                  position:"absolute", left:0, right:0, top:`${scanY}%`,
                  height:3,
                  background:"linear-gradient(90deg,transparent,#4ade80,#22d3ee,#4ade80,transparent)",
                  boxShadow:"0 0 18px #4ade80, 0 0 36px rgba(74,222,128,0.4)",
                  zIndex:15,
                  transition:"top 0.03s linear",
                }}/>
                {/* scanned area tint */}
                <div style={{
                  position:"absolute", left:0, right:0, top:0, height:`${scanY}%`,
                  background:"rgba(74,222,128,0.05)", zIndex:14,
                }}/>
                {/* corner brackets */}
                {[[6,6],[6,88],[88,6],[88,88]].map(([x,y],i) => (
                  <div key={i} style={{
                    position:"absolute", left:`${x}%`, top:`${y}%`,
                    width:18, height:18, zIndex:16,
                    borderTop:    y<50 ? "2px solid #4ade80" : undefined,
                    borderBottom: y>50 ? "2px solid #4ade80" : undefined,
                    borderLeft:   x<50 ? "2px solid #4ade80" : undefined,
                    borderRight:  x>50 ? "2px solid #4ade80" : undefined,
                  }}/>
                ))}
                <div style={{
                  position:"absolute", top:"48%", left:"50%",
                  transform:"translate(-50%,-50%)",
                  fontSize:10, fontWeight:900, color:"#4ade80",
                  textTransform:"uppercase", letterSpacing:3, zIndex:17,
                  background:"rgba(0,0,0,0.5)", padding:"4px 10px", borderRadius:8,
                }}>SCANNING</div>
              </>
            )}

            {/* "placing" phase — pulsing target ring where reward will appear */}
            {phase === "placing" && (
              <div style={{
                position:"absolute", bottom:"8%", left:"9%",
                width:60, height:60,
                border:"3px solid #4ade80",
                borderRadius:"50%",
                animation:"pulseRing 0.6s ease-in-out infinite",
                zIndex:15,
                display:"flex", alignItems:"center", justifyContent:"center",
                fontSize:24,
              }}>
                {reward.emoji}
              </div>
            )}

            {/* SVG reward — appears on reveal */}
            <svg viewBox="0 0 100 165" style={{
              position:"absolute", bottom:0, left:"4%",
              width:"18%", height:"auto",
              filter:"drop-shadow(3px 6px 10px rgba(0,0,0,0.5))",
              zIndex:10,
              opacity: revealed ? 1 : 0,
              transform: revealed ? "translateY(0) scale(1)" : "translateY(20px) scale(0.85)",
              transition:"opacity 0.8s ease, transform 0.8s cubic-bezier(.34,1.56,.64,1)",
            }}
              dangerouslySetInnerHTML={{__html: (REWARD_SVG[derivedArchetype]||REWARD_SVG.default)()}}
            />

            {/* "New" badge */}
            <div style={{
              position:"absolute", bottom:"34%", left:"24%",
              background:`linear-gradient(135deg,${color.grad[0]},${color.grad[1]})`,
              borderRadius:99, padding:"3px 10px", fontSize:9, fontWeight:900,
              color:"white", letterSpacing:1, textTransform:"uppercase",
              boxShadow:`0 2px 10px ${color.hex}66`, zIndex:11,
              opacity: revealed ? 1 : 0,
              transition:"opacity 0.5s ease 0.9s",
            }}>✦ New</div>

            {/* reward name badge bottom right */}
            <div style={{
              position:"absolute", bottom:10, right:10,
              background:"rgba(0,0,0,0.72)", backdropFilter:"blur(10px)",
              borderRadius:12, padding:"5px 11px",
              display:"flex", alignItems:"center", gap:6, zIndex:11,
              opacity: revealed ? 1 : 0,
              transition:"opacity 0.5s ease 1s",
            }}>
              <span style={{fontSize:14}}>{reward.emoji}</span>
              <span style={{fontSize:10,fontWeight:900,color:"white"}}>{reward.name}</span>
            </div>
          </div>
        </div>

        {/* Reward explanation */}
        <div style={{
          width:"100%", borderRadius:20,
          background:"rgba(255,255,255,0.1)", backdropFilter:"blur(20px)",
          border:"1px solid rgba(255,255,255,0.18)",
          padding:18, display:"flex", alignItems:"flex-start", gap:14,
          opacity: revealed ? 1 : 0,
          transition:"opacity 0.6s ease 1.1s",
        }}>
          <div style={{fontSize:36, flexShrink:0}}>{reward.emoji}</div>
          <div>
            <div style={{fontSize:13,fontWeight:900,color:"white",marginBottom:5}}>🎁 {reward.name}</div>
            <p style={{fontSize:12,color:"rgba(255,255,255,0.75)",fontWeight:600,margin:0,lineHeight:1.6}}>
              {reward.why}
            </p>
          </div>
        </div>

        {/* Actions */}
        <div style={{
          width:"100%", display:"flex", flexDirection:"column", gap:10,
          opacity: revealed ? 1 : 0,
          transition:"opacity 0.5s ease 1.2s",
        }}>
          <Btn onClick={()=>update({step:4})}
            style={{width:"100%", background:"rgba(255,255,255,0.12)",
              border:"1px solid rgba(255,255,255,0.22)",
              color:"white", padding:"14px 0", borderRadius:16,
              fontSize:11, textTransform:"uppercase", letterSpacing:2}}>
            ← Back to Vibe Card
          </Btn>
          <Btn onClick={reset}
            style={{width:"100%",
              background:`linear-gradient(135deg,${color.grad[0]},${color.grad[1]})`,
              color:"white", padding:"14px 0", borderRadius:16,
              fontSize:11, textTransform:"uppercase", letterSpacing:2,
              boxShadow:`0 4px 20px ${color.hex}55`}}>
            🔄 Start Over
          </Btn>
        </div>
      </div>
    </div>
  );
}

// ─── ROUTER ───────────────────────────────────────────────────────────────────

function Router() {
  const {state} = useGame();
  return (
    <div style={{width:"100%",height:"100%"}}>
      {state.step===1 && <Step1/>}
      {state.step===2 && <Step2/>}
      {state.step===3 && <Step3/>}
      {state.step===4 && <Step4/>}
      {state.step===5 && <Step5/>}
    </div>
  );
}

export default function App() {
  return (
    <Provider>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@500;700;900&display=swap');
        * { font-family:'Quicksand',sans-serif; box-sizing:border-box; }
        body { margin:0; padding:0; }
        @keyframes bounce { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-12px)} }
        @keyframes pulse  { 0%,100%{transform:scale(1)} 50%{transform:scale(1.1)} }
        @keyframes scanLine { 0%{top:0%} 100%{top:105%} }
        @keyframes pulseRing { 0%,100%{transform:scale(1);opacity:1} 50%{transform:scale(1.15);opacity:0.6} }
        ::-webkit-scrollbar{width:4px} ::-webkit-scrollbar-thumb{background:#c8e6c9;border-radius:4px}
      `}</style>
      <Router/>
    </Provider>
  );
}
