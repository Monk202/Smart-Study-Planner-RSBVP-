<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="ExamPlan - Artificial Intelligence for Better Life. RSBVP, Rajya Stariya Bal Vaigyanik Pradarshani 2026-27. Kendriya Vidyalaya Mandi.">
<meta name="theme-color" content="#14215c">
<title>ExamPlan | AI for Better Life | RSBVP 2026-27 | KV Mandi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700;800&family=Noto+Sans+Devanagari:wght@500;700&display=swap" rel="stylesheet">
<style>
/* ExamPlan - Project RSBVP, Kendriya Vidyalaya Mandi
   Group Leader: Anshul Sharma | Group Member: Aadarsh | Guide Teacher: Naresh Kumar */
:root{
  --navy:#14215c;--blue:#2457e6;--cyan:#0ea5c6;--saffron:#f59e0b;--violet:#6d3fe0;
  --bg:#eef3fb;--card:#fff;--soft:#f6f8fd;--ink:#0f1a36;--muted:#5b6b8c;--line:#dde5f3;--inp:#fff;
  --green:#16a34a;--red:#dc2626;--amber:#d97706;
  --shadow:0 1px 2px rgba(15,26,54,.06),0 10px 28px rgba(20,33,92,.09);
  --grad:linear-gradient(135deg,#0d1650 0%,#2457e6 58%,#0ea5c6 100%);
  --head:"Poppins","Segoe UI",system-ui,sans-serif;
  --body:"Segoe UI","Noto Sans Devanagari",system-ui,-apple-system,Roboto,Arial,sans-serif;
}
[data-theme=dark]{--bg:#0a1126;--card:#121b38;--soft:#182246;--ink:#e8eefc;--muted:#97a6c9;--line:#25335f;--inp:#0e1630;--navy:#9db8ff;--blue:#4d7bff;--shadow:0 10px 28px rgba(0,0,0,.4)}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;font-family:var(--body);background:var(--bg);color:var(--ink);font-size:16px;line-height:1.55;overflow-wrap:anywhere;transition:background .3s,color .3s}
h1,h2,h3,.logo{font-family:var(--head)}

/* ---- Top bar and header ---- */
.school-bar{background:#0a1238;color:#fff;display:flex;justify-content:center;align-items:center;gap:10px;flex-wrap:wrap;padding:9px 12px;font-weight:600;font-size:.92rem;text-align:center}
.school-bar .tri{display:inline-flex;gap:0;border-radius:3px;overflow:hidden}
.school-bar .tri i{width:10px;height:18px;display:block}
.site-header{background:var(--grad);color:#fff;padding:16px 14px 14px;box-shadow:0 4px 18px rgba(13,22,80,.3);position:sticky;top:0;z-index:20}
.header-inner{max-width:900px;margin:0 auto}
.top{display:flex;justify-content:space-between;align-items:center;gap:10px}
.logo{margin:0;font-size:1.6rem;font-weight:800;letter-spacing:-.01em}
.tagline{margin:0;opacity:.9;font-size:.85rem}
.theme-btn{border:1px solid rgba(255,255,255,.4);background:rgba(255,255,255,.14);color:#fff;border-radius:99px;min-width:44px;min-height:44px;font-size:1.2rem;cursor:pointer}
nav{display:flex;gap:8px;margin-top:12px;overflow-x:auto;padding-bottom:2px;scrollbar-width:none}
nav::-webkit-scrollbar{display:none}
nav button{flex:0 0 auto;border:1px solid rgba(255,255,255,.35);background:rgba(255,255,255,.12);color:#fff;padding:9px 15px;min-height:44px;border-radius:99px;font-size:.92rem;font-weight:600;cursor:pointer;transition:.2s;font-family:inherit}
nav button:hover{background:rgba(255,255,255,.25)}
nav button.on{background:#fff;color:#14215c;border-color:#fff;box-shadow:0 4px 12px rgba(0,0,0,.2)}

/* ---- Layout / cards ---- */
main{max-width:900px;margin:0 auto;padding:16px 12px}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:18px;margin-bottom:14px;box-shadow:var(--shadow)}
.card.empty{text-align:center}
h2{margin:0 0 10px;font-size:1.12rem;color:var(--navy)}
p{margin:0 0 10px}
.note{font-size:.85rem;color:var(--muted);margin:4px 0}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px}
.stat{border:1px solid var(--line);border-radius:12px;padding:12px 8px;text-align:center;background:var(--soft);font-size:.85rem;color:var(--muted)}
.stat b{display:block;font-family:var(--head);font-size:1.5rem;color:var(--blue)}
@media(min-width:700px){.grid.g4{grid-template-columns:repeat(4,1fr)}.grid.g3{grid-template-columns:repeat(3,1fr)}}

/* ---- Welcome hero (theme) ---- */
.hero{position:relative;overflow:hidden;color:#fff;border-radius:22px;padding:30px 18px 24px;margin-bottom:14px;background:var(--grad);text-align:center;box-shadow:0 16px 40px rgba(20,33,92,.35)}
.hero svg.net{position:absolute;inset:0;width:100%;height:100%;opacity:.28;pointer-events:none}
.hero>*:not(svg){position:relative}
.event{display:inline-block;background:rgba(255,255,255,.16);border:1px solid rgba(255,255,255,.35);padding:6px 16px;border-radius:99px;font-weight:700;font-size:.95rem}
.hi{font-family:"Noto Sans Devanagari",var(--body);font-size:1.15rem;font-weight:700;margin:12px 0 2px}
.hero .rs{font-family:var(--head);font-size:2.2rem;font-weight:800;letter-spacing:.04em;margin:0}
.hero .theme-lbl{margin:10px 0 0;font-size:.85rem;opacity:.85}
.hero h1{margin:2px 0 8px;font-size:clamp(1.55rem,6.4vw,2.5rem);line-height:1.15;font-weight:800}
.hero h1 em{font-style:normal;color:#ffd36b}
.hero p.sub{max-width:520px;margin:0 auto 16px;opacity:.95}
.team{display:grid;gap:10px;margin:18px 0 6px}
@media(min-width:700px){.team{grid-template-columns:repeat(3,1fr)}}
.member{background:rgba(255,255,255,.14);border:1px solid rgba(255,255,255,.3);border-radius:14px;padding:12px 10px;backdrop-filter:blur(4px)}
.member .ic{font-size:1.6rem}
.member small{display:block;opacity:.85;font-size:.78rem}
.member b{font-family:var(--head);font-size:1.05rem}
.school-line{margin-top:12px;font-weight:600;opacity:.95}
.hero .btn{background:#fff;color:#14215c}

/* ---- Buttons ---- */
.btn{background:var(--blue);color:#fff;border:0;border-radius:12px;padding:10px 16px;min-height:44px;font-size:1rem;font-weight:600;margin:3px 4px 3px 0;cursor:pointer;font-family:inherit;transition:transform .15s,background .15s;box-shadow:0 4px 12px rgba(36,87,230,.28)}
.btn:hover{filter:brightness(1.08);transform:translateY(-1px)}
.btn.alt{background:var(--card);color:var(--blue);border:1.5px solid var(--blue);box-shadow:none}
.btn.alt.on{background:var(--blue);color:#fff}
.btn.red{background:var(--red);box-shadow:0 4px 12px rgba(220,38,38,.25)}
.btn.gold{background:var(--saffron);color:#1b1300;box-shadow:0 4px 12px rgba(245,158,11,.35)}
.small{min-height:36px;padding:6px 12px;font-size:.85rem;border-radius:10px}
.big{font-size:1.05rem;padding:13px 24px}
button:focus-visible,input:focus-visible,select:focus-visible,textarea:focus-visible{outline:3px solid #93c5fd;outline-offset:2px}

/* ---- Forms ---- */
label{display:block;margin:12px 0 4px;font-weight:600;font-size:.9rem;color:var(--muted)}
input,select,textarea{width:100%;padding:11px 12px;border:1.5px solid var(--line);border-radius:10px;font-size:1rem;background:var(--inp);color:var(--ink);font-family:inherit}
input:focus,select:focus{border-color:var(--blue);box-shadow:0 0 0 3px rgba(36,87,230,.18)}
input[type=checkbox]{width:22px;height:22px;flex:0 0 auto;accent-color:var(--blue);cursor:pointer}
.days label{display:inline-flex;gap:5px;align-items:center;margin:4px 10px 4px 0;font-weight:500}
.chk{display:flex;gap:10px;align-items:center;font-weight:400;margin:6px 0;color:var(--ink)}
details{border:1px solid var(--line);border-radius:12px;padding:10px 12px;margin:10px 0;background:var(--soft)}
summary{padding:6px 0;cursor:pointer;color:var(--navy)}

/* ---- Rows, tags, progress ---- */
.row{display:flex;gap:10px;align-items:center;padding:10px 0;border-bottom:1px solid var(--line);flex-wrap:wrap}
.row:last-child{border-bottom:0}
.row>span{flex:1 1 180px}
.bar{background:var(--line);height:12px;border-radius:99px;overflow:hidden;margin:6px 0}
.bar i{display:block;height:100%;background:linear-gradient(90deg,var(--blue),var(--cyan));border-radius:99px;transition:width .6s ease}
.tag{background:rgba(36,87,230,.12);border:1px solid rgba(36,87,230,.3);color:var(--blue);border-radius:99px;padding:1px 9px;font-size:.78rem;font-weight:600}
.done{text-decoration:line-through;color:#94a3b8}
.warn{border-left:5px solid var(--amber);background:rgba(217,119,6,.12);border-radius:10px;padding:10px 12px;margin:8px 0;font-size:.92rem}
.quote{border-left:5px solid var(--saffron);background:var(--soft);border-radius:10px;padding:12px 14px;font-style:italic}
.quote small{display:block;font-style:normal;color:var(--muted);margin-top:4px}

/* ---- Charts ---- */
.hb{margin:10px 0}.hl{display:flex;justify-content:space-between;gap:8px;font-size:.9rem}
.hb.two .bar i.b2{background:linear-gradient(90deg,var(--saffron),#fbbf24)}
.bar.g i{background:var(--green)}.bar.a i{background:var(--amber)}.bar.r i{background:var(--red)}
.chart-wrap{display:flex;gap:16px;align-items:center;flex-wrap:wrap;justify-content:center}
svg.chart{width:100%;max-width:520px;height:auto}
svg text{fill:var(--muted);font-size:11px;font-family:var(--body)}
svg text.v{fill:var(--ink);font-weight:700}
.legend{display:flex;gap:14px;font-size:.82rem;color:var(--muted);flex-wrap:wrap}
.legend i{display:inline-block;width:12px;height:12px;border-radius:3px;margin-right:5px;vertical-align:-1px}

/* ---- Focus timer ---- */
.timer{text-align:center}
.ring{position:relative;width:220px;height:220px;margin:8px auto}
.ring svg{width:100%;height:100%;transform:rotate(-90deg)}
.ring .t{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;font-family:var(--head);font-size:2.6rem;font-weight:800;color:var(--ink)}
.ring .t small{font-size:.8rem;font-weight:500;color:var(--muted)}

/* ---- Badges ---- */
.badges{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:10px}
.badge{border:1px dashed var(--line);border-radius:14px;padding:12px 8px;text-align:center;background:var(--soft);opacity:.55;filter:grayscale(1);font-size:.82rem}
.badge.on{opacity:1;filter:none;border:1px solid var(--saffron);background:rgba(245,158,11,.12)}
.badge b{display:block;font-size:1.7rem}

/* ---- Toast ---- */
#msg{position:fixed;left:12px;right:12px;bottom:14px;max-width:520px;margin:0 auto;z-index:99;padding:13px 16px;border-radius:14px;color:#fff;text-align:center;font-weight:600;box-shadow:0 10px 30px rgba(0,0,0,.3);animation:pop .25s ease}
#msg.ok{background:var(--green)}#msg.err{background:var(--red)}#msg.hide{display:none}
@keyframes pop{from{transform:translateY(14px);opacity:0}to{transform:none;opacity:1}}

/* ---- Footer ---- */
footer{padding:10px 12px 70px}
.foot-card{max-width:900px;margin:0 auto;text-align:center;background:#0a1238;color:#cbd5e1;border-radius:18px;padding:22px 16px;font-size:.9rem}
.foot-card p{margin:0 0 6px}
.foot-title{color:#fff;font-weight:800;font-size:1.05rem;font-family:var(--head)}
.foot-card b{color:#fff}
.foot-team{display:flex;flex-wrap:wrap;gap:8px 22px;justify-content:center;margin:10px 0}
.foot-note{opacity:.8;margin-bottom:12px!important}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
</style>
</head>
<body>

<div class="school-bar">
  <span class="tri" aria-hidden="true"><i style="background:#ff9933"></i><i style="background:#fff"></i><i style="background:#138808"></i></span>
  <span>Kendriya Vidyalaya Mandi</span>
</div>

<header class="site-header">
  <div class="header-inner">
    <div class="top">
      <div>
        <h1 class="logo">📚 ExamPlan</h1>
        <p class="tagline">Artificial Intelligence for Better Life &middot; RSBVP 2026-27</p>
      </div>
      <button class="theme-btn" id="themeBtn" aria-label="Switch light or dark mode">🌙</button>
    </div>
    <nav id="nav" aria-label="Main">
      <button data-tab="home">🏠 Home</button>
      <button data-tab="plan">📅 My Plan</button>
      <button data-tab="progress">📈 Progress</button>
      <button data-tab="charts">📊 Charts</button>
      <button data-tab="focus">⏱️ Focus</button>
      <button data-tab="team">👥 Team</button>
    </nav>
  </div>
</header>

<div id="msg" class="hide" role="status"></div>
<main id="view"></main>

<footer>
  <div class="foot-card">
    <p class="foot-title">ExamPlan &middot; RSBVP 2026-27</p>
    <p>राज्य स्तरीय बाल वैज्ञानिक प्रदर्शनी 2026-27</p>
    <p>Theme: <b>Artificial Intelligence for Better Life</b></p>
    <div class="foot-team">
      <span>Group Leader: <b>Anshul Sharma</b></span>
      <span>Group Member: <b>Aadarsh</b></span>
      <span>Guide Teacher: <b>Naresh Kumar</b></span>
    </div>
    <p>Kendriya Vidyalaya Mandi</p>
    <p class="foot-note">This is a school project. Your data stays in this browser only.</p>
    <button class="btn red small" data-act="reset">Reset all data</button>
  </div>
</footer>

<script>
/* ExamPlan built-in syllabus data (CBSE / NCERT chapter lists) for classes 5 to 12.
   NCERT is replacing books class by class, so names can differ from your school's book or edition.
   Empty lists [] mean "no built-in chapters yet": use option 2 (manual) to type them.
   You can edit this file: add or rename chapters inside the [ ] lists. Keep the commas and quotes. */
const SYLLABUS = {
  '5': {
    'Mathematics': ['We the Travellers - I', 'Fractions', 'Angles as Turns', 'We the Travellers - II', 'Far and Near', 'The Dairy Farm', 'Shapes and Patterns', 'Weight and Capacity', 'Coconut Farm', 'Symmetrical Designs', 'Grandmother\u2019s Quilt', 'Racing Seconds', 'Animal Jumps', 'Maps and Locations', 'Data Through Pictures'],
    'English': ['Papa\u2019s Spectacles', 'Gone with the Scooter', 'The Rainbow', 'The Wise Parrot', 'The Frog', 'What a Tank!', 'Gilli Danda', 'The Decision of the Panchayat', 'Vocation', 'Glass Bangles'],
    'Hindi': ['किरन', 'न्याय की कुर्सी', 'चाँद का कुर्ता', 'साङकेन', 'सुंदरिया', 'चतुर चित्रकार', 'मेरा बचपन', 'काजीरंगा राष्ट्रीय उद्यान की यात्रा', 'न्याय', 'तीन मछलियाँ', 'हमारे ये कलामंदिर', 'गंगा की कहानी'],
    'EVS': ['Water - The Essence of Life', 'Journey of a River', 'The Mystery of Food', 'Our School - A Happy Place', 'Our Vibrant Country', 'Some Unique Places', 'Energy - How Things Work', 'Clothes - How Things Are Made', 'Rhythms of Nature', 'Earth - Our Shared Home']
  },
  '6': {
    'Mathematics': ['Patterns in Mathematics', 'Lines and Angles', 'Number Play', 'Data Handling and Presentation', 'Prime Time', 'Perimeter and Area', 'Fractions', 'Playing with Constructions', 'Symmetry', 'The Other Side of Zero'],
    'Science': ['The Wonderful World of Science', 'Diversity in the Living World', 'Mindful Eating: A Path to a Healthy Body', 'Exploring Magnets', 'Measurement of Length and Motion', 'Materials Around Us', 'Temperature and Its Measurement', 'A Journey through States of Water', 'Methods of Separation in Everyday Life', 'Living Creatures: Exploring Their Characteristics', 'Nature\u2019s Treasures', 'Beyond Earth'],
    'Social Science': ['Locating Places on the Earth', 'Oceans and Continents', 'Landforms and Life', 'Timeline and Sources of History', 'India, That Is Bharat', 'The Beginnings of Indian Civilisation', 'India\u2019s Cultural Roots', 'Unity in Diversity, or \u2018Many in the One\u2019', 'Family and Community', 'Grassroots Democracy - Part 1: Governance', 'Grassroots Democracy - Part 2: Local Government in Rural Areas', 'Grassroots Democracy - Part 3: Local Government in Urban Areas', 'The Value of Work', 'Economic Activities Around Us'],
    'English': ['A Bottle of Dew', 'The Raven and the Fox', 'Rama to the Rescue', 'The Unlikely Best Friends', 'A Friend\u2019s Prayer', 'The Chair', 'Neem Baba', 'What a Bird Thought', 'Spices that Heal Us', 'Change of Heart', 'The Winner', 'Yoga - A Way of Life', 'Hamara Bharat - Incredible India!', 'The Kites', 'Ila Sachani: Embroidering Dreams with her Feet', 'National War Memorial'],
    'Hindi': ['मातृभूमि', 'गोल', 'पहली बूँद', 'हार की जीत', 'रहीम के दोहे', 'मेरी माँ', 'जलाते चलो', 'सत्रिया और बिहू नृत्य', 'मैया मैं नहिं माखन खायो', 'परीक्षा', 'चेतक की वीरता', 'हिंद महासागर में छोटा-सा हिंदुस्तान', 'पेड़ की बात']
  },
  /* Class 7: Maths has only the 8 chapters of Part 1 listed here. Add Part 2 chapters manually. English shows the 5 units. */
  '7': {
    'Mathematics': ['Large Numbers Around Us', 'Arithmetic Expressions', 'A Peek Beyond the Point', 'Expressions Using Letter-Numbers', 'Parallel and Intersecting Lines', 'Number Play', 'A Tale of Three Intersecting Lines', 'Working with Fractions'],
    'Science': ['The Ever-Evolving World of Science', 'Exploring Substances: Acidic, Basic, and Neutral', 'Electricity: Circuits and their Components', 'The World of Metals and Non-metals', 'Changes Around Us: Physical and Chemical', 'Adolescence: A Stage of Growth and Change', 'Heat Transfer in Nature', 'Measurement of Time and Motion', 'Life Processes in Animals', 'Life Processes in Plants', 'Light: Shadows and Reflections', 'Earth, Moon, and the Sun'],
    'Social Science': ['Geographical Diversity of India', 'Understanding the Weather', 'Climates of India', 'New Beginnings: Cities and States', 'The Rise of Empires', 'The Age of Reorganisation', 'The Gupta Era: An Age of Tireless Creativity', 'How Land Became Sacred', 'From Pilgrimage to Trades, Beyond India', 'From the Rulers to Ruled: Types of Government', 'The Constitution of India', 'From Barter to Money', 'Understanding Markets'],
    'English': ['Unit 1: Learning Together', 'Unit 2: Wit and Humour', 'Unit 3: Dreams and Discoveries', 'Unit 4: Travel and Adventure', 'Unit 5: Bravehearts'],
    'Hindi': ['माँ, कह एक कहानी', 'तीन बुद्धिमान (लोककथा)', 'फूल और काँटा', 'पानी रे पानी', 'नहीं होना बीमार', 'गिरिधर', 'वर्षा-बहार', 'बिरजू महाराज से साक्षात्कार', 'चिड़िया', 'मीरा के पद']
  },
  /* Classes 8 and 9: chapter lists not added yet (books changed recently). Use option 2 (manual). */
  '8': { 'Mathematics': [], 'Science': [], 'Social Science': [], 'English': [], 'Hindi': [] },
  '9': { 'Mathematics': [], 'Science': [], 'Social Science': [], 'English': [], 'Hindi': [] },
  '10': {
    'Mathematics': ['Real Numbers', 'Polynomials', 'Pair of Linear Equations in Two Variables', 'Quadratic Equations', 'Arithmetic Progressions', 'Triangles', 'Coordinate Geometry', 'Introduction to Trigonometry', 'Some Applications of Trigonometry', 'Circles', 'Areas Related to Circles', 'Surface Areas and Volumes', 'Statistics', 'Probability'],
    'Science': ['Chemical Reactions and Equations', 'Acids, Bases and Salts', 'Metals and Non-metals', 'Carbon and its Compounds', 'Life Processes', 'Control and Coordination', 'How do Organisms Reproduce?', 'Heredity', 'Light - Reflection and Refraction', 'The Human Eye and the Colourful World', 'Electricity', 'Magnetic Effects of Electric Current', 'Our Environment'],
    'English': ['First Flight: A Letter to God', 'First Flight: Nelson Mandela: Long Walk to Freedom', 'First Flight: Two Stories about Flying', 'First Flight: From the Diary of Anne Frank', 'First Flight: Glimpses of India', 'First Flight: Mijbil the Otter', 'First Flight: Madam Rides the Bus', 'First Flight: The Sermon at Benares', 'First Flight: The Proposal', 'Poem: Dust of Snow', 'Poem: Fire and Ice', 'Poem: A Tiger in the Zoo', 'Poem: How to Tell Wild Animals', 'Poem: The Ball Poem', 'Poem: Amanda!', 'Poem: The Trees', 'Poem: Fog', 'Poem: The Tale of Custard the Dragon', 'Poem: For Anne Gregory', 'Footprints: A Triumph of Surgery', 'Footprints: The Thief\u2019s Story', 'Footprints: The Midnight Visitor', 'Footprints: A Question of Trust', 'Footprints: Footprints without Feet', 'Footprints: The Making of a Scientist', 'Footprints: The Necklace', 'Footprints: Bholi', 'Footprints: The Book That Saved the Earth'],
    'Hindi': ['Kshitij: Surdas ke Pad', 'Kshitij: Ram-Lakshman-Parshuram Samvad', 'Kshitij: Aatmakathya', 'Kshitij: Utsah aur At Nahin Rahi Hai', 'Kshitij: Yeh Danturit Muskan aur Fasal', 'Kshitij: Sangatkar', 'Kshitij: Netaji ka Chashma', 'Kshitij: Balgobin Bhagat', 'Kshitij: Lakhnavi Andaz', 'Kshitij: Ek Kahani Yeh Bhi', 'Kshitij: Naubatkhane Mein Ibadat', 'Kshitij: Sanskriti', 'Kritika: Mata ka Anchal', 'Kritika: Sana-Sana Hath Jodi', 'Kritika: Main Kyon Likhta Hoon?'],
    'History': ['The Rise of Nationalism in Europe', 'Nationalism in India', 'The Making of a Global World', 'The Age of Industrialisation', 'Print Culture and the Modern World'],
    'Geography': ['Resources and Development', 'Forest and Wildlife Resources', 'Water Resources', 'Agriculture', 'Minerals and Energy Resources', 'Manufacturing Industries', 'Lifelines of National Economy'],
    'Political Science': ['Power Sharing', 'Federalism', 'Gender, Religion and Caste', 'Political Parties', 'Outcomes of Democracy'],
    'Economics': ['Development', 'Sectors of the Indian Economy', 'Money and Credit', 'Globalisation and the Indian Economy', 'Consumer Rights']
  },
  '11': {
    'Physics': ['Units and Measurements', 'Motion in a Straight Line', 'Motion in a Plane', 'Laws of Motion', 'Work, Energy and Power', 'System of Particles and Rotational Motion', 'Gravitation', 'Mechanical Properties of Solids', 'Mechanical Properties of Fluids', 'Thermal Properties of Matter', 'Thermodynamics', 'Kinetic Theory', 'Oscillations', 'Waves'],
    'Chemistry': ['Some Basic Concepts of Chemistry', 'Structure of Atom', 'Classification of Elements and Periodicity in Properties', 'Chemical Bonding and Molecular Structure', 'Thermodynamics', 'Equilibrium', 'Redox Reactions', 'Organic Chemistry: Some Basic Principles and Techniques', 'Hydrocarbons'],
    'Mathematics': ['Sets', 'Relations and Functions', 'Trigonometric Functions', 'Complex Numbers and Quadratic Equations', 'Linear Inequalities', 'Permutations and Combinations', 'Binomial Theorem', 'Sequences and Series', 'Straight Lines', 'Conic Sections', 'Introduction to Three Dimensional Geometry', 'Limits and Derivatives', 'Statistics', 'Probability'],
    'Biology': ['The Living World', 'Biological Classification', 'Plant Kingdom', 'Animal Kingdom', 'Morphology of Flowering Plants', 'Anatomy of Flowering Plants', 'Structural Organisation in Animals', 'Cell: The Unit of Life', 'Biomolecules', 'Cell Cycle and Cell Division', 'Photosynthesis in Higher Plants', 'Respiration in Plants', 'Plant Growth and Development', 'Breathing and Exchange of Gases', 'Body Fluids and Circulation', 'Excretory Products and their Elimination', 'Locomotion and Movement', 'Neural Control and Coordination', 'Chemical Coordination and Integration']
  },
  '12': {
    'Physics': ['Electric Charges and Fields', 'Electrostatic Potential and Capacitance', 'Current Electricity', 'Moving Charges and Magnetism', 'Magnetism and Matter', 'Electromagnetic Induction', 'Alternating Current', 'Electromagnetic Waves', 'Ray Optics and Optical Instruments', 'Wave Optics', 'Dual Nature of Radiation and Matter', 'Atoms', 'Nuclei', 'Semiconductor Electronics'],
    'Chemistry': ['Solutions', 'Electrochemistry', 'Chemical Kinetics', 'The d- and f-Block Elements', 'Coordination Compounds', 'Haloalkanes and Haloarenes', 'Alcohols, Phenols and Ethers', 'Aldehydes, Ketones and Carboxylic Acids', 'Amines', 'Biomolecules'],
    'Mathematics': ['Relations and Functions', 'Inverse Trigonometric Functions', 'Matrices', 'Determinants', 'Continuity and Differentiability', 'Application of Derivatives', 'Integrals', 'Application of Integrals', 'Differential Equations', 'Vector Algebra', 'Three Dimensional Geometry', 'Linear Programming', 'Probability'],
    'Biology': ['Sexual Reproduction in Flowering Plants', 'Human Reproduction', 'Reproductive Health', 'Principles of Inheritance and Variation', 'Molecular Basis of Inheritance', 'Evolution', 'Human Health and Disease', 'Microbes in Human Welfare', 'Biotechnology: Principles and Processes', 'Biotechnology and its Applications', 'Organisms and Populations', 'Ecosystem', 'Biodiversity and Conservation']
  }
};
</script>
<script>
'use strict';
/* ExamPlan - flow: Get Started > About you > 3 ways to add data > My Plan. Extra tabs: Charts, Focus, Team */

// ---------- Helpers ----------
const KEY = 'examplan_v3', TKEY = 'examplan_theme', $ = id => document.getElementById(id);
const arr = a => Array.isArray(a) ? a : [];
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const uid = () => Math.random().toString(36).slice(2, 9);
const today = () => { const d = new Date(); d.setHours(0, 0, 0, 0); return d; };
const fmt = d => d.getFullYear() + '-' + String(d.getMonth() + 1).padStart(2, '0') + '-' + String(d.getDate()).padStart(2, '0');
const parse = s => new Date(s + 'T00:00:00');
const daysTo = s => Math.round((parse(s) - today()) / 864e5);
const validDate = s => /^\d{4}-\d{2}-\d{2}$/.test(s || '') && !isNaN(parse(s));
const DAYS = ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'];
const hm = v => String(Math.floor(v / 60) % 24).padStart(2, '0') + ':' + String(v % 60).padStart(2, '0');
const num = (v, lo, hi) => { if (v === null || v === undefined || String(v).trim() === '') return null; const n = Number(v); return Number.isFinite(n) && n >= lo && n <= hi ? n : null; };
const CLASSES = [['5', 'Class 5'], ['6', 'Class 6'], ['7', 'Class 7'], ['8', 'Class 8'], ['9', 'Class 9'], ['10', 'Class 10'],
  ['11|PCM', 'Class 11 (PCM)'], ['11|PCB', 'Class 11 (PCB)'], ['11|PCMB', 'Class 11 (PCMB)'],
  ['12|PCM', 'Class 12 (PCM)'], ['12|PCB', 'Class 12 (PCB)'], ['12|PCMB', 'Class 12 (PCMB)']];
const clsName = v => (CLASSES.find(c => c[0] === v) || [v, 'Class ' + v])[1];
const STREAMS = { PCM: ['Physics', 'Chemistry', 'Mathematics'], PCB: ['Physics', 'Chemistry', 'Biology'], PCMB: ['Physics', 'Chemistry', 'Mathematics', 'Biology'] };
const QUOTES = [
  ['Small steps every day build big results.', 'ExamPlan tip'],
  ['AI can guide your plan, but your effort makes it work.', 'Theme: AI for Better Life'],
  ['Study smart: hard topics first, when your mind is fresh.', 'ExamPlan tip'],
  ['Mistakes in a practice test are free lessons.', 'ExamPlan tip'],
  ['Technology is best when it helps people learn and live better.', 'Theme: AI for Better Life'],
  ['Take a short break. A rested brain remembers more.', 'ExamPlan tip'],
  ['Consistency beats last-night cramming.', 'ExamPlan tip']
];
let S, tab = 'home', page = '', view = 'today';       // page: '' (3 options) | 'syl' | 'man' | 'saved'
let qa = { cls: '10', type: 'exam', exam: '' };
function msg(t, k) { const m = $('msg'); m.textContent = t; m.className = k || 'ok'; clearTimeout(msg.t); msg.t = setTimeout(() => m.className = 'hide', 4500); }

// ---------- Theme (light / dark) ----------
function setTheme(t) {
  document.documentElement.dataset.theme = t; $('themeBtn').textContent = t === 'dark' ? '☀️' : '🌙';
  try { localStorage.setItem(TKEY, t); } catch (e) {}
}
$('themeBtn').addEventListener('click', () => { setTheme(document.documentElement.dataset.theme === 'dark' ? 'light' : 'dark'); render(); });
try { setTheme(localStorage.getItem(TKEY) || 'light'); } catch (e) { setTheme('light'); }

// ---------- Storage ----------
const blank = () => ({ stage: 0, profile: { name: '', cls: '10', hours: 2, off: [] }, subjects: [], chapters: [], sessions: [], notes: [], warn: [], demo: false, focus: {} });
function load() {
  S = blank();
  try {
    const d = JSON.parse(localStorage.getItem(KEY) || 'null');
    if (!d || typeof d !== 'object') return;
    S.profile = { ...S.profile, ...(d.profile || {}) };
    S.profile.hours = num(S.profile.hours, 0.5, 8) ?? 2;
    S.profile.off = arr(S.profile.off).filter(x => x >= 0 && x <= 6);
    if (!CLASSES.some(c => c[0] === S.profile.cls)) S.profile.cls = '10';
    S.stage = [0, 1, 2].includes(d.stage) ? d.stage : 0;
    S.subjects = arr(d.subjects).filter(s => s && s.id && s.name && validDate(s.exam)).map(s => ({ ...s, type: s.type === 'goal' ? 'goal' : 'exam', src: s.src === 'syllabus' ? 'syllabus' : 'manual' }));
    S.chapters = arr(d.chapters).filter(c => c && c.id && c.name && S.subjects.some(s => s.id === c.subjectId)).map(c => ({
      id: c.id, subjectId: c.subjectId, name: c.name, imp: num(c.imp, 1, 5) ?? 3, hours: num(c.hours, 0.25, 100) ?? 1,
      test: c.test == null ? null : num(c.test, 0, 100), done: !!c.done, src: c.src === 'syllabus' ? 'syllabus' : 'manual', lastP: num(c.lastP, 0, 100), snap: c.snap || null }));
    S.sessions = arr(d.sessions).filter(x => x && x.id && validDate(x.date) && x.mins > 0 && S.chapters.some(c => c.id === x.chapId));
    S.notes = arr(d.notes); S.warn = arr(d.warn); S.demo = !!d.demo;
    S.focus = d.focus && typeof d.focus === 'object' ? d.focus : {};
  } catch (e) { S = blank(); msg('Saved data could not be read, starting fresh', 'err'); }
}
function save() { try { localStorage.setItem(KEY, JSON.stringify(S)); } catch (e) { msg('Could not save data', 'err'); } }

// ---------- Math model: P = 100 x (0.40 U + 0.25 M + 0.35 N) ----------
const subj = id => S.subjects.find(s => s.id === id);
function priority(c) {
  const s = subj(c.subjectId), D = s ? Math.max(0, daysTo(s.exam)) : 0;
  const U = Math.max(0, 1 - D / 30), M = (c.imp - 1) / 4, N = c.test == null ? 0.5 : 1 - c.test / 100;
  const P = 100 * (0.40 * U + 0.25 * M + 0.35 * N);
  return Number.isFinite(P) ? Math.min(100, Math.max(0, P)) : 0;
}
const doneMin = c => S.sessions.reduce((a, x) => a + (x.chapId === c.id && x.done ? x.mins : 0), 0);
const remH = c => c.done ? 0 : Math.max(0, c.hours - doneMin(c) / 60);

// ---------- Scheduler: earliest deadline first, priority breaks ties ----------
function plan() {
  S.sessions = S.sessions.filter(x => x.done);
  S.warn = []; S.notes = [];
  const t = today(), used = {}, days = [];
  S.sessions.forEach(x => used[x.date] = (used[x.date] || 0) + x.mins);
  const horizon = Math.max(0, ...S.subjects.map(s => daysTo(s.exam)));
  for (let i = 0; i < horizon; i++) {
    const d = new Date(t); d.setDate(t.getDate() + i);
    if (S.profile.off.includes(d.getDay())) continue;
    const k = fmt(d), free = S.profile.hours * 60 - (used[k] || 0);
    if (free > 0) days.push({ k, i, free });
  }
  const items = S.chapters.filter(c => !c.done && subj(c.subjectId)).map(c => {
    const s = subj(c.subjectId); return { c, s, p: priority(c), end: daysTo(s.exam), rem: Math.round(remH(c) * 60) };
  }).sort((a, b) => a.end - b.end || b.p - a.p);
  let start = 0;
  items.forEach(it => {
    const { c, s, p } = it, D = it.end;
    if (c.lastP != null && Math.abs(p - c.lastP) >= 3) {
      const w = [];
      if (c.snap) {
        if (c.snap.test !== c.test) w.push('the test score changed');
        if (c.snap.imp !== c.imp) w.push('importance changed');
        if (c.snap.D !== D) w.push('the deadline is closer or its date changed');
      }
      S.notes.push(`${s.name} › ${c.name}: priority ${c.lastP.toFixed(0)} → ${p.toFixed(0)} (${p > c.lastP ? 'went up' : 'went down'}${w.length ? ' because ' + w.join(', ') : ''})`);
    }
    c.lastP = p; c.snap = { test: c.test, imp: c.imp, D };
    for (let j = start; j < days.length && days[j].i < D && it.rem > 0; j++) {
      const d = days[j], m = Math.min(d.free, 60, it.rem);
      if (m <= 0) continue;
      S.sessions.push({ id: uid(), chapId: c.id, date: d.k, mins: m, type: c.test == null || c.test < 50 ? 'Learning' : c.test < 80 ? 'Practice' : 'Revision', done: false });
      d.free -= m; it.rem -= m;
      while (start < days.length && days[start].free <= 0) start++;
    }
    if (it.rem > 0) S.warn.push(`${s.name} › ${c.name}: ${(it.rem / 60).toFixed(1)} hours could not be scheduled before the ${s.type === 'goal' ? 'goal date' : 'exam'} (${s.exam}). Increase daily hours, free up unavailable days, or check the date.`);
  });
  save();
}
function changed(text) { if (S.subjects.length) plan(); else save(); if (text) msg(text); render(); }

// ---------- Stats: streak, badges, study minutes ----------
function minsOn(k) { return S.sessions.reduce((a, x) => a + (x.date === k && x.done ? x.mins : 0), 0) + (S.focus[k] || 0); }
function dayKey(offset) { const d = today(); d.setDate(d.getDate() + offset); return fmt(d); }
function streak() { let n = 0, i = minsOn(dayKey(0)) > 0 ? 0 : -1; while (minsOn(dayKey(i)) > 0 && n < 400) { n++; i--; } return n; }
const focusTotal = () => Object.values(S.focus).reduce((a, b) => a + (+b || 0), 0);
function badges() {
  const ch = S.chapters, done = ch.filter(c => c.done).length, ses = S.sessions.filter(x => x.done).length, st = streak();
  return [
    ['🚀', 'First step', 'Finish 1 study session', ses >= 1], ['🔥', '3-day streak', 'Study 3 days in a row', st >= 3],
    ['⭐', '7-day streak', 'Study 7 days in a row', st >= 7], ['🎯', 'Half way', 'Finish 50% chapters', ch.length > 0 && done / ch.length >= .5],
    ['🏆', 'Syllabus master', 'Finish all chapters', ch.length > 0 && done === ch.length], ['⏱️', 'Focus hero', '60 focus minutes', focusTotal() >= 60]
  ];
}

// ---------- Small view helpers ----------
const bar = (p, cls) => `<div class="bar ${cls || ''}"><i style="width:${Math.round(p)}%"></i></div>`;
const pct = (a, b) => b ? a / b * 100 : 0;
const opt = (v, l, cur) => `<option value="${esc(v)}" ${String(cur) === v ? 'selected' : ''}>${l}</option>`;
const back = '<button class="btn alt" data-act="go" data-id="">&larr; Back</button>';
function dayList(k) {
  let off = 0;
  return S.sessions.filter(x => x.date === k).map(x => {
    const c = S.chapters.find(y => y.id === x.chapId), s = c && subj(c.subjectId);
    return c && s ? { x, c, s, p: priority(c) } : null;
  }).filter(Boolean).sort((a, b) => b.p - a.p).map(r => { const a = 900 + off; off += r.x.mins; r.time = hm(a) + '-' + hm(a + r.x.mins); return r; });
}
const sessRow = r => `<div class="row"><input type="checkbox" data-act="togSess" data-id="${r.x.id}" ${r.x.done ? 'checked' : ''} aria-label="Mark done">
  <span class="${r.x.done ? 'done' : ''}">${r.time} · <b>${esc(r.s.name)}</b> › ${esc(r.c.name)}<br>${r.x.mins} min · <span class="tag">${r.x.type}</span> · Priority ${r.p.toFixed(0)}</span></div>`;
const warnBox = () => S.warn.map(w => `<div class="warn">${esc(w)}</div>`).join('') + S.notes.map(n => `<div class="warn">${esc(n)}</div>`).join('');
function dl(k) { const n = daysTo(k); return n === 0 ? 'Today' : n === 1 ? 'Tomorrow' : DAYS[parse(k).getDay()] + ' ' + k; }
const dateFields = () => `<label>Type</label><select name="type">${opt('exam', 'Exam (I have an exam)', qa.type)}${opt('goal', 'Syllabus goal (no exam)', qa.type)}</select>
  <label>Exam date, or the date you want to finish the syllabus</label><input name="exam" type="date" value="${esc(qa.exam)}">
  <p class="note">For a syllabus goal you can leave the date empty. It will default to 30 days from today.</p>`;
const quoteCard = () => { const q = QUOTES[Math.floor(today() / 864e5) % QUOTES.length]; return `<div class="quote">“${q[0]}”<small>${q[1]}</small></div>`; };

// ---------- Screens ----------
function teamCards() {
  return `<div class="team">
  <div class="member"><div class="ic"></div><small>Group Leader</small><b>Anshul Sharma</b></div>
  <div class="member"><div class="ic"></div><small>Group Member</small><b>Aadarsh</b></div>
  <div class="member"><div class="ic">🎓</div><small>Guide Teacher</small><b>Naresh Kumar</b></div></div>`;
}
const NET = `<svg class="net" viewBox="0 0 400 300" preserveAspectRatio="xMidYMid slice" aria-hidden="true"><g stroke="#fff" stroke-width="1" fill="none">
<path d="M20 40L110 90L90 190L200 150L190 250M110 90L200 40L300 110L200 150L300 210L380 150L300 110M200 40L380 60L380 150M90 190L20 260L190 250L300 210"/></g>
<g fill="#fff"><circle cx="20" cy="40" r="4"/><circle cx="110" cy="90" r="5"/><circle cx="90" cy="190" r="4"/><circle cx="200" cy="150" r="6"/><circle cx="190" cy="250" r="4"/><circle cx="200" cy="40" r="4"/><circle cx="300" cy="110" r="5"/><circle cx="300" cy="210" r="4"/><circle cx="380" cy="150" r="4"/><circle cx="380" cy="60" r="4"/><circle cx="20" cy="260" r="4"/></g></svg>`;
function heroCard(withBtn) {
  return `<section class="hero">${NET}
  <span class="event">RSBVP 2026-27</span>
  <p class="hi">राज्य स्तरीय बाल वैज्ञानिक प्रदर्शनी 2026-27</p>
  <p class="theme-lbl">Our Theme</p>
  <h1>Artificial Intelligence <em>for Better Life</em></h1>
  <p class="sub">ExamPlan is our AI-style study planner. It looks at your deadlines, chapter importance and test scores, then decides what you should study each day.</p>
  ${withBtn ? '<button class="btn big" data-act="start">Get Started</button>' : ''}
  ${teamCards()}
  <p class="school-line">andKendriya Vidyalaya Mandi</p></section>`;
}
function aboutCard(title, button) {
  const p = S.profile;
  return `<div class="card"><h2>${title}</h2><form id="fProfile">
  <label>Name (optional)</label><input name="name" maxlength="40" value="${esc(p.name)}">
  <label>Class</label><select name="cls">${CLASSES.map(c => opt(c[0], c[1], p.cls)).join('')}</select>
  <label>Daily study hours (0.5 - 8)</label><input name="hours" type="number" step="0.5" value="${p.hours}">
  <label>Unavailable days</label><div class="days">${DAYS.map((d, i) => `<label><input type="checkbox" name="off" value="${i}" ${p.off.includes(i) ? 'checked' : ''}>${d}</label>`).join('')}</div>
  <button class="btn big">${button}</button></form></div>`;
}
function countdown() {
  const up = S.subjects.filter(s => daysTo(s.exam) >= 0).sort((a, b) => a.exam.localeCompare(b.exam));
  if (!up.length) return '';
  return `<div class="card"><h2>⏳ Countdown</h2><div class="grid g3">${up.slice(0, 3).map(s => `<div class="stat"><b>${daysTo(s.exam)}</b>days to ${esc(s.name)} ${s.type === 'goal' ? 'goal' : 'exam'}</div>`).join('')}</div></div>`;
}

function viewHome() {
  if (S.stage === 0) return heroCard(true) + quoteCard();
  if (S.stage === 1) return aboutCard('Step 1: About you', 'Continue');
  if (page === 'syl') return viewSyl();
  if (page === 'man') return viewMan();
  if (page === 'saved') return viewSaved();
  const ch = S.chapters, done = ch.filter(c => c.done).length;
  return `<div class="card"><h2>Step 2: Add your data</h2><p>${S.profile.name ? 'Hello, ' + esc(S.profile.name) + '. ' : ''}${clsName(S.profile.cls)}. Choose one option.</p>
  <div class="grid g3"><div class="stat"><b>🔥 ${streak()}</b>day streak</div><div class="stat"><b>${done}/${ch.length}</b>chapters done</div><div class="stat"><b>${focusTotal()}</b>focus minutes</div></div></div>
  ${countdown()}${quoteCard()}<div style="height:14px"></div>
  <div class="card"><h2>1. Add data from syllabus</h2><p>Pick subjects and chapters that are already listed for your class.</p><button class="btn big" data-act="go" data-id="syl">Open</button></div>
  <div class="card"><h2>2. Add data manually</h2><p>Type your own subjects and chapters.</p><button class="btn big" data-act="go" data-id="man">Open</button></div>
  <div class="card"><h2>3. Load saved data</h2><p>See, edit or delete the subjects and chapters you saved before.</p><button class="btn big" data-act="go" data-id="saved">Open</button></div>
  <div class="card"><h2>Your details</h2><button class="btn alt" data-act="editProfile">Change class, hours or days</button>${ch.length ? '<button class="btn alt" data-tab="plan">View my plan</button>' : ''}</div>`;
}

function pickList() {
  const [c, st] = qa.cls.split('|'), data = (typeof SYLLABUS !== 'undefined' && SYLLABUS[c]) || {};
  const names = Object.keys(data).filter(n => +c < 11 || STREAMS[st].includes(n));
  return names.map(n => !data[n].length
    ? `<p class="note"><b>${esc(n)}</b>: no built-in chapters yet. Use option 2 (manual) to add them.</p>`
    : `<details open><summary><b>${esc(n)}</b> (${data[n].length} chapters)</summary>
    <button type="button" class="btn alt small" data-act="selOn" data-id="${esc(n)}">Select all</button><button type="button" class="btn alt small" data-act="selOff" data-id="${esc(n)}">Select none</button>
    ${data[n].map((ch, k) => `<label class="chk"><input type="checkbox" name="ch" data-s="${esc(n)}" value="${esc(n)}||${k}" checked> ${esc(ch)}</label>`).join('')}</details>`).join('');
}
function viewSyl() {
  return back + `<div class="card"><h2>Add data from syllabus</h2><form id="fSyl">
  <label>Class</label><select name="cls">${CLASSES.map(c => opt(c[0], c[1], qa.cls)).join('')}</select>
  ${dateFields()}
  <p class="note">Tick the chapters you want. Each starts with importance 3 and 2 hours (change later in option 3).</p>
  ${pickList()}<button class="btn big">Add selected chapters</button></form></div>`;
}
function viewMan() {
  return back + `<div class="card"><h2>Add a subject</h2><form id="fSub"><label>Subject name</label><input name="name" maxlength="40" required>
  ${dateFields()}<button class="btn">Add subject</button></form></div>
  <div class="card"><h2>Add a chapter</h2>${S.subjects.length ? `<form id="fChap"><label>Subject</label><select name="sub">${S.subjects.map(s => `<option value="${s.id}">${esc(s.name)}</option>`).join('')}</select>
  <label>Chapter name</label><input name="name" maxlength="60" required>
  <label>Importance (1-5)</label><input name="imp" type="number" min="1" max="5" value="3">
  <label>Estimated hours</label><input name="hours" type="number" step="0.25" min="0.25" value="2">
  <label>Practice test score 0-100 (optional)</label><input name="test" type="number" min="0" max="100">
  <button class="btn">Add chapter</button></form>` : '<p>Add a subject first.</p>'}</div>
  ${S.chapters.length ? '<button class="btn alt" data-tab="plan">View my plan</button>' : ''}`;
}
function viewSaved() {
  if (!S.subjects.length) return back + '<div class="card empty"><p>No saved data yet. Use option 1 or 2 to add some.</p></div>';
  return back + `<div class="card"><h2>Subjects</h2>${S.subjects.map(s => `<div class="row"><span>${esc(s.name)} · ${s.type === 'goal' ? 'Goal' : 'Exam'}: ${s.exam}</span><button class="btn alt small" data-act="editSub" data-id="${s.id}">Edit date</button><button class="btn red small" data-act="delSub" data-id="${s.id}">Delete</button></div>`).join('')}</div>
  <div class="card"><h2>Chapters</h2><p class="note">Tick the box when you finish a chapter. Its line will be cut.</p>${S.chapters.map(c => `<div class="row"><input type="checkbox" data-act="togChap" data-id="${c.id}" ${c.done ? 'checked' : ''} aria-label="Chapter completed"><span class="${c.done ? 'done' : ''}">${esc(subj(c.subjectId).name)} › ${esc(c.name)}<br>Importance ${c.imp} · Test ${c.test == null ? '-' : c.test} · ${c.hours}h · Priority ${priority(c).toFixed(0)} · <span class="tag">${c.src}</span></span>
  <button class="btn alt small" data-act="editChap" data-id="${c.id}">Edit</button><button class="btn red small" data-act="delChap" data-id="${c.id}">Delete</button></div>`).join('') || '<p>No chapters yet.</p>'}</div>
  <button class="btn alt" data-tab="plan">View my plan</button>`;
}

function viewPlan() {
  const ch = S.chapters;
  if (!S.subjects.length || !ch.length) return `<div class="card empty"><h2>No plan yet</h2><p>Add your subjects and chapters to get a study plan, or try the demo.</p><button class="btn big" data-tab="home">Get Started</button><button class="btn alt" data-act="demo">Load Demo Data</button></div>`;
  const done = ch.filter(c => c.done).length, rem = ch.reduce((a, c) => a + remH(c), 0);
  if (done === ch.length) return '<div class="card empty"><h2>🏆 All chapters completed!</h2><p>Great work. Check your badges in the Charts tab.</p></div>';
  const lim = view === 'today' ? 0 : view === 'week' ? 6 : 1e9;
  const dates = [...new Set(S.sessions.map(x => x.date))].filter(k => { const n = daysTo(k); return n >= 0 && n <= lim; }).sort();
  const filt = [['today', 'Today'], ['week', 'This week'], ['all', 'All']].map(([v, l]) => `<button class="btn alt ${view === v ? 'on' : ''}" data-act="view" data-id="${v}">${l}</button>`).join('');
  return `<div class="card"><h2>Hello${S.profile.name ? ', ' + esc(S.profile.name) : ''}! ${S.demo ? '(Demo data - fictional)' : ''}</h2>
  <p>${done} of ${ch.length} chapters done · ${rem.toFixed(1)} hours left · 🔥 ${streak()} day streak</p>${bar(pct(done, ch.length))}</div>
  ${countdown()}${warnBox()}<div class="card">${filt}<button class="btn" data-act="plan">Regenerate</button></div>
  ${dates.map(k => `<div class="card"><h2>${dl(k)}</h2>${dayList(k).map(sessRow).join('')}</div>`).join('') || `<div class="card">No sessions ${view === 'today' ? 'today' : 'in this range'}.</div>`}
  <div class="card"><h2>Upcoming exams and goals</h2>${S.subjects.slice().sort((a, b) => a.exam.localeCompare(b.exam)).map(s => `<div class="row"><span>${esc(s.name)} (${s.type === 'goal' ? 'goal' : 'exam'})</span><span>${s.exam} (${daysTo(s.exam) >= 0 ? daysTo(s.exam) + ' days left' : 'finished'})</span></div>`).join('')}</div>`;
}

function viewProgress() {
  const ch = S.chapters, done = ch.filter(c => c.done).length, hrs = S.sessions.reduce((a, x) => a + (x.done ? x.mins : 0), 0) / 60;
  return `<div class="card"><h2>Overall: ${pct(done, ch.length).toFixed(0)}%</h2>${bar(pct(done, ch.length))}<p>Study hours completed: ${hrs.toFixed(1)} · Hours left: ${ch.reduce((a, c) => a + remH(c), 0).toFixed(1)}</p></div>
  ${S.subjects.map(s => { const cs = ch.filter(c => c.subjectId === s.id), d = cs.filter(c => c.done).length;
    return `<div class="card"><h2>${esc(s.name)} (${d}/${cs.length})</h2>${bar(pct(d, cs.length))}${cs.map(c => `<div class="row"><input type="checkbox" data-act="togChap" data-id="${c.id}" ${c.done ? 'checked' : ''} aria-label="Chapter completed"><span class="${c.done ? 'done' : ''}">${esc(c.name)}</span><span>Test: ${c.test == null ? '-' : c.test + '%'}</span></div>`).join('')}</div>`; }).join('') || '<div class="card empty">No data yet.</div>'}`;
}

// ---------- Charts tab ----------
function donut(p) {
  const r = 52, c = 2 * Math.PI * r;
  return `<svg viewBox="0 0 140 140" width="170" height="170" role="img" aria-label="${p.toFixed(0)} percent complete"><circle cx="70" cy="70" r="${r}" fill="none" stroke="var(--line)" stroke-width="16"/>
  <circle cx="70" cy="70" r="${r}" fill="none" stroke="var(--blue)" stroke-width="16" stroke-linecap="round" stroke-dasharray="${(p / 100 * c).toFixed(1)} ${c.toFixed(1)}" transform="rotate(-90 70 70)"/>
  <text x="70" y="76" text-anchor="middle" class="v" style="font-size:24px;font-family:var(--head)">${p.toFixed(0)}%</text></svg>`;
}
function weekChart() {
  const vals = [], labs = [];
  for (let i = -6; i <= 0; i++) { vals.push(minsOn(dayKey(i))); labs.push(i === 0 ? 'Today' : DAYS[parse(dayKey(i)).getDay()]); }
  const max = Math.max(30, ...vals);
  return `<svg class="chart" viewBox="0 0 350 180" role="img" aria-label="Study minutes in the last 7 days"><line x1="10" y1="140" x2="340" y2="140" stroke="var(--line)"/>
  ${vals.map((v, i) => { const h = v / max * 105, x = 16 + i * 47; return `<rect x="${x}" y="${140 - h}" width="34" height="${h}" rx="6" fill="${i === 6 ? 'var(--saffron)' : 'var(--blue)'}"/>
  <text x="${x + 17}" y="${134 - h}" text-anchor="middle" class="v">${v || ''}</text><text x="${x + 17}" y="158" text-anchor="middle">${labs[i]}</text>`; }).join('')}</svg>`;
}
function viewCharts() {
  const ch = S.chapters;
  if (!S.subjects.length || !ch.length) return `<div class="card empty"><h2>No charts yet</h2><p>Add subjects and chapters to see your progress as graphs, or try the demo.</p><button class="btn big" data-tab="home">Get Started</button><button class="btn alt" data-act="demo">Load Demo Data</button></div>`;
  const done = ch.filter(c => c.done).length, p = pct(done, ch.length);
  const doneH = S.sessions.reduce((a, x) => a + (x.done ? x.mins : 0), 0) / 60, totH = ch.reduce((a, c) => a + c.hours, 0);
  const scored = ch.filter(c => c.test != null), avg = scored.length ? scored.reduce((a, c) => a + c.test, 0) / scored.length : null;
  const subs = S.subjects.map(s => { const cs = ch.filter(c => c.subjectId === s.id); return { s, n: cs.length, d: cs.filter(c => c.done).length, plan: cs.reduce((a, c) => a + c.hours, 0), got: S.sessions.filter(x => x.done && cs.some(c => c.id === x.chapId)).reduce((a, x) => a + x.mins, 0) / 60 }; });
  return `<div class="card"><h2>📊 Overall progress</h2><div class="chart-wrap">${donut(p)}
    <div class="grid" style="flex:1 1 220px"><div class="stat"><b>${done}/${ch.length}</b>chapters done</div><div class="stat"><b>🔥 ${streak()}</b>day streak</div><div class="stat"><b>${doneH.toFixed(1)}h</b>of ${totH.toFixed(1)}h studied</div><div class="stat"><b>${avg == null ? '-' : avg.toFixed(0) + '%'}</b>average test score</div></div></div></div>
  <div class="card"><h2>Bar graph: chapters finished by subject</h2>${subs.map(o => `<div class="hb"><div class="hl"><span>${esc(o.s.name)}</span><b>${o.d}/${o.n} (${pct(o.d, o.n).toFixed(0)}%)</b></div>${bar(pct(o.d, o.n))}</div>`).join('')}</div>
  <div class="card"><h2>Study minutes: last 7 days</h2><div class="chart-wrap">${weekChart()}</div><p class="note">Includes finished plan sessions and Focus timer minutes.</p></div>
  <div class="card"><h2>Planned hours vs studied hours</h2><div class="legend"><span><i style="background:var(--saffron)"></i>Planned</span><span><i style="background:var(--blue)"></i>Studied</span></div>
  ${subs.map(o => { const m = Math.max(o.plan, o.got, .1); return `<div class="hb two"><div class="hl"><span>${esc(o.s.name)}</span><b>${o.got.toFixed(1)}h / ${o.plan.toFixed(1)}h</b></div><div class="bar"><i class="b2" style="width:${o.plan / m * 100}%"></i></div><div class="bar"><i style="width:${o.got / m * 100}%"></i></div></div>`; }).join('')}</div>
  <div class="card"><h2>Practice test scores</h2>${scored.length ? scored.map(c => `<div class="hb"><div class="hl"><span>${esc(c.name)}</span><b>${c.test}%</b></div>${bar(c.test, c.test < 50 ? 'r' : c.test < 80 ? 'a' : 'g')}</div>`).join('') + '<p class="note">Red: below 50 · Amber: 50 to 79 · Green: 80 and above</p>' : '<p>No test scores yet. Add a score to a chapter (Home › option 3 › Edit) to see this chart.</p>'}</div>
  <div class="card"><h2>🏅 Your badges</h2><div class="badges">${badges().map(b => `<div class="badge ${b[3] ? 'on' : ''}"><b>${b[0]}</b>${b[1]}<br><span class="note">${b[2]}</span></div>`).join('')}</div></div>`;
}

// ---------- Focus timer (Pomodoro) ----------
const MODES = { focus: ['Focus', 25], short: ['Short break', 5], long: ['Long break', 15] };
let T = { mode: 'focus', left: 25 * 60, run: false, id: null };
const tTotal = () => MODES[T.mode][1] * 60;
function tDraw() {
  const el = $('tm'); if (!el) return;
  el.firstChild.textContent = String(Math.floor(T.left / 60)).padStart(2, '0') + ':' + String(T.left % 60).padStart(2, '0');
  const c = 2 * Math.PI * 96; $('tr').setAttribute('stroke-dasharray', ((1 - T.left / tTotal()) * c).toFixed(1) + ' ' + c.toFixed(1));
}
function tTick() {
  T.left--; tDraw();
  if (T.left > 0) return;
  clearInterval(T.id); T.run = false;
  if (T.mode === 'focus') { const k = fmt(today()); S.focus[k] = (S.focus[k] || 0) + MODES.focus[1]; save(); msg('Focus session complete! +25 minutes. Take a break.'); T.mode = 'short'; }
  else { msg('Break over. Ready for the next focus round?'); T.mode = 'focus'; }
  T.left = tTotal(); if (tab === 'focus') render();
}
function viewFocus() {
  const k = fmt(today()), c = 2 * Math.PI * 96;
  return `<div class="card timer"><h2>⏱️ Focus timer</h2><p class="note">Study for 25 minutes, then rest. Finished rounds are added to your charts.</p>
  <div>${Object.keys(MODES).map(m => `<button class="btn alt small ${T.mode === m ? 'on' : ''}" data-act="tMode" data-id="${m}">${MODES[m][0]}</button>`).join('')}</div>
  <div class="ring"><svg viewBox="0 0 220 220"><circle cx="110" cy="110" r="96" fill="none" stroke="var(--line)" stroke-width="14"/><circle id="tr" cx="110" cy="110" r="96" fill="none" stroke="var(--saffron)" stroke-width="14" stroke-linecap="round" stroke-dasharray="${((1 - T.left / tTotal()) * c).toFixed(1)} ${c.toFixed(1)}"/></svg>
  <div class="t" id="tm">00:00<small>${MODES[T.mode][0]}</small></div></div>
  <button class="btn big gold" data-act="tToggle">${T.run ? 'Pause' : 'Start'}</button><button class="btn alt big" data-act="tReset">Reset</button></div>
  <div class="card"><div class="grid g3"><div class="stat"><b>${S.focus[k] || 0}</b>focus minutes today</div><div class="stat"><b>${focusTotal()}</b>total focus minutes</div><div class="stat"><b>🔥 ${streak()}</b>day streak</div></div></div>${quoteCard()}`;
}

// ---------- Team tab ----------
function viewTeam() {
  return heroCard(false) + `<div class="card"><h2>About our project</h2>
  <p><b>Theme:</b> Artificial Intelligence for Better Life.</p>
  <p><b>Event:</b> RSBVP, राज्य स्तरीय बाल वैज्ञानिक प्रदर्शनी 2026-27.</p>
  <p><b>What ExamPlan does:</b> It builds a daily study plan from your exam dates, chapter importance and practice test scores. Each chapter gets a priority score, and the scheduler studies the most urgent chapters first.</p>
  <p><b>How AI helps life:</b> A good plan saves time, lowers exam stress and lets every student learn at their own pace.</p>
  <p class="note">Priority = 40% urgency + 25% importance + 35% need from test score.</p></div>`;
}

function render() {
  document.querySelectorAll('#nav button').forEach(b => b.classList.toggle('on', b.dataset.tab === tab));
  const v = { home: viewHome, plan: viewPlan, progress: viewProgress, charts: viewCharts, focus: viewFocus, team: viewTeam }[tab];
  try { $('view').innerHTML = v(); if (tab === 'focus') tDraw(); } catch (e) { $('view').innerHTML = '<div class="card">Something went wrong. Try Reset all data at the bottom of the page.</div>'; console.error(e); }
}

// ---------- Forms ----------
const addChapter = (sb, name, imp, hours, test, src) => S.chapters.push({ id: uid(), subjectId: sb.id, name, imp, hours, test, done: false, src, lastP: null, snap: null });
function pickDate(f) {
  let date = f.exam.value;
  if (f.type.value === 'goal' && !date) { const g = today(); g.setDate(g.getDate() + 30); date = fmt(g); }
  return validDate(date) && daysTo(date) >= 1 ? date : null;
}
const forms = {
  fProfile(f) {
    const hours = num(f.hours.value, 0.5, 8);
    if (hours === null) return msg('Hours must be between 0.5 and 8', 'err');
    S.profile = { name: f.name.value.trim(), cls: f.cls.value, hours, off: [...f.querySelectorAll('[name=off]:checked')].map(x => +x.value) };
    qa.cls = S.profile.cls;
    if (S.stage < 2) { S.stage = 2; tab = 'home'; page = ''; }
    changed('Details saved');
  },
  fSyl(f) {
    const type = f.type.value, date = pickDate(f);
    if (!date) return msg('Please choose a date after today', 'err');
    const data = SYLLABUS[f.cls.value.split('|')[0]] || {};
    const picks = [...f.querySelectorAll('input[name=ch]:checked')];
    if (!picks.length) return msg('Tick at least one chapter', 'err');
    let added = 0;
    picks.forEach(pk => {
      const [n, k] = pk.value.split('||'), cn = (data[n] || [])[+k];
      if (!cn) return;
      let sb = S.subjects.find(x => x.name === n);
      if (!sb) { sb = { id: uid(), name: n, exam: date, type, src: 'syllabus' }; S.subjects.push(sb); }
      if (S.chapters.some(c => c.subjectId === sb.id && c.name === cn)) return;
      addChapter(sb, cn, 3, 2, null, 'syllabus'); added++;
    });
    tab = 'plan'; changed(added + ' chapters added');
  },
  fSub(f) {
    const name = f.name.value.trim(), date = pickDate(f);
    if (!name) return msg('Please enter a subject name', 'err');
    if (!date) return msg('Please choose a date after today', 'err');
    S.subjects.push({ id: uid(), name, exam: date, type: f.type.value, src: 'manual' }); changed('Subject added');
  },
  fChap(f) {
    const name = f.name.value.trim(), imp = num(f.imp.value, 1, 5), hours = num(f.hours.value, 0.25, 100);
    const raw = f.test.value.trim(), test = raw === '' ? null : num(raw, 0, 100), sb = subj(f.sub.value);
    if (!name || !sb) return msg('Please enter a chapter name', 'err');
    if (imp === null) return msg('Importance must be between 1 and 5', 'err');
    if (hours === null) return msg('Hours must be 0.25 or more', 'err');
    if (raw !== '' && test === null) return msg('Test score must be between 0 and 100', 'err');
    addChapter(sb, name, imp, hours, test, 'manual'); changed('Chapter added');
  }
};
document.addEventListener('submit', e => { e.preventDefault(); const h = forms[e.target.id]; if (h) h(e.target); });
document.addEventListener('change', e => {
  const f = e.target.closest && e.target.closest('#fSyl');
  if (!f || e.target.name === 'ch') return;
  qa = { cls: f.cls.value, type: f.type.value, exam: f.exam.value };
  if (e.target.name === 'cls') render();
});

// ---------- Buttons ----------
const acts = {
  start() { S.stage = 1; save(); render(); window.scrollTo(0, 0); },
  go(id) { page = id || ''; render(); window.scrollTo(0, 0); },
  view(id) { view = id; render(); },
  editProfile() { S.stage = 1; render(); window.scrollTo(0, 0); },
  selOn(id) { document.querySelectorAll('#fSyl input[name=ch]').forEach(c => { if (c.dataset.s === id) c.checked = true; }); },
  selOff(id) { document.querySelectorAll('#fSyl input[name=ch]').forEach(c => { if (c.dataset.s === id) c.checked = false; }); },
  plan: () => changed('Plan regenerated'),
  togSess(id) { const x = S.sessions.find(y => y.id === id); if (x) { x.done = !x.done; save(); render(); if (x.done) msg('Session done! Keep going 🔥'); } },
  togChap(id) { const c = S.chapters.find(y => y.id === id); if (c) { c.done = !c.done; changed(c.done ? 'Chapter completed! 🎉' : 'Chapter updated'); } },
  delChap(id) { if (!confirm('Delete this chapter?')) return; S.chapters = S.chapters.filter(c => c.id !== id); S.sessions = S.sessions.filter(x => x.chapId !== id); changed('Chapter deleted'); },
  delSub(id) {
    if (!confirm('This subject and all its chapters will be deleted. Are you sure?')) return;
    const ids = S.chapters.filter(c => c.subjectId === id).map(c => c.id);
    S.subjects = S.subjects.filter(s => s.id !== id); S.chapters = S.chapters.filter(c => c.subjectId !== id);
    S.sessions = S.sessions.filter(x => !ids.includes(x.chapId)); changed('Subject deleted');
  },
  editSub(id) {
    const s = subj(id), v = prompt('New date (YYYY-MM-DD)', s.exam);
    if (v === null) return;
    if (!validDate(v) || daysTo(v) < 1) return msg('The date is invalid or in the past', 'err');
    s.exam = v; changed('Date updated');
  },
  editChap(id) {
    const c = S.chapters.find(y => y.id === id);
    const imp = num(prompt('Importance (1-5)', c.imp), 1, 5), hours = num(prompt('Estimated hours', c.hours), 0.25, 100);
    const t = prompt('Practice test score 0-100 (leave empty if none)', c.test == null ? '' : c.test);
    if (imp === null || hours === null || t === null) return msg('Edit cancelled or value invalid', 'err');
    const test = t.trim() === '' ? null : num(t, 0, 100);
    if (t.trim() !== '' && test === null) return msg('Test score must be between 0 and 100', 'err');
    Object.assign(c, { imp, hours, test }); changed('Chapter updated and plan regenerated');
  },
  tToggle() {
    if (T.run) { clearInterval(T.id); T.run = false; } else { T.run = true; T.id = setInterval(tTick, 1000); }
    render();
  },
  tReset() { clearInterval(T.id); T.run = false; T.left = tTotal(); render(); },
  tMode(id) { clearInterval(T.id); T.run = false; T.mode = id; T.left = tTotal(); render(); },
  reset() { if (!confirm('All ExamPlan data will be deleted. Are you sure?')) return; try { localStorage.removeItem(KEY); } catch (e) {} S = blank(); tab = 'home'; page = ''; render(); msg('Data has been reset'); },
  demo() {
    if ((S.subjects.length || S.chapters.length) && !confirm('Loading demo data will replace your current data. Continue?')) return;
    const add = n => { const d = today(); d.setDate(d.getDate() + n); return fmt(d); };
    const sc = [['Maths (demo)', 10, [['Algebra', 5, 4, 40], ['Geometry', 4, 3, null], ['Mensuration', 3, 2, 75]]],
      ['Science (demo)', 20, [['Force and Motion', 5, 3, 35], ['Light', 4, 2, null], ['Cells', 3, 2, 90]]],
      ['English (demo)', 35, [['Grammar', 3, 2, 60], ['Essay Writing', 4, 3, null]]]];
    S = blank(); S.stage = 2; S.demo = true; S.profile = { name: 'Demo Student (fictional)', cls: '9', hours: 2, off: [0] };
    sc.forEach(([n, d, cs]) => { const sb = { id: uid(), name: n, exam: add(d), type: n.startsWith('English') ? 'goal' : 'exam', src: 'manual' }; S.subjects.push(sb);
      cs.forEach(([cn, imp, hours, test]) => addChapter(sb, cn, imp, hours, test, 'manual')); });
    tab = 'charts'; changed('Demo data loaded (fictional)');
  }
};
document.addEventListener('click', e => {
  const t = e.target.closest('[data-tab],[data-act]'); if (!t) return;
  if (t.dataset.tab) { tab = t.dataset.tab; if (tab === 'home') page = ''; render(); window.scrollTo(0, 0); }
  else if (acts[t.dataset.act]) acts[t.dataset.act](t.dataset.id);
});

load(); qa.cls = S.profile.cls; render();
</script>
</body>
</html>
