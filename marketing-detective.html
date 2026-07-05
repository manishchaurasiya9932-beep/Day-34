<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Marketing Detective</title>
<style>
  :root{
    --accent:#ff6b35; --accent-dim:#ff6b3540; --accent-glow:#ff6b3599;
    --bg-0:#0d0d10; --bg-1:#16161a; --bg-2:#1e1e24; --paper:#e8dcc4; --paper-2:#f2e9d3;
    --ink:#2b2620; --cork:#3a2c22; --cork-2:#4a3928; --pin:#c0392b;
    --text:#e9e6df; --text-dim:#a8a49a; --success:#3fd67a; --danger:#ff5c5c;
    --font-head:'Georgia', 'Times New Roman', serif; --font-body:'Segoe UI', Arial, sans-serif;
    --font-hand: 'Segoe Print','Bradley Hand', cursive;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html,body{height:100%;}
  body{
    background: radial-gradient(ellipse at top, var(--bg-1), var(--bg-0));
    color:var(--text); font-family:var(--font-body); min-height:100vh; overflow-x:hidden;
    -webkit-font-smoothing:antialiased;
  }
  #app{min-height:100vh; position:relative;}
  .screen{ min-height:100vh; display:flex; flex-direction:column; align-items:center; justify-content:center; padding:32px 16px; animation:fadeIn .6s ease; position:relative;}
  @keyframes fadeIn{from{opacity:0; transform:translateY(8px);} to{opacity:1; transform:translateY(0);}}
  .noise{position:fixed; inset:0; pointer-events:none; opacity:.04; z-index:0;
    background-image: radial-gradient(circle at 20% 30%, #fff 0, transparent 1px), radial-gradient(circle at 70% 60%, #fff 0, transparent 1px), radial-gradient(circle at 40% 80%, #fff 0, transparent 1px);
    background-size: 60px 60px, 90px 90px, 120px 120px;}
  h1,h2,h3{font-family:var(--font-head); letter-spacing:.5px;}
  .glow{ text-shadow: 0 0 18px var(--accent-glow); }
  .btn{
    background:linear-gradient(180deg,var(--accent),#d4501e); color:#fff; border:none; padding:14px 30px;
    font-size:15px; font-weight:700; border-radius:8px; cursor:pointer; letter-spacing:.5px;
    box-shadow:0 4px 18px var(--accent-dim), inset 0 1px 0 rgba(255,255,255,.25);
    transition:transform .15s ease, box-shadow .15s ease; text-transform:uppercase;
  }
  .btn:hover{ transform:translateY(-2px); box-shadow:0 8px 26px var(--accent-glow), inset 0 1px 0 rgba(255,255,255,.3);}
  .btn:active{ transform:translateY(0px) scale(.98); }
  .btn.ghost{ background:transparent; border:1px solid #ffffff33; color:var(--text); box-shadow:none;}
  .btn.ghost:hover{ border-color:var(--accent); color:var(--accent); box-shadow:0 0 16px var(--accent-dim);}
  .btn:disabled{opacity:.4; cursor:not-allowed; transform:none; box-shadow:none;}

  /* ---------- Title / Theme ---------- */
  .title-wrap{ text-align:center; max-width:720px; z-index:1;}
  .badge{ display:inline-block; padding:6px 16px; border:1px solid var(--accent); color:var(--accent); border-radius:100px; font-size:11px; letter-spacing:2px; text-transform:uppercase; margin-bottom:22px;}
  .title-wrap h1{ font-size:52px; margin-bottom:10px;}
  .title-wrap p{ color:var(--text-dim); font-size:16px; margin-bottom:36px; line-height:1.6;}
  .theme-grid{ display:flex; flex-wrap:wrap; gap:16px; justify-content:center; margin-bottom:34px;}
  .theme-card{
    width:130px; padding:16px 10px; border-radius:12px; cursor:pointer; border:2px solid transparent;
    background:var(--bg-2); transition:all .2s ease; text-align:center;
  }
  .theme-card:hover{ transform:translateY(-4px); }
  .theme-card.selected{ border-color:var(--t-accent); box-shadow:0 0 24px var(--t-accent-glow);}
  .swatch-row{ display:flex; justify-content:center; gap:6px; margin-bottom:10px;}
  .swatch{ width:18px; height:18px; border-radius:50%; box-shadow:inset 0 0 0 1px rgba(255,255,255,.2);}
  .theme-card span{ font-size:12px; color:var(--text-dim); font-weight:600; letter-spacing:.3px;}

  /* ---------- Case Assignment (folder) ---------- */
  .folder-wrap{ max-width:640px; width:100%; z-index:1;}
  .stamp{
    position:absolute; top:22px; right:28px; border:3px solid var(--danger); color:var(--danger);
    padding:6px 14px; font-weight:800; font-size:13px; letter-spacing:2px; transform:rotate(-14deg);
    border-radius:6px; opacity:.9; font-family:var(--font-head);
  }
  .folder{
    background:linear-gradient(160deg, var(--paper-2), var(--paper));
    color:var(--ink); border-radius:6px; padding:34px 34px 28px; position:relative;
    box-shadow:0 20px 60px rgba(0,0,0,.55), 0 0 0 1px rgba(0,0,0,.08);
    background-image: repeating-linear-gradient(0deg, rgba(0,0,0,.015) 0px, transparent 2px, transparent 26px);
  }
  .folder::before{ content:''; position:absolute; top:-14px; left:26px; width:120px; height:26px; background:var(--paper-2); border-radius:6px 6px 0 0;}
  .case-label{ font-size:11px; letter-spacing:2px; text-transform:uppercase; color:#8a7a5c; margin-bottom:6px;}
  .folder h2{ font-size:28px; margin-bottom:4px;}
  .folder .industry{ font-style:italic; color:#6b5d42; margin-bottom:18px; font-size:14px;}
  .field-row{ display:flex; gap:14px; margin-bottom:14px; flex-wrap:wrap;}
  .field{ flex:1; min-width:180px;}
  .field label{ display:block; font-size:10px; text-transform:uppercase; letter-spacing:1.5px; color:#8a7a5c; margin-bottom:3px; font-weight:700;}
  .field div{ font-size:14.5px; line-height:1.4;}
  .chips{ display:flex; flex-wrap:wrap; gap:6px; margin-top:4px;}
  .chip{ background:#00000012; padding:3px 10px; border-radius:100px; font-size:12px; border:1px solid #00000022;}
  .divider{ height:1px; background:repeating-linear-gradient(90deg, #00000030 0 6px, transparent 6px 12px); margin:18px 0;}
  .folder-actions{ text-align:right; margin-top:22px;}

  /* ---------- Investigation Board ---------- */
  .board-screen{ align-items:stretch; padding:20px;}
  .board-header{ display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:12px; padding:6px 12px 18px; z-index:1;}
  .board-header h2{ font-size:20px;}
  .progress-track{ width:220px; height:8px; background:#ffffff14; border-radius:100px; overflow:hidden;}
  .progress-fill{ height:100%; background:linear-gradient(90deg,var(--t-accent),#fff8); border-radius:100px; transition:width .4s ease;}
  .cork{
    flex:1; background:
      radial-gradient(circle at 15% 20%, rgba(0,0,0,.25), transparent 60%),
      radial-gradient(circle at 80% 70%, rgba(0,0,0,.25), transparent 60%),
      repeating-radial-gradient(circle, #00000009 0, transparent 2px, transparent 4px),
      linear-gradient(160deg, var(--cork-2), var(--cork));
    border-radius:14px; position:relative; min-height:60vh; padding:26px;
    box-shadow: inset 0 0 60px rgba(0,0,0,.5), 0 10px 40px rgba(0,0,0,.4);
    display:grid; grid-template-columns:repeat(auto-fill, minmax(210px,1fr)); gap:22px; align-content:start;
    border:10px solid #2a2018;
  }
  .card{
    background:linear-gradient(170deg,var(--paper-2),var(--paper)); color:var(--ink); border-radius:3px;
    padding:16px 14px 14px; position:relative; cursor:grab; user-select:none;
    box-shadow:0 8px 18px rgba(0,0,0,.4), 0 1px 0 rgba(255,255,255,.5) inset;
    transform:rotate(var(--r,-1deg)); transition:transform .2s ease, box-shadow .2s ease;
    font-size:13px; line-height:1.45; min-height:120px;
  }
  .card:hover{ transform:rotate(0deg) translateY(-4px) scale(1.02); box-shadow:0 16px 30px rgba(0,0,0,.55); z-index:5;}
  .card.dragging{ opacity:.4; }
  .card.pinned{ outline:2px solid var(--t-accent); box-shadow:0 0 22px var(--t-accent-glow);}
  .pin{
    position:absolute; top:-9px; left:50%; transform:translateX(-50%); width:16px; height:16px; border-radius:50%;
    background:radial-gradient(circle at 35% 30%, #ff8a7a, var(--pin)); box-shadow:0 3px 6px rgba(0,0,0,.5);
  }
  .card h4{ font-size:13px; margin-bottom:6px; text-transform:uppercase; letter-spacing:.5px; color:#5a4a2f; border-bottom:1px dashed #00000030; padding-bottom:5px;}
  .card .tag{ position:absolute; bottom:8px; right:10px; font-size:9px; text-transform:uppercase; letter-spacing:1px; color:#8a7a5c; font-weight:700;}
  .sticky{ background:#fff2a8; transform:rotate(var(--r,1.5deg)); }
  .sticky h4{ color:#7a6a1f; border-bottom-color:#00000020;}
  .metric-grid{ display:grid; grid-template-columns:1fr 1fr; gap:6px; margin-top:4px;}
  .metric-grid div{ font-size:12px;}
  .metric-grid b{ display:block; font-size:15px; color:#3a3020;}

  .locker{
    margin-top:20px; border:2px dashed #ffffff30; border-radius:14px; padding:18px; min-height:100px;
    background:#00000022; z-index:1;
  }
  .locker.dragover{ border-color:var(--t-accent); background:var(--t-accent-dim); }
  .locker-title{ font-size:12px; text-transform:uppercase; letter-spacing:2px; color:var(--text-dim); margin-bottom:10px;}
  .locker-empty{ color:#ffffff40; font-size:13px; font-style:italic; text-align:center; padding:20px 0;}
  .locker-items{ display:flex; flex-wrap:wrap; gap:12px;}

  .board-footer{ display:flex; justify-content:space-between; align-items:center; margin-top:20px; flex-wrap:wrap; gap:12px; z-index:1;}
  .hint{ color:var(--text-dim); font-size:13px; font-style:italic;}

  /* ---------- Solve modal ---------- */
  .overlay{ position:fixed; inset:0; background:rgba(0,0,0,.7); backdrop-filter:blur(4px); display:flex; align-items:center; justify-content:center; z-index:50; padding:20px; animation:fadeIn .3s ease;}
  .modal{ background:var(--bg-2); border-radius:16px; padding:30px; max-width:560px; width:100%; box-shadow:0 30px 80px rgba(0,0,0,.6); border:1px solid #ffffff14;}
  .modal h3{ margin-bottom:6px;}
  .modal p.sub{ color:var(--text-dim); font-size:13px; margin-bottom:18px;}
  .option{
    display:block; width:100%; text-align:left; background:#ffffff08; border:1px solid #ffffff18; color:var(--text);
    padding:14px 16px; border-radius:10px; margin-bottom:10px; cursor:pointer; font-size:14px; transition:all .15s ease;
  }
  .option:hover{ background:#ffffff14; border-color:var(--t-accent);}
  .option.correct{ background:#3fd67a22; border-color:var(--success); }
  .option.wrong{ background:#ff5c5c22; border-color:var(--danger); }
  .modal-actions{ display:flex; justify-content:flex-end; gap:10px; margin-top:16px;}

  /* ---------- Verdict / Case closed ---------- */
  .verdict-screen{ text-align:center; z-index:1;}
  .stamp-big{
    font-family:var(--font-head); font-size:64px; font-weight:900; letter-spacing:4px; border:6px solid;
    padding:14px 40px; border-radius:10px; transform:rotate(-8deg); display:inline-block; margin-bottom:30px;
    animation:stampIn .5s cubic-bezier(.2,1.4,.4,1);
  }
  @keyframes stampIn{ 0%{ transform:rotate(-8deg) scale(3); opacity:0;} 70%{opacity:1;} 100%{ transform:rotate(-8deg) scale(1); opacity:1;} }
  .stamp-big.win{ color:var(--success); border-color:var(--success); text-shadow:0 0 30px #3fd67a99;}
  .stamp-big.lose{ color:var(--danger); border-color:var(--danger); text-shadow:0 0 30px #ff5c5c99;}

  /* ---------- Learning report ---------- */
  .report-wrap{ max-width:700px; width:100%; z-index:1;}
  .report-card{ background:linear-gradient(170deg,var(--paper-2),var(--paper)); color:var(--ink); border-radius:10px; padding:30px; box-shadow:0 20px 60px rgba(0,0,0,.5); margin-bottom:20px;}
  .report-card h3{ color:#4a3928; margin-bottom:10px; font-size:19px; border-bottom:2px solid #00000020; padding-bottom:8px;}
  .report-card ul{ padding-left:20px; margin-top:8px;}
  .report-card li{ margin-bottom:6px; font-size:14px; line-height:1.5;}
  .clue-list{ display:flex; flex-direction:column; gap:8px; margin-top:10px;}
  .clue-item{ background:#00000010; padding:10px 14px; border-radius:6px; font-size:13.5px; border-left:3px solid var(--accent);}
  .chart-bars{ display:flex; align-items:end; gap:10px; height:120px; margin-top:14px;}
  .bar-col{ flex:1; display:flex; flex-direction:column; align-items:center; justify-content:end; height:100%;}
  .bar{ width:60%; background:linear-gradient(180deg,var(--t-accent),#d4501e); border-radius:6px 6px 0 0; transition:height 1s cubic-bezier(.2,1,.3,1);}
  .bar-label{ font-size:10px; color:#5a4a2f; margin-top:6px; text-align:center;}
  .final-actions{ display:flex; gap:12px; justify-content:center; margin-top:10px; z-index:1;}
  .score-pill{ display:inline-block; background:#00000015; padding:6px 16px; border-radius:100px; font-size:12px; font-weight:700; color:#4a3928; margin-left:8px;}

  @media (max-width:640px){
    .title-wrap h1{ font-size:36px;}
    .folder{ padding:22px 18px;}
    .stamp-big{ font-size:38px; padding:10px 22px;}
  }
</style>
</head>
<body>
<div class="noise"></div>
<div id="app"></div>

<script>
(function(){
"use strict";

/* ============ THEMES ============ */
const THEMES = [
  {id:'claude', name:'Claude Orange', accent:'#ff6b35', accent2:'#d4501e'},
  {id:'midnight', name:'Midnight Blue', accent:'#3d8bff', accent2:'#1e5fbf'},
  {id:'noir', name:'Noir Green', accent:'#39d98a', accent2:'#1fa868'},
  {id:'crimson', name:'Crimson', accent:'#ff4757', accent2:'#c62b3a'},
  {id:'violet', name:'Violet Vice', accent:'#a05bff', accent2:'#6f2fd6'},
  {id:'gold', name:'Old Gold', accent:'#e0b13f', accent2:'#a97e1f'},
];

function hexToRgba(hex, a){
  const h = hex.replace('#','');
  const r = parseInt(h.substring(0,2),16), g = parseInt(h.substring(2,4),16), b = parseInt(h.substring(4,6),16);
  return `rgba(${r},${g},${b},${a})`;
}
function applyTheme(theme){
  const root = document.documentElement.style;
  root.setProperty('--t-accent', theme.accent);
  root.setProperty('--t-accent-glow', hexToRgba(theme.accent,.55));
  root.setProperty('--t-accent-dim', hexToRgba(theme.accent,.18));
  root.setProperty('--accent', theme.accent);
  root.setProperty('--accent-glow', hexToRgba(theme.accent,.6));
  root.setProperty('--accent-dim', hexToRgba(theme.accent,.25));
}

/* ============ CASE DATA ============ */
const CASES = [
  {
    company:"Bloomvale Skincare", industry:"Beauty & Cosmetics",
    objective:"Drive online sales for a new anti-aging serum line among women aged 35-55.",
    audience:"Women, 35-55, urban & semi-urban, household income upper-middle, skincare-conscious.",
    channels:["Instagram Reels","Influencer Marketing","Google Search Ads"],
    budget:[{c:"Influencer Marketing",p:62},{c:"Instagram Reels",p:26},{c:"Google Search Ads",p:12}],
    metrics:{reach:"2.4M", ctr:"0.6%", engagement:"8.9%", conversions:"0.4%", sales:"₹6.1L (target ₹40L)"},
    comments:[
      "\"Loved the reel, but where do I even buy this? Their Instagram bio link is broken.\"",
      "\"The influencer looked 22, not exactly who I pictured using anti-aging cream.\"",
      "\"Nice video but I still don't know what makes this serum different from The Ordinary.\""
    ],
    social:{platform:"Instagram", followers:"310K", avgLikes:"18K", avgComments:"92", sentiment:"Mixed-Positive (video quality), Negative (relevance & clarity)"},
    mistake:"Influencer-audience mismatch: the brand hired young, 20-something beauty influencers to promote an anti-aging product meant for women 35-55, so the content resonated visually but failed to build purchase trust with the actual target demographic.",
    clues:[
      "High engagement (8.9%) but extremely low conversion (0.4%) — people watched and liked, but didn't buy.",
      "Customer comments repeatedly question relevance ('who is this for?') rather than praising product fit.",
      "62% of budget concentrated in influencer marketing with almost no spend on trust-building content like dermatologist endorsements or before/after case studies for the actual age group."
    ],
    explanation:"Bloomvale over-indexed on influencer virality without checking whether the influencers' own audience actually overlapped with their target buyer. High reach and engagement created a false sense of success while conversions stayed flat, because 20-something followers of the influencers were not the ones needing an anti-aging serum, and the 35-55 target audience saw the ads only secondhand and didn't trust the message.",
    improvements:[
      "Partner with micro-influencers or dermatologists whose actual audience is 35-55.",
      "Reallocate 15-20% of influencer budget into retargeting ads with testimonials from real customers in the target age range.",
      "Fix broken bio links and simplify the path from ad to purchase.",
      "Use before/after UGC content instead of purely aesthetic reels."
    ]
  },
  {
    company:"UrbanCrate Meal Kits", industry:"Food & Beverage / D2C",
    objective:"Acquire new subscribers for a weekly meal-kit delivery service in Tier-1 cities.",
    audience:"Working professionals, 25-40, dual-income households, time-starved cooks.",
    channels:["Facebook Ads","YouTube Pre-roll","Referral Program"],
    budget:[{c:"Facebook Ads",p:55},{c:"YouTube Pre-roll",p:30},{c:"Referral Program",p:15}],
    metrics:{reach:"1.8M", ctr:"2.1%", engagement:"5.4%", conversions:"3.2%", sales:"1,240 trial signups, 62 converted to paid"},
    comments:[
      "\"Signed up for the ₹99 trial, had no idea the real plan was ₹1,899/week until checkout.\"",
      "\"Felt tricked honestly, cancelled immediately after the trial box.\"",
      "\"Good food quality but the pricing jump killed my trust.\""
    ],
    social:{platform:"Facebook", followers:"142K", avgLikes:"2.1K", avgComments:"340", sentiment:"Negative — many comments call out 'hidden pricing' and 'bait and switch'"},
    mistake:"Deceptive pricing funnel: the ₹99 trial offer was heavily promoted while the actual recurring subscription price was buried in fine print, causing a huge trial-to-paid drop-off (1,240 → 62, a 95% churn) due to broken trust rather than product quality.",
    clues:[
      "Trial signups are strong (3.2% conversion, 1,240 people) but paid conversion from trial is only 5%.",
      "Comment volume (340) is unusually high for the engagement level and is dominated by pricing complaints, not product complaints.",
      "Budget allocation has zero spend on transparent onboarding or email nurture sequences that could clarify pricing before checkout."
    ],
    explanation:"UrbanCrate optimized the top of funnel aggressively with a low-friction ₹99 hook but failed to build a transparent bridge to the real price point. This created a spike in vanity metrics (signups, reach) while destroying trust exactly at the moment of highest scrutiny — checkout — leading to mass abandonment and public negative sentiment that will hurt future acquisition costs.",
    improvements:[
      "Disclose the full subscription price clearly in ad creative and landing page, not just at checkout.",
      "Redesign the funnel to include a mid-funnel email/SMS sequence explaining value before the trial ends.",
      "Test a lower ongoing price with smaller initial discount instead of a steep bait price.",
      "Respond publicly to pricing complaints to rebuild trust."
    ]
  },
  {
    company:"Trekwell Outdoor Gear", industry:"Retail / Outdoor Apparel",
    objective:"Increase footfall and sales at 12 new physical stores in Tier-2 cities.",
    audience:"Young adults, 18-30, trekking and outdoor enthusiasts, budget-conscious.",
    channels:["Local Newspaper Ads","Radio Spots","In-store Flyers"],
    budget:[{c:"Local Newspaper Ads",p:45},{c:"Radio Spots",p:35},{c:"In-store Flyers",p:20}],
    metrics:{reach:"310K (estimated)", ctr:"N/A", engagement:"N/A", conversions:"Footfall up 4% vs 25% target", sales:"₹18L vs ₹65L target"},
    comments:[
      "\"Never heard of this brand until I walked past the store.\"",
      "\"My little brother (19) says he found out about them on someone else's Instagram story, not from the brand.\"",
      "\"Why doesn't this brand have real information anywhere online? I searched and found almost nothing.\""
    ],
    social:{platform:"Instagram", followers:"3.2K", avgLikes:"40", avgComments:"2", sentiment:"Negligible presence — audience largely unaware brand exists online"},
    mistake:"Channel mismatch with target audience: an 18-30 year old digitally-native audience was targeted almost entirely through traditional offline media (newspaper, radio, flyers), channels this demographic barely consumes, resulting in near-invisible brand awareness among the intended buyers.",
    clues:[
      "Zero social media or digital ad spend despite targeting an 18-30 audience that lives primarily on Instagram and YouTube.",
      "Footfall (4%) and sales (₹18L) drastically underperform the 25%/₹65L target despite spend being fully utilized.",
      "Almost no organic social following (3.2K) for a brand opening 12 new stores, showing no digital word-of-mouth machinery in place."
    ],
    explanation:"Trekwell allocated its entire budget to channels optimized for an older, more geographically-local audience, while its actual buyers — young, mobile-first outdoor enthusiasts — discover brands through short-form video, influencer content, and search. The mismatch meant spend was 'reaching' people, but not the right people, producing weak footfall despite full budget utilization.",
    improvements:[
      "Shift 40-50% of budget to Instagram/YouTube ads and local micro-influencer trekking content.",
      "Build a basic digital presence (Google Business listing, Instagram page) before store launches.",
      "Use geo-targeted social ads timed to each store opening.",
      "Keep radio only in markets where research confirms strong reach among the target age group."
    ]
  },
  {
    company:"Papernest Stationery Co.", industry:"E-commerce / Stationery",
    objective:"Boost repeat purchases via a new loyalty rewards program.",
    audience:"Students and young professionals, 16-28, existing customer base.",
    channels:["Email Marketing","App Push Notifications","SMS"],
    budget:[{c:"Email Marketing",p:20},{c:"App Push Notifications",p:70},{c:"SMS",p:10}],
    metrics:{reach:"480K existing users", ctr:"1.1% (push)", engagement:"Uninstall rate up 6%", conversions:"1.8%", sales:"Repeat purchase rate flat at 14%"},
    comments:[
      "\"Getting 4-5 notifications a day from this app, I muted it and honestly considering deleting.\"",
      "\"Every push feels like 'BUY NOW', none of it feels personal.\"",
      "\"I liked the loyalty program idea but the spam made me trust the brand less.\""
    ],
    social:{platform:"App Store Reviews", followers:"N/A", avgLikes:"N/A", avgComments:"N/A", sentiment:"Rating dropped from 4.3 to 3.6 in the campaign period, with 'too many notifications' the top complaint"},
    mistake:"Notification overload without personalization: the brand relied on high-frequency, generic push notifications (70% of budget) to drive loyalty engagement, which triggered notification fatigue, rising uninstall rates, and a drop in app store rating instead of increasing repeat purchases.",
    clues:[
      "70% of the budget went to blanket push notifications while only 20% went to more targeted, permission-based email.",
      "App uninstall rate rose 6% and app store rating fell from 4.3 to 3.6 during the very campaign meant to boost loyalty.",
      "Conversion from push notifications is low (1.8%) despite high send frequency, suggesting fatigue rather than genuine disinterest in the offer."
    ],
    explanation:"Papernest treated push notifications as a volume game rather than a precision one. Instead of segmenting users by purchase history and sending timely, relevant offers, they blasted frequent generic messages to the entire base. This created annoyance rather than affinity, actively damaging the brand relationship the loyalty program was meant to strengthen.",
    improvements:[
      "Segment users by purchase recency/frequency and personalize offers accordingly.",
      "Cap notification frequency (e.g., max 2-3/week) and A/B test timing.",
      "Shift more budget to email, which allows richer, less intrusive storytelling about rewards.",
      "Introduce an in-app notification preference center to rebuild trust."
    ]
  },
  {
    company:"FitCore Gyms", industry:"Fitness & Wellness",
    objective:"Fill new-year membership slots at 8 gym locations.",
    audience:"Adults 22-45 seeking New Year fitness resolutions.",
    channels:["Facebook Ads","Google Display Network","Local Flyers"],
    budget:[{c:"Facebook Ads",p:40},{c:"Google Display Network",p:45},{c:"Local Flyers",p:15}],
    metrics:{reach:"1.1M", ctr:"0.3%", engagement:"1.9%", conversions:"0.2%", sales:"210 new memberships vs 1,500 target"},
    comments:[
      "\"I keep seeing the same generic gym banner ad everywhere, it's honestly become background noise.\"",
      "\"Doesn't even say which of their 8 locations is nearest to me.\"",
      "\"The ad looks like every other gym ad I've seen, nothing makes this one stand out.\""
    ],
    social:{platform:"Facebook", followers:"58K", avgLikes:"310", avgComments:"14", sentiment:"Neutral/Indifferent — very low interaction relative to reach"},
    mistake:"Generic, undifferentiated creative fatigue: the campaign used the same broad, non-personalized display banner across all locations and audiences for the full campaign duration, leading to extremely low CTR (0.3%) as audiences tuned out repetitive, location-agnostic messaging.",
    clues:[
      "CTR (0.3%) is far below industry norms for display/social fitness ads, despite a 1.1M reach, indicating message fatigue not lack of reach.",
      "Customer comments explicitly mention seeing 'the same ad everywhere' and note it doesn't specify a nearby location.",
      "85% of budget went into broad, single-creative display and social placements with no geo-personalization or creative rotation."
    ],
    explanation:"FitCore ran a single static creative across a huge, undifferentiated audience for an extended period without rotating messaging or personalizing by location. This is a classic case of ad/banner blindness: reach kept growing but relevance kept dropping, so the campaign burned impressions on an audience that had stopped noticing the ad entirely.",
    improvements:[
      "Create location-specific ad variants with local gym names/addresses.",
      "Rotate creative every 1-2 weeks to avoid fatigue; use dynamic ads.",
      "Use retargeting for people who visited the site but didn't convert, with a differentiated offer.",
      "Add urgency/social proof (member count, transformation stories) unique to each location."
    ]
  },
  {
    company:"Lumora Home Decor", industry:"Home Furnishing / E-commerce",
    objective:"Launch a premium festive-season lighting collection.",
    audience:"Homeowners, 28-50, mid-to-high income, festive shoppers.",
    channels:["Instagram Ads","Pinterest","Email"],
    budget:[{c:"Instagram Ads",p:50},{c:"Pinterest",p:30},{c:"Email",p:20}],
    metrics:{reach:"890K", ctr:"1.6%", engagement:"6.2%", conversions:"2.9%", sales:"₹22L vs ₹35L target (added carts worth ₹58L never checked out)"},
    comments:[
      "\"Added 3 items to cart on mobile, page froze during checkout, gave up.\"",
      "\"Tried checking out twice on my phone, way too many steps, switched to desktop and forgot.\"",
      "\"The lights look gorgeous in the ad but I couldn't even zoom into the product photos on my phone.\""
    ],
    social:{platform:"Instagram", followers:"96K", avgLikes:"4.8K", avgComments:"210", sentiment:"Very positive on product aesthetics, frustrated on the mobile shopping experience"},
    mistake:"Poor mobile checkout experience: despite strong ad performance and desire (high engagement, ₹58L worth of abandoned carts), the mobile checkout flow was slow and cumbersome, causing the majority of interested, high-income mobile shoppers to abandon purchases right before payment.",
    clues:[
      "₹58L in abandoned cart value is nearly triple the ₹22L actually sold — demand clearly existed but didn't convert to cash.",
      "Multiple customer comments specifically describe checkout friction on mobile (freezing, too many steps), not product dissatisfaction.",
      "Engagement (6.2%) and CTR (1.6%) are strong and product sentiment is positive, isolating the failure point to post-click experience, not the ad or product itself."
    ],
    explanation:"Lumora's campaign successfully generated desire and traffic — the marketing itself worked. But a slow, multi-step, non-mobile-optimized checkout process created a bottleneck exactly where the money changes hands, since most of this audience was shopping on mobile. The mismatch between strong top-of-funnel performance and weak final conversion points directly to a broken checkout experience rather than a messaging or targeting problem.",
    improvements:[
      "Audit and rebuild the mobile checkout flow: fewer steps, guest checkout, saved payment options.",
      "Add cart-abandonment email/SMS recovery flows with a small incentive.",
      "Load-test the site for festive-season traffic spikes.",
      "Enable pinch-to-zoom and higher-res product images on mobile listings."
    ]
  },
  {
    company:"GreenPlate Foods", industry:"Packaged / Health Food",
    objective:"Build awareness and trial for a new low-sugar snack line.",
    audience:"Health-conscious parents and young professionals, 25-45.",
    channels:["TV Commercial","Print Ads","Sampling Booths"],
    budget:[{c:"TV Commercial",p:65},{c:"Print Ads",p:20},{c:"Sampling Booths",p:15}],
    metrics:{reach:"5.2M (TV GRP estimate)", ctr:"N/A", engagement:"N/A", conversions:"Trial rate 0.9%", sales:"₹9L vs ₹50L target"},
    comments:[
      "\"Saw the ad on TV but couldn't find it in any store near me.\"",
      "\"Went to 3 supermarkets, none stocked it, gave up looking.\"",
      "\"Cool ad, but is this even available yet or is it just a teaser?\""
    ],
    social:{platform:"Twitter/X", followers:"4.1K", avgLikes:"60", avgComments:"25", sentiment:"Curious but frustrated — 'where can I buy this' is the most common comment type"},
    mistake:"Awareness-distribution mismatch: the brand spent 65% of its budget on mass-reach TV advertising before securing adequate retail distribution, creating high awareness and demand that consumers could not act on because the product simply wasn't available on enough shelves.",
    clues:[
      "Reach is very high (5.2M) but trial rate is extremely low (0.9%), an unusual gap suggesting an access problem rather than an interest problem.",
      "Multiple independent customer comments describe visiting real stores and not finding the product.",
      "Only 15% of budget went to sampling/in-store activities that would typically pair with a distribution-limited launch."
    ],
    explanation:"GreenPlate ran a mass-awareness campaign (TV) at national scale before its supply chain and retail distribution could support the resulting demand. Consumers who saw the ad were willing to try the product but physically could not find it, wasting a large share of the media budget on stoking demand that had nowhere to go, while also risking long-term brand frustration ('all hype, no availability').",
    improvements:[
      "Sequence the rollout: build distribution city-by-city before scaling awareness spend to match.",
      "Shift initial spend toward hyperlocal awareness (in areas with confirmed stock) and sampling.",
      "Use a store-locator tool/QR code in the ad itself once distribution catches up.",
      "Communicate a clear launch timeline if distribution is still rolling out ('coming to your city soon')."
    ]
  },
  {
    company:"NovaTech Wireless Earbuds", industry:"Consumer Electronics",
    objective:"Launch a mid-range wireless earbuds model against established competitors.",
    audience:"Tech-savvy young adults, 18-32, value-for-money buyers.",
    channels:["YouTube Tech Reviewers","Amazon Ads","Twitter/X"],
    budget:[{c:"YouTube Tech Reviewers",p:70},{c:"Amazon Ads",p:20},{c:"Twitter/X",p:10}],
    metrics:{reach:"2.9M", ctr:"3.4%", engagement:"7.1%", conversions:"1.1%", sales:"3,400 units vs 20,000 target"},
    comments:[
      "\"The reviewer clearly said battery life was 'just okay', that stuck with me more than anything else.\"",
      "\"Everyone's praising the sound but the 4-hour battery is a dealbreaker for my daily commute.\"",
      "\"Nice earbuds but why launch now when the battery is worse than 2-year-old competitor models?\""
    ],
    social:{platform:"YouTube comments", followers:"N/A", avgLikes:"N/A", avgComments:"N/A", sentiment:"Positive on sound quality, consistently negative on battery life comparisons"},
    mistake:"Ignoring a known product weakness in messaging: the brand's own influencer campaign surfaced a clear, repeated criticism (weak battery life vs competitors) but marketing continued to emphasize sound quality without addressing or reframing the battery concern, letting a single weakness dominate purchase hesitation.",
    clues:[
      "CTR (3.4%) and engagement (7.1%) are strong, meaning the campaign successfully drove interest and curiosity.",
      "Conversion (1.1%) is far below what such strong upper-funnel numbers would predict, pointing to a decision-stage objection.",
      "Reviewer and customer comments consistently and specifically cite battery life as the reason for hesitation, not price or sound quality."
    ],
    explanation:"NovaTech's campaign was effective at creating awareness and curiosity, but it never adapted its messaging after reviewers and early customers flagged battery life as a genuine weak point. Repeated, consistent objections at the comment level are a strong signal marketing should address head-on (e.g., reframing with a fast-charging feature) rather than continue to push the same 'great sound' message, which left the objection unresolved for every subsequent viewer.",
    improvements:[
      "Directly address the battery concern in follow-up creative (e.g., highlight fast-charge features, or a case-based charging story).",
      "Offer a comparison chart that's honest about trade-offs but reframes them positively (e.g., lighter, better sound-per-rupee).",
      "Brief influencers to discuss real use-case battery scenarios rather than only lab specs.",
      "Consider a mid-cycle firmware/feature update to genuinely improve battery performance."
    ]
  },
  {
    company:"Sundrop Kids Apparel", industry:"Children's Fashion / E-commerce",
    objective:"Grow sales during back-to-school season.",
    audience:"Parents of children aged 5-14, middle income.",
    channels:["Facebook Ads","Google Shopping","WhatsApp Broadcast"],
    budget:[{c:"Facebook Ads",p:45},{c:"Google Shopping",p:35},{c:"WhatsApp Broadcast",p:20}],
    metrics:{reach:"640K", ctr:"1.9%", engagement:"4.4%", conversions:"2.6%", sales:"₹14L vs ₹28L target"},
    comments:[
      "\"Ordered size 8 based on their chart, it fit my 5-year-old, sizing makes zero sense.\"",
      "\"Returned two orders already because the fit was way off from what the size guide said.\"",
      "\"Cute clothes but I'm scared to order again after two bad size experiences.\""
    ],
    social:{platform:"Facebook", followers:"71K", avgLikes:"1.4K", avgComments:"180", sentiment:"Positive on design, strongly negative on sizing accuracy and return experience"},
    mistake:"Inaccurate sizing information driving returns and lost trust: the marketing and product pages promoted an outdated or inconsistent size chart, resulting in a high rate of returns and public complaints that suppressed repeat purchases and increased hesitancy among new back-to-school shoppers.",
    clues:[
      "Conversion (2.6%) is respectable, but sales still fall far short of target, suggesting revenue is being lost after purchase, not before.",
      "Comment sentiment is split: design praised, but sizing complaints are frequent and specific ('size 8 fit my 5-year-old').",
      "Return-driven comments appear repeatedly across independent customers, indicating a systemic sizing chart issue, not isolated incidents."
    ],
    explanation:"Sundrop's marketing did its job in generating interest and initial purchases, but a flawed or unclear sizing chart caused a wave of returns and public complaints right when back-to-school shoppers needed confidence the most. This is a case where the marketing funnel is healthy but a product-information gap (sizing) creates real revenue leakage and erodes trust for future campaigns.",
    improvements:[
      "Audit and correct the size chart with real garment measurements, not just age ranges.",
      "Add customer-submitted fit photos/reviews per size on product pages.",
      "Offer free size-exchange (not full return) to reduce friction and cost.",
      "Communicate the fix publicly to rebuild trust with parents who had bad experiences."
    ]
  },
  {
    company:"Skyline Coworking Spaces", industry:"Commercial Real Estate / Coworking",
    objective:"Fill unsold desks and private cabins across 5 new coworking centers.",
    audience:"Freelancers, startups, and small business teams, 24-45.",
    channels:["LinkedIn Ads","Google Search Ads","Cold Email"],
    budget:[{c:"LinkedIn Ads",p:50},{c:"Google Search Ads",p:35},{c:"Cold Email",p:15}],
    metrics:{reach:"320K", ctr:"1.2%", engagement:"3.1%", conversions:"0.8%", sales:"38 desks booked vs 300 target"},
    comments:[
      "\"Their landing page has a big form asking for company size, budget, and 6 other fields before I can even see pricing.\"",
      "\"Tried booking a tour but had to fill a long form and never heard back for 4 days.\"",
      "\"I just wanted to see prices per desk, not fill out a lead form.\""
    ],
    social:{platform:"LinkedIn", followers:"12K", avgLikes:"90", avgComments:"6", sentiment:"Neutral, low volume — main external complaint is lead-form friction and slow follow-up"},
    mistake:"High-friction lead capture with slow follow-up: the campaign drove qualified clicks (good CTR for LinkedIn/B2B) but funneled them into a long, gated lead form with no visible pricing, and follow-up from the sales team took days, causing serious drop-off at the consideration stage.",
    clues:[
      "CTR (1.2%) is solid for LinkedIn B2B ads, showing the targeting and ad copy attracted the right professional audience.",
      "Conversion (0.8%) is very low relative to that CTR, and 38 desks booked is far below the 300 target despite spend being spent as planned.",
      "Comments consistently describe an overly long lead form with no visible pricing and multi-day delays in sales follow-up."
    ],
    explanation:"Skyline succeeded at attracting the right B2B audience through LinkedIn and Search, but placed a heavy, opaque lead-capture form between an interested prospect and basic information like pricing, and then took days to follow up. For a considered but time-sensitive purchase like office space, this friction and delay caused prospects to look elsewhere before ever speaking to sales.",
    improvements:[
      "Publish transparent starting price ranges on the landing page instead of gating them behind a form.",
      "Shorten the lead form to 2-3 essential fields; use progressive profiling later.",
      "Set an SLA for sales follow-up (e.g., within 2 hours) and automate an instant confirmation email/booking calendar link.",
      "Add a self-serve 'book a tour' calendar to remove the human bottleneck."
    ]
  }
];

/* ============ STATE ============ */
let state = {
  screen:'title', // title, assignment, board, report
  theme: THEMES[0],
  caseIdx: null,
  lockerIds: [],
  solved: false,
  correctPick: null,
  showModal: false,
  playedCases: []
};

function pickNewCase(){
  let idx;
  const avail = CASES.map((_,i)=>i).filter(i=>!state.playedCases.includes(i));
  const pool = avail.length ? avail : CASES.map((_,i)=>i);
  idx = pool[Math.floor(Math.random()*pool.length)];
  state.caseIdx = idx;
  state.playedCases.push(idx);
  if(state.playedCases.length > CASES.length) state.playedCases = [idx];
  state.lockerIds = [];
  state.solved = false;
  state.correctPick = null;
  state.showModal = false;
}

/* ============ EVIDENCE CARD DEFS ============ */
function getEvidenceCards(kase){
  return [
    {id:'objective', type:'card', title:'Campaign Objective', body:kase.objective, tag:'Brief'},
    {id:'audience', type:'card', title:'Target Audience', body:kase.audience, tag:'Brief'},
    {id:'channels', type:'chips', title:'Marketing Channels', items:kase.channels, tag:'Strategy'},
    {id:'budget', type:'budget', title:'Budget Allocation', data:kase.budget, tag:'Strategy'},
    {id:'metrics', type:'metrics', title:'Campaign Metrics', data:kase.metrics, tag:'Data'},
    {id:'social', type:'social', title:'Social Performance', data:kase.social, tag:'Data'},
    {id:'c0', type:'sticky', title:'Customer Comment', body:kase.comments[0], tag:'Testimony'},
    {id:'c1', type:'sticky', title:'Customer Comment', body:kase.comments[1], tag:'Testimony'},
    {id:'c2', type:'sticky', title:'Customer Comment', body:kase.comments[2], tag:'Testimony'},
  ];
}

/* ============ RENDER HELPERS ============ */
function el(html){ const d = document.createElement('div'); d.innerHTML = html.trim(); return d.firstElementChild; }
function rot(seed){ return ((seed*37)%7 - 3).toFixed(1); }

/* ============ SCREENS ============ */
function renderTitle(){
  const s = document.createElement('div');
  s.className = 'screen title-wrap';
  s.innerHTML = `
    <div class="badge">🔍 Case File System v1.0</div>
    <h1 class="glow">Marketing Detective</h1>
    <p>Every campaign hides a mistake. Study the evidence, interrogate the metrics, and crack the case before the client loses more money.</p>
    <div class="theme-grid" id="themeGrid"></div>
    <button class="btn" id="startBtn">Accept Your First Case</button>
  `;
  const grid = s.querySelector('#themeGrid');
  THEMES.forEach((t,i)=>{
    const card = el(`
      <div class="theme-card ${t.id===state.theme.id?'selected':''}" data-id="${t.id}">
        <div class="swatch-row">
          <div class="swatch" style="background:${t.accent}"></div>
          <div class="swatch" style="background:${t.accent2}"></div>
        </div>
        <span>${t.name}</span>
      </div>`);
    card.addEventListener('click', ()=>{
      state.theme = t;
      applyTheme(t);
      grid.querySelectorAll('.theme-card').forEach(c=>c.classList.remove('selected'));
      card.classList.add('selected');
    });
    grid.appendChild(card);
  });
  s.querySelector('#startBtn').addEventListener('click', ()=>{
    pickNewCase();
    state.screen='assignment';
    render();
  });
  return s;
}

function renderAssignment(){
  const kase = CASES[state.caseIdx];
  const s = document.createElement('div');
  s.className = 'screen';
  s.innerHTML = `
    <div class="folder-wrap">
      <div class="stamp">CONFIDENTIAL</div>
      <div class="folder">
        <div class="case-label">Case File #${String(state.caseIdx+1).padStart(3,'0')}</div>
        <h2>${kase.company}</h2>
        <div class="industry">${kase.industry}</div>
        <div class="divider"></div>
        <div class="field-row">
          <div class="field"><label>Objective</label><div>${kase.objective}</div></div>
        </div>
        <div class="field-row">
          <div class="field"><label>Target Audience</label><div>${kase.audience}</div></div>
        </div>
        <div class="field-row">
          <div class="field"><label>Channels Used</label><div class="chips">${kase.channels.map(c=>`<span class="chip">${c}</span>`).join('')}</div></div>
        </div>
        <div class="divider"></div>
        <p style="font-size:13px; color:#6b5d42; font-style:italic;">The client suspects something went wrong. Your job: examine every piece of evidence on the board, then identify the single primary marketing mistake.</p>
        <div class="folder-actions">
          <button class="btn" id="openBoard">Open Investigation Board</button>
        </div>
      </div>
    </div>
  `;
  s.querySelector('#openBoard').addEventListener('click', ()=>{
    state.screen='board';
    render();
  });
  return s;
}

function renderBoard(){
  const kase = CASES[state.caseIdx];
  const cards = getEvidenceCards(kase);
  const s = document.createElement('div');
  s.className = 'screen board-screen';

  const progressPct = Math.round((state.lockerIds.length / cards.length) * 100);

  s.innerHTML = `
    <div class="board-header">
      <div>
        <h2>🕵️ Investigating: ${kase.company}</h2>
        <div class="hint">Drag evidence into the locker as you examine it. Examine everything before you solve the case.</div>
      </div>
      <div style="text-align:right;">
        <div class="progress-track"><div class="progress-fill" style="width:${progressPct}%"></div></div>
        <div class="hint" style="margin-top:4px;">${state.lockerIds.length} / ${cards.length} examined</div>
      </div>
    </div>
    <div class="cork" id="cork"></div>
    <div class="locker" id="locker">
      <div class="locker-title">🔒 Evidence Locker</div>
      <div class="locker-items" id="lockerItems"></div>
    </div>
    <div class="board-footer">
      <button class="btn ghost" id="backBtn">← Back to Case File</button>
      <button class="btn" id="solveBtn">Solve the Case</button>
    </div>
  `;

  const cork = s.querySelector('#cork');
  cards.forEach((card, i)=>{
    if(state.lockerIds.includes(card.id)) return;
    cork.appendChild(renderCard(card, i));
  });

  const lockerItems = s.querySelector('#lockerItems');
  if(state.lockerIds.length===0){
    lockerItems.innerHTML = `<div class="locker-empty">Drag evidence cards here once reviewed…</div>`;
  } else {
    state.lockerIds.forEach(id=>{
      const card = cards.find(c=>c.id===id);
      const mini = el(`<div class="chip" style="font-size:12px; padding:6px 12px;">✔ ${card.title}</div>`);
      lockerItems.appendChild(mini);
    });
  }

  const locker = s.querySelector('#locker');
  locker.addEventListener('dragover', e=>{ e.preventDefault(); locker.classList.add('dragover'); });
  locker.addEventListener('dragleave', ()=> locker.classList.remove('dragover'));
  locker.addEventListener('drop', e=>{
    e.preventDefault();
    locker.classList.remove('dragover');
    const id = e.dataTransfer.getData('text/plain');
    if(id && !state.lockerIds.includes(id)){
      state.lockerIds.push(id);
      render();
    }
  });

  s.querySelector('#backBtn').addEventListener('click', ()=>{ state.screen='assignment'; render(); });
  s.querySelector('#solveBtn').addEventListener('click', ()=>{ state.showModal = true; renderModal(); });

  return s;
}

function renderCard(card, i){
  let inner = '';
  const cls = ['card'];
  if(card.type==='sticky') cls.push('sticky');
  if(card.type==='budget' || card.type==='metrics' || card.type==='social') cls.push('');

  if(card.type==='card'){
    inner = `<h4>${card.title}</h4><div>${card.body}</div>`;
  } else if(card.type==='chips'){
    inner = `<h4>${card.title}</h4><div class="chips">${card.items.map(x=>`<span class="chip">${x}</span>`).join('')}</div>`;
  } else if(card.type==='budget'){
    inner = `<h4>${card.title}</h4>` + card.data.map(b=>`<div style="display:flex;justify-content:space-between;font-size:12px;margin-bottom:3px;"><span>${b.c}</span><b>${b.p}%</b></div>`).join('');
  } else if(card.type==='metrics'){
    inner = `<h4>${card.title}</h4><div class="metric-grid">` +
      Object.entries(card.data).map(([k,v])=>`<div>${cap(k)}<b>${v}</b></div>`).join('') + `</div>`;
  } else if(card.type==='social'){
    inner = `<h4>${card.title}</h4><div class="metric-grid">` +
      Object.entries(card.data).map(([k,v])=>`<div>${cap(k)}<b style="font-size:12px;">${v}</b></div>`).join('') + `</div>`;
  } else if(card.type==='sticky'){
    inner = `<h4>${card.title}</h4><div style="font-family:var(--font-hand); font-size:14px;">${card.body}</div>`;
  }

  const c = el(`<div class="${cls.join(' ')}" draggable="true" style="--r:${rot(i+1)}deg;"><div class="pin"></div>${inner}<div class="tag">${card.tag}</div></div>`);
  c.addEventListener('dragstart', e=>{
    e.dataTransfer.setData('text/plain', card.id);
    c.classList.add('dragging');
  });
  c.addEventListener('dragend', ()=> c.classList.remove('dragging'));
  return c;
}

function cap(k){
  return k.replace(/([A-Z])/g,' $1').replace(/^./,s=>s.toUpperCase())+': ';
}

/* ============ SOLVE MODAL ============ */
function buildOptions(kase){
  // build 4 options: 1 correct, 3 decoys pulled from other cases' mistakes
  const decoyPool = CASES.filter(c=>c!==kase).map(c=>shortMistake(c.mistake));
  shuffle(decoyPool);
  const decoys = decoyPool.slice(0,3);
  const correct = shortMistake(kase.mistake);
  const opts = shuffle([{text:correct, correct:true}, ...decoys.map(d=>({text:d, correct:false}))]);
  return opts;
}
function shortMistake(m){ return m.split(':')[0]; }
function shuffle(arr){ for(let i=arr.length-1;i>0;i--){ const j=Math.floor(Math.random()*(i+1)); [arr[i],arr[j]]=[arr[j],arr[i]]; } return arr; }

let currentOptions = null;

function renderModal(){
  const kase = CASES[state.caseIdx];
  if(!currentOptions || !state._modalCaseIdx || state._modalCaseIdx !== state.caseIdx){
    currentOptions = buildOptions(kase);
    state._modalCaseIdx = state.caseIdx;
  }
  let overlay = document.getElementById('overlay');
  if(overlay) overlay.remove();
  overlay = el(`
    <div class="overlay" id="overlay">
      <div class="modal">
        <h3>What is the primary marketing mistake?</h3>
        <p class="sub">Choose the single issue that best explains the campaign's core failure.</p>
        <div id="optionsWrap"></div>
        <div class="modal-actions">
          <button class="btn ghost" id="cancelModal">Cancel</button>
        </div>
      </div>
    </div>
  `);
  document.body.appendChild(overlay);
  const wrap = overlay.querySelector('#optionsWrap');
  currentOptions.forEach(opt=>{
    const btn = el(`<button class="option">${opt.text}</button>`);
    btn.addEventListener('click', ()=>{
      wrap.querySelectorAll('.option').forEach(b=>b.disabled=true);
      currentOptions.forEach((o,idx)=>{
        const b = wrap.children[idx];
        if(o.correct) b.classList.add('correct');
        else if(o===opt) b.classList.add('wrong');
      });
      state.correctPick = opt.correct;
      setTimeout(()=>{
        overlay.remove();
        state.solved = true;
        state.screen='verdict';
        render();
      }, 1100);
    });
    wrap.appendChild(btn);
  });
  overlay.querySelector('#cancelModal').addEventListener('click', ()=> overlay.remove());
}

/* ============ VERDICT SCREEN ============ */
function renderVerdict(){
  const kase = CASES[state.caseIdx];
  const s = document.createElement('div');
  s.className = 'screen verdict-screen';
  const win = state.correctPick;
  s.innerHTML = `
    <div class="stamp-big ${win?'win':'lose'}">${win ? 'CASE SOLVED' : 'CASE MISSED'}</div>
    <h2 style="margin-bottom:10px;">${win ? 'Sharp instincts, detective.' : 'Close, but not quite.'}</h2>
    <p style="color:var(--text-dim); max-width:520px; margin-bottom:26px;">
      ${win ? ('You correctly identified the core marketing failure behind ' + kase.company + "'s underperformance.") : ('The real culprit behind ' + kase.company + "'s underperformance was different. Review the full breakdown in the learning report.")}
    </p>
    <button class="btn" id="toReport">View Learning Report</button>
  `;
  s.querySelector('#toReport').addEventListener('click', ()=>{ state.screen='report'; render(); });
  return s;
}

/* ============ LEARNING REPORT ============ */
function renderReport(){
  const kase = CASES[state.caseIdx];
  const s = document.createElement('div');
  s.className = 'screen report-wrap';

  // fake bar chart data derived from metrics for visual flair
  const barVals = [72, 38, 91, 24].map(v=>v); // reach, ctr-ish, engagement-ish, conversion-ish (illustrative)

  s.innerHTML = `
    <h2 style="margin-bottom:18px; text-align:center;">📋 Marketing Learning Report<span class="score-pill">${state.correctPick?'VERDICT: CORRECT':'VERDICT: INCORRECT'}</span></h2>

    <div class="report-card">
      <h3>Primary Marketing Mistake</h3>
      <p>${kase.mistake}</p>
    </div>

    <div class="report-card">
      <h3>Supporting Clues</h3>
      <div class="clue-list">
        ${kase.clues.map(c=>`<div class="clue-item">${c}</div>`).join('')}
      </div>
    </div>

    <div class="report-card">
      <h3>Full Explanation</h3>
      <p>${kase.explanation}</p>
    </div>

    <div class="report-card">
      <h3>Suggested Improvements</h3>
      <ul>${kase.improvements.map(i=>`<li>${i}</li>`).join('')}</ul>
    </div>

    <div class="report-card">
      <h3>Performance Snapshot</h3>
      <div class="chart-bars">
        ${['Reach','CTR/Interest','Engagement','Conversion'].map((label,i)=>`
          <div class="bar-col">
            <div class="bar" style="height:${barVals[i]}%"></div>
            <div class="bar-label">${label}</div>
          </div>`).join('')}
      </div>
    </div>

    <div class="final-actions">
      <button class="btn ghost" id="replaySame">Review Case Again</button>
      <button class="btn" id="nextCase">Accept New Case</button>
    </div>
  `;

  s.querySelector('#replaySame').addEventListener('click', ()=>{ state.screen='assignment'; state.lockerIds=[]; state.solved=false; render(); });
  s.querySelector('#nextCase').addEventListener('click', ()=>{ pickNewCase(); currentOptions=null; state.screen='assignment'; render(); });

  return s;
}

/* ============ MAIN RENDER ============ */
function render(){
  applyTheme(state.theme);
  const app = document.getElementById('app');
  app.innerHTML = '';
  let node;
  switch(state.screen){
    case 'title': node = renderTitle(); break;
    case 'assignment': node = renderAssignment(); break;
    case 'board': node = renderBoard(); break;
    case 'verdict': node = renderVerdict(); break;
    case 'report': node = renderReport(); break;
    default: node = renderTitle();
  }
  app.appendChild(node);
  window.scrollTo({top:0, behavior:'smooth'});
}

applyTheme(state.theme);
render();
})();
</script>
</body>
</html>
