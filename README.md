<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="ExamPlan - a smart study planner. Project RSBVP by Anshul, Kendriya Vidyalaya Mandi.">
<meta name="theme-color" content="#1e3a8a">
<title>ExamPlan | Project RSBVP - Anshul, Kendriya Vidyalaya Mandi</title>
<style>
/* ExamPlan - Project RSBVP by Anshul, Kendriya Vidyalaya Mandi */
:root{
  --navy:#1e3a8a;--blue:#2563eb;--sky:#60a5fa;--violet:#7c3aed;
  --bg:#f1f5fb;--card:#fff;--ink:#0f172a;--muted:#64748b;--line:#e2e8f0;
  --green:#16a34a;--red:#dc2626;--amber:#d97706;
  --shadow:0 1px 2px rgba(15,23,42,.06),0 8px 24px rgba(30,58,138,.08);
  --grad:linear-gradient(135deg,#1e3a8a 0%,#2563eb 55%,#7c3aed 100%);
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;font-family:"Segoe UI",system-ui,-apple-system,Roboto,Arial,sans-serif;background:var(--bg);color:var(--ink);font-size:16px;line-height:1.55;overflow-wrap:anywhere}

/* ---- School bar + header ---- */
.school-bar{background:#0f1f4d;color:#fff;text-align:center;padding:9px 12px;font-weight:700;letter-spacing:.04em;font-size:.95rem;text-transform:uppercase}
.school-icon{margin-right:6px}
.site-header{background:var(--grad);color:#fff;padding:18px 14px 16px;box-shadow:0 4px 18px rgba(30,58,138,.3)}
.header-inner{max-width:860px;margin:0 auto}
.logo{margin:0;font-size:1.8rem;font-weight:800;letter-spacing:-.02em;color:#fff}
.logo-mark{display:inline-block;margin-right:4px}
.tagline{margin:2px 0 14px;opacity:.9;font-size:.95rem}
.tagline b{background:rgba(255,255,255,.2);padding:1px 8px;border-radius:99px}
nav{display:flex;flex-wrap:wrap;gap:8px}
nav button{border:1px solid rgba(255,255,255,.35);background:rgba(255,255,255,.12);color:#fff;padding:10px 16px;min-height:44px;border-radius:99px;font-size:.95rem;font-weight:600;cursor:pointer;transition:.2s}
nav button:hover{background:rgba(255,255,255,.25)}
nav button.on{background:#fff;color:var(--navy);border-color:#fff;box-shadow:0 4px 12px rgba(0,0,0,.18)}
.intro{margin:0;padding:12px 14px;background:#eaf0ff;border-bottom:1px solid #d3defa;text-align:center;color:#1e3a8a;font-size:.95rem}

/* ---- Layout / cards ---- */
main{max-width:860px;margin:0 auto;padding:16px 12px}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:18px;margin-bottom:14px;box-shadow:var(--shadow)}
.card.empty{text-align:center}
h2{margin:0 0 10px;font-size:1.15rem;color:var(--navy)}
p{margin:0 0 10px}
.note{font-size:.85rem;color:var(--muted);margin:4px 0}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px}
.stat{border:1px solid var(--line);border-radius:12px;padding:10px;text-align:center;background:#f8fafc}
.stat b{display:block;font-size:1.3rem;color:var(--blue)}
@media(min-width:700px){.grid{grid-template-columns:repeat(3,1fr)}}

/* ---- Welcome hero ---- */
.center{text-align:center;padding:38px 18px;background:var(--grad);color:#fff;border:0;border-radius:20px}
.center h1{margin:0 0 10px;font-size:1.9rem;color:#fff;letter-spacing:-.02em}
.center p{opacity:.95;max-width:480px;margin:0 auto 14px}
.center .btn{background:#fff;color:var(--navy);box-shadow:0 8px 20px rgba(0,0,0,.25)}
.hero-badges{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin:0 0 18px}
.hero-badges span{background:rgba(255,255,255,.18);border:1px solid rgba(255,255,255,.3);padding:4px 12px;border-radius:99px;font-size:.85rem}

/* ---- Buttons ---- */
.btn{background:var(--blue);color:#fff;border:0;border-radius:12px;padding:10px 16px;min-height:44px;font-size:1rem;font-weight:600;margin:3px 4px 3px 0;cursor:pointer;transition:transform .15s,box-shadow .15s,background .15s;box-shadow:0 4px 12px rgba(37,99,235,.28)}
.btn:hover{background:#1d4ed8;transform:translateY(-1px)}
.btn:active{transform:translateY(0)}
.btn.alt{background:#fff;color:var(--blue);border:1.5px solid var(--blue);box-shadow:none}
.btn.alt:hover{background:#eff6ff}
.btn.alt.on{background:var(--blue);color:#fff}
.btn.red{background:var(--red);box-shadow:0 4px 12px rgba(220,38,38,.25)}
.btn.red:hover{background:#b91c1c}
.small{min-height:36px;padding:6px 12px;font-size:.85rem;border-radius:10px}
.big{font-size:1.05rem;padding:14px 24px}
button:focus-visible,input:focus-visible,select:focus-visible,textarea:focus-visible{outline:3px solid #93c5fd;outline-offset:2px}

/* ---- Forms ---- */
label{display:block;margin:12px 0 4px;font-weight:600;font-size:.9rem;color:#334155}
input,select,textarea{width:100%;padding:11px 12px;border:1.5px solid #cbd5e1;border-radius:10px;font-size:1rem;background:#fff;color:var(--ink);font-family:inherit;transition:border-color .15s,box-shadow .15s}
input:focus,select:focus,textarea:focus{border-color:var(--blue);box-shadow:0 0 0 3px rgba(37,99,235,.15)}
input[type=checkbox]{width:22px;height:22px;flex:0 0 auto;accent-color:var(--blue);cursor:pointer}
textarea{min-height:110px}
.days label{display:inline-flex;gap:5px;align-items:center;margin:4px 10px 4px 0;font-weight:500}
.chk{display:flex;gap:10px;align-items:center;font-weight:400;margin:6px 0}
details{border:1px solid var(--line);border-radius:12px;padding:10px 12px;margin:10px 0;background:#f8fafc}
summary{padding:6px 0;cursor:pointer;color:var(--navy)}

/* ---- Rows, tags, progress ---- */
.row{display:flex;gap:10px;align-items:center;padding:10px 0;border-bottom:1px solid #eef2f7;flex-wrap:wrap}
.row:last-child{border-bottom:0}
.row>span{flex:1 1 180px}
.bar{background:#e2e8f0;height:12px;border-radius:99px;overflow:hidden;margin:6px 0}
.bar i{display:block;height:100%;background:linear-gradient(90deg,var(--blue),var(--violet));border-radius:99px;transition:width .5s ease}
.tag{background:#eff6ff;border:1px solid #bfdbfe;color:#1d4ed8;border-radius:99px;padding:1px 9px;font-size:.78rem;font-weight:600}
.done{text-decoration:line-through;color:#94a3b8}
.warn{border-left:5px solid var(--amber);background:#fffbeb;border-radius:10px;padding:10px 12px;margin:8px 0;font-size:.92rem}

/* ---- Toast ---- */
#msg{position:fixed;left:12px;right:12px;bottom:14px;max-width:520px;margin:0 auto;z-index:9;padding:13px 16px;border-radius:14px;color:#fff;text-align:center;font-weight:600;box-shadow:0 10px 30px rgba(0,0,0,.25);animation:pop .25s ease}
#msg.ok{background:var(--green)}#msg.err{background:var(--red)}#msg.hide{display:none}
@keyframes pop{from{transform:translateY(14px);opacity:0}to{transform:none;opacity:1}}

/* ---- Footer ---- */
footer{padding:10px 12px 70px}
.foot-card{max-width:860px;margin:0 auto;text-align:center;background:#0f1f4d;color:#cbd5e1;border-radius:18px;padding:20px 16px;font-size:.9rem}
.foot-card p{margin:0 0 6px}
.foot-title{color:#fff;font-weight:800;font-size:1.05rem}
.foot-card b{color:#fff}
.foot-note{opacity:.8;margin-bottom:12px!important}

@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}

</style>
</head>
<body>

<div class="school-bar">
  <span class="school-icon" aria-hidden="true">🏫</span>
  <span class="school-name">Kendriya Vidyalaya Mandi</span>
</div>

<header class="site-header">
  <div class="header-inner">
    <div class="brand">
      <h1 class="logo"><span class="logo-mark" aria-hidden="true">📚</span> ExamPlan</h1>
      <p class="tagline">Smart study planner &middot; Project <b>RSBVP</b></p>
    </div>
    <nav id="nav" aria-label="Main">
      <button data-tab="home">🏠 Home</button>
      <button data-tab="plan">📅 My Plan</button>
      <button data-tab="progress">📈 Progress</button>
    </nav>
  </div>
</header>

<p class="intro">
  Hi, I am <b>Anshul</b>. I created this website for my project <b>RSBVP</b> at <b>Kendriya Vidyalaya Mandi</b>.
</p>

<div id="msg" class="hide" role="status"></div>
<main id="view"></main>

<footer>
  <div class="foot-card">
    <p class="foot-title">ExamPlan &middot; Project RSBVP</p>
    <p>Created by <b>Anshul</b> &middot; Kendriya Vidyalaya Mandi</p>
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
/* ExamPlan - flow: Get Started > About you > 3 ways to add data > My Plan */

// ---------- Helpers ----------
const KEY = 'examplan_v3', $ = id => document.getElementById(id);
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
// Class choices. For 11 and 12 the stream (PCM / PCB / PCMB) is part of the choice.
const CLASSES = [['5', 'Class 5'], ['6', 'Class 6'], ['7', 'Class 7'], ['8', 'Class 8'], ['9', 'Class 9'], ['10', 'Class 10'],
  ['11|PCM', 'Class 11 (PCM)'], ['11|PCB', 'Class 11 (PCB)'], ['11|PCMB', 'Class 11 (PCMB)'],
  ['12|PCM', 'Class 12 (PCM)'], ['12|PCB', 'Class 12 (PCB)'], ['12|PCMB', 'Class 12 (PCMB)']];
const clsName = v => (CLASSES.find(c => c[0] === v) || [v, 'Class ' + v])[1];
const STREAMS = { PCM: ['Physics', 'Chemistry', 'Mathematics'], PCB: ['Physics', 'Chemistry', 'Biology'], PCMB: ['Physics', 'Chemistry', 'Mathematics', 'Biology'] };
let S, tab = 'home', page = '', view = 'today';       // page: '' (3 options) | 'syl' | 'man' | 'saved'
let qa = { cls: '10', type: 'exam', exam: '' };        // remembers the syllabus form choices
function msg(t, k) { const m = $('msg'); m.textContent = t; m.className = k || 'ok'; clearTimeout(msg.t); msg.t = setTimeout(() => m.className = 'hide', 4500); }

// ---------- Storage (touches only the ExamPlan key) ----------
const blank = () => ({ stage: 0, profile: { name: '', cls: '10', hours: 2, off: [] }, subjects: [], chapters: [], sessions: [], notes: [], warn: [], demo: false });
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
  } catch (e) { S = blank(); msg('Saved data could not be read, starting fresh', 'err'); }
}
function save() { try { localStorage.setItem(KEY, JSON.stringify(S)); } catch (e) { msg('Could not save data', 'err'); } }

// ---------- Math model: P = 100 x (0.40 U + 0.25 M + 0.35 N) (weights are project assumptions) ----------
// U = urgency (closer deadline = higher), M = importance, N = need from test score (no score = neutral 0.5, never 0).
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
  S.sessions = S.sessions.filter(x => x.done);          // keep completed work, rebuild the rest
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
      const d = days[j], m = Math.min(d.free, 60, it.rem);   // max 60 minutes per session
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

// ---------- Small view helpers ----------
const bar = p => `<div class="bar"><i style="width:${Math.round(p)}%"></i></div>`;
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

// ---------- Screens ----------
function aboutCard(title, button) {
  const p = S.profile;
  return `<div class="card"><h2>${title}</h2><form id="fProfile">
  <label>Name (optional)</label><input name="name" maxlength="40" value="${esc(p.name)}">
  <label>Class</label><select name="cls">${CLASSES.map(c => opt(c[0], c[1], p.cls)).join('')}</select>
  <label>Daily study hours (0.5 - 8)</label><input name="hours" type="number" step="0.5" value="${p.hours}">
  <label>Unavailable days</label><div class="days">${DAYS.map((d, i) => `<label><input type="checkbox" name="off" value="${i}" ${p.off.includes(i) ? 'checked' : ''}>${d}</label>`).join('')}</div>
  <button class="btn big">${button}</button></form></div>`;
}

function viewHome() {
  if (S.stage === 0) return `<div class="card center"><h1>Welcome to ExamPlan</h1><div class="hero-badges"><span>Project RSBVP</span><span>by Anshul</span><span>Kendriya Vidyalaya Mandi</span></div><p>Make a smart study plan for your exams or your syllabus goal. Add your chapters, and ExamPlan decides what to study each day.</p><button class="btn big" data-act="start">Get Started</button></div>`;
  if (S.stage === 1) return aboutCard('Step 1: About you', 'Continue');
  if (page === 'syl') return viewSyl();
  if (page === 'man') return viewMan();
  if (page === 'saved') return viewSaved();
  return `<div class="card"><h2>Step 2: Add your data</h2><p>${S.profile.name ? 'Hello, ' + esc(S.profile.name) + '. ' : ''}${clsName(S.profile.cls)}. Choose one option.</p></div>
  <div class="card"><h2>1. Add data from syllabus</h2><p>Pick subjects and chapters that are already listed for your class.</p><button class="btn big" data-act="go" data-id="syl">Open</button></div>
  <div class="card"><h2>2. Add data manually</h2><p>Type your own subjects and chapters.</p><button class="btn big" data-act="go" data-id="man">Open</button></div>
  <div class="card"><h2>3. Load saved data</h2><p>See, edit or delete the subjects and chapters you saved before.</p><button class="btn big" data-act="go" data-id="saved">Open</button></div>
  ${S.chapters.length ? '<button class="btn alt" data-tab="plan">View my plan</button>' : ''}`;
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
  if (done === ch.length) return '<div class="card empty"><h2>All chapters completed!</h2></div>';
  const lim = view === 'today' ? 0 : view === 'week' ? 6 : 1e9;
  const dates = [...new Set(S.sessions.map(x => x.date))].filter(k => { const n = daysTo(k); return n >= 0 && n <= lim; }).sort();
  const filt = [['today', 'Today'], ['week', 'This week'], ['all', 'All']].map(([v, l]) => `<button class="btn alt ${view === v ? 'on' : ''}" data-act="view" data-id="${v}">${l}</button>`).join('');
  return `<div class="card"><h2>Hello${S.profile.name ? ', ' + esc(S.profile.name) : ''}! ${S.demo ? '(Demo data - fictional)' : ''}</h2>
  <p>${done} of ${ch.length} chapters done · ${rem.toFixed(1)} hours left</p>${bar(pct(done, ch.length))}</div>
  ${warnBox()}<div class="card">${filt}<button class="btn" data-act="plan">Regenerate</button></div>
  ${dates.map(k => `<div class="card"><h2>${dl(k)}</h2>${dayList(k).map(sessRow).join('')}</div>`).join('') || `<div class="card">No sessions ${view === 'today' ? 'today' : 'in this range'}.</div>`}
  <div class="card"><h2>Upcoming exams and goals</h2>${S.subjects.slice().sort((a, b) => a.exam.localeCompare(b.exam)).map(s => `<div class="row"><span>${esc(s.name)} (${s.type === 'goal' ? 'goal' : 'exam'})</span><span>${s.exam} (${daysTo(s.exam) >= 0 ? daysTo(s.exam) + ' days left' : 'finished'})</span></div>`).join('')}</div>`;
}

function viewProgress() {
  const ch = S.chapters, done = ch.filter(c => c.done).length, hrs = S.sessions.reduce((a, x) => a + (x.done ? x.mins : 0), 0) / 60;
  return `<div class="card"><h2>Overall: ${pct(done, ch.length).toFixed(0)}%</h2>${bar(pct(done, ch.length))}<p>Study hours completed: ${hrs.toFixed(1)} · Hours left: ${ch.reduce((a, c) => a + remH(c), 0).toFixed(1)}</p></div>
  ${S.subjects.map(s => { const cs = ch.filter(c => c.subjectId === s.id), d = cs.filter(c => c.done).length;
    return `<div class="card"><h2>${esc(s.name)} (${d}/${cs.length})</h2>${bar(pct(d, cs.length))}${cs.map(c => `<div class="row"><input type="checkbox" data-act="togChap" data-id="${c.id}" ${c.done ? 'checked' : ''} aria-label="Chapter completed"><span class="${c.done ? 'done' : ''}">${esc(c.name)}</span><span>Test: ${c.test == null ? '-' : c.test + '%'}</span></div>`).join('')}</div>`; }).join('') || '<div class="card empty">No data yet.</div>'}`;
}

function render() {
  document.querySelectorAll('#nav button').forEach(b => b.classList.toggle('on', b.dataset.tab === tab));
  const v = { home: viewHome, plan: viewPlan, progress: viewProgress }[tab];
  try { $('view').innerHTML = v(); } catch (e) { $('view').innerHTML = '<div class="card">Something went wrong. Try Reset all data at the bottom of the page.</div>'; console.error(e); }
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
    if (typeof SYLLABUS === 'undefined') return msg('syllabus.js is not loaded. Check that it is in the same folder as index.html', 'err');
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
document.addEventListener('change', e => {              // changing the class redraws the chapter list
  const f = e.target.closest && e.target.closest('#fSyl');
  if (!f || e.target.name === 'ch') return;
  qa = { cls: f.cls.value, type: f.type.value, exam: f.exam.value };
  if (e.target.name === 'cls') render();
});

// ---------- Buttons ----------
const acts = {
  start() { S.stage = 1; save(); render(); },
  go(id) { page = id || ''; render(); window.scrollTo(0, 0); },
  view(id) { view = id; render(); },
  selOn(id) { document.querySelectorAll('#fSyl input[name=ch]').forEach(c => { if (c.dataset.s === id) c.checked = true; }); },
  selOff(id) { document.querySelectorAll('#fSyl input[name=ch]').forEach(c => { if (c.dataset.s === id) c.checked = false; }); },
  plan: () => changed('Plan regenerated'),
  togSess(id) { const x = S.sessions.find(y => y.id === id); if (x) { x.done = !x.done; save(); render(); } },
  togChap(id) { const c = S.chapters.find(y => y.id === id); if (c) { c.done = !c.done; changed('Chapter updated'); } },
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
    tab = 'plan'; changed('Demo data loaded (fictional)');
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
