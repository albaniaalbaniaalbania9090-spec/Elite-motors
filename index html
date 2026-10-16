
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#090d0a">
<title>ELITE MOTORS | عالم الدراجات النارية</title>
<style>
:root{--green:#b7ff35;--bg:#090d0a;--panel:#141a16;--muted:#b8c0b8}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:#fff;font-family:Arial,Tahoma,sans-serif}
header{padding:18px 5%;background:#101610;border-bottom:2px solid var(--green);display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap}
.logo{font-size:24px;font-weight:900;color:var(--green);letter-spacing:1px}
.tag{font-size:12px;color:var(--muted);margin-top:5px}
select,input,button{font:inherit}
select,input{background:#1a211b;color:white;border:1px solid #384339;padding:12px;border-radius:9px;width:100%}
button{cursor:pointer;border:0;border-radius:9px;padding:12px;font-weight:bold}
.lang{background:var(--green);color:#101510}
.hero{text-align:center;padding:38px 16px 28px;background:radial-gradient(ellipse at top,#263621,#090d0a 72%)}
.hero h1{font-size:clamp(27px,6vw,44px);margin:0 0 12px}
.hero h1 span{color:var(--green)}
.hero p{color:#c3cbc2;line-height:1.8}
.searchbox{max-width:750px;margin:22px auto 0;display:grid;grid-template-columns:2fr 1fr;gap:10px}
.stats{display:flex;justify-content:center;gap:24px;flex-wrap:wrap;color:var(--green);font-size:13px;margin-top:20px}
.section{padding:22px 5% 8px}
.section h2{font-size:23px}
.section h2 span{color:var(--green)}
.filters{display:flex;gap:9px;flex-wrap:wrap;margin:15px 0}
.filters button{background:#202820;color:#fff;border:1px solid #394339}
.filters button.active{background:var(--green);color:#101510}
.grid{padding:12px 5% 45px;display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,245px),1fr));gap:18px}
.card{background:var(--panel);border:1px solid #293329;border-radius:14px;overflow:hidden;transition:.2s}
.card:hover{border-color:var(--green);transform:translateY(-3px)}
.photo{height:190px;background:#202820;position:relative;overflow:hidden}
.photo img{width:100%;height:100%;object-fit:cover;display:block}
.category{position:absolute;top:10px;right:10px;background:#101510e8;color:var(--green);padding:6px 9px;border-radius:6px;font-size:12px}
.info{padding:15px}
.info h3{margin:2px 0 12px;font-size:18px}
.specs{color:#c0c9bf;font-size:13px;line-height:1.9;min-height:46px}
.price{color:var(--green);font-weight:bold;margin-top:12px;line-height:1.8}
.price small{display:block;color:#b8c0b8;font-weight:normal}
.details{background:#263326;color:white;width:100%;margin-top:8px}
.details:hover{background:#354734}
.inquire{background:var(--green);color:#101510;width:100%;margin-top:8px}
.empty{grid-column:1/-1;text-align:center;color:var(--muted);padding:40px}
.about{background:#121812;padding:28px 6%;line-height:2;color:#d3dbd1}
.about h2{color:var(--green)}
footer{text-align:center;padding:28px 15px;border-top:1px solid #283128;color:#adb6ab;font-size:13px;line-height:2}
dialog{background:#141a16;color:white;border:1px solid var(--green);border-radius:15px;width:min(92%,500px);padding:22px}
dialog::backdrop{background:#000c}
dialog img{width:100%;max-height:240px;object-fit:cover;border-radius:10px}
dialog h2{color:var(--green)}
.close{background:#343c34;color:white;width:100%;margin-top:12px}
@media(max-width:480px){header{padding:15px}.logo{font-size:20px}.searchbox{grid-template-columns:1fr}.photo{height:200px}}
</style>
</head>
<body>
<header>
  <div>
    <div class="logo">ELITE MOTORS 🏍️</div>
    <div class="tag" data-i="tag">عالم الدراجات النارية الفاخرة</div>
  </div>
  <button class="lang" id="langBtn" onclick="toggleLang()">Français 🇫🇷</button>
</header>

<section class="hero">
  <h1 data-i="hero">اكتشف <span>دراجة أحلامك</span></h1>
  <p data-i="intro">اكتشف تشكيلة الدراجات النارية الرياضية والمغامرات من Kawasaki</p>
  <div class="searchbox">
    <input id="search" data-ph="search" placeholder="🔎 ابحث باسم الدراجة..." oninput="render()">
    <select id="sort" onchange="render()">
      <option value="default" data-i="sort">ترتيب الموديلات</option>
      <option value="az" data-i="az">الاسم: أ إلى ي</option>
    </select>
  </div>
  <div class="stats">
    <span>🏁 <b id="count">16</b> <span data-i="models">موديل</span></span>
    <span>🌐 العربية / Français</span>
    <span>⚡ Kawasaki</span>
  </div>
</section>

<section class="section">
  <h2><span>✦</span> <span data-i="catalog">كتالوج الدراجات</span></h2>
  <div class="filters" id="filters"></div>
</section>

<main class="grid" id="bikes"></main>

<section class="about">
  <h2 data-i="about">عن ELITE MOTORS</h2>
  <p data-i="aboutText">وجهتك لاكتشاف الدراجات النارية الرياضية، دراجات الطرق والمغامرات. قارن الموديلات، اطّلع على المواصفات، واطلب معلومات عن الدراجة التي تناسبك.</p>
  <p data-i="notice">تنبيه: الأسعار والتوفّر يتحدّدان حسب السوق والمورّد. الصور قد لا تمثّل كل سنة صنع بدقّة؛ تأكّد من الموديل قبل الشراء.</p>
</section>

<footer>
  <b style="color:#b7ff35">ELITE MOTORS</b>
  <div data-i="footer">شغفك بالموتورات يبدأ من هنا.</div>
  <div>© 2026 ELITE MOTORS</div>
</footer>

<dialog id="modal">
  <div id="modalContent"></div>
  <button class="close" onclick="document.getElementById('modal').close()" data-i="close">إغلاق</button>
</dialog>

<script>
const bikes=[
{name:"Ninja H2",cc:"998 cc",cat:"Sport",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_H2.jpg",desc:"Supercharged sport motorcycle."},
{name:"Ninja ZX-10R",cc:"998 cc",cat:"Sport",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_ZX-10R.jpg",desc:"Superbike performance."},
{name:"Ninja ZX-6R",cc:"636 cc",cat:"Sport",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_ZX-6R.jpg",desc:"Middleweight supersport."},
{name:"Ninja 1000SX",cc:"1043 cc",cat:"Touring",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_1000.jpg",desc:"Sport touring motorcycle."},
{name:"Ninja 650",cc:"649 cc",cat:"Sport",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_650.jpg",desc:"Everyday sport performance."},
{name:"Ninja 500",cc:"451 cc",cat:"Sport",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_500.jpg",desc:"Lightweight sport motorcycle."},
{name:"Ninja 400",cc:"399 cc",cat:"Sport",year:"2023",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Ninja_400.jpg",desc:"Agile lightweight sport bike."},
{name:"Z H2",cc:"998 cc",cat:"Naked",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Z_H2.jpg",desc:"Supercharged naked motorcycle."},
{name:"Z900",cc:"948 cc",cat:"Naked",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Z900.jpg",desc:"Powerful naked roadster."},
{name:"Z650",cc:"649 cc",cat:"Naked",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Z650.jpg",desc:"Versatile naked roadster."},
{name:"Z500",cc:"451 cc",cat:"Naked",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Z500.jpg",desc:"Light urban roadster."},
{name:"Versys 1000",cc:"1043 cc",cat:"Touring",year:"2024",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Versys_1000.jpg",desc:"Long-distance adventure touring."},
{name:"Versys 650",cc:"649 cc",cat:"Touring",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Versys_650.jpg",desc:"Comfortable touring motorcycle."},
{name:"Vulcan S",cc:"649 cc",cat:"Cruiser",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_Vulcan_S.jpg",desc:"Relaxed cruiser riding."},
{name:"KLR650",cc:"652 cc",cat:"Adventure",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_KLR650.jpg",desc:"Adventure and long-distance travel."},
{name:"KLX300",cc:"292 cc",cat:"Off-road",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_KLX300.jpg",desc:"Dual-sport riding."},
{name:"KX450",cc:"449 cc",cat:"Off-road",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_KX450.jpg",desc:"Motocross competition motorcycle."},
{name:"KX250",cc:"249 cc",cat:"Off-road",year:"2025",img:"https://commons.wikimedia.org/wiki/Special:FilePath/Kawasaki_KX250.jpg",desc:"Motocross agility and control."}
];

const translations={
ar:{
tag:"عالم الدراجات النارية الفاخرة",
hero:'اكتشف <span>دراجة أحلامك</span>',
intro:"اكتشف تشكيلة الدراجات النارية الرياضية والمغامرات من Kawasaki",
search:"🔎 ابحث باسم الدراجة...",
sort:"ترتيب الموديلات",az:"الاسم: أ إلى ي",models:"موديل",
catalog:"كتالوج الدراجات",about:"عن ELITE MOTORS",
aboutText:"وجهتك لاكتشاف الدراجات النارية الرياضية، دراجات الطرق والمغامرات. قارن الموديلات، اطّلع على المواصفات، واطلب معلومات عن الدراجة التي تناسبك.",
notice:"تنبيه: الأسعار والتوفّر يتحدّدان حسب السوق والمورّد. الصور قد لا تمثّل كل سنة صنع بدقّة؛ تأكّد من الموديل قبل الشراء.",
footer:"شغفك بالموتورات يبدأ من هنا.",close:"إغلاق",details:"تفاصيل الدراجة",ask:"استفسر عن الدراجة",
price:"السعر بالدينار التونسي",euro:"السعر باليورو",cc:"سعة المحرك",year:"سنة الموديل",category:"الفئة",
noResults:"ما لقيناش موديل يطابق البحث.",all:"الكل",Sport:"رياضية",Naked:"رودستر",Touring:"سياحية",Cruiser:"كروزر",Adventure:"مغامرات","Off-road":"طرق وعرة",
desc:"معلومات",currencyNote:"السعر النهائي عند الاستفسار."
},
fr:{
tag:"Le monde des motos premium",
hero:'Découvrez <span>votre moto idéale</span>',
intro:"Découvrez une sélection de motos sportives et d'aventure Kawasaki",
search:"🔎 Rechercher une moto...",
sort:"Trier les modèles",az:"Nom : A à Z",models:"modèles",
catalog:"Catalogue des motos",about:"À propos d'ELITE MOTORS",
aboutText:"Découvrez des motos sportives, routières et d'aventure. Comparez les modèles, consultez les caractéristiques et demandez des informations sur votre moto préférée.",
notice:"Attention : prix et disponibilité selon le marché et le fournisseur. Les images peuvent ne pas correspondre exactement à chaque année-modèle. Vérifiez avant achat.",
footer:"Votre passion moto commence ici.",close:"Fermer",details:"Détails de la moto",ask:"Demander des informations",
price:"Prix en dinars tunisiens",euro:"Prix en euros",cc:"Cylindrée",year:"Année-modèle",category:"Catégorie",
noResults:"Aucun modèle ne correspond à votre recherche.",all:"Tout",Sport:"Sportive",Naked:"Roadster",Touring:"Tourisme",Cruiser:"Cruiser",Adventure:"Aventure","Off-road":"Tout-terrain",
desc:"Informations",currencyNote:"Prix final sur demande."
}
};

let lang="ar",cat="all";
function tr(key){return translations[lang][key]||key}
function toggleLang(){
lang=lang==="ar"?"fr":"ar";
document.documentElement.lang=lang;
document.documentElement.dir=lang==="ar"?"rtl":"ltr";
document.getElementById("langBtn").textContent=lang==="ar"?"Français 🇫🇷":"العربية 🇹🇳";
document.querySelectorAll("[data-i]").forEach(el=>{
const k=el.dataset.i;
if(translations[lang][k])el.innerHTML=translations[lang][k];
});
document.getElementById("search").placeholder=tr("search");
renderFilters();render();
}
function renderFilters(){
const cats=["all","Sport","Naked","Touring","Cruiser","Adventure","Off-road"];
document.getElementById("filters").innerHTML=cats.map(c=>
`<button class="${cat===c?'active':''}" onclick="setCat('${c}')">${tr(c)}</button>`
).join("");
}
function setCat(c){cat=c;renderFilters();render()}
function render(){
let q=document.getElementById("search").value.toLowerCase();
let list=bikes.filter(b=>(cat==="all"||b.cat===cat)&&
(b.name.toLowerCase().includes(q)||b.cc.toLowerCase().includes(q)||tr(b.cat).toLowerCase().includes(q)));
if(document.getElementById("sort").value==="az")list.sort((a,b)=>a.name.localeCompare(b.name));
document.getElementById("count").textContent=list.length;
document.getElementById("bikes").innerHTML=list.map((b,i)=>`
<article class="card">
<div class="photo">
<img loading="lazy" src="${b.img}" alt="${b.name}" onerror="this.onerror=null;this.src='https://placehold.co/640x400/202820/b7ff35?text=ELITE+MOTORS'">
<span class="category">${tr(b.cat)}</span>
</div>
<div class="info">
<h3>Kawasaki ${b.name}</h3>
<div class="specs">🏍️ ${tr("cc")}: ${b.cc}<br>📅 ${tr("year")}: ${b.year}</div>
<div class="price">${tr("price")}: <small>${lang==="ar"?"عند الاستفسار":"Sur demande"}</small>
<small>${tr("euro")}: ${lang==="ar"?"عند الاستفسار":"Sur demande"}</small></div>
<button class="details" onclick="showDetails('${b.name}')">${tr("details")}</button>
<button class="inquire" onclick="askBike('${b.name}')">✉️ ${tr("ask")}</button>
</div></article>`).join("")||`<div class="empty">${tr("noResults")}</div>`;
}
function showDetails(name){
const b=bikes.find(x=>x.name===name);
document.getElementById("modalContent").innerHTML=`
<img src="${b.img}" alt="${b.name}" onerror="this.onerror=null;this.src='https://placehold.co/640x400/202820/b7ff35?text=Kawasaki'">
<h2>Kawasaki ${b.name}</h2>
<p>${tr("cc")}: ${b.cc}</p>
<p>${tr("year")}: ${b.year}</p>
<p>${tr("category")}: ${tr(b.cat)}</p>
<p>${tr("desc")}: ${b.desc}</p>
<p>${tr("price")}: ${tr("currencyNote")}</p>
<p>${tr("euro")}: ${tr("currencyNote")}</p>`;
document.getElementById("modal").showModal();
}
function askBike(name){
const subject=encodeURIComponent("ELITE MOTORS - Kawasaki "+name);
const body=encodeURIComponent((lang==="ar"?"السلام عليكم، نحب معلومات على الدراجة: ":"Bonjour, je souhaite des informations sur la moto : ")+"Kawasaki "+name);
window.location.href="mailto:?subject="+subject+"&body="+body;
}
renderFilters();render();
</script>
</body>
</html>
