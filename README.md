# Bushbush
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SkillPilot | Skill-Based Hiring</title>

<style>
:root {
  --primary: #126b57;
  --dark: #12483d;
  --bg: #f3f7f6;
  --card: #ffffff;
  --text: #172b27;
  --muted: #5b6c67;
  --border: #dce7e3;
}
* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
}

header {
  background: linear-gradient(120deg, var(--dark), var(--primary));
  color: white;
  padding: 28px 7%;
}

header h1 { margin: 0 0 8px; font-size: 32px; }
header p { margin: 0; line-height: 1.6; }

.hero-tag {
  display: inline-block;
  margin-top: 14px;
  padding: 6px 10px;
  border: 1px solid #ffffff70;
  border-radius: 20px;
  font-size: 12px;
}

main {
  max-width: 1150px;
  margin: 26px auto;
  padding: 0 16px;
}

.intro {
  margin-bottom: 20px;
  line-height: 1.6;
}

.features {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
  margin-bottom: 22px;
}

.feature, .card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 20px;
  box-shadow: 0 3px 12px #10251a08;
}

.feature h3 { margin: 8px 0; font-size: 16px; }
.feature p { margin: 0; color: var(--muted); font-size: 13px; line-height: 1.6; }
.feature-icon { font-size: 25px; }

.workspace {
  display: grid;
  grid-template-columns: 330px minmax(0, 1fr);
  gap: 20px;
  align-items: start;
}

h2 { font-size: 21px; margin-top: 0; }
h3 { font-size: 17px; }

label {
  display: block;
  font-weight: bold;
  margin: 15px 0 7px;
  font-size: 14px;
}

input, select, textarea {
  width: 100%;
  padding: 11px;
  border: 1px solid #cbd8d4;
  border-radius: 7px;
  font: inherit;
  background: white;
  color: var(--text);
}

textarea { min-height: 85px; resize: vertical; }

button {
  border: 0;
  border-radius: 8px;
  padding: 12px 14px;
  font-weight: bold;
  cursor: pointer;
  margin: 12px 6px 0 0;
}

button:focus, input:focus, select:focus, textarea:focus {
  outline: 2px solid #61a998;
  outline-offset: 2px;
}

.primary { background: var(--primary); color: white; }
.secondary { background: #e4efeb; color: #164c40; }
.full { width: 100%; }

.small {
  color: var(--muted);
  font-size: 13px;
  line-height: 1.6;
}

.status {
  display: inline-block;
  padding: 6px 9px;
  background: #fff0cb;
  border-radius: 5px;
  font-size: 11px;
  font-weight: bold;
}

.section {
  border-top: 1px solid var(--border);
  padding-top: 16px;
  margin-top: 20px;
}

.result-block {
  background: #f7faf9;
  padding: 14px;
  border-radius: 9px;
  margin: 12px 0;
  line-height: 1.6;
  overflow-wrap: anywhere;
}

.result-block h3 { margin-top: 0; }

.question {
  background: white;
  border: 1px solid var(--border);
  border-radius: 9px;
  padding: 13px;
  margin: 10px 0;
}

.question strong { display: block; line-height: 1.5; }
.skill-tag {
  display: inline-block;
  background: #e4efeb;
  color: #164c40;
  border-radius: 20px;
  padding: 4px 9px;
  font-size: 12px;
  margin-top: 8px;
}

.rubric-row {
  display: grid;
  grid-template-columns: 1fr 95px;
  gap: 12px;
  align-items: center;
  padding: 12px 0;
  border-bottom: 1px solid var(--border);
}

.rubric-row label { margin: 0 0 5px; }
.rubric-row select { padding: 9px; }

.score-total {
  font-size: 25px;
  font-weight: bold;
  color: var(--primary);
  margin: 12px 0;
}

.notice {
  background: #fff7e6;
  padding: 12px;
  border-radius: 8px;
  font-size: 13px;
  line-height: 1.6;
}

.empty {
  color: var(--muted);
  padding: 24px 8px;
  line-height: 1.7;
}

.actions { margin-top: 15px; }

footer {
  text-align: center;
  padding: 24px 16px;
  color: var(--muted);
  font-size: 12px;
}

[hidden] { display: none !important; }

@media(max-width: 800px) {
  .workspace { grid-template-columns: 1fr; }
  .features { grid-template-columns: 1fr; }
  header { padding: 24px 5%; }
}

@media print {
  header, .features, .form-card, .actions, footer,
  .status, .intro, #message, #scoreControls {
    display: none !important;
  }
  body { background: white; }
  main { margin: 0; max-width: none; }
  .workspace { display: block; }
  .card { box-shadow: none; border: none; padding: 0; }
  .result-block { break-inside: avoid; }
}
</style>
</head>

<body>

<header>
  <h1>SkillPilot</h1>
  <p>Job-specific interview kits and structured skill evaluation</p>
  <span class="hero-tag">A practical hiring preparation prototype</span>
</header>

<main>
  <p class="intro">
    Prepare a job profile, connect interview questions to required skills,
    and use a consistent scoring rubric in one place.
  </p>

  <section class="features">
    <article class="feature">
      <div class="feature-icon">🎯</div>
      <h3>Skill-to-question mapping</h3>
      <p>See which required skill each interview question is designed to assess.</p>
    </article>
    <article class="feature">
      <div class="feature-icon">📋</div>
      <h3>Clear scoring guidance</h3>
      <p>Use the same job-related scoring criteria for each candidate.</p>
    </article>
    <article class="feature">
      <div class="feature-icon">🌱</div>
      <h3>Fresher-friendly interviews</h3>
      <p>Prepare questions appropriate for entry-level candidates.</p>
    </article>
  </section>

  <div class="workspace">

    <section class="card form-card">
      <h2>Create an interview kit</h2>
      <p class="small">Enter the job details below.</p>

      <form id="jobForm">
        <label for="title">Job title *</label>
        <input id="title" required
          placeholder="e.g. Junior Python Developer">

        <label for="company">Company name</label>
        <input id="company" placeholder="e.g. ABC Technologies">

        <label for="level">Experience level</label>
        <select id="level">
          <option value="fresher">Entry level / Fresher</option>
          <option value="junior">Junior (1–3 years)</option>
          <option value="mid">Mid-level (3–5 years)</option>
          <option value="senior">Senior (5+ years)</option>
        </select>

        <label for="skills">Required skills *</label>
        <textarea id="skills" required
          placeholder="Python, SQL, problem solving"></textarea>
        <p class="small">Separate skills with commas.</p>

        <label for="details">Additional job details</label>
        <textarea id="details"
          placeholder="Main duties, qualifications, work arrangement..."></textarea>

        <button class="primary full" type="submit">
          Generate interview kit
        </button>
      </form>

      <p class="small">
        This demo uses local JavaScript templates. It does not send your
        information to an AI service.
      </p>
    </section>

    <section class="card" aria-live="polite">
      <span class="status">TEMPLATE-BASED PROTOTYPE</span>
      <h2 id="resultTitle">Your interview kit</h2>
      <p id="companyLine" class="small">
        Enter job details to see your interview kit here.
      </p>

      <div id="emptyState" class="empty">
        <strong>What you will get</strong>
        <p>1. Job summary and responsibilities</p>
        <p>2. Required skills</p>
        <p>3. Interview questions mapped to skills</p>
        <p>4. A scoring rubric out of 20</p>
      </div>

      <div id="results" hidden>
        <div class="result-block">
          <h3>1. Job summary</h3>
          <p id="summary"></p>
        </div>

        <div class="result-block">
          <h3>2. Responsibilities</h3>
          <ol id="responsibilities"></ol>
        </div>

        <div class="result-block">
          <h3>3. Required skills</h3>
          <ul id="skillList"></ul>
        </div>

        <div class="result-block">
          <h3>4. Interview questions linked to skills</h3>
          <p class="small">
            Each question has a related skill, so the interviewer knows
            what they are assessing.
          </p>
          <div id="questions"></div>
        </div>

        <div class="result-block">
          <h3>5. Candidate scoring rubric</h3>
          <p class="small">
            Select a score for each category. The total updates automatically.
            Leave categories unscored until the interview is complete.
          </p>

          <div id="scoreControls">
            <div id="rubric"></div>
            <div class="score-total">
              Total: <span id="scoreTotal">0</span> / 20
            </div>
            <p id="scoreStatus" class="small">
              No categories scored yet.
            </p>
            <button type="button" class="secondary"
              onclick="resetScores()">Reset scores</button>
          </div>
        </div>

        <div class="result-block">
          <h3>6. Additional job details</h3>
          <p id="detailsOutput"></p>
        </div>

        <div class="notice">
          <strong>Important:</strong> This is a template-generated draft,
          not a real AI-generated or validated job specification.
          Review the content before use. Scores should support human
          judgment, not make automatic hiring decisions.
        </div>

        <div class="actions">
          <button type="button" class="primary" onclick="copyResult()">
            Copy interview kit
          </button>
          <button type="button" class="secondary" onclick="downloadResult()">
            Download TXT
          </button>
          <button type="button" class="secondary" onclick="window.print()">
            Save as PDF
          </button>
        </div>
      </div>

      <p id="message" class="small" aria-live="polite"></p>
    </section>
  </div>
</main>

<footer>
  SkillPilot — helping teams prepare structured, job-related interviews.
  Human review is required.
</footer>

<script>
let currentKit = null;

const rubricCategories = [
  {
    name: "Technical knowledge",
    guidance: {
      1: "Shows limited understanding of the required concepts.",
      3: "Shows a reasonable understanding, with some gaps.",
      5: "Explains the concepts clearly and accurately."
    }
  },
  {
    name: "Problem-solving",
    guidance: {
      1: "Struggles to explain a clear approach.",
      3: "Provides a workable approach with some guidance.",
      5: "Explains a logical approach and considers alternatives."
    }
  },
  {
    name: "Communication",
    guidance: {
      1: "Explanation is difficult to follow.",
      3: "Explains the main points understandably.",
      5: "Explains ideas clearly and answers relevant follow-up questions."
    }
  },
  {
    name: "Practical application",
    guidance: {
      1: "Provides little relevant practical evidence.",
      3: "Gives a partly correct example or solution.",
      5: "Provides a relevant example or workable solution."
    }
  }
];

function addText(tag, text, parent) {
  const element = document.createElement(tag);
  element.textContent = text;
  parent.appendChild(element);
  return element;
}

function makeList(items, parent) {
  parent.replaceChildren();
  items.forEach(item => addText("li", item, parent));
}

function generate(event) {
  event.preventDefault();

  const title = document.getElementById("title").value.trim();
  const company = document.getElementById("company").value.trim();
  const level = document.getElementById("level").value;
  const rawSkills = document.getElementById("skills").value.trim();
  const details = document.getElementById("details").value.trim();

  const skills = [...new Set(
    rawSkills.split(",").map(s => s.trim()).filter(Boolean)
  )];

  if (!title || skills.length === 0) {
    document.getElementById("message").textContent =
      "Please enter a job title and at least one skill.";
    return;
  }

  const companyName = company || "Hiring organization";
  const isFresher = level === "fresher";

  const responsibilities = [
    `Perform tasks related to the ${title} role.`,
    `Apply relevant skills such as ${skills.slice(0, 3).join(", ")}.`,
    "Collaborate with team members and communicate progress.",
    "Test work, solve issues, and document important decisions."
  ];

  const questions = skills.map((skill, index) => ({
    skill,
    question: isFresher
      ? `Explain the basics of ${skill} and give a simple example.`
      : `Describe how you would use ${skill} to solve a job-related problem.`,
    followup: isFresher
      ? `What would you do if you got stuck while using ${skill}?`
      : `How would you check whether your approach using ${skill} worked?`
  }));

  questions.push({
    skill: "Problem-solving",
    question: isFresher
      ? "Describe a simple problem you solved in your studies or a project."
      : "Describe a challenging work problem and how you approached it.",
    followup: "What would you do differently next time?"
  });

  questions.push({
    skill: "Communication",
    question: "How would you explain your work or ask for help when needed?",
    followup: "How would you communicate a delay to your team?"
  });

  currentKit = {
    title, companyName, level, skills, responsibilities, questions,
    details: details || "Confirm duties, qualifications, location, work arrangement, and salary with the employer."
  };

  document.getElementById("resultTitle").textContent =
    title + " — Interview Kit";

  document.getElementById("companyLine").textContent =
    "Prepared for " + companyName + " | " +
    document.getElementById("level").selectedOptions[0].textContent;

  document.getElementById("summary").textContent =
    companyName + " is preparing for the " + title +
    " role. Candidates should demonstrate relevant skills, solve job-related problems, and communicate clearly. " +
    (isFresher
      ? "Questions are designed for entry-level candidates and may be answered using academic or project examples."
      : "Questions should be adapted to the responsibilities and experience expected for this role.");

  makeList(responsibilities, document.getElementById("responsibilities"));
  makeList(skills, document.getElementById("skillList"));

  const questionsArea = document.getElementById("questions");
  questionsArea.replaceChildren();

  questions.forEach((item, index) => {
    const card = document.createElement("div");
    card.className = "question";

    addText("strong", (index + 1) + ". " + item.question, card);

    const tag = addText("span", "Skill assessed: " + item.skill, card);
    tag.className = "skill-tag";

    const followup = document.createElement("p");
    followup.className = "small";
    followup.textContent = "Follow-up: " + item.followup;
    card.appendChild(followup);

    questionsArea.appendChild(card);
  });

  document.getElementById("detailsOutput").textContent = currentKit.details;

  buildRubric();
  document.getElementById("emptyState").hidden = true;
  document.getElementById("results").hidden = false;
  document.getElementById("message").textContent =
    "Interview kit created. Review the questions and criteria before use.";

  document.getElementById("results").scrollIntoView({
    behavior: "smooth", block: "start"
  });
}

function buildRubric() {
  const area = document.getElementById("rubric");
  area.replaceChildren();

  rubricCategories.forEach((category, index) => {
    const row = document.createElement("div");
    row.className = "rubric-row";

    const left = document.createElement("div");
    const label = addText("label", category.name, left);
    label.htmlFor = "score" + index;

    const guidance = addText(
      "p",
      "1: " + category.guidance[1] + "\n" +
      "3: " + category.guidance[3] + "\n" +
      "5: " + category.guidance[5],
      left
    );
    guidance.className = "small";
    guidance.style.whiteSpace = "pre-line";

    const select = document.createElement("select");
    select.id = "score" + index;
    select.setAttribute("aria-label", category.name + " score");

    const placeholder = document.createElement("option");
    placeholder.value = "";
    placeholder.textContent = "Not scored";
    select.appendChild(placeholder);

    for (let score = 0; score <= 5; score++) {
      const option = document.createElement("option");
      option.value = String(score);
      option.textContent = score + " / 5";
      select.appendChild(option);
    }

    select.addEventListener("change", updateScore);
    row.append(left, select);
    area.appendChild(row);
  });

  updateScore();
}

function updateScore() {
  let total = 0;
  let completed = 0;

  rubricCategories.forEach((category, index) => {
    const value = document.getElementById("score" + index).value;
    if (value !== "") {
      total += Number(value);
      completed++;
    }
  });

  document.getElementById("scoreTotal").textContent = total;
  document.getElementById("scoreStatus").textContent =
    completed === 4
      ? "All four categories scored. Final total: " + total + " / 20."
      : completed + " of 4 categories scored. This is a partial total.";
}

function resetScores() {
  rubricCategories.forEach((category, index) => {
    document.getElementById("score" + index).value = "";
  });
  updateScore();
}

function getKitText() {
  if (!currentKit) return "";

  let text = "SKILLPILOT — INTERVIEW KIT\n\n";
  text += "JOB: " + currentKit.title + "\n";
  text += "ORGANIZATION: " + currentKit.companyName + "\n";
  text += "EXPERIENCE: " +
    document.getElementById("level").selectedOptions[0].textContent + "\n\n";

  text += "RESPONSIBILITIES\n";
  currentKit.responsibilities.forEach((x, i) => {
    text += (i + 1) + ". " + x + "\n";
  });

  text += "\nREQUIRED SKILLS\n";
  currentKit.skills.forEach((x, i) => {
    text += (i + 1) + ". " + x + "\n";
  });

  text += "\nSKILL-LINKED INTERVIEW QUESTIONS\n";
  currentKit.questions.forEach((q, i) => {
    text += (i + 1) + ". " + q.question + "\n";
    text += "   Skill assessed: " + q.skill + "\n";
    text += "   Follow-up: " + q.followup + "\n";
  });

  text += "\nSCORING RUBRIC\n";
  let total = 0;
  let completed = 0;

  rubricCategories.forEach((category, i) => {
    const value = document.getElementById("score" + i).value;
    text += category.name + ": " +
      (value === "" ? "Not scored" : value + " / 5") + "\n";
    text += "  Score 1: " + category.guidance[1] + "\n";
    text += "  Score 3: " + category.guidance[3] + "\n";
    text += "  Score 5: " + category.guidance[5] + "\n";

    if (value !== "") {
      total += Number(value);
      completed++;
    }
  });

  text += "\n" + (completed === 4 ? "TOTAL SCORE: " + total + " / 20" :
    "PARTIAL SCORE: " + total + " / 20 (" + completed + " of 4 categories scored)") + "\n";

  text += "\nADDITIONAL DETAILS\n" + currentKit.details + "\n";
  text += "\nNOTE: Template-based prototype. Review all material. " +
    "Scores support human judgment and must not make automatic hiring decisions.\n";

  return text;
}

async function copyResult() {
  try {
    await navigator.clipboard.writeText(getKitText());
    document.getElementById("message").textContent = "Interview kit copied.";
  } catch (error) {
    document.getElementById("message").textContent =
      "Copy is unavailable here. You can select the output or download the TXT file.";
  }
}

function downloadResult() {
  const blob = new Blob([getKitText()], { type: "text/plain;charset=utf-8" });
  const url = URL.createObjectURL(blob);
  const link = document.createElement("a");

  link.href = url;
  link.download = "SkillPilot-Interview-Kit.txt";
  document.body.appendChild(link);
  link.click();
  link.remove();
  URL.revokeObjectURL(url);

  document.getElementById("message").textContent =
    "Download started.";
}

document.getElementById("jobForm").addEventListener("submit", generate);
</script>
</body>
</html>
