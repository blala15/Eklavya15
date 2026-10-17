<!DOCTYPE html>
<html lang="en"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Eklavya – Waste to Energy</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
<style>
:root{--bg:#f4f8f1;--card:rgba(255,255,255,.75);--tx:#10261a;--mut:#4b6355;--ac:#0f9d58;--ac2:#f59e0b;--bd:rgba(15,157,88,.2);box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#07140d;--card:rgba(20,45,32,.7);--tx:#e8f6ec;--mut:#9bb8a5;--bd:rgba(80,220,140,.18)}}
:root[data-theme="dark"]{--bg:#07140d;--card:rgba(20,45,32,.7);--tx:#e8f6ec;--mut:#9bb8a5;--bd:rgba(80,220,140,.18)}
*{box-sizing:border-box}html{scroll-behavior:smooth;scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;font-family:Poppins,"Noto Sans Devanagari",system-ui,sans-serif;background:var(--bg);color:var(--tx);background-image:radial-gradient(circle at 15% 0,rgba(15,157,88,.25),transparent 40%),radial-gradient(circle at 90% 20%,rgba(245,158,11,.22),transparent 35%);background-attachment:fixed}
header{position:sticky;top:env(safe-area-inset-top,0px);z-index:20;display:flex;align-items:center;gap:10px;padding:10px 5vw;background:var(--card);backdrop-filter:blur(14px);border-bottom:1px solid var(--bd)}
.brand{display:flex;align-items:center;gap:10px;font-weight:800;font-size:1.3rem;margin-right:auto}
.brand small{display:block;font-weight:400;font-size:.62rem;color:var(--mut);letter-spacing:.5px}
button{font:inherit;cursor:pointer;border:0;border-radius:999px;padding:9px 18px;background:linear-gradient(135deg,var(--ac),#0b7a45);color:#fff;font-weight:600;transition:.2s}
button:hover{transform:translateY(-2px);box-shadow:0 6px 18px rgba(15,157,88,.4)}
button.g{background:transparent;color:var(--tx);border:1px solid var(--bd)}
.hero{text-align:center;padding:9vh 5vw 5vh;max-width:900px;margin:auto}
.hero h1{font-size:clamp(2rem,6vw,3.8rem);line-height:1.1;margin:.3em 0;background:linear-gradient(90deg,var(--ac),var(--ac2));-webkit-background-clip:text;background-clip:text;color:transparent}
.hero p{color:var(--mut);font-size:1.1rem}
.flame{animation:fl 2.4s ease-in-out infinite;transform-origin:50% 100%}@keyframes fl{50%{transform:scale(1.08,1.15)}}
.stats{display:flex;flex-wrap:wrap;gap:12px;justify-content:center;margin-top:24px}
.stats div{background:var(--card);border:1px solid var(--bd);border-radius:16px;padding:12px 20px}.stats b{display:block;font-size:1.5rem;color:var(--ac)}
section{max-width:1050px;margin:0 auto;padding:30px 5vw}
h2{font-size:1.8rem;margin:0 0 14px}
.card{background:var(--card);backdrop-filter:blur(12px);border:1px solid var(--bd);border-radius:24px;padding:24px;box-shadow:0 10px 40px rgba(0,0,0,.08)}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}@media(max-width:760px){.grid{grid-template-columns:1fr}}
input,select{width:100%;padding:12px 14px;border-radius:14px;border:1px solid var(--bd);background:var(--bg);color:var(--tx);font:inherit;margin:6px 0}
select[size]{height:220px;padding:6px}
.chips{display:flex;gap:8px;flex-wrap:wrap;margin:8px 0}.chips button{padding:6px 14px;font-size:.85rem}.chips button.on{background:var(--ac2);color:#2a1b00}
.res{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:10px}
.res div{background:var(--bg);border:1px solid var(--bd);border-radius:16px;padding:12px}.res b{display:block;font-size:1.35rem;color:var(--ac)}.res span{font-size:.78rem;color:var(--mut)}
.big{grid-column:1/-1;background:linear-gradient(135deg,var(--ac),#0b7a45)!important;color:#fff}.big b,.big span{color:#fff!important}.big b{font-size:2.2rem}
.note{font-size:.85rem;color:var(--mut);margin-top:10px}
.steps{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px}.steps .card{padding:18px}.steps i{font-size:2rem;font-style:normal}
#chatBtn{position:fixed;right:18px;bottom:calc(18px + env(safe-area-inset-bottom,0px));z-index:30;width:60px;height:60px;padding:0;font-size:1.6rem}
#chat{position:fixed;right:18px;bottom:calc(88px + env(safe-area-inset-bottom,0px));width:min(360px,92vw);height:460px;z-index:30;display:none;flex-direction:column;background:var(--bg);border:1px solid var(--bd);border-radius:22px;overflow:hidden;box-shadow:0 20px 60px rgba(0,0,0,.35)}
#chat.o{display:flex}#chat h4{margin:0;padding:14px;background:linear-gradient(135deg,var(--ac),#0b7a45);color:#fff}
#msgs{flex:1;overflow:auto;padding:12px;display:flex;flex-direction:column;gap:8px}
.m{padding:9px 13px;border-radius:16px;max-width:85%;font-size:.9rem;line-height:1.4}.m.b{background:var(--card);border:1px solid var(--bd)}.m.u{background:var(--ac);color:#fff;align-self:flex-end}
#chat form{display:flex;gap:6px;padding:10px;border-top:1px solid var(--bd)}#chat input{margin:0}
#modal{position:fixed;inset:0;background:rgba(0,0,0,.55);display:none;place-items:center;z-index:40}#modal.o{display:grid}
#modal .card{width:min(400px,92vw);background:var(--bg)}
footer{text-align:center;color:var(--mut);padding:30px;font-size:.85rem}
nav{display:flex;gap:16px;margin-right:6px}nav a{color:var(--tx);text-decoration:none;font-size:.9rem;font-weight:600}nav a:hover{color:var(--ac)}@media(max-width:980px){nav{display:none}}
.price{font-size:2.8rem;font-weight:800;background:linear-gradient(90deg,var(--ac),var(--ac2));-webkit-background-clip:text;background-clip:text;color:transparent}
.specs{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:10px}.specs div{background:var(--bg);border:1px solid var(--bd);border-radius:14px;padding:10px 14px}.specs span{display:block;font-size:.75rem;color:var(--mut)}.specs b{font-size:.92rem}
textarea{width:100%;padding:12px 14px;border-radius:14px;border:1px solid var(--bd);background:var(--bg);color:var(--tx);font:inherit;margin:6px 0;min-height:80px}
details{background:var(--bg);border:1px solid var(--bd);border-radius:14px;padding:10px 14px;margin:8px 0}summary{cursor:pointer;font-weight:600}details p{margin:8px 0 0;color:var(--mut);font-size:.9rem}
.tot{font-size:1.5rem;font-weight:800;color:var(--ac)}.ok{color:var(--ac);font-weight:600;margin-top:10px}.ct{display:flex;gap:10px;align-items:center;margin:6px 0}.ct i{font-style:normal;font-size:1.4rem}
</style></head><body>
<header>
<div class="brand"><svg width="44" height="44" viewBox="0 0 64 64"><defs><linearGradient id="lg" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#0f9d58"/><stop offset="1" stop-color="#f59e0b"/></linearGradient></defs><circle cx="32" cy="32" r="30" fill="url(#lg)"/><path d="M20 12Q50 32 20 52" fill="none" stroke="#fff" stroke-width="3" stroke-linecap="round"/><path d="M20 32H52M46 26l6 6-6 6" fill="none" stroke="#fff" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/><path class="flame" d="M30 44c-6-4-4-10 0-14 0 4 3 5 4 3 2-3 1-6-1-8 7 2 10 9 7 15-2 4-7 6-10 4z" fill="#fff" opacity=".92"/></svg><div>Eklavya<small data-t="tag"></small></div></div>
<nav><a href="#calc" data-t="calc0"></a><a href="#machine" data-t="nMach"></a><a href="#order" data-t="nOrder"></a><a href="#support" data-t="nSup"></a></nav>
<button class="g" id="theme" aria-label="theme">◐</button>
<button class="g" id="lang">हिन्दी</button>
<button id="auth" data-t="login"></button>
</header>

<div class="hero"><h1 data-t="h1"></h1><p data-t="sub"></p>
<button onclick="document.getElementById('calc').scrollIntoView()" data-t="cta"></button>
<div class="stats"><div><b id="cnt">0</b><span data-t="s1"></span></div><div><b>70%</b><span data-t="s2"></span></div><div><b>0</b><span data-t="s3"></span></div></div></div>

<section id="calc"><h2 data-t="calc"></h2>
<div class="card grid"><div>
<div class="chips" id="chips"></div>
<input id="q" data-ph="search" autocomplete="off">
<select id="list" size="8"></select>
<label data-t="kg"></label><input id="kg" type="number" min="0" step="any" value="100">
</div><div><div class="res" id="out"></div><p class="note" id="note"></p></div></div></section>

<section><h2 data-t="how"></h2><div class="steps" id="steps"></div></section>

<section id="machine"><h2 data-t="mTitle"></h2>
<div class="card grid"><div><svg viewBox="0 0 320 200" width="100%" role="img" aria-label="Eklavya-10"><defs><linearGradient id="mg" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#0f9d58"/><stop offset="1" stop-color="#0b7a45"/></linearGradient></defs><rect x="6" y="150" width="308" height="34" rx="8" fill="#334155"/><path d="M20 40h70l-14 40H34z" fill="#f59e0b"/><rect x="34" y="80" width="42" height="70" rx="6" fill="url(#mg)"/><rect x="110" y="60" width="56" height="90" rx="10" fill="url(#mg)"/><path class="flame" d="M138 140c-14-8-9-24 0-32 0 9 6 11 9 6 4-6 2-12-2-17 15 4 22 20 15 33-4 8-15 12-22 10z" fill="#fbbf24"/><rect x="184" y="90" width="36" height="60" rx="6" fill="#475569"/><rect x="236" y="70" width="70" height="80" rx="10" fill="#0b7a45"/><path d="M276 82l-14 26h12l-6 28 20-34h-13l8-20z" fill="#fde047"/><path d="M76 120h34M166 120h18M220 120h16" stroke="#94a3b8" stroke-width="5"/></svg></div>
<div><div class="price">₹20,00,000</div><p class="note" data-t="mPer"></p><p data-t="mDesc"></p><button data-go="order" data-t="orderNow"></button></div></div>
<div class="card" style="margin-top:20px"><h3 data-t="specs"></h3><div class="specs" id="specs"></div><p class="note" data-t="mNote"></p></div></section>

<section id="order"><h2 data-t="oTitle"></h2><div class="card"><form id="oForm" class="grid"><div><input id="oName" data-ph="name" required><input id="oPhone" type="tel" data-ph="phone" required><input id="oEmail" type="email" data-ph="email" required><select id="oOrg"></select><input id="oCity" data-ph="city" required></div><div><textarea id="oAddr" data-ph="addr"></textarea><label data-t="qty"></label><input id="oQty" type="number" min="1" max="50" value="1"><select id="oPay"></select><div><span class="note" data-t="total"></span> <span class="tot" id="oTotal"></span></div><button style="width:100%;margin-top:10px" data-t="place"></button><p class="ok" id="oMsg"></p></div></form></div></section>

<section id="support"><h2 data-t="sTitle"></h2><div class="card grid"><div><div class="ct"><i>📞</i><div><b>1800-000-0000</b><br><span class="note" data-t="hours"></span></div></div><div class="ct"><i>✉️</i><b>support@eklavya.example</b></div><div class="ct"><i>💬</i><b data-t="chatus"></b></div><h3 data-t="faqT"></h3><div id="faq"></div></div>
<form id="tForm"><h3 data-t="ticket"></h3><input id="tEmail" type="email" data-ph="email" required><select id="tCat"></select><textarea id="tMsg" data-ph="tmsg" required></textarea><button style="width:100%" data-t="send"></button><p class="ok" id="tOut"></p></form></div></section>
<footer>© 2026 Eklavya · <span data-t="foot"></span></footer>

<button id="chatBtn" aria-label="chat">💬</button>
<div id="chat"><h4 data-t="bot"></h4><div id="msgs"></div><form id="cf"><input id="ci" data-ph="ask" autocomplete="off"><button>➤</button></form></div>
<div id="modal"><div class="card"><h2 id="mt"></h2><form id="af"><input id="nm" data-ph="name"><input id="em" type="email" data-ph="email" required><input id="pw" type="password" data-ph="pass" required minlength="4"><button style="width:100%" id="sub"></button><p class="note" id="msg"></p></form><button class="g" id="sw" style="width:100%"></button><button class="g" id="cl" style="width:100%;margin-top:8px">✕</button></div></div>

<script>
const T={en:{tag:"WASTE → ENERGY",login:"Login / Sign up",logout:"Logout",h1:"Turning waste into clean power for every home",sub:"A modular thermochemical gasifier converts dry municipal and farm waste into syngas, driving a micro-generator for off-grid electricity in informal settlements.",cta:"Calculate energy",s1:"waste types",s2:"gasifier efficiency",s3:"grid needed",calc:"Waste-to-Electricity Calculator",kg:"Weight of waste (kg)",how:"How Eklavya works",foot:"Clean energy for all",bot:"Eklavya Assistant",search:"Search 1000+ waste types…",ask:"Ask me anything…",name:"Name",email:"Email",pass:"Password",signup:"Create account",in:"Login",toSign:"New here? Sign up",toLog:"Have an account? Login",hi:"Hello",elec:"Electricity",syn:"Syngas (Nm³)",hh:"Homes powered (1 day)",led:"LED bulb hours (10 W)",run:"Run-time on 5 kW unit (h)",ash:"Biochar/ash (kg)",rec:"Energy saved by recycling",all:"All",F:"Farm",M:"Municipal",X:"Metals",nometal:"Metals do not burn, so gasification produces 0 kWh. Sell them to recyclers: recycling saves the energy shown above, far more than any fuel value.",est:"Estimates: gasifier 70% cold-gas efficiency, syngas engine 28%. Real output varies.",ok:"Welcome!",bad:"Wrong email or password",exists:"Account already exists",steps:[["🚯","Collect","Local youth collect dry waste door to door."],["✂️","Dry & shred","Sun-dry and shred to cut moisture below 15%."],["🔥","Gasify","Oxygen-limited thermochemical conversion gives syngas."],["⚡","Generate","A micro-generator turns syngas into electricity."]],chips:["How does it work?","Can iron burn?","Is plastic safe?","How much power?"],hello:"Namaste! I am the Eklavya assistant. Ask about gasification, waste types or the calculator.",def:"I can explain gasification, which wastes give most energy, metals, safety, and how to use the calculator. Try one of those!"},
hi:{tag:"कचरे से ऊर्जा",login:"लॉगिन / साइन अप",logout:"लॉगआउट",h1:"कचरे से हर घर के लिए स्वच्छ बिजली",sub:"मॉड्यूलर थर्मोकेमिकल गैसीफायर सूखे शहरी और खेती के कचरे को सिनगैस में बदलता है, जो माइक्रो-जनरेटर चलाकर झुग्गी बस्तियों को ऑफ-ग्रिड बिजली देता है।",cta:"ऊर्जा निकालें",s1:"कचरे के प्रकार",s2:"गैसीफायर दक्षता",s3:"ग्रिड की ज़रूरत",calc:"कचरे से बिजली कैलकुलेटर",kg:"कचरे का वज़न (किलो)",how:"एकलव्य कैसे काम करता है",foot:"सबके लिए स्वच्छ ऊर्जा",bot:"एकलव्य सहायक",search:"1000+ कचरा प्रकार खोजें…",ask:"कुछ भी पूछें…",name:"नाम",email:"ईमेल",pass:"पासवर्ड",signup:"खाता बनाएँ",in:"लॉगिन",toSign:"नए हैं? साइन अप करें",toLog:"खाता है? लॉगिन करें",hi:"नमस्ते",elec:"बिजली",syn:"सिनगैस (Nm³)",hh:"घर रोशन (1 दिन)",led:"LED बल्ब घंटे (10 W)",run:"5 kW यूनिट चलने का समय (घं.)",ash:"बायोचार/राख (किलो)",rec:"रीसाइक्लिंग से बचत ऊर्जा",all:"सभी",F:"खेती",M:"शहरी",X:"धातु",nometal:"धातुएँ जलती नहीं, इसलिए गैसीफिकेशन से 0 kWh मिलता है। इन्हें कबाड़ी को बेचें: रीसाइक्लिंग से ऊपर दिखाई ऊर्जा बचती है।",est:"अनुमान: गैसीफायर दक्षता 70%, सिनगैस इंजन 28%। वास्तविक उत्पादन अलग हो सकता है।",ok:"स्वागत है!",bad:"ईमेल या पासवर्ड गलत है",exists:"खाता पहले से मौजूद है",steps:[["🚯","संग्रह","स्थानीय युवा घर-घर से सूखा कचरा इकट्ठा करते हैं।"],["✂️","सुखाएँ व काटें","धूप में सुखाकर नमी 15% से कम करें।"],["🔥","गैसीफिकेशन","कम ऑक्सीजन में थर्मोकेमिकल प्रक्रिया से सिनगैस बनती है।"],["⚡","बिजली","माइक्रो-जनरेटर सिनगैस से बिजली बनाता है।"]],chips:["यह कैसे काम करता है?","क्या लोहा जल सकता है?","क्या प्लास्टिक सुरक्षित है?","कितनी बिजली?"],hello:"नमस्ते! मैं एकलव्य सहायक हूँ। गैसीफिकेशन, कचरे के प्रकार या कैलकुलेटर के बारे में पूछें।",def:"मैं गैसीफिकेशन, सबसे ज़्यादा ऊर्जा देने वाले कचरे, धातु, सुरक्षा और कैलकुलेटर के बारे में बता सकता हूँ।"}};
// base: en|hi|cat|dryLHV MJ/kg (metals: recycling MJ/kg saved)
const B=`Rice straw|धान का पुआल|F|15
Wheat straw|गेहूं का भूसा|F|17
Rice husk|धान की भूसी|F|15.5
Sugarcane bagasse|गन्ने की खोई|F|17.5
Sugarcane trash|गन्ने की पत्तियाँ|F|16
Corn stalk|मक्का का डंठल|F|17
Corn cob|मक्का का भुट्टा|F|17.5
Cotton stalk|कपास की डंडी|F|18
Mustard stalk|सरसों का डंठल|F|17.5
Groundnut shell|मूंगफली का छिलका|F|18.5
Coconut shell|नारियल का खोल|F|20
Coconut husk|नारियल की जटा|F|18
Coir pith|नारियल का बुरादा|F|18
Jute stick|जूट की लकड़ी|F|18
Banana stem|केले का तना|F|15
Soybean straw|सोयाबीन का भूसा|F|17
Pigeon pea stalk|अरहर की डंडी|F|18
Sorghum stalk|ज्वार का डंठल|F|17
Millet stalk|बाजरा का डंठल|F|17
Barley straw|जौ का भूसा|F|17
Sunflower stalk|सूरजमुखी का डंठल|F|17.5
Tea waste|चाय का कचरा|F|18
Coffee husk|कॉफी की भूसी|F|17
Cashew shell|काजू का छिलका|F|22
Palm kernel shell|पाम गुठली का खोल|F|20
Mango seed|आम की गुठली|F|18
Water hyacinth|जलकुंभी|F|14
Cow dung cake|उपला (गोबर)|F|15
Poultry litter|मुर्गी की बीट|F|14
Sawdust|लकड़ी का बुरादा|F|18.5
Wood chips|लकड़ी के टुकड़े|F|19
Bamboo waste|बांस का कचरा|F|18
Tree prunings|पेड़ की छंटाई|F|18.5
Dry leaves|सूखे पत्ते|F|16
Grass clippings|घास की कतरन|F|16
Vegetable waste|सब्जी का कचरा|F|15
Fruit peels|फलों के छिलके|F|16
Rice bran|चावल का चोकर|F|17
Oil cake|खली|F|19
Jatropha cake|जटरोफा खली|F|20
Food leftovers|बचा खाना|M|19
Paper|कागज़|M|16.5
Cardboard|गत्ता|M|16
Newspaper|अखबार|M|17
Cotton cloth|सूती कपड़ा|M|16.5
Jute sack|बोरी|M|17
Wooden furniture scrap|लकड़ी का फर्नीचर|M|18
Leather scraps|चमड़े के टुकड़े|M|18
Rubber|रबर|M|30
Tyres|टायर|M|32
HDPE plastic|HDPE प्लास्टिक|M|43
Polythene bags|पॉलीथिन थैली|M|43
PP plastic|PP प्लास्टिक|M|44
PET bottles|PET बोतल|M|23
Thermocol foam|थर्मोकोल|M|40
Snack packets|चिप्स के पैकेट|M|30
Diapers|डायपर|M|20
Dry mixed household waste|सूखा मिश्रित कचरा|M|15
Cigarette butts|सिगरेट के टुकड़े|M|17
Old sandals|पुरानी चप्पल|M|28
Foam mattress|फोम गद्दा|M|26
Synthetic cloth|सिंथेटिक कपड़ा|M|22
Plastic toys|प्लास्टिक खिलौने|M|38
Cable insulation|तार का प्लास्टिक कवर|M|25
Steel scrap|स्टील कबाड़|X|11
Iron scrap|लोहा कबाड़|X|10
Cast iron|ढलवां लोहा|X|10
Tin cans|टिन के डिब्बे|X|11
Iron nails|लोहे की कीलें|X|10
Rebar|सरिया|X|11
Steel utensils|स्टील के बर्तन|X|12
Tin roof sheets|टीन की चादर|X|10
Stainless steel|स्टेनलेस स्टील|X|15
Galvanized iron|गैल्वनाइज़्ड लोहा|X|10
Iron wire mesh|लोहे की जाली|X|10
Metal bottle caps|धातु के ढक्कन|X|11
Aluminium cans|एल्युमिनियम कैन|X|190
Copper wire|तांबे का तार|X|70
Brass scrap|पीतल कबाड़|X|60
Iron pipes|लोहे के पाइप|X|10`.split('\n').map(l=>{const[a,b,c,d]=l.split('|');return{a,b,c,l:+d}});
// variants: en, hi, moisture, lhv factor
const V=[["sun-dried","धूप में सूखा",.10,1],["air-dry","हवा में सूखा",.15,1],["shredded","कतरा हुआ",.12,1],["chopped","कटा हुआ",.20,1],["baled","गठरी",.15,1],["pelletized","पेलेट",.08,1],["briquetted","ब्रिकेट",.08,1],["powdered","पाउडर",.10,1],["damp","नम",.35,1],["fresh/wet","गीला",.55,1],["rain-soaked","बारिश में भीगा",.65,1],["mixed with soil","मिट्टी मिला",.15,.8],["part-burnt","अधजला",.05,.9]];
const items=[];B.forEach(b=>V.forEach(v=>items.push({en:b.a+" – "+v[0],hi:b.b+" – "+v[1],c:b.c,l:b.l*v[3],m:v[2]})));
let lang="en",cat="all",user=null,mode="login";const $=i=>document.getElementById(i),t=k=>T[lang][k];
try{lang=localStorage.getItem("ek_l")||"en";user=JSON.parse(localStorage.getItem("ek_u")||"null")}catch(e){}
const fmt=n=>n>=100?n.toFixed(0):n>=1?n.toFixed(1):n.toFixed(2);
function calc(it,kg){if(it.c=="X"){const k=kg*it.l/3.6;return{x:1,rec:k}}
const net=Math.max(0,it.l*(1-it.m)-2.44*it.m),sg=kg*net*.7,e=sg/3.6*.28;return{e,syn:sg/4.8,ash:kg*(1-it.m)*.1}}
function render(){const q=$("q").value.toLowerCase();const f=items.filter(i=>(cat=="all"||i.c==cat)&&(i.en+i.hi).toLowerCase().includes(q));
const sel=$("list").value;$("list").innerHTML=f.slice(0,300).map(i=>`<option value="${items.indexOf(i)}">${i[lang]}</option>`).join("");
$("list").value=sel&&f.some(i=>items.indexOf(i)==sel)?sel:(f[0]?items.indexOf(f[0]):"");result()}
function result(){const it=items[$("list").value],kg=Math.max(0,+$("kg").value||0);if(!it){$("out").innerHTML="";return}
const r=calc(it,kg);let h="";
if(r.x){h=`<div class="big"><b>0 kWh</b><span>${t("elec")}</span></div><div class="big" style="background:linear-gradient(135deg,#f59e0b,#c2410c)!important"><b>${fmt(r.rec)} kWh</b><span>${t("rec")}</span></div>`;$("note").textContent=t("nometal")}
else{h=`<div class="big"><b>${fmt(r.e)} kWh</b><span>${t("elec")}</span></div><div><b>${fmt(r.syn)}</b><span>${t("syn")}</span></div><div><b>${fmt(r.e/1.5)}</b><span>${t("hh")}</span></div><div><b>${fmt(r.e*100)}</b><span>${t("led")}</span></div><div><b>${fmt(r.e/5)}</b><span>${t("run")}</span></div><div><b>${fmt(r.ash)}</b><span>${t("ash")}</span></div>`;$("note").textContent=t("est")}
$("out").innerHTML=h}
function ui(){document.documentElement.lang=lang;document.querySelectorAll("[data-t]").forEach(e=>e.textContent=t(e.dataset.t));document.querySelectorAll("[data-ph]").forEach(e=>e.placeholder=t(e.dataset.ph));
$("lang").textContent=lang=="en"?"हिन्दी":"English";$("auth").textContent=user?`${t("hi")}, ${user.n} · ${t("logout")}`:t("login");
$("chips").innerHTML=["all"].map(c=>`<button class="${c==cat?"on":""}" data-c="${c}">${t(c)}</button>`).join("");
$("steps").innerHTML=t("steps").map((s,i)=>`<div class="card"><i>${s[0]}</i><h3>${i+1}. ${s[1]}</h3><p class="note">${s[2]}</p></div>`).join("");
$("cnt").textContent=items.length.toLocaleString();authUI();render()}
function authUI(){$("mt").textContent=mode=="login"?t("in"):t("signup");$("sub").textContent=mode=="login"?t("in"):t("signup");$("sw").textContent=mode=="login"?t("toSign"):t("toLog");$("nm").style.display=mode=="login"?"none":"block"}
$("chips").onclick=e=>{if(e.target.dataset.c){cat=e.target.dataset.c;ui()}};
$("q").oninput=render;$("list").onchange=result;$("kg").oninput=result;
$("lang").onclick=()=>{lang=lang=="en"?"hi":"en";try{localStorage.setItem("ek_l",lang)}catch(e){}ui();$("msgs").innerHTML="";bot(t("hello"),1)};
$("theme").onclick=()=>{const r=document.documentElement,d=getComputedStyle(r).getPropertyValue("--bg").trim()=="#07140d";r.dataset.theme=d?"light":"dark"};
// auth (demo only: stored in this browser)
$("auth").onclick=()=>{if(user){user=null;try{localStorage.removeItem("ek_u")}catch(e){}ui()}else{$("modal").classList.add("o");authUI()}};
$("cl").onclick=()=>$("modal").classList.remove("o");$("sw").onclick=()=>{mode=mode=="login"?"signup":"login";authUI()};
$("af").onsubmit=e=>{e.preventDefault();let us={};try{us=JSON.parse(localStorage.getItem("ek_us")||"{}")}catch(x){}
const em=$("em").value.trim().toLowerCase(),pw=btoa(unescape(encodeURIComponent($("pw").value)));
if(mode=="signup"){if(us[em]){$("msg").textContent=t("exists");return}us[em]={n:$("nm").value||em.split("@")[0],p:pw};try{localStorage.setItem("ek_us",JSON.stringify(us))}catch(x){}}
else if(!us[em]||us[em].p!=pw){$("msg").textContent=t("bad");return}
user={n:us[em].n};try{localStorage.setItem("ek_u",JSON.stringify(user))}catch(x){}$("msg").textContent=t("ok");setTimeout(()=>{$("modal").classList.remove("o");$("msg").textContent="";ui()},500)};
// chatbot
const KB=[[/iron|steel|metal|लोहा|स्टील|धातु|aluminium/i,"Metals like iron and steel don’t burn in a gasifier, so they give 0 kWh. Sell them to recyclers: recycling steel or aluminium saves a lot of energy, shown in the calculator.","लोहा और स्टील गैसीफायर में नहीं जलते, इसलिए 0 kWh मिलता है। इन्हें कबाड़ी को बेचें; रीसाइक्लिंग से काफी ऊर्जा बचती है।"],
[/plastic|pvc|प्लास्टिक/i,"Plastics have high energy (PE/PP ~43 MJ/kg) but need hot, controlled gasification and gas cleaning. Avoid PVC (releases chlorine). Never burn plastic openly.","प्लास्टिक में ऊर्जा ज़्यादा होती है पर नियंत्रित गर्मी और गैस सफाई चाहिए। PVC से बचें और प्लास्टिक कभी खुले में न जलाएँ।"],
[/how|work|gasif|syngas|कैसे|गैस/i,"Dry waste is heated with limited oxygen (~800–1000 °C). It breaks down into syngas (CO, H₂, CH₄) that fuels a micro-generator. Ash/biochar is left over.","सूखा कचरा सीमित ऑक्सीजन में 800–1000 °C तक गर्म होता है और सिनगैस (CO, H₂, CH₄) बनती है जो माइक्रो-जनरेटर चलाती है। बचा हुआ बायोचार/राख होता है।"],
[/power|kwh|electric|energy|बिजली|ऊर्जा|कितनी/i,"Roughly 1 kg of dry biomass gives 0.8–1.2 kWh of electricity. Wet waste gives much less, so dry it first. Use the calculator for exact estimates.","लगभग 1 किलो सूखा बायोमास 0.8–1.2 kWh बिजली देता है। गीला कचरा कम देता है, पहले सुखाएँ। सटीक अनुमान के लिए कैलकुलेटर देखें।"],
[/wet|moist|dry|नमी|गीला|सूखा/i,"Moisture below 15% is best. Water absorbs heat, so wet waste can drop to zero net energy.","नमी 15% से कम सबसे अच्छी है। पानी गर्मी सोखता है, इसलिए गीला कचरा बहुत कम ऊर्जा देता है।"],
[/safe|pollut|smoke|सुरक्षित|धुआँ/i,"Closed gasification is far cleaner than open burning, but syngas has carbon monoxide: keep good ventilation, gas filters and trained operators.","बंद गैसीफिकेशन खुले में जलाने से कहीं साफ है, पर सिनगैस में CO होती है: हवादार जगह, फ़िल्टर और प्रशिक्षित ऑपरेटर ज़रूरी हैं।"],
[/login|sign|account|लॉगिन|खाता/i,"Use the Login / Sign up button at the top right. This demo saves accounts only in your own browser.","ऊपर दाईं ओर लॉगिन / साइन अप बटन दबाएँ। यह डेमो खाते केवल आपके ब्राउज़र में रखता है।"],
[/hello|hi|hey|नमस्ते/i,"Namaste! How can I help?","नमस्ते! मैं कैसे मदद करूँ?"]];
function bot(x,silent){const d=document.createElement("div");d.className="m b";d.textContent=x;$("msgs").append(d);$("msgs").scrollTop=1e9}
function user_(x){const d=document.createElement("div");d.className="m u";d.textContent=x;$("msgs").append(d)}
const PRICE=2000000,inr=n=>"₹"+n.toLocaleString("en-IN");
const kgOf=s=>{const m=s.match(/(\d+(?:\.\d+)?)\s*(kgs?|kilos?|किलो|quintals?|क्विंटल|tonnes?|tons?|टन)\b/i);if(!m)return null;let n=+m[1],u=m[2].toLowerCase();if(/quin|क्विं/.test(u))n*=100;else if(/ton|टन/.test(u))n*=1000;return n};
function smart(q){const ql=q.toLowerCase(),L=lang=="en",kg=kgOf(q);let best=null;
B.forEach(b=>[b.a.toLowerCase(),b.b].forEach(n=>{if(ql.includes(n)&&(!best||n.length>best.len))best={b,len:n.length}}));
if(!best)B.forEach(b=>b.a.toLowerCase().split(" ").forEach(w=>{if(w.length>4&&!/^(waste|mixed|household|scraps|plastic|sheets|cloth|bottles)$/.test(w)&&ql.includes(w)&&!best)best={b,len:0}}));
const h=q.match(/(\d+)\s*(homes?|households?|houses?|families|घर|परिवार)/i);
if(h){const n=+h[1],d=n*1.5,m=Math.ceil(d/80);return{t:L?`${n} homes need about ${fmt(d)} kWh/day (at 1.5 kWh per home). One Eklavya-10 makes ≈80 kWh/day, so you need ${m} machine(s), costing ${inr(m*PRICE)}.`:`${n} घरों को लगभग ${fmt(d)} kWh/दिन चाहिए (1.5 kWh प्रति घर)। एक एकलव्य-10 ≈80 kWh/दिन बनाती है, इसलिए ${m} मशीन चाहिए, लागत ${inr(m*PRICE)}।`,go:"order"}}
if(best){const b=best.b,v=/wet|गीला/i.test(q)?V[9]:V.find(v=>ql.includes(v[0].split("/")[0]))||V[0];const it={c:b.c,l:b.l*v[3],m:v[2]},w=kg||1,r=calc(it,w),nm=L?b.a:b.b,vn=L?v[0]:v[1];
if(r.x)return{t:L?`${nm} can’t be gasified: 0 kWh. But recycling ${fmt(w)} kg saves ≈${fmt(r.rec)} kWh of energy. Sell it to a recycler.`:`${nm} गैसीफाई नहीं होता: 0 kWh। पर ${fmt(w)} किलो रीसाइकल करने से ≈${fmt(r.rec)} kWh ऊर्जा बचती है।`};
return{t:L?`${fmt(w)} kg of ${nm} (${vn}) gives ≈${fmt(r.e)} kWh of electricity, about ${fmt(r.syn)} Nm³ syngas, enough for ${fmt(r.e/1.5)} homes for a day.${kg?"":" Tell me a weight (e.g. 250 kg) for an exact figure."}`:`${fmt(w)} किलो ${nm} (${vn}) से ≈${fmt(r.e)} kWh बिजली, ≈${fmt(r.syn)} Nm³ सिनगैस, यानी ${fmt(r.e/1.5)} घरों को एक दिन की बिजली।${kg?"":" सटीक नतीजे के लिए वज़न बताइए (जैसे 250 किलो)।"}`}}
if(/price|cost|कीमत|दाम|लागत|₹|rupee|rs\b/i.test(q)){const m=q.match(/(\d+)\s*(machines?|units?|मशीन)/i),n=m?+m[1]:1;return{t:L?`Eklavya-10 costs ${inr(PRICE)} per machine${n>1?`, so ${n} machines = ${inr(n*PRICE)}`:""}. Taxes and transport are quoted separately.`:`एकलव्य-10 की कीमत ${inr(PRICE)} प्रति मशीन है${n>1?`, यानी ${n} मशीन = ${inr(n*PRICE)}`:""}। कर और ढुलाई अलग से।`,go:"order"}}
return null}
KB[KB.length-1][0]=/\b(hello|hi|hey)\b|नमस्ते/i;
KB.push([/machine|spec|model|capacity|मशीन|क्षमता/i,"Eklavya-10: 10 kW downdraft gasifier + syngas generator, 10–12 kg/h dry feed, ≈80 kWh/day (about 50 homes), ₹20,00,000. Full specs are in the Machine section.","एकलव्य-10: 10 kW डाउनड्राफ्ट गैसीफायर + सिनगैस जनरेटर, 10–12 किलो/घंटा सूखा कचरा, ≈80 kWh/दिन (लगभग 50 घर), ₹20,00,000। पूरी विशेषताएँ मशीन सेक्शन में हैं।","machine"],
[/order|buy|purchase|book|खरीद|ऑर्डर|बुक/i,"You can order from the Order section: fill in your details and quantity and you’ll get an order ID instantly.","ऑर्डर सेक्शन में अपना विवरण और संख्या भरें, तुरंत ऑर्डर आईडी मिलेगी।","order"],
[/support|complaint|repair|ticket|customer|service|सहायता|शिकायत|सर्विस|ग्राहक/i,"Our customer service team can help by phone, email or a support ticket. Open the Support section.","हमारी ग्राहक सेवा फोन, ईमेल या सपोर्ट टिकट से मदद करती है। सपोर्ट सेक्शन खोलें।","support"],
[/warrant|amc|maintenance|वारंटी|रखरखाव/i,"2-year warranty plus an optional annual maintenance contract. Routine tasks: filter cleaning, ash removal, engine oil changes.","2 साल की वारंटी और वैकल्पिक वार्षिक रखरखाव अनुबंध। नियमित काम: फ़िल्टर सफाई, राख निकालना, इंजन ऑयल बदलना।","support"],
[/subsid|loan|emi|financ|सब्सिडी|लोन|ऋण/i,"You can choose bank financing when ordering. Government renewable-energy schemes may also help; check current MNRE and state schemes.","ऑर्डर में बैंक वित्तपोषण चुन सकते हैं। सरकारी नवीकरणीय ऊर्जा योजनाएँ भी मदद कर सकती हैं; MNRE और राज्य योजनाएँ देखें।","order"],
[/best|most|highest|सबसे/i,"Highest energy per kg: plastics (PE/PP), tyres and rubber, then nut shells, wood and straws. Metals give none. Dry fuel always beats wet.","प्रति किलो सबसे ज़्यादा ऊर्जा: प्लास्टिक (PE/PP), टायर-रबर, फिर खोल, लकड़ी और भूसा। धातु से कुछ नहीं। सूखा ईंधन हमेशा बेहतर।"],
[/ash|biochar|राख|बायोचार/i,"About 10% of dry feed remains as biochar/ash, useful as a soil amendment or in bricks.","सूखे कचरे का लगभग 10% बायोचार/राख बचता है, जो मिट्टी सुधारने या ईंट में काम आता है।"]);
function ask(x){user_(x);const d=document.createElement("div");d.className="m b";d.textContent="…";$("msgs").append(d);$("msgs").scrollTop=1e9;
setTimeout(()=>{d.remove();let r=smart(x);if(!r){let bs=0;KB.forEach(k=>{const s=(x.match(new RegExp(k[0].source,"gi"))||[]).length;if(s>bs){bs=s;r={t:k[lang=="en"?1:2],go:k[3]}}})}
if(!r)r={t:t("def")};bot(r.t);if(r.go){const b=document.createElement("button");b.className="g";b.textContent=t("goto");b.onclick=()=>{$(r.go).scrollIntoView();$("chat").classList.remove("o")};$("msgs").append(b);$("msgs").scrollTop=1e9}},450)}
$("cf").onsubmit=e=>{e.preventDefault();const v=$("ci").value.trim();if(v){$("ci").value="";ask(v)}};
$("chatBtn").onclick=()=>{$("chat").classList.toggle("o");if(!$("msgs").children.length){bot(t("hello"));const c=document.createElement("div");c.className="chips";t("chips").forEach(q=>{const b=document.createElement("button");b.className="g";b.textContent=q;b.onclick=()=>ask(q);c.append(b)});$("msgs").append(c)}};

Object.assign(T.en,{calc0:"Calculator",nMach:"Machine",nOrder:"Order",nSup:"Support",goto:"Go to section →",mTitle:"The Eklavya-10 Machine",mPer:"per machine · taxes and transport extra",mDesc:"A containerised waste-to-energy unit: a downdraft thermochemical gasifier feeds a syngas generator, giving about 80 kWh a day, enough for around 50 homes. Built for narrow lanes: one operator, no grid needed.",orderNow:"Order now",specs:"Technical specifications",mNote:"Proposed design targets for the Eklavya-10; confirm final figures before purchase.",oTitle:"Order the machine",phone:"Phone",city:"City",addr:"Delivery address",qty:"Quantity",total:"Total:",place:"Place order",oOk:"Order {id} received for {amt}. Our team will call you to confirm.",sTitle:"Customer service",hours:"Mon–Sat, 9am–7pm IST (placeholder number)",chatus:"Use the chat bubble for instant help",faqT:"Frequently asked questions",ticket:"Raise a support ticket",tmsg:"Describe your issue…",send:"Submit ticket",tOk:"Ticket {id} created. We’ll reply by email within 24 hours."});
Object.assign(T.hi,{calc0:"कैलकुलेटर",nMach:"मशीन",nOrder:"ऑर्डर",nSup:"सहायता",goto:"सेक्शन पर जाएँ →",mTitle:"एकलव्य-10 मशीन",mPer:"प्रति मशीन · कर और ढुलाई अलग",mDesc:"कंटेनर में बनी कचरे से ऊर्जा इकाई: डाउनड्राफ्ट थर्मोकेमिकल गैसीफायर सिनगैस जनरेटर चलाता है, लगभग 80 kWh रोज़, यानी करीब 50 घरों के लिए। संकरी गलियों के लिए: एक ऑपरेटर, ग्रिड की ज़रूरत नहीं।",orderNow:"अभी ऑर्डर करें",specs:"तकनीकी विशेषताएँ",mNote:"ये एकलव्य-10 के प्रस्तावित डिज़ाइन लक्ष्य हैं; खरीद से पहले अंतिम आँकड़े पक्के करें।",oTitle:"मशीन ऑर्डर करें",phone:"फ़ोन",city:"शहर",addr:"डिलीवरी पता",qty:"संख्या",total:"कुल:",place:"ऑर्डर दें",oOk:"ऑर्डर {id} {amt} के लिए मिल गया। हमारी टीम पुष्टि के लिए कॉल करेगी।",sTitle:"ग्राहक सेवा",hours:"सोम–शनि, सुबह 9 से शाम 7 (IST) (नमूना नंबर)",chatus:"तुरंत मदद के लिए चैट बबल इस्तेमाल करें",faqT:"अक्सर पूछे जाने वाले प्रश्न",ticket:"सपोर्ट टिकट बनाएँ",tmsg:"अपनी समस्या लिखें…",send:"टिकट भेजें",tOk:"टिकट {id} बन गया। हम 24 घंटे में ईमेल से जवाब देंगे।"});
const S=[["Electrical output","विद्युत आउटपुट","10 kW continuous (12 kVA)"],["Technology","तकनीक","Downdraft gasifier + syngas engine-generator"],["Feedstock","कच्चा माल","Dry farm and municipal waste, under 15% moisture, 10–50 mm pieces"],["Feed rate","खपत दर","10–12 kg/h"],["Syngas output","सिनगैस","≈25–28 Nm³/h (4.5–5 MJ/Nm³)"],["Reactor temperature","रिएक्टर तापमान","800–1,000 °C"],["Efficiency","दक्षता","Cold-gas ≈70%, overall electrical ≈20%"],["Gas cleaning","गैस सफाई","Cyclone, water scrubber, bag filter, tar cracker"],["Power supply","बिजली आपूर्ति","230 V single-phase / 415 V three-phase, 50 Hz"],["Daily energy","दैनिक ऊर्जा","≈80 kWh over 8 h (about 50 homes)"],["Controls","नियंत्रण","PLC touchscreen, remote monitoring, auto-shutdown on CO or overheating"],["Size / weight","आकार / वज़न","Containerised, 2.4 × 1.6 × 2.2 m, ≈1,800 kg"],["Residue","अवशेष","≈10% biochar/ash"],["Start-up time","शुरू होने का समय","15–20 minutes"],["Staffing","कर्मचारी","1 trained operator per shift"],["Warranty","वारंटी","2 years + optional AMC"],["Delivery","डिलीवरी","8–10 weeks from order"],["Price","कीमत","₹20,00,000 per machine"]];
const FQ=[["How long does installation take?","इंस्टॉलेशन में कितना समय लगता है?","About 8–10 weeks from order, including site preparation and operator training.","ऑर्डर से लगभग 8–10 हफ़्ते, साइट तैयारी और ऑपरेटर प्रशिक्षण सहित।"],["Is the gas safe?","क्या गैस सुरक्षित है?","The unit has CO sensors, auto-shutdown and filters. Keep it in a ventilated area with a trained operator.","यूनिट में CO सेंसर, ऑटो-शटडाउन और फ़िल्टर हैं। हवादार जगह और प्रशिक्षित ऑपरेटर ज़रूरी हैं।"],["What if I need spare parts?","स्पेयर पार्ट्स चाहिए तो?","Raise a ticket and pick “Spare parts”. We confirm availability within 24 hours.","टिकट बनाकर “स्पेयर पार्ट्स” चुनें। हम 24 घंटे में उपलब्धता बताएँगे।"],["Can I cancel an order?","क्या ऑर्डर रद्द हो सकता है?","Call us before dispatch to cancel or change the quantity.","डिस्पैच से पहले कॉल करके रद्द करें या संख्या बदलें।"]];
const ORG=[["Community / RWA","समुदाय / RWA"],["NGO","NGO"],["Municipality","नगर निकाय"],["Business","व्यवसाय"],["Individual","व्यक्तिगत"]],PAY=[["Full payment","पूरा भुगतान"],["Bank financing","बैंक वित्तपोषण"],["Quote first","पहले कोटेशन"]],CAT=[["Technical issue","तकनीकी समस्या"],["Spare parts","स्पेयर पार्ट्स"],["Billing","बिलिंग"],["Training","प्रशिक्षण"],["Other","अन्य"]];
const opts=a=>a.map((x,i)=>`<option value="${i}">${x[lang=="en"?0:1]}</option>`).join("");
function tot(){$("oTotal").textContent=inr(Math.max(1,Math.min(50,+$("oQty").value||1))*PRICE)}
function ui2(){$("specs").innerHTML=S.map(s=>`<div><span>${s[lang=="en"?0:1]}</span><b>${s[2]}</b></div>`).join("");
$("faq").innerHTML=FQ.map(f=>`<details><summary>${f[lang=="en"?0:1]}</summary><p>${f[lang=="en"?2:3]}</p></details>`).join("");
[["oOrg",ORG],["oPay",PAY],["tCat",CAT]].forEach(([id,a])=>{const v=$(id).value||0;$(id).innerHTML=opts(a);$(id).value=v});
tot();if(user){if(!$("oName").value)$("oName").value=user.n}}
const _ui=ui;ui=function(){_ui();ui2()};
const save=(k,o)=>{try{const a=JSON.parse(localStorage.getItem(k)||"[]");a.push(o);localStorage.setItem(k,JSON.stringify(a))}catch(e){}};
const mk=p=>p+"-"+Date.now().toString(36).toUpperCase();
$("oQty").oninput=tot;
$("oForm").onsubmit=e=>{e.preventDefault();const q=Math.max(1,Math.min(50,+$("oQty").value||1)),id=mk("EK");save("ek_orders",{id,name:$("oName").value,phone:$("oPhone").value,email:$("oEmail").value,city:$("oCity").value,addr:$("oAddr").value,q,total:q*PRICE});$("oMsg").textContent=t("oOk").replace("{id}",id).replace("{amt}",inr(q*PRICE));e.target.reset();tot()};
$("tForm").onsubmit=e=>{e.preventDefault();const id=mk("TK");save("ek_tickets",{id,email:$("tEmail").value,cat:$("tCat").value,msg:$("tMsg").value});$("tOut").textContent=t("tOk").replace("{id}",id);e.target.reset()};
document.querySelectorAll("[data-go]").forEach(b=>b.onclick=()=>$(b.dataset.go).scrollIntoView());
ui();
</script></body></html>
