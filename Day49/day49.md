day49- Build Personal AI Playbook

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Personal AI Playbook</title>

<style>
:root{
  --bg:#f5f1eb;
  --card:#fffdf9;
  --text:#211d19;
  --muted:#756e67;
  --border:#ded6cc;
  --accent:#8a5a3b;
  --accent-light:#eadbcf;
  --shadow:0 12px 35px rgba(50,35,20,.08);
}

[data-theme="dark"]{
  --bg:#171412;
  --card:#211d1a;
  --text:#f5eee8;
  --muted:#aaa098;
  --border:#3b342e;
  --accent:#d39a70;
  --accent-light:#3b2b21;
  --shadow:0 12px 35px rgba(0,0,0,.35);
}

*{box-sizing:border-box}

body{
  margin:0;
  background:var(--bg);
  color:var(--text);
  font-family:Inter,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
}

button,input,textarea,select{
  font:inherit;
}

button{
  cursor:pointer;
}

.app{
  min-height:100vh;
  display:grid;
  grid-template-columns:250px 1fr;
}

.sidebar{
  background:var(--card);
  border-right:1px solid var(--border);
  padding:24px 16px;
  position:sticky;
  top:0;
  height:100vh;
}

.logo{
  font-size:20px;
  font-weight:800;
  padding:8px 10px 25px;
}

.logo span{
  color:var(--accent);
}

.nav button{
  width:100%;
  border:0;
  background:transparent;
  color:var(--muted);
  padding:12px;
  border-radius:10px;
  text-align:left;
  margin-bottom:4px;
}

.nav button:hover,
.nav button.active{
  background:var(--accent-light);
  color:var(--text);
}

.sidebar-info{
  position:absolute;
  bottom:20px;
  left:20px;
  right:20px;
  font-size:12px;
  color:var(--muted);
}

.main{
  max-width:1250px;
  width:100%;
  margin:auto;
  padding:30px;
}

.header{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
  margin-bottom:20px;
}

.header h1{
  margin:0;
  font-size:30px;
}

.actions{
  display:flex;
  gap:8px;
  flex-wrap:wrap;
}

.btn{
  border:1px solid var(--border);
  background:var(--card);
  color:var(--text);
  border-radius:9px;
  padding:9px 14px;
}

.btn:hover{
  transform:translateY(-1px);
}

.btn.primary{
  background:var(--accent);
  border-color:var(--accent);
  color:white;
}

.explainer{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:16px;
  padding:20px;
  margin-bottom:20px;
  box-shadow:var(--shadow);
}

.explainer strong{
  font-size:16px;
}

.explainer p{
  color:var(--muted);
  margin-bottom:12px;
}

.section{
  display:none;
}

.section.active{
  display:block;
}

.cards{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:15px;
}

.card{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:16px;
  padding:18px;
  box-shadow:var(--shadow);
}

.stat{
  font-size:32px;
  font-weight:800;
  margin-top:5px;
}

.muted{
  color:var(--muted);
}

.tag{
  display:inline-block;
  background:var(--accent-light);
  border-radius:20px;
  padding:4px 9px;
  font-size:12px;
  margin:3px 0;
}

.workflow{
  display:flex;
  justify-content:space-between;
  gap:15px;
  padding:15px 0;
  border-bottom:1px solid var(--border);
}

.workflow:last-child{
  border-bottom:0;
}

.workflow h3{
  margin:5px 0;
}

.searchbar{
  display:flex;
  gap:10px;
  margin:18px 0;
}

.searchbar input,
.searchbar select,
.field input,
.field textarea,
.field select{
  width:100%;
  padding:10px;
  border-radius:9px;
  border:1px solid var(--border);
  background:var(--card);
  color:var(--text);
}

.builder{
  display:grid;
  grid-template-columns:330px 1fr;
  gap:18px;
}

.picker,
.assembled,
.preview{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:16px;
  padding:16px;
}

.block-picker{
  display:flex;
  flex-direction:column;
  gap:8px;
  margin-top:12px;
}

.block-button{
  text-align:left;
  border:1px solid var(--border);
  background:transparent;
  color:var(--text);
  border-radius:10px;
  padding:11px;
}

.block-button small{
  display:block;
  color:var(--muted);
  margin-top:4px;
}

.assembled-block{
  border:1px solid var(--border);
  border-radius:12px;
  padding:13px;
  margin-bottom:10px;
}

.block-top{
  display:flex;
  justify-content:space-between;
  gap:10px;
}

.assembled-block textarea{
  margin-top:10px;
  width:100%;
  min-height:75px;
  padding:10px;
  border:1px solid var(--border);
  border-radius:8px;
  background:var(--card);
  color:var(--text);
}

.preview{
  margin-top:15px;
  white-space:pre-wrap;
  min-height:180px;
}

.loop-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:15px;
}

.field{
  margin-bottom:14px;
}

.field label{
  display:block;
  font-weight:700;
  margin-bottom:6px;
}

.modal{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.7);
  display:none;
  align-items:center;
  justify-content:center;
  padding:20px;
  z-index:20;
}

.modal.show{
  display:flex;
}

.modal-content{
  background:var(--card);
  color:var(--text);
  max-width:650px;
  width:100%;
  border-radius:18px;
  padding:25px;
}

.toast{
  position:fixed;
  right:20px;
  bottom:20px;
  background:var(--text);
  color:var(--bg);
  padding:12px 16px;
  border-radius:9px;
  display:none;
}

@media(max-width:850px){
  .app{
    grid-template-columns:1fr;
  }

  .sidebar{
    height:auto;
    position:relative;
    border-right:0;
    border-bottom:1px solid var(--border);
  }

  .sidebar-info{
    position:static;
    margin-top:20px;
  }

  .main{
    padding:20px;
  }

  .cards,
  .builder,
  .loop-grid{
    grid-template-columns:1fr;
  }

  .header{
    align-items:flex-start;
    flex-direction:column;
  }
}
</style>
</head>

<body>

<div class="app">

<aside class="sidebar">

<div class="logo">
Personal <span>AI</span> Playbook
</div>

<div class="nav">

<button class="active" onclick="showSection('dashboard',this)">
▦ Dashboard
</button>

<button onclick="showSection('workflows',this)">
◇ My Workflows
</button>

<button onclick="showSection('prompt',this)">
✦ Prompt Builder
</button>

<button onclick="showSection('loop',this)">
↻ Loop Builder
</button>

<button onclick="showSection('settings',this)">
⚙ Settings
</button>

</div>

<div class="sidebar-info">
Build reusable AI systems instead of collecting hundreds of disconnected prompts.
<br><br>
Keyboard:
<strong>Ctrl/⌘ K</strong> search
<br>
<strong>N</strong> new workflow
</div>

</aside>


<main class="main">

<div class="header">

<h1 id="pageTitle">Dashboard</h1>

<div class="actions">

<button class="btn" onclick="openHelp()">
? What is this?
</button>

<button class="btn" onclick="toggleTheme()">
☾ Theme
</button>

</div>

</div>


<div class="explainer" id="explainer">

<strong>
Your personal AI workspace for sales, leads and customer communication.
</strong>

<p>
Save reusable AI workflows, build prompts from modular components,
and create controlled improvement loops. The goal is to build
repeatable AI systems rather than one-off prompts.
</p>

<button class="btn" onclick="dismissExplainer()">
Dismiss
</button>

</div>


<!-- DASHBOARD -->

<section id="dashboard" class="section active">

<div class="cards">

<div class="card">
<div class="muted">Saved workflows</div>
<div class="stat" id="workflowCount">0</div>
</div>

<div class="card">
<div class="muted">Favorites</div>
<div class="stat" id="favoriteCount">0</div>
</div>

<div class="card">
<div class="muted">Workflow categories</div>
<div class="stat">4</div>
</div>

</div>


<div class="card" style="margin-top:15px">

<h2>Recommended workflows</h2>

<p class="muted">
AI systems selected for a founder focused on sales and customer communication.
</p>

<div id="recommendations"></div>

</div>

</section>


<!-- WORKFLOWS -->

<section id="workflows" class="section">

<div class="header">

<div>
<h2>My Workflows</h2>

<div class="muted">
Create, edit, search, favorite and reuse your AI workflows.
</div>
</div>

<button class="btn primary" onclick="createWorkflow()">
+ New workflow
</button>

</div>


<div class="searchbar">

<input
id="search"
placeholder="Search workflows..."
oninput="renderWorkflows()"
>

<select id="categoryFilter" onchange="renderWorkflows()">

<option value="all">All categories</option>
<option>Lead generation</option>
<option>Outreach</option>
<option>Follow-up</option>
<option>Sales strategy</option>

</select>

<button class="btn" onclick="exportLibrary()">
Export
</button>

<label class="btn">
Import
<input
type="file"
id="importInput"
accept=".json"
hidden
>
</label>

</div>


<div class="card" id="workflowList"></div>

</section>


<!-- PROMPT BUILDER -->

<section id="prompt" class="section">

<div class="header">

<div>

<h2>Prompt Builder</h2>

<div class="muted">
Assemble reusable prompts from explainable building blocks.
</div>

</div>

<button class="btn primary" onclick="copyPrompt()">
Copy prompt
</button>

</div>


<div class="builder">

<div class="picker">

<strong>Add a building block</strong>

<div class="muted">
Each block explains what it does and why it matters.
</div>

<div class="block-picker" id="blockPicker"></div>

</div>


<div>

<div class="assembled">

<h3>Assembled prompt</h3>

<div id="assembledBlocks"></div>

</div>


<div class="preview">

<strong>Live preview</strong>

<div id="promptPreview"></div>

</div>

</div>

</div>

</section>


<!-- LOOP BUILDER -->

<section id="loop" class="section">

<div class="header">

<div>

<h2>Loop Builder</h2>

<div class="muted">
Turn a normal prompt into a controlled repeat-and-improve system.
</div>

</div>

<button class="btn primary" onclick="copyLoop()">
Copy loop prompt
</button>

</div>


<div class="loop-grid">

<div class="card">

<div class="field">

<label>
Goal
<span class="muted">
— the result the loop should pursue.
</span>
</label>

<textarea id="loopGoal"
placeholder="Example: Improve this cold email until every quality criterion passes."
oninput="updateLoop()"></textarea>

</div>


<div class="field">

<label>
Evaluation criteria
<span class="muted">
— how each iteration is judged.
</span>
</label>

<textarea id="loopCriteria"
oninput="updateLoop()">Clear value proposition; specific personalization; concise CTA; no unsupported claims.</textarea>

</div>


<div class="field">

<label>
Improvement strategy
<span class="muted">
— what changes after evaluation.
</span>
</label>

<select id="loopStrategy" onchange="updateLoop()">

<option>
Fix the weakest criterion first
</option>

<option>
Rewrite the entire output each round
</option>

<option>
Make one controlled change per round
</option>

</select>

</div>

</div>


<div class="card">

<div class="field">

<label>
Stop condition
<span class="muted">
— when the loop must end.
</span>
</label>

<select id="loopStop" onchange="updateLoop">

<option>Stop when all criteria pass</option>
<option>Stop after 3 iterations</option>
<option>Stop when improvement becomes negligible</option>

</select>

</div>


<div class="field">

<label>
Safety rules
<span class="muted">
— boundaries that must never be crossed.
</span>
</label>

<textarea id="loopSafety"
oninput="updateLoop()">Never invent customer facts. Preserve truthful claims. Stop if required information is missing.</textarea>

</div>


<div class="field">

<label>
Base prompt
<span class="muted">
— the task being improved.
</span>
</label>

<textarea id="loopBase"
placeholder="Paste your normal prompt here."
oninput="updateLoop()"></textarea>

</div>

</div>

</div>


<div class="preview">

<strong>Generated loop prompt</strong>

<div id="loopPreview"></div>

</div>

</section>


<!-- SETTINGS -->

<section id="settings" class="section">

<div class="card">

<h2>Settings</h2>

<p class="muted">
Your workflows are stored locally in this browser.
Export the workflow library when you want a portable backup.
</p>

<button class="btn" onclick="resetData()">
Reset demo data
</button>

</div>

</section>

</main>
</div>


<!-- HELP MODAL -->

<div class="modal" id="helpModal">

<div class="modal-content">

<button class="btn" style="float:right" onclick="closeHelp()">
×
</button>

<h2>What is Personal AI Playbook?</h2>

<p>
Personal AI Playbook is a reusable AI workflow workspace.
Instead of collecting hundreds of disconnected prompts,
you create modular systems for recurring business tasks.
</p>

<p>
<strong>Dashboard</strong> provides an overview.
<strong>My Workflows</strong> stores reusable workflows.
<strong>Prompt Builder</strong> combines explainable prompt components.
<strong>Loop Builder</strong> adds evaluation, improvement,
stop conditions and safety rules.
</p>

<p>
Everything is designed to work locally in the browser.
Your workflow library can be exported as JSON.
</p>

</div>

</div>


<div class="toast" id="toast"></div>


<script>

const defaultWorkflows = [

{
id:1,
name:"Lead Qualification",
category:"Lead generation",
favorite:true,
description:"Score and prioritize prospects using fit, need, urgency and evidence."
},

{
id:2,
name:"Personalized Cold Outreach",
category:"Outreach",
favorite:false,
description:"Create short, research-grounded outreach without inventing prospect facts."
},

{
id:3,
name:"Follow-up Sequence",
category:"Follow-up",
favorite:false,
description:"Create helpful follow-ups that add value instead of repeating the same pitch."
},

{
id:4,
name:"Sales Objection Coach",
category:"Sales strategy",
favorite:false,
description:"Turn customer objections into concise, evidence-based responses."
}

];


let workflows =
JSON.parse(localStorage.getItem("personalAIWorkflows"))
|| defaultWorkflows;


/* NAVIGATION */

function showSection(id,button){

document.querySelectorAll(".section")
.forEach(section=>section.classList.remove("active"));

document.getElementById(id).classList.add("active");

document.querySelectorAll(".nav button")
.forEach(btn=>btn.classList.remove("active"));

button.classList.add("active");

const titles={
dashboard:"Dashboard",
workflows:"My Workflows",
prompt:"Prompt Builder",
loop:"Loop Builder",
settings:"Settings"
};

document.getElementById("pageTitle").textContent=titles[id];

}


/* STORAGE */

function saveWorkflows(){

localStorage.setItem(
"personalAIWorkflows",
JSON.stringify(workflows)
);

renderAll();

}


/* DASHBOARD */

function renderDashboard(){

document.getElementById("workflowCount")
.textContent=workflows.length;

document.getElementById("favoriteCount")
.textContent=
workflows.filter(w=>w.favorite).length;

document.getElementById("recommendations")
.innerHTML=

workflows.slice(0,4).map(w=>`

<div class="workflow">

<div>

<span class="tag">${w.category}</span>

<h3>${w.name}</h3>

<div class="muted">
${w.description}
</div>

</div>

<button class="btn"
onclick="editWorkflow(${w.id})">
Open
</button>

</div>

`).join("");

}


/* WORKFLOWS */

function renderWorkflows(){

const query=
(document.getElementById("search").value||"")
.toLowerCase();

const category=
document.getElementById("categoryFilter").value;

const filtered=workflows.filter(w=>{

const matchesSearch=
`${w.name} ${w.description} ${w.category}`
.toLowerCase()
.includes(query);

const matchesCategory=
category==="all" ||
w.category===category;

return matchesSearch && matchesCategory;

});


document.getElementById("workflowList").innerHTML=

filtered.length?

filtered.map(w=>`

<div class="workflow">

<div>

<span class="tag">${w.category}</span>

<h3>
${w.name}
${w.favorite?" ★":""}
</h3>

<div class="muted">
${w.description}
</div>

</div>

<div class="actions">

<button class="btn"
onclick="toggleFavorite(${w.id})">
${w.favorite?"★":"☆"}
</button>

<button class="btn"
onclick="editWorkflow(${w.id})">
Edit
</button>

<button class="btn"
onclick="duplicateWorkflow(${w.id})">
Duplicate
</button>

</div>

</div>

`).join("")

:

`<div style="padding:40px;text-align:center"
class="muted">
No workflows found.
</div>`;

}


function createWorkflow(){

const name=
prompt("Workflow name:");

if(!name)return;

const description=
prompt(
"What does this workflow help you do?"
);

const categories=[
"Lead generation",
"Outreach",
"Follow-up",
"Sales strategy"
];

const category=
prompt(
"Category: Lead generation, Outreach, Follow-up, or Sales strategy",
"Outreach"
);

workflows.unshift({

id:Date.now(),

name:name,

description:description||"Reusable AI workflow.",

category:categories.includes(category)
?category
:"Outreach",

favorite:false

});

saveWorkflows();

}


function editWorkflow(id){

const workflow=
workflows.find(w=>w.id===id);

if(!workflow)return;

const name=
prompt("Workflow name:",workflow.name);

if(name!==null)
workflow.name=name;

const description=
prompt(
"Description:",
workflow.description
);

if(description!==null)
workflow.description=description;

saveWorkflows();

}


function duplicateWorkflow(id){

const original=
workflows.find(w=>w.id===id);

workflows.unshift({

...original,

id:Date.now(),

name:original.name+" Copy",

favorite:false

});

saveWorkflows();

}


function toggleFavorite(id){

const workflow=
workflows.find(w=>w.id===id);

workflow.favorite=!workflow.favorite;

saveWorkflows();

}


/* EXPORT */

function exportLibrary(){

const data={
exportedAt:new Date().toISOString(),
workflows:workflows
};

const blob=
new Blob(
[JSON.stringify(data,null,2)],
{type:"application/json"}
);

const url=
URL.createObjectURL(blob);

const link=document.createElement("a");

link.href=url;

link.download="workflow-library.json";

link.click();

URL.revokeObjectURL(url);

showToast("Workflow library exported");

}


/* IMPORT */

document.getElementById("importInput")
.addEventListener("change",function(){

const file=this.files[0];

if(!file)return;

const reader=new FileReader();

reader.onload=function(){

try{

const data=
JSON.parse(reader.result);

workflows=
data.workflows||data;

saveWorkflows();

showToast("Library imported");

}catch{

showToast("Invalid JSON file");

}

};

reader.readAsText(file);

});


/* PROMPT BUILDER */

const blocks={

role:{
name:"Role",
description:
"Defines who the AI should act as so its expertise and perspective stay consistent.",
example:
"You are a B2B sales strategist and customer-communication specialist."
},

objective:{
name:"Objective",
description:
"Defines the result the AI must produce. A clear target reduces vague answers.",
example:
"Create a concise outreach message that earns a reply."
},

context:{
name:"Context",
description:
"Supplies relevant facts, audience information and background.",
example:
"The prospect is a mid-sized company exploring workflow automation."
},

constraints:{
name:"Constraints",
description:
"Sets boundaries such as length, factual limits or exclusions.",
example:
"Keep it under 120 words. Never invent facts."
},

reasoning:{
name:"Reasoning strategy",
description:
"Provides a practical task approach without requesting hidden chain-of-thought.",
example:
"Identify the likely pain point, match one relevant benefit, then write the message."
},

output:{
name:"Output format",
description:
"Defines the structure of the answer so the result is predictable and reusable.",
example:
"Output: Subject line + message + one CTA."
},

tone:{
name:"Tone",
description:
"Controls communication style for your audience and brand.",
example:
"Helpful, confident, concise and human."
},

examples:{
name:"Examples",
description:
"Shows a reference pattern that the AI can follow.",
example:
"Observation → problem → value → low-friction CTA."
},

quality:{
name:"Quality checks",
description:
"Adds a final verification pass before the AI delivers the result.",
example:
"Verify claims, remove filler, and make the CTA clear."
}

};


let selectedBlocks=[
"role",
"objective",
"context",
"constraints",
"output",
"tone",
"quality"
];


function renderBlockPicker(){

document.getElementById("blockPicker")
.innerHTML=

Object.entries(blocks).map(([key,b])=>`

<button class="block-button"
onclick="addBlock('${key}')">

<strong>${b.name}</strong>

<small>
${b.description}
</small>

</button>

`).join("");

}


function addBlock(key){

if(!selectedBlocks.includes(key))
selectedBlocks.push(key);

renderPromptBuilder();

}


function removeBlock(index){

selectedBlocks.splice(index,1);

renderPromptBuilder();

}


function renderPromptBuilder(){

document.getElementById("assembledBlocks")
.innerHTML=

selectedBlocks.map((key,index)=>{

const block=blocks[key];

return `

<div class="assembled-block">

<div class="block-top">

<div>

<strong>${block.name}</strong>

<div class="muted">
${block.description}
</div>

</div>

<button class="btn"
onclick="removeBlock(${index})">
Remove
</button>

</div>

<textarea
data-block="${index}"
oninput="updatePromptPreview()">${block.example}</textarea>

</div>

`;

}).join("");

updatePromptPreview();

}


function updatePromptPreview(){

const output=

selectedBlocks.map((key,index)=>{

const block=blocks[key];

const textarea=
document.querySelector(
`textarea[data-block="${index}"]`
);

return `${block.name}:
${textarea?textarea.value:block.example}`;

}).join("\n\n");

document.getElementById("promptPreview")
.textContent=output;

}


function copyPrompt(){

copyText(
document.getElementById("promptPreview")
.textContent
);

}


/* LOOP BUILDER */

function updateLoop(){

const goal=
document.getElementById("loopGoal").value
||"[Define goal]";

const criteria=
document.getElementById("loopCriteria").value;

const strategy=
document.getElementById("loopStrategy").value;

const stop=
document.getElementById("loopStop").value;

const safety=
document.getElementById("loopSafety").value;

const base=
document.getElementById("loopBase").value
||"[Paste base prompt]";


document.getElementById("loopPreview")
.textContent=

`AUTONOMOUS IMPROVEMENT LOOP

Base prompt:
${base}

Goal:
${goal}

For every iteration:

1. Produce the best current output.
2. Evaluate the output using these criteria:
${criteria}

3. Improvement strategy:
${strategy}

4. Compare the new result against the previous result.

Stop condition:
${stop}

Safety rules:
${safety}

Never invent missing information.
Never hide uncertainty.
Stop when the stop condition is reached.`;

}


function copyLoop(){

copyText(
document.getElementById("loopPreview")
.textContent
);

}


/* UTILITIES */

function copyText(text){

navigator.clipboard.writeText(text);

showToast("Copied to clipboard");

}


function showToast(message){

const toast=
document.getElementById("toast");

toast.textContent=message;

toast.style.display="block";

setTimeout(()=>{
toast.style.display="none";
},1800);

}


function toggleTheme(){

const current=
document.documentElement.dataset.theme;

const next=
current==="dark"?"":"dark";

document.documentElement.dataset.theme=next;

localStorage.setItem(
"personalAITheme",
next
);

}


function dismissExplainer(){

document.getElementById("explainer")
.style.display="none";

localStorage.setItem(
"personalAIExplainerDismissed",
"yes"
);

}


function openHelp(){

document.getElementById("helpModal")
.classList.add("show");

}


function closeHelp(){

document.getElementById("helpModal")
.classList.remove("show");

}


function resetData(){

if(!confirm(
"Reset your workflow library to the demo workflows?"
))return;

workflows=
JSON.parse(JSON.stringify(defaultWorkflows));

saveWorkflows();

showToast("Demo data restored");

}


/* KEYBOARD SHORTCUTS */

document.addEventListener("keydown",function(event){

if(
(event.ctrlKey||event.metaKey) &&
event.key.toLowerCase()==="k"
){

event.preventDefault();

const workflowsButton=
document.querySelectorAll(".nav button")[1];

showSection("workflows",workflowsButton);

document.getElementById("search").focus();

}

if(
event.key.toLowerCase()==="n" &&
!["INPUT","TEXTAREA","SELECT"].includes(
document.activeElement.tagName
)
){

createWorkflow();

}

if(event.key==="Escape")
closeHelp();

});


/* INITIALIZE */

if(
localStorage.getItem("personalAITheme")
){

document.documentElement.dataset.theme=
localStorage.getItem("personalAITheme");

}

if(
localStorage.getItem(
"personalAIExplainerDismissed"
)
){

document.getElementById("explainer")
.style.display="none";

}

function renderAll(){

renderDashboard();

renderWorkflows();

}

renderBlockPicker();

renderPromptBuilder();

updateLoop();

renderAll();

</script>

</body>
</html>
{
  "exportedAt": "2026-09-08",
  "workflows": [
    {
      "id": 1,
      "name": "Lead Qualification",
      "category": "Lead generation",
      "favorite": true,
      "description": "Score and prioritize prospects using fit, need, urgency and evidence.",
      "template": "Act as a B2B sales strategist. Evaluate the lead using only supplied facts. Score fit, need, urgency and evidence quality from 1–5. Explain each score, identify missing information, and recommend the next action."
    },
    {
      "id": 2,
      "name": "Personalized Cold Outreach",
      "category": "Outreach",
      "favorite": false,
      "description": "Create short, research-grounded outreach without inventing prospect facts.",
      "template": "Act as a B2B sales copywriter. Using the supplied prospect facts, write a concise cold email with one specific observation, one relevant business problem, one credible value proposition and one low-friction CTA. Never invent facts."
    },
    {
      "id": 3,
      "name": "Follow-up Sequence",
      "category": "Follow-up",
      "favorite": false,
      "description": "Create helpful follow-ups that add value instead of repeating the same pitch.",
      "template": "Create a 3-step follow-up sequence. Each message should add a new useful angle, stay concise, avoid pressure, and end with a simple CTA. Personalize only from supplied facts."
    },
    {
      "id": 4,
      "name": "Sales Objection Coach",
      "category": "Sales strategy",
      "favorite": false,
      "description": "Turn customer objections into concise, evidence-based responses.",
      "template": "Act as a sales coach. Classify the objection, identify the likely underlying concern, draft a concise response, suggest one clarifying question, and flag any claim that requires evidence."
    }
  ]
}
