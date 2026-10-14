<!--
author:   HR Learning & Development Team
email:    learning@yourorganisation.org
version:  2.1.0
language: en-GB
narrator: UK English Female
comment:  Assessing AI Competency Gaps in HR Professionals — a self-paced microcredential for TRAINERS, adapted from UNESCO AI Competency Framework LO5.1.2 (Acquire Level). Trainers learn how to define required competencies, assess current AI knowledge and tool use, score and interpret results, calculate gaps, and plan development for the HR professionals and TVET learners they train.
mode:     Textbook
script:   https://cdn.jsdelivr.net/npm/chart.js
import:   https://raw.githubusercontent.com/liaScript/CONTRIB/master/README.md

logo: https://cdn-icons-png.flaticon.com/512/8055/8055805.png

icon: https://cdn-icons-png.flaticon.com/512/8055/8055805.png

link: https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap

color:
    primary:   #1f5c99
    secondary: #f2a900
    backgroundColor: #fafbfc

style: |
  body { font-family: 'Inter', sans-serif; }

  .lo-box {
    background: #eaf3fb;
    border-left: 6px solid #1f5c99;
    padding: 16px 20px;
    border-radius: 6px;
    margin: 16px 0;
  }

  .case-box {
    background: #fff8e8;
    border-left: 6px solid #f2a900;
    padding: 16px 20px;
    border-radius: 6px;
    margin: 16px 0;
  }

  .warning-box {
    background: #fdecea;
    border-left: 6px solid #d93025;
    padding: 16px 20px;
    border-radius: 6px;
    margin: 16px 0;
  }

  .tip-box {
    background: #e9f9ee;
    border-left: 6px solid #1e8e3e;
    padding: 16px 20px;
    border-radius: 6px;
    margin: 16px 0;
  }

  .takeaway-box {
    background: #f1ecfb;
    border-left: 6px solid #6a3fc7;
    padding: 16px 20px;
    border-radius: 6px;
    margin: 16px 0;
    font-weight: 600;
  }

  .time-chip {
    display: inline-block;
    background: #1f5c99;
    color: white;
    border-radius: 14px;
    padding: 2px 12px;
    font-size: 0.85em;
    margin-bottom: 10px;
  }

  h1 { border-bottom: 4px solid #f2a900; padding-bottom: 6px; color: #17426e; }
  h2 { color: #1f5c99; }
  h3 { color: #17426e; }

  .hero {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 20px;
    background: linear-gradient(135deg, #1f5c99 0%, #17426e 60%, #0f2f50 100%);
    color: #ffffff;
    border-radius: 14px;
    padding: 24px 28px;
    margin: 8px 0 22px;
    box-shadow: 0 6px 18px rgba(15, 47, 80, 0.25);
  }
  .hero-text { flex: 1 1 280px; }
  .hero-kicker { font-size: 0.8em; letter-spacing: 0.12em; font-weight: 800; color: #f2a900; }
  .hero-sub { font-size: 0.95em; opacity: 0.9; margin: 4px 0 10px; }
  .hero-line { font-size: 1.6em; font-weight: 800; line-height: 1.2; margin-bottom: 14px; }
  .hero-badges span {
    display: inline-block;
    background: rgba(255, 255, 255, 0.16);
    border: 1px solid rgba(255, 255, 255, 0.35);
    border-radius: 16px;
    padding: 3px 12px;
    margin: 0 6px 6px 0;
    font-size: 0.85em;
  }
  .hero svg { flex: 0 1 300px; max-width: 100%; height: auto; }

  .figure {
    text-align: center;
    background: #ffffff;
    border: 1px solid #e1e6ec;
    border-radius: 12px;
    padding: 14px;
    margin: 18px 0;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  }
  .figure svg { max-width: 100%; height: auto; }
  .fig-cap { font-size: 0.85em; color: #5f6b7a; margin-top: 6px; }

  table { width: 100%; border-collapse: collapse; }
  th, td { border: 1px solid #ddd; padding: 8px 10px; text-align: left; }
  th { background: #1f5c99; color: white; }

  @media (max-width: 600px) {
    .lo-box, .case-box, .warning-box, .tip-box, .takeaway-box {
      padding: 10px 12px;
      font-size: 0.95em;
    }
  }

translation:
  de: AI-Kompetenzlücke-DE.md

@accessibility
<div class="tip-box">
**Accessibility note:** All images include descriptive alt text. All embedded videos include closed-caption notes below the player. Headings follow a strict H1 → H2 → H3 hierarchy for screen-reader navigation. Colour choices meet WCAG AA contrast standards.
</div>
@end

--------------------------------------------------------------------------

# Assessing AI Competency Gaps in HR Professionals

<div class="hero">
<div class="hero-text">
<div class="hero-kicker">SELF-PACED MICROCREDENTIAL FOR TRAINERS</div>
<div class="hero-sub">UNESCO LO5.1.2 · Acquire Level (Adapted)</div>
<div class="hero-line">Find the gap.<br>Score it.<br>Close it.</div>
<div class="hero-badges"><span>🎯 Define</span><span>🔍 Assess</span><span>📊 Score</span><span>🌱 Develop</span></div>
</div>
<svg viewBox="0 0 320 200" role="img" aria-label="Illustration of a friendly robot beside a gauge that measures an AI competency gap" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<rect x="4" y="4" width="312" height="192" rx="18" fill="#ffffff" fill-opacity="0.10"/>
<line x1="76" y1="40" x2="76" y2="27" stroke="#ffffff" stroke-width="3"/>
<circle cx="76" cy="22" r="6" fill="#f2a900"/>
<rect x="42" y="40" width="68" height="54" rx="14" fill="#ffffff"/>
<circle cx="62" cy="64" r="7" fill="#1f5c99"/>
<circle cx="90" cy="64" r="7" fill="#1f5c99"/>
<path d="M62 80 Q76 90 90 80" stroke="#1f5c99" stroke-width="3" fill="none" stroke-linecap="round"/>
<rect x="50" y="100" width="52" height="52" rx="10" fill="#f2a900"/>
<rect x="64" y="114" width="24" height="10" rx="3" fill="#ffffff" fill-opacity="0.85"/>
<rect x="26" y="106" width="16" height="8" rx="4" fill="#ffffff"/>
<rect x="110" y="106" width="16" height="8" rx="4" fill="#ffffff"/>
<rect x="58" y="154" width="14" height="20" rx="4" fill="#ffffff"/>
<rect x="80" y="154" width="14" height="20" rx="4" fill="#ffffff"/>
<path d="M170 150 A60 60 0 0 1 200 98" stroke="#ff8a80" stroke-width="14" fill="none"/>
<path d="M200 98 A60 60 0 0 1 260 98" stroke="#f2a900" stroke-width="14" fill="none"/>
<path d="M260 98 A60 60 0 0 1 290 150" stroke="#69f0ae" stroke-width="14" fill="none"/>
<line x1="230" y1="150" x2="247" y2="103" stroke="#ffffff" stroke-width="4" stroke-linecap="round"/>
<circle cx="230" cy="150" r="8" fill="#ffffff"/>
<text x="230" y="178" text-anchor="middle" fill="#ffffff" font-size="12" font-weight="700">COMPETENCY GAP</text>
</svg>
</div>

--{{0}}--
Welcome to this self-paced microcredential for trainers. In this course you will learn how to find out what HR professionals currently know about AI, compare that with what they need to know, score the difference, and turn the result into a development plan.

<div class="lo-box">

### 🎯 Module Overview

| | |
|---|---|
| **Duration** | 45–60 minutes |
| **Level** | Acquire (UNESCO AI Competency Framework — Adapted LO5.1.2) |
| **Delivery** | Self-paced interactive LiaScript microcredential |
| **Audience** | Trainers, facilitators and L&D staff who train HR professionals and TVET learners |
| **You will learn to** | Define required AI competencies, assess current knowledge and tool use, score, calculate and interpret gaps, plan development and measure improvement |

</div>

--{{1}}--
This is not a technical AI course, and it is not a course for HR learners themselves. It is a course about how a trainer assesses and develops AI competency at the Acquire level: awareness, ethical understanding, and responsible workplace application.

## Why This Module Exists

Many HR professionals already use AI tools, but nobody has checked **how well, how safely, or for what**. A trainer who delivers the same content to everyone wastes time for some learners and leaves serious risks for others.

<div class="lo-box">

This microcredential helps you, the trainer, to:

- 🎯 Define the **required** AI competency profile for HR professionals at Acquire level
- 🔍 Find out each learner's **current** AI knowledge, skills, awareness and tool use
- 📊 Score the evidence consistently and **calculate the gap** between current and required
- 🧭 Interpret scores and decide which learners need which support
- 🌱 Build targeted development plans and **re-assess** to prove improvement

</div>

## Learning Outcomes

By the end of this module, you will be able to:

1. Explain the Acquire level and the five AI competency areas that HR professionals need.
2. Select and combine assessment methods to establish a learner's current AI knowledge, skills and tool use.
3. Score evidence with a rubric, calculate competency gaps, and interpret the results fairly.
4. Investigate how HR professionals actually use AI tools, and identify risky or underused practice.
5. Create a personalised development plan, run a post-assessment, and report improvement.

--------------------------------------------------------------------------

## 🧭 Quick Navigation

| Section | Focus | Time |
|---|---|---|
| 1. The Trainer's Role and the Gap Concept | What a gap is and how to explain the course to learners | 8–10 min |
| 2. Defining the Required Competency Profile | The target your learners are measured against | 8–10 min |
| 3. Assessing Current Competency | Methods and tools to find out what learners know and do | 10–12 min |
| 4. Scoring, Calculating and Interpreting the Gap | The scoring system and a worked example | 12–15 min |
| 5. Closing the Gap and Measuring Progress | Development plans, post-assessment, reporting | 8–10 min |

<div class="figure">
<svg viewBox="0 0 720 150" role="img" aria-label="Learning roadmap with five stations: gap concept, required profile, assess, score and interpret, close and measure" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<line x1="60" y1="70" x2="660" y2="70" stroke="#cfd6de" stroke-width="8" stroke-linecap="round"/>
<circle cx="60" cy="70" r="26" fill="#1f5c99"/>
<circle cx="210" cy="70" r="26" fill="#2f7fc1"/>
<circle cx="360" cy="70" r="26" fill="#6a3fc7"/>
<circle cx="510" cy="70" r="26" fill="#1e8e3e"/>
<circle cx="660" cy="70" r="26" fill="#f2a900"/>
<text x="60" y="78" text-anchor="middle" fill="#ffffff" font-size="22" font-weight="800">1</text>
<text x="210" y="78" text-anchor="middle" fill="#ffffff" font-size="22" font-weight="800">2</text>
<text x="360" y="78" text-anchor="middle" fill="#ffffff" font-size="22" font-weight="800">3</text>
<text x="510" y="78" text-anchor="middle" fill="#ffffff" font-size="22" font-weight="800">4</text>
<text x="660" y="78" text-anchor="middle" fill="#ffffff" font-size="22" font-weight="800">5</text>
<text x="660" y="28" text-anchor="middle" font-size="20">🏁</text>
<text x="60" y="118" text-anchor="middle" fill="#17426e" font-size="13" font-weight="700">Gap concept</text>
<text x="210" y="118" text-anchor="middle" fill="#17426e" font-size="13" font-weight="700">Required profile</text>
<text x="360" y="118" text-anchor="middle" fill="#17426e" font-size="13" font-weight="700">Assess</text>
<text x="510" y="118" text-anchor="middle" fill="#17426e" font-size="13" font-weight="700">Score and interpret</text>
<text x="660" y="118" text-anchor="middle" fill="#17426e" font-size="13" font-weight="700">Close and measure</text>
<text x="60" y="136" text-anchor="middle" fill="#5f6b7a" font-size="11">8–10 min</text>
<text x="210" y="136" text-anchor="middle" fill="#5f6b7a" font-size="11">8–10 min</text>
<text x="360" y="136" text-anchor="middle" fill="#5f6b7a" font-size="11">10–12 min</text>
<text x="510" y="136" text-anchor="middle" fill="#5f6b7a" font-size="11">12–15 min</text>
<text x="660" y="136" text-anchor="middle" fill="#5f6b7a" font-size="11">8–10 min</text>
</svg>
<div class="fig-cap">Figure 1: Your learning roadmap through the five sections</div>
</div>

<div class="tip-box">
💡 **Tip:** Use the table of contents icon in the LiaScript toolbar at any time to jump directly to a section. Your progress is tracked automatically as you move through the slides.
</div>

--------------------------------------------------------------------------

# Section 1: The Trainer's Role and the Gap Concept

<span class="time-chip">⏱ 8–10 minutes</span>

--{{0}}--
Let's begin by agreeing on what a competency gap is, and what your role as a trainer is in finding it.

## What Is an AI Competency Gap?

<div class="lo-box">

**Competency gap = Required competency − Current competency**

- **Required competency:** what an HR professional needs to know and do with AI to work safely and effectively at the Acquire level.
- **Current competency:** what the learner can actually demonstrate today, based on evidence.
- **Gap:** the difference. It tells you *what* to teach, *to whom*, and *how urgently*.

</div>

<div class="figure">
<svg viewBox="0 0 560 250" role="img" aria-label="Bar diagram: the learner's current competency is lower than the required level, and the difference between the two bars is the gap" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<defs><marker id="arGap" viewBox="0 0 10 10" refX="5" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0 0 L10 5 L0 10 z" fill="#d93025"/></marker></defs>
<line x1="40" y1="200" x2="520" y2="200" stroke="#9aa5b1" stroke-width="2"/>
<rect x="110" y="110" width="100" height="90" rx="6" fill="#1f5c99"/>
<rect x="110" y="60" width="100" height="50" rx="6" fill="#d93025" fill-opacity="0.12" stroke="#d93025" stroke-width="2" stroke-dasharray="6 4"/>
<rect x="350" y="60" width="100" height="140" rx="6" fill="#f2a900"/>
<line x1="110" y1="60" x2="450" y2="60" stroke="#f2a900" stroke-width="2" stroke-dasharray="5 4"/>
<line x1="250" y1="108" x2="250" y2="64" stroke="#d93025" stroke-width="3" marker-start="url(#arGap)" marker-end="url(#arGap)"/>
<text x="266" y="92" fill="#d93025" font-size="18" font-weight="800">GAP</text>
<text x="160" y="160" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="700">Current</text>
<text x="400" y="135" text-anchor="middle" fill="#17426e" font-size="15" font-weight="700">Required</text>
<text x="400" y="154" text-anchor="middle" fill="#17426e" font-size="13">Level 3</text>
<text x="160" y="222" text-anchor="middle" fill="#5f6b7a" font-size="12">What the learner can show today</text>
<text x="400" y="222" text-anchor="middle" fill="#5f6b7a" font-size="12">What the role needs</text>
<text x="280" y="244" text-anchor="middle" fill="#17426e" font-size="14" font-weight="700">Gap = Required − Current</text>
</svg>
<div class="fig-cap">Figure 2: The competency gap is the distance between the required and the evidenced level</div>
</div>

--{{1}}--
Notice that current competency is based on evidence, not on what the learner says about themselves. Self-ratings are useful, but people often overestimate or underestimate their own ability. That is why this course teaches you to combine several sources of evidence.

### The Five-Step Gap Assessment Cycle

| Step | Trainer action | Output |
|---|---|---|
| 1. **Define** | Set the required competency profile | Target levels per competency area |
| 2. **Assess** | Collect evidence of current knowledge, skills and tool use | Raw evidence per learner |
| 3. **Score** | Convert evidence to rubric scores | Competency profile per learner |
| 4. **Interpret** | Calculate gaps, flag risks, group learners | Priority list of gaps |
| 5. **Develop and re-assess** | Plan learning, then repeat the assessment | Measured improvement |

<div class="figure">
<svg viewBox="0 0 760 225" role="img" aria-label="Cycle diagram: define, assess, score, interpret, develop, then repeat the cycle" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<defs><marker id="arCyc" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0 0 L10 5 L0 10 z" fill="#6b7785"/></marker></defs>
<line x1="116" y1="62" x2="194" y2="62" stroke="#6b7785" stroke-width="3" marker-end="url(#arCyc)"/>
<line x1="266" y1="62" x2="344" y2="62" stroke="#6b7785" stroke-width="3" marker-end="url(#arCyc)"/>
<line x1="416" y1="62" x2="494" y2="62" stroke="#6b7785" stroke-width="3" marker-end="url(#arCyc)"/>
<line x1="566" y1="62" x2="644" y2="62" stroke="#6b7785" stroke-width="3" marker-end="url(#arCyc)"/>
<circle cx="80" cy="62" r="34" fill="#1f5c99"/>
<circle cx="230" cy="62" r="34" fill="#2f7fc1"/>
<circle cx="380" cy="62" r="34" fill="#6a3fc7"/>
<circle cx="530" cy="62" r="34" fill="#1e8e3e"/>
<circle cx="680" cy="62" r="34" fill="#f2a900"/>
<text x="80" y="72" text-anchor="middle" font-size="28">🎯</text>
<text x="230" y="72" text-anchor="middle" font-size="28">🔍</text>
<text x="380" y="72" text-anchor="middle" font-size="28">📊</text>
<text x="530" y="72" text-anchor="middle" font-size="28">🧭</text>
<text x="680" y="72" text-anchor="middle" font-size="28">🌱</text>
<text x="80" y="122" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">1 Define</text>
<text x="230" y="122" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">2 Assess</text>
<text x="380" y="122" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">3 Score</text>
<text x="530" y="122" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">4 Interpret</text>
<text x="680" y="122" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">5 Develop</text>
<text x="80" y="141" text-anchor="middle" fill="#5f6b7a" font-size="12">Set the target</text>
<text x="230" y="141" text-anchor="middle" fill="#5f6b7a" font-size="12">Collect evidence</text>
<text x="380" y="141" text-anchor="middle" fill="#5f6b7a" font-size="12">Rubric + weights</text>
<text x="530" y="141" text-anchor="middle" fill="#5f6b7a" font-size="12">Gap + red flags</text>
<text x="680" y="141" text-anchor="middle" fill="#5f6b7a" font-size="12">Plan + re-assess</text>
<path d="M680 160 Q380 218 80 160" stroke="#6b7785" stroke-width="3" fill="none" stroke-dasharray="7 5" marker-end="url(#arCyc)"/>
<text x="380" y="212" text-anchor="middle" fill="#6b7785" font-size="12" font-style="italic">Repeat the cycle after training to show progress</text>
</svg>
<div class="fig-cap">Figure 3: The five-step gap assessment cycle</div>
</div>

!?[Artificial Intelligence Explained Simply](https://www.youtube.com/watch?v=ad79nYk2keg)

--{{2}}--
This short video gives you plain-language background on how generative AI works. It is useful for trainers who want a common starting point before assessing learners.

<div class="tip-box">
🎧 **Closed captions:** This video includes YouTube auto-generated captions. Click the CC icon in the player to enable them.
</div>

## How to Explain This Programme to HR Learners

--{{0}}--
How you introduce the assessment affects how honest your learners will be. If they think it is a test they can fail, they will answer aspirationally. Use this briefing.

<div class="case-box">

### 🗣️ Trainer Briefing Script (adapt to your own words)

1. **Purpose:** "This is not a pass or fail test. It shows us where you are today so we can give you the right support."
2. **What we will do:** "You will complete a short questionnaire, a knowledge quiz, some workplace scenarios, and a conversation about the AI tools you use."
3. **Honesty:** "Please answer as you really work, not as you think you should. Nobody is penalised for a low starting score."
4. **Confidentiality:** "Your individual results are shared only with you and your trainer. Group reports are anonymised."
5. **What happens next:** "You will get a personal profile and a development plan, and we will repeat the assessment at the end to show your progress."

</div>

<div class="warning-box">

⚠️ **Common trainer mistakes**

- Presenting the baseline as a test, which produces inflated, "aspirational" answers
- Relying on self-rating alone
- Using one generic course for every learner
- Skipping the tool-use conversation, where the most serious risks usually appear

</div>

---

### ✍️ Reflection

Think about a group you train. What would make them answer a baseline assessment honestly, and what might make them hide their real practice?

[[ Write a few sentences here... ]]

---

### ✅ Check Your Understanding

**1. What is a competency gap?**

[( )] The score a learner gets on a quiz
[(X)] The difference between the required competency and the learner's evidenced current competency
[( )] The difference between two learners' scores
[( )] A learner's own opinion of what they do not know

**2. Why should a trainer not rely on self-rating alone?**

[( )] Self-rating is illegal in HR settings
[( )] Learners never rate themselves accurately
[(X)] People often over- or underestimate their ability, so self-rating needs to be checked against other evidence
[( )] Self-rating takes too long

<div class="takeaway-box">
✅ **Checkpoint reached:** You can define a competency gap and explain the assessment to learners in a way that encourages honest answers.
</div>

--------------------------------------------------------------------------

# Section 2: Defining the Required Competency Profile

<span class="time-chip">⏱ 8–10 minutes</span>

--{{0}}--
You cannot measure a gap without a target. This section defines what an HR professional should be able to do at the Acquire level, across five competency areas adapted from the UNESCO framework.

## The Acquire Level

At the Acquire level a learner is expected to **understand, recognise and apply basic practice responsibly**. They are not expected to build, train or customise AI systems.

<div class="lo-box">

**Required level for every competency area in this programme: Level 3 (Practising)** on the four-level rubric introduced in Section 4. Level 4 is a stretch goal, not a requirement.

</div>

## The Five Competency Areas and What "Good" Looks Like

| # | Competency area | What the HR professional should be able to do at Acquire level |
|---|---|---|
| 1 | **Human-Centred AI** | Treat AI as decision support, not decision-maker. Keep meaningful human oversight over recruitment, disciplinary and performance decisions. |
| 2 | **AI Ethics and Data Privacy** | Recognise bias, fairness and transparency risks. Protect personal and confidential data. Follow organisational policy. |
| 3 | **AI Foundations** | Explain in simple terms what generative AI is, what it can do, and its limits, including hallucination. |
| 4 | **AI Tool Selection and Use** | Choose a suitable tool for a task (for example ChatGPT, Consensus, Copilot, Perplexity), write clear prompts, and verify outputs. |
| 5 | **Professional Learning** | Keep learning, update practice as tools change, and share good practice with colleagues. |

<div class="figure">
<svg viewBox="0 0 640 370" role="img" aria-label="Wheel diagram showing the five competency areas around the Acquire level target: human-centred AI, ethics and data privacy, AI foundations, tool selection and use, and professional learning" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<g stroke="#cfd6de" stroke-width="3">
<line x1="320" y1="190" x2="320" y2="60"/>
<line x1="320" y1="190" x2="443.6" y2="149.8"/>
<line x1="320" y1="190" x2="396.4" y2="295.2"/>
<line x1="320" y1="190" x2="243.6" y2="295.2"/>
<line x1="320" y1="190" x2="196.4" y2="149.8"/>
</g>
<circle cx="320" cy="190" r="56" fill="#17426e"/>
<text x="320" y="182" text-anchor="middle" fill="#ffffff" font-size="14" font-weight="700">ACQUIRE</text>
<text x="320" y="202" text-anchor="middle" fill="#f2a900" font-size="18" font-weight="800">Level 3</text>
<circle cx="320" cy="60" r="32" fill="#1f5c99"/>
<circle cx="443.6" cy="149.8" r="32" fill="#6a3fc7"/>
<circle cx="396.4" cy="295.2" r="32" fill="#1e8e3e"/>
<circle cx="243.6" cy="295.2" r="32" fill="#ef6c00"/>
<circle cx="196.4" cy="149.8" r="32" fill="#2f7fc1"/>
<text x="320" y="71" text-anchor="middle" font-size="30">🤝</text>
<text x="443.6" y="161" text-anchor="middle" font-size="30">⚖️</text>
<text x="396.4" y="306" text-anchor="middle" font-size="30">🧠</text>
<text x="243.6" y="306" text-anchor="middle" font-size="30">🛠️</text>
<text x="196.4" y="161" text-anchor="middle" font-size="30">📚</text>
<text x="320" y="18" text-anchor="middle" fill="#17426e" font-size="14" font-weight="800">1 Human-Centred AI</text>
<text x="484" y="154" text-anchor="start" fill="#17426e" font-size="14" font-weight="800">2 Ethics and</text>
<text x="484" y="172" text-anchor="start" fill="#17426e" font-size="14" font-weight="800">Data Privacy</text>
<text x="396.4" y="350" text-anchor="middle" fill="#17426e" font-size="14" font-weight="800">3 AI Foundations</text>
<text x="243.6" y="350" text-anchor="middle" fill="#17426e" font-size="14" font-weight="800">4 Tool Selection and Use</text>
<text x="156" y="154" text-anchor="end" fill="#17426e" font-size="14" font-weight="800">5 Professional</text>
<text x="156" y="172" text-anchor="end" fill="#17426e" font-size="14" font-weight="800">Learning</text>
</svg>
<div class="fig-cap">Figure 4: The five AI competency areas, all measured against the Acquire-level target</div>
</div>

## Turning Competencies into Observable Indicators

--{{1}}--
A trainer can only assess what can be observed. For each competency area, write indicators: short statements that describe something a learner says, writes, or does.

| Competency area | Example observable indicator |
|---|---|
| Human-Centred AI | "Explains why an AI shortlist must be reviewed by a person before candidates are rejected." |
| AI Ethics and Data Privacy | "Refuses to paste salary or personal records into a public AI tool and names the policy reason." |
| AI Foundations | "Describes hallucination in their own words and gives a workplace example." |
| AI Tool Selection and Use | "Picks a citation-based tool for policy research and checks at least one source." |
| Professional Learning | "Names one way they will keep up with AI changes, such as a trusted newsletter or peer group." |

<div class="tip-box">
💡 **Trainer tip:** Write three to five indicators per competency area. Fewer than three gives a shaky score; more than five makes assessment slow.
</div>

## Adjusting the Required Level for Roles

The default target is Level 3 for everyone. You can raise or lower it for specific roles, but record the reason.

| Role example | Adjustment | Reason |
|---|---|---|
| Recruitment officer | Ethics and Human-Centred target stays at 3, with extra focus on bias | Screening decisions directly affect candidates |
| Payroll or HR data analyst | Data Privacy target raised to 4 | Handles sensitive pay and personal data daily |
| HR assistant (low AI use) | Tool Selection target may stay at 2 initially | Limited current tool use; build up gradually |

---

### 🧩 Scenario-Based Question

<div class="case-box">

**Scenario:** A trainer writes the indicator "Understands AI ethics." A colleague says it is hard to assess.

**What is the best improvement?**

</div>

[( )] Remove the indicator because ethics cannot be assessed
[( )] Keep it and ask learners to rate themselves from 1 to 5
[(X)] Rewrite it as an observable statement, for example "Identifies the bias risk in an AI candidate shortlist and proposes a human check"
[( )] Replace it with a question about how many AI tools the learner owns

*Observable indicators describe what a learner says or does, so two trainers can score the same evidence in the same way.*

<div class="takeaway-box">
✅ **Checkpoint reached:** You now have a defined target: five competency areas, observable indicators, and a required level for each role.
</div>

--------------------------------------------------------------------------

# Section 3: Assessing Current Competency

<span class="time-chip">⏱ 10–12 minutes</span>

--{{0}}--
Now we find out where learners are today. The key principle is triangulation: use more than one method so that no single source misleads you.

## Five Assessment Methods

| Method | What it shows | Strength | Limitation |
|---|---|---|---|
| **Self-assessment questionnaire** | Learner's confidence and awareness | Fast, builds self-reflection | Prone to over- or underestimation |
| **Knowledge check (quiz)** | What the learner knows | Objective, easy to score | Does not show what they do at work |
| **Workplace scenario / work sample** | How the learner applies knowledge | Closest to real practice | Needs a clear rubric and takes longer |
| **Tool-use audit (interview or log)** | Which tools they use, for what, and how safely | Reveals real behaviour and risk | Depends on honest disclosure |
| **Observation or output review** | Real prompts, drafts and checks | Strong evidence of actual skill | Time-consuming; needs consent |

<div class="figure">
<svg viewBox="0 0 760 250" role="img" aria-label="Triangulation diagram: self-assessment, knowledge check and practical evidence combine into one competency score, which is then used to calculate the gap" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<defs><marker id="arTri" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto"><path d="M0 0 L10 5 L0 10 z" fill="#6b7785"/></marker></defs>
<rect x="20" y="20" width="210" height="56" rx="12" fill="#eaf3fb" stroke="#1f5c99" stroke-width="2"/>
<text x="125" y="44" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">Self-assessment · 20%</text>
<text x="125" y="63" text-anchor="middle" fill="#5f6b7a" font-size="12">What I think I can do</text>
<rect x="20" y="97" width="210" height="56" rx="12" fill="#f1ecfb" stroke="#6a3fc7" stroke-width="2"/>
<text x="125" y="121" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">Knowledge check · 30%</text>
<text x="125" y="140" text-anchor="middle" fill="#5f6b7a" font-size="12">What I know</text>
<rect x="20" y="174" width="210" height="56" rx="12" fill="#fff8e8" stroke="#f2a900" stroke-width="2"/>
<text x="125" y="198" text-anchor="middle" fill="#17426e" font-size="15" font-weight="800">Practical evidence · 50%</text>
<text x="125" y="217" text-anchor="middle" fill="#5f6b7a" font-size="12">What I actually do</text>
<line x1="232" y1="48" x2="404" y2="110" stroke="#1f5c99" stroke-width="3" marker-end="url(#arTri)"/>
<line x1="232" y1="125" x2="404" y2="125" stroke="#6a3fc7" stroke-width="6" marker-end="url(#arTri)"/>
<line x1="232" y1="202" x2="404" y2="140" stroke="#f2a900" stroke-width="10" marker-end="url(#arTri)"/>
<circle cx="470" cy="125" r="62" fill="#1f5c99"/>
<text x="470" y="118" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="700">Competency</text>
<text x="470" y="138" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="700">score</text>
<text x="470" y="156" text-anchor="middle" fill="#f2a900" font-size="12">scale 1–4</text>
<line x1="534" y1="125" x2="596" y2="125" stroke="#6b7785" stroke-width="3" marker-end="url(#arTri)"/>
<rect x="600" y="92" width="140" height="66" rx="12" fill="#fdecea" stroke="#d93025" stroke-width="2"/>
<text x="670" y="118" text-anchor="middle" fill="#d93025" font-size="15" font-weight="800">GAP =</text>
<text x="670" y="138" text-anchor="middle" fill="#17426e" font-size="13">Required − Score</text>
</svg>
<div class="fig-cap">Figure 5: Triangulation — three sources of evidence, weighted, produce one fair score. Thicker arrows carry more weight.</div>
</div>

<div class="lo-box">

**Recommended minimum for this programme:** a self-assessment, a knowledge check, **and** at least one scenario or work sample. Add the tool-use audit for every learner who uses AI tools at work.

</div>

## Method 1: Self-Assessment Questionnaire

Ask learners to rate each statement from **1 (low confidence)** to **4 (high confidence)**:

- I can explain in simple terms how generative AI produces its answers.
- I can spot bias and limitations in AI outputs.
- I know which HR data must never be entered into public AI tools.
- I know how to verify AI-generated information before using it.
- I can choose the right AI tool for a given HR task.
- I regularly update my AI knowledge and practice.

<div class="tip-box">
💡 **Trainer tip:** Use the same four-point scale as the rubric so that self-ratings and scored evidence can be compared directly.
</div>

## Method 2: Knowledge Check

Keep it short: 8 to 12 questions, with at least one question per competency area. Mix question types and record each answer against its competency area.

Here is a sample item you could reuse:

**Which statement best describes "responsible AI use" in HR?**

[( )] Using AI for every task to save time
[(X)] Using AI critically, verifying outputs, and protecting data
[( )] Avoiding AI completely
[( )] Letting AI make final HR decisions

## Method 3: Workplace Scenarios and Work Samples

Scenarios test application, not recall. Give a realistic situation and score the learner's response against your indicators.

<div class="case-box">

**Sample scenario for scoring:** An HR employee uploads salary data into ChatGPT to draft a compensation summary. What should they do, and why?

**Look for:** a clear decision (do not upload), the correct reason (confidential data and privacy risk), and a next step (check organisational policy and use an approved, secure system).

</div>

## Method 4: Finding Out How Learners Use AI Tools (Tool-Use Audit)

--{{1}}--
This method answers the question trainers ask most: how do I know how they actually use the tools? Run a short structured conversation, or ask learners to complete a one-page audit form. Cover six areas.

| Audit area | Questions to ask | What to look for |
|---|---|---|
| **1. Which tools** | Which AI tools have you used in the last month? Which are approved by the organisation? | Use of unapproved tools; only one tool used for everything |
| **2. Frequency** | How often do you use them: daily, weekly, occasionally, never? | Very high use with no checking; or avoidance due to fear |
| **3. Task types** | What tasks do you use them for (drafting, research, data, summaries)? | Tool matched to task, or mismatched (for example using a general chatbot for citable research) |
| **4. Data handled** | What information do you put into the tool? Have you ever pasted names, pay, or health information? | **Any confidential data in public tools is a red flag** |
| **5. Verification** | How do you check what the tool tells you? Have you ever found an error? | No checking habit; trusting fluent answers |
| **6. Policy and disclosure** | Do you know your organisation's AI policy? Do you tell colleagues or candidates when AI was used? | No policy awareness; no transparency |

<div class="warning-box">

⚠️ **Red flags that need immediate follow-up, regardless of the overall score**

- Confidential or personal data entered into a public AI tool
- AI output used for a decision about a person without human review
- No awareness that an AI organisational policy exists

</div>

### Tool-Use Audit Scoring Guide

| Level | Typical evidence |
|---|---|
| **1 – Unaware** | Does not use AI, or uses it without thinking about risks; cannot name approved tools |
| **2 – Aware** | Uses one or two tools; knows risks exist but checks inconsistently |
| **3 – Practising** | Uses suitable tools for different tasks; verifies outputs; protects data; knows the policy |
| **4 – Proficient** | Does all of the above consistently, and coaches colleagues |

<div class="figure">
<svg viewBox="0 0 640 245" role="img" aria-label="Staircase of four levels from unaware to proficient, with a flag marking Level 3 as the Acquire target" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<line x1="20" y1="210" x2="620" y2="210" stroke="#9aa5b1" stroke-width="2"/>
<rect x="30" y="160" width="140" height="50" rx="6" fill="#d93025"/>
<rect x="185" y="120" width="140" height="90" rx="6" fill="#ef6c00"/>
<rect x="340" y="80" width="140" height="130" rx="6" fill="#1e8e3e"/>
<rect x="495" y="40" width="130" height="170" rx="6" fill="#0b5d2a"/>
<text x="100" y="192" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="800">1 · Unaware</text>
<text x="255" y="192" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="800">2 · Aware</text>
<text x="410" y="192" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="800">3 · Practising</text>
<text x="560" y="192" text-anchor="middle" fill="#ffffff" font-size="15" font-weight="800">4 · Proficient</text>
<text x="100" y="230" text-anchor="middle" fill="#5f6b7a" font-size="11">Unsafe or no use</text>
<text x="255" y="230" text-anchor="middle" fill="#5f6b7a" font-size="11">Inconsistent checking</text>
<text x="410" y="230" text-anchor="middle" fill="#5f6b7a" font-size="11">Safe and consistent</text>
<text x="560" y="230" text-anchor="middle" fill="#5f6b7a" font-size="11">Coaches others</text>
<line x1="410" y1="80" x2="410" y2="34" stroke="#17426e" stroke-width="3"/>
<polygon points="410,34 372,46 410,58" fill="#f2a900"/>
<text x="362" y="51" text-anchor="end" fill="#17426e" font-size="13" font-weight="800">🎯 Acquire target</text>
</svg>
<div class="fig-cap">Figure 6: The four-level rubric. Level 3 is the Acquire-level target for tool use and every other competency area.</div>
</div>

---

### ✅ Check Your Understanding

**1. A learner scores high on the knowledge quiz but admits pasting candidate CVs into a public chatbot. What does this tell you?**

[( )] Nothing, because the quiz score is high
[(X)] Knowledge is present but practice is unsafe, so the application and data-privacy scores should be low and a follow-up is needed
[( )] The quiz was too easy and should be removed
[( )] The learner should be removed from the course

**2. Select all methods that provide evidence of what a learner actually does at work:**

[[ ]] Self-assessment questionnaire
[[X]] Workplace scenario or work sample
[[X]] Tool-use audit
[[X]] Observation or output review

**3. Why use more than one assessment method?**

[( )] To make the assessment longer
[(X)] To triangulate: each method has blind spots that the others cover
[( )] Because one method is not allowed
[( )] To give learners more chances to pass

<div class="takeaway-box">
✅ **Checkpoint reached:** You can select assessment methods, run a tool-use audit, and recognise the red flags that need immediate action.
</div>

--------------------------------------------------------------------------

# Section 4: Scoring, Calculating and Interpreting the Gap

<span class="time-chip">⏱ 12–15 minutes</span>

--{{0}}--
This is the heart of the course. Here you learn how to turn evidence into scores, calculate the gap, and decide what it means.

## Step 1: The Four-Level Rubric

Score every competency area from 1 to 4.

| Level | Label | Meaning |
|---|---|---|
| **1** | Unaware | Little or no knowledge; practice may be unsafe |
| **2** | Aware | Knows basic ideas; applies them inconsistently |
| **3** | Practising | Applies the competency correctly and consistently with guidance available. **This is the Acquire target** |
| **4** | Proficient | Applies it confidently, adapts to new situations, and helps others |

## Step 2: Weight the Evidence

Convert each source to the 1–4 scale, then combine them with weights. Practical evidence counts most, because it is closest to real behaviour.

| Evidence source | Weight |
|---|---|
| Self-assessment | 20% |
| Knowledge check | 30% |
| Scenario, work sample or tool-use audit | 50% |

**Competency score = (0.2 × Self) + (0.3 × Knowledge) + (0.5 × Practical)**

<div class="figure">
<svg viewBox="0 0 600 200" role="img" aria-label="Donut chart of evidence weights: self-assessment 20 percent, knowledge check 30 percent, practical evidence 50 percent" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<g transform="rotate(-90 110 100)">
<circle cx="110" cy="100" r="60" fill="none" stroke="#1f5c99" stroke-width="34" stroke-dasharray="75.4 301.6"/>
<circle cx="110" cy="100" r="60" fill="none" stroke="#6a3fc7" stroke-width="34" stroke-dasharray="113.1 263.9" stroke-dashoffset="-75.4"/>
<circle cx="110" cy="100" r="60" fill="none" stroke="#f2a900" stroke-width="34" stroke-dasharray="188.5 188.5" stroke-dashoffset="-188.5"/>
</g>
<text x="110" y="98" text-anchor="middle" fill="#17426e" font-size="22" font-weight="800">100%</text>
<text x="110" y="117" text-anchor="middle" fill="#5f6b7a" font-size="12">of evidence</text>
<rect x="230" y="38" width="18" height="18" rx="4" fill="#1f5c99"/>
<text x="258" y="52" fill="#17426e" font-size="14" font-weight="700">Self-assessment — 20%</text>
<rect x="230" y="78" width="18" height="18" rx="4" fill="#6a3fc7"/>
<text x="258" y="92" fill="#17426e" font-size="14" font-weight="700">Knowledge check — 30%</text>
<rect x="230" y="118" width="18" height="18" rx="4" fill="#f2a900"/>
<text x="258" y="132" fill="#17426e" font-size="14" font-weight="700">Scenario, work sample or tool-use audit — 50%</text>
<text x="230" y="170" fill="#5f6b7a" font-size="12" font-style="italic">Practical evidence counts most because it is closest to real behaviour.</text>
</svg>
<div class="fig-cap">Figure 7: How each source of evidence is weighted</div>
</div>

<div class="tip-box">
💡 **Converting a quiz percentage to the 1–4 scale:** below 40% = 1, 40–59% = 2, 60–79% = 3, 80% and above = 4. Agree these cut-points with your team before you start, and use them for every learner.
</div>

## Step 3: Calculate the Gap

**Gap = Required level − Current score** (if the result is negative, record the gap as 0, meaning the requirement is met)

**Readiness index = Average of current scores ÷ Average of required levels**

## Step 4: Interpret the Gap

| Gap size | Category | Trainer response |
|---|---|---|
| **0** | Requirement met | Maintain; offer stretch tasks toward Level 4 |
| **0.1 – 0.5** | Minor gap | Self-study, short practice tasks |
| **0.6 – 1.0** | Moderate gap | Guided activities, coaching, scheduled practice |
| **Above 1.0** | Major gap | Priority training, mentoring, and re-assessment sooner |

<div class="figure">
<svg viewBox="0 0 680 140" role="img" aria-label="Traffic-light scale of gap sizes: 0 met, 0.1 to 0.5 minor, 0.6 to 1.0 moderate, above 1.0 major, with the matching trainer response under each" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<text x="20" y="28" fill="#17426e" font-size="15" font-weight="800">Gap size → trainer response</text>
<rect x="20" y="44" width="96" height="40" rx="8" fill="#1e8e3e"/>
<rect x="120" y="44" width="156" height="40" rx="8" fill="#f2a900"/>
<rect x="280" y="44" width="196" height="40" rx="8" fill="#ef6c00"/>
<rect x="480" y="44" width="176" height="40" rx="8" fill="#d93025"/>
<text x="68" y="69" text-anchor="middle" fill="#ffffff" font-size="14" font-weight="800">0 · Met</text>
<text x="198" y="69" text-anchor="middle" fill="#17426e" font-size="14" font-weight="800">0.1–0.5 · Minor</text>
<text x="378" y="69" text-anchor="middle" fill="#ffffff" font-size="14" font-weight="800">0.6–1.0 · Moderate</text>
<text x="568" y="69" text-anchor="middle" fill="#ffffff" font-size="14" font-weight="800">&gt; 1.0 · Major</text>
<text x="68" y="108" text-anchor="middle" fill="#5f6b7a" font-size="12">Stretch tasks</text>
<text x="198" y="108" text-anchor="middle" fill="#5f6b7a" font-size="12">Self-study</text>
<text x="378" y="108" text-anchor="middle" fill="#5f6b7a" font-size="12">Coaching and practice</text>
<text x="568" y="108" text-anchor="middle" fill="#5f6b7a" font-size="12">Priority training</text>
</svg>
<div class="fig-cap">Figure 8: Reading the gap — from requirement met to major gap</div>
</div>

--{{1}}--
Two further checks make interpretation fairer. First, the perception gap: compare the learner's self-rating with their weighted score. A difference of 1.0 or more where the self-rating is higher is an overconfidence flag, which matters most in ethics and data privacy. Second, red flags from the tool-use audit override a good average. A learner with a 3.0 average who pastes confidential data into public tools still needs urgent follow-up.

## Worked Example: Amira, HR Officer

<div class="case-box">

Amira completed all three assessment methods. Required level is 3.0 for every area.

| Competency area | Self | Knowledge | Practical | **Score** | **Gap** | Self minus score | Category |
|---|---|---|---|---|---|---|---|
| Human-Centred AI | 4 | 3 | 3 | **3.2** | 0 | +0.8 | Met |
| AI Ethics and Data Privacy | 4 | 2 | 2 | **2.4** | 0.6 | **+1.6** ⚠️ | Moderate |
| AI Foundations | 3 | 3 | 2 | **2.5** | 0.5 | +0.5 | Minor |
| AI Tool Selection and Use | 3 | 2 | 2 | **2.2** | 0.8 | +0.8 | Moderate |
| Professional Learning | 2 | 2 | 2 | **2.0** | 1.0 | 0.0 | Moderate (top priority) |

**Working for Ethics:** (0.2 × 4) + (0.3 × 2) + (0.5 × 2) = 0.8 + 0.6 + 1.0 = **2.4**. Gap = 3.0 − 2.4 = **0.6**.

**Readiness index:** average current = (3.2 + 2.4 + 2.5 + 2.2 + 2.0) ÷ 5 = 2.46. Required average = 3.0. Readiness = 2.46 ÷ 3.0 = **82%**.

</div>

<div class="figure">
<svg viewBox="0 0 700 340" role="img" aria-label="Radar chart comparing Amira's scores with the required level of 3.0 across five competency areas. Her scores are 3.2, 2.4, 2.5, 2.2 and 2.0" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<g fill="none" stroke="#cfd6de" stroke-width="1">
<polygon points="220,160 248.5,180.7 237.6,214.3 202.4,214.3 191.5,180.7"/>
<polygon points="220,130 277.1,171.5 255.3,238.5 184.7,238.5 162.9,171.5"/>
<polygon points="220,100 305.6,162.2 272.9,262.8 167.1,262.8 134.4,162.2"/>
<polygon points="220,70 334.1,152.9 290.6,287.1 149.4,287.1 105.9,152.9"/>
<line x1="220" y1="190" x2="220" y2="70"/>
<line x1="220" y1="190" x2="334.1" y2="152.9"/>
<line x1="220" y1="190" x2="290.6" y2="287.1"/>
<line x1="220" y1="190" x2="149.4" y2="287.1"/>
<line x1="220" y1="190" x2="105.9" y2="152.9"/>
</g>
<polygon points="220,100 305.6,162.2 272.9,262.8 167.1,262.8 134.4,162.2" fill="#f2a900" fill-opacity="0.12" stroke="#f2a900" stroke-width="3" stroke-dasharray="8 5"/>
<polygon points="220,94 288.5,167.8 264.1,250.7 181.2,243.4 162.9,171.5" fill="#1f5c99" fill-opacity="0.30" stroke="#1f5c99" stroke-width="3"/>
<circle cx="220" cy="94" r="5" fill="#1f5c99"/>
<circle cx="288.5" cy="167.8" r="5" fill="#d93025"/>
<circle cx="264.1" cy="250.7" r="5" fill="#d93025"/>
<circle cx="181.2" cy="243.4" r="5" fill="#d93025"/>
<circle cx="162.9" cy="171.5" r="5" fill="#d93025"/>
<g fill="#8a95a3" font-size="10">
<text x="225" y="162">1</text>
<text x="225" y="132">2</text>
<text x="225" y="102">3</text>
<text x="225" y="72">4</text>
</g>
<g fill="#17426e" font-size="13" font-weight="700">
<text x="220" y="54" text-anchor="middle">Human-Centred AI</text>
<text x="346" y="150">Ethics and Privacy</text>
<text x="305" y="314" text-anchor="middle">AI Foundations</text>
<text x="140" y="314" text-anchor="middle">Tool Selection</text>
<text x="96" y="150" text-anchor="end">Prof. Learning</text>
</g>
<line x1="500" y1="110" x2="540" y2="110" stroke="#f2a900" stroke-width="3" stroke-dasharray="8 5"/>
<text x="550" y="115" fill="#17426e" font-size="13">Required level (3.0)</text>
<rect x="500" y="136" width="40" height="14" fill="#1f5c99" fill-opacity="0.35" stroke="#1f5c99" stroke-width="2"/>
<text x="550" y="148" fill="#17426e" font-size="13">Amira's score (example)</text>
<circle cx="520" cy="178" r="5" fill="#d93025"/>
<text x="550" y="183" fill="#17426e" font-size="13">Area with a gap</text>
<text x="500" y="220" fill="#5f6b7a" font-size="12" font-style="italic">Inside the gold ring = gap</text>
</svg>
<div class="fig-cap">Figure 9: Amira's competency profile compared with the required level</div>
</div>

<div class="figure">
<svg viewBox="0 0 700 250" role="img" aria-label="Horizontal bar chart of Amira's gaps: Human-Centred AI met, Ethics and Data Privacy 0.6, AI Foundations 0.5, Tool Selection and Use 0.8, Professional Learning 1.0" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<text x="20" y="26" fill="#17426e" font-size="15" font-weight="800">Gap by competency area (Required 3.0 − Score)</text>
<line x1="200" y1="38" x2="200" y2="218" stroke="#9aa5b1" stroke-width="2"/>
<g fill="#17426e" font-size="13" font-weight="700" text-anchor="end">
<text x="190" y="61">Human-Centred AI</text>
<text x="190" y="97">Ethics and Data Privacy</text>
<text x="190" y="133">AI Foundations</text>
<text x="190" y="169">Tool Selection and Use</text>
<text x="190" y="205">Professional Learning</text>
</g>
<text x="210" y="61" fill="#1e8e3e" font-size="14" font-weight="800">✓ Met</text>
<rect x="200" y="80" width="180" height="24" rx="4" fill="#ef6c00"/>
<text x="390" y="97" fill="#17426e" font-size="14" font-weight="800">0.6 ⚠️ overconfident</text>
<rect x="200" y="116" width="150" height="24" rx="4" fill="#f2a900"/>
<text x="360" y="133" fill="#17426e" font-size="14" font-weight="800">0.5</text>
<rect x="200" y="152" width="240" height="24" rx="4" fill="#ef6c00"/>
<text x="450" y="169" fill="#17426e" font-size="14" font-weight="800">0.8</text>
<rect x="200" y="188" width="300" height="24" rx="4" fill="#ef6c00"/>
<text x="510" y="205" fill="#17426e" font-size="14" font-weight="800">1.0 · top priority</text>
<text x="200" y="240" fill="#5f6b7a" font-size="12" font-style="italic">Longest bar = first priority, unless a red flag or overconfidence says otherwise</text>
</svg>
<div class="fig-cap">Figure 10: Amira's gap by competency area</div>
</div>

--{{2}}--
Read the radar chart like this: where the blue shape falls inside the gold ring, there is a gap. The further inside, the larger the gap.

### What the Trainer Concludes About Amira

- **Strength:** Human-Centred AI meets the requirement.
- **Urgent:** Ethics and Data Privacy. The gap is moderate, but Amira rated herself 4 while the evidence says 2.4, so she may not realise her practice is risky. Start here with a short scenario-based session and review her tool-use audit for data handling.
- **Priority gap:** Professional Learning (1.0). Set up a simple routine for keeping up to date.
- **Next:** Tool Selection and AI Foundations through guided practice and short self-study.

## Reading Group Results

When you assess a whole cohort, add a group view.

| Group question | How to answer it |
|---|---|
| Which competency has the largest average gap? | Average the gap for each area across learners; plan group sessions for the largest |
| Who needs individual support? | List learners with any gap above 1.0 or any red flag |
| Who is ready for a stretch task? | List learners with all gaps at 0 |
| Is there an overconfidence pattern? | Count learners where self minus score is 1.0 or more |

<div class="warning-box">

⚠️ **Fairness and privacy when scoring**

- Use the same rubric, weights and cut-points for every learner
- Where possible, have a second trainer score a sample to check consistency
- Share individual results only with the learner and the trainer; report group data anonymised
- Treat the score as a guide to support, never as grounds for punishment

</div>

---

### 🧩 Practice: Calculate a Score

<div class="case-box">

**Scenario:** A learner has Self = 3, Knowledge = 4, Practical = 2 for AI Tool Selection and Use. Required level is 3.

**What is the competency score?** (0.2 × 3) + (0.3 × 4) + (0.5 × 2)

</div>

[( )] 2.5
[(X)] 2.8
[( )] 3.0
[( )] 3.4

*Working: 0.6 + 1.2 + 1.0 = 2.8. Gap = 3.0 − 2.8 = 0.2, a minor gap.*

### Interpret This Result

A learner has a score of 2.9 on every area but told you in the audit that they regularly paste candidate details into a public chatbot. What is the best response?

[( )] No action, because all gaps are minor
[(X)] Treat as a priority: raise the data-privacy issue immediately, review policy with the learner, and re-check practice, despite the good average
[( )] Remove them from the course
[( )] Wait until the post-assessment

<div class="takeaway-box">
✅ **Checkpoint reached:** You can weight evidence, calculate scores and gaps, flag overconfidence and red flags, and decide the right response for each category.
</div>

--------------------------------------------------------------------------

# Section 5: Closing the Gap and Measuring Progress

<span class="time-chip">⏱ 8–10 minutes</span>

--{{0}}--
A gap analysis is only useful if it leads to action. This section covers how to plan development, run the post-assessment and report progress.

## Matching Development Activities to Gap Size

| Gap category | Suggested activities |
|---|---|
| **Minor** | Self-study tasks, short guided practice, a checklist for verifying outputs |
| **Moderate** | Coaching sessions, practice with a feedback loop, scenario workshops |
| **Major** | Structured training, mentoring, and an early re-assessment |
| **Met** | Peer-coaching role, stretch tasks, contribution to policy review |

### Good Practice for All Learners

- ✅ Practise with AI tools in low-risk situations first
- ✅ Verify AI outputs against trusted sources
- ✅ Use different tools for different purposes (for example a drafting tool, a citation-based research tool, an office productivity tool)
- ✅ Apply fairness, transparency and privacy consistently

## The Feedback Conversation

--{{1}}--
Share each learner's profile in a short one-to-one conversation. Start with strengths, show the gap clearly, and agree actions together.

<div class="case-box">

### 🗣️ Suggested Structure (10–15 minutes)

1. **Start with strengths:** "Here is where you already meet the requirement."
2. **Show the profile:** the radar chart and the gap table.
3. **Discuss perception gaps gently:** "You rated yourself 4 on ethics, and your scenario answers suggested 2. What do you think explains that?"
4. **Agree two or three priorities** (not all gaps at once).
5. **Set a date** for re-assessment.

</div>

<div class="figure">
<svg viewBox="0 0 700 110" role="img" aria-label="Five-step feedback conversation: strengths, profile, perception gaps, priorities, date" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<polygon points="10,20 120,20 140,50 120,80 10,80 30,50" fill="#1e8e3e"/>
<polygon points="144,20 254,20 274,50 254,80 144,80 164,50" fill="#1f5c99"/>
<polygon points="278,20 388,20 408,50 388,80 278,80 298,50" fill="#6a3fc7"/>
<polygon points="412,20 522,20 542,50 522,80 412,80 432,50" fill="#ef6c00"/>
<polygon points="546,20 656,20 676,50 656,80 546,80 566,50" fill="#f2a900"/>
<g fill="#ffffff" font-size="14" font-weight="800" text-anchor="middle">
<text x="75" y="45">1</text>
<text x="209" y="45">2</text>
<text x="343" y="45">3</text>
<text x="477" y="45">4</text>
<text x="611" y="45" fill="#17426e">5</text>
</g>
<g fill="#ffffff" font-size="13" font-weight="700" text-anchor="middle">
<text x="75" y="64">Strengths</text>
<text x="209" y="64">Profile</text>
<text x="343" y="64">Perception</text>
<text x="477" y="64">Priorities</text>
<text x="611" y="64" fill="#17426e">Date</text>
</g>
</svg>
<div class="fig-cap">Figure 11: The feedback conversation in five moves</div>
</div>

## Personal Development Plan Template

Complete this with the learner.

| Item | Learner's plan |
|---|---|
| Learner name and date | |
| Priority competency (largest gap or red flag) | |
| Current score and target | |
| Actions (what, how, how often) | |
| AI tool to practise with, and the task | |
| One ethical rule the learner will follow | |
| Support from trainer (coaching, resources) | |
| Re-assessment date | |

Try completing a plan for the Amira example in the box below.

My priority competency for Amira is:

[[ Write here... ]]

The first action I would agree with her:

[[ Write here... ]]

## Post-Assessment

Repeat the **same** methods and the **same** rubric, weights and cut-points as the baseline. Changing the instrument makes the comparison meaningless.

### Measuring Improvement

| Measure | Formula | Meaning |
|---|---|---|
| **Change in score** | Post − Pre | Raw improvement |
| **Normalised gain** | (Post − Pre) ÷ (4 − Pre) | Share of the possible improvement achieved |
| **Gap closed** | Pre gap − Post gap | How much of the gap has been closed |

**Worked example (Amira, Ethics):** Pre = 2.4, Post = 3.2. Change = 0.8. Normalised gain = 0.8 ÷ (4 − 2.4) = 0.8 ÷ 1.6 = **0.5**, so she achieved half of the possible improvement. The gap has closed from 0.6 to 0, so the requirement is now met.

### Example Progress Report

| Competency | Pre | Post | Required | Status |
|---|---|---|---|---|
| Human-Centred AI | 3.2 | 3.4 | 3.0 | Met |
| Ethics and Data Privacy | 2.4 | 3.2 | 3.0 | Met |
| AI Foundations | 2.5 | 3.3 | 3.0 | Met |
| Tool Selection and Use | 2.2 | 3.1 | 3.0 | Met |
| Professional Learning | 2.0 | 3.0 | 3.0 | Met |

<div class="figure">
<svg viewBox="0 0 720 340" role="img" aria-label="Grouped bar chart of before and after scores for five competency areas, with a dashed line at the required level of 3.0. After scores are 3.4, 3.2, 3.3, 3.1 and 3.0" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<rect x="70" y="8" width="14" height="14" rx="3" fill="#d93025"/>
<text x="90" y="20" fill="#17426e" font-size="13" font-weight="700">Before</text>
<rect x="160" y="8" width="14" height="14" rx="3" fill="#1e8e3e"/>
<text x="180" y="20" fill="#17426e" font-size="13" font-weight="700">After</text>
<line x1="250" y1="15" x2="284" y2="15" stroke="#f2a900" stroke-width="3" stroke-dasharray="6 4"/>
<text x="292" y="20" fill="#17426e" font-size="13" font-weight="700">Required level (3.0)</text>
<g stroke="#e1e6ec" stroke-width="1">
<line x1="60" y1="210" x2="690" y2="210"/>
<line x1="60" y1="150" x2="690" y2="150"/>
<line x1="60" y1="30" x2="690" y2="30"/>
</g>
<line x1="60" y1="270" x2="690" y2="270" stroke="#9aa5b1" stroke-width="2"/>
<g fill="#8a95a3" font-size="11" text-anchor="end">
<text x="52" y="274">0</text>
<text x="52" y="214">1</text>
<text x="52" y="154">2</text>
<text x="52" y="94">3</text>
<text x="52" y="34">4</text>
</g>
<g fill="#d93025">
<rect x="82" y="78" width="36" height="192" rx="3"/>
<rect x="206" y="126" width="36" height="144" rx="3"/>
<rect x="330" y="120" width="36" height="150" rx="3"/>
<rect x="454" y="138" width="36" height="132" rx="3"/>
<rect x="578" y="150" width="36" height="120" rx="3"/>
</g>
<g fill="#1e8e3e">
<rect x="126" y="66" width="36" height="204" rx="3"/>
<rect x="250" y="78" width="36" height="192" rx="3"/>
<rect x="374" y="72" width="36" height="198" rx="3"/>
<rect x="498" y="84" width="36" height="186" rx="3"/>
<rect x="622" y="90" width="36" height="180" rx="3"/>
</g>
<line x1="60" y1="90" x2="690" y2="90" stroke="#f2a900" stroke-width="3" stroke-dasharray="8 5"/>
<g fill="#17426e" font-size="11" font-weight="700" text-anchor="middle">
<text x="100" y="72">3.2</text>
<text x="144" y="60">3.4</text>
<text x="224" y="120">2.4</text>
<text x="268" y="72">3.2</text>
<text x="348" y="114">2.5</text>
<text x="392" y="66">3.3</text>
<text x="472" y="132">2.2</text>
<text x="516" y="78">3.1</text>
<text x="596" y="144">2.0</text>
<text x="640" y="84">3.0</text>
</g>
<g fill="#17426e" font-size="12" font-weight="700" text-anchor="middle">
<text x="122" y="292">Human-Centred</text>
<text x="246" y="292">Ethics and Privacy</text>
<text x="370" y="292">AI Foundations</text>
<text x="494" y="292">Tool Selection</text>
<text x="618" y="292">Prof. Learning</text>
</g>
<text x="360" y="320" text-anchor="middle" fill="#5f6b7a" font-size="12" font-style="italic">Example data: Amira, before and after development activities</text>
</svg>
<div class="fig-cap">Figure 12: Before and after scores against the required level</div>
</div>

<div class="tip-box">
💡 **Trainer tip:** If a learner's score does not improve, do not assume the learner failed. Check whether the activities matched the gap, whether the learner had time to practise, and whether the instrument was applied consistently.
</div>

---

### ✅ Final Knowledge Check

**1. Which is the correct order of the gap assessment cycle?**

[( )] Score, define, develop, assess, interpret
[(X)] Define, assess, score, interpret, develop and re-assess
[( )] Assess, develop, define, score, interpret
[( )] Develop, assess, define, interpret, score

**2. Why must the post-assessment use the same instrument as the baseline?**

[( )] To save preparation time
[(X)] So that changes in scores reflect real learning, not changes in the test
[( )] Because learners prefer repeated questions
[( )] Because the rubric cannot be changed after the course

**3. A learner has a gap of 0.8 in Tool Selection and Use. What category is it and what is a suitable response?**

[( )] Minor; self-study only
[(X)] Moderate; guided activities, coaching and practice with feedback
[( )] Major; remove the learner from the programme
[( )] Met; no action

**4. Which finding should trigger immediate follow-up even when the average score is good?**

[( )] The learner prefers one tool over others
[(X)] The learner enters confidential data into a public AI tool
[( )] The learner rated themselves lower than their score
[( )] The learner asked a question during the quiz

### ✍️ Final Reflection

- Which method in this course will you use first with your own learners, and why?
- What is the biggest risk to a fair assessment in your setting, and how will you reduce it?
- How will you keep your own AI knowledge current?

[[ Write a few sentences here... ]]

<div class="takeaway-box">

### 🏆 Key Takeaways

- A competency gap is **Required − Current**, based on **evidence**, not opinion
- Use **several methods** (self-assessment, knowledge check, scenarios, tool-use audit) and weight practical evidence most
- Score with a **consistent rubric**, calculate the gap, and check for **overconfidence** and **red flags**
- Respond to **gap size** with matched development activities
- **Re-assess with the same instrument** and report improvement honestly

</div>

--------------------------------------------------------------------------

## 📦 Your Trainer Portfolio

By completing this module you have produced:

- ✅ A defined required competency profile with observable indicators
- ✅ A planned assessment blueprint using at least three methods
- ✅ A worked gap calculation and interpretation (Amira example)
- ✅ A draft development plan and a post-assessment approach
- ✅ A personal reflection on applying gap assessment in your own training context

### Success Criteria Checklist

- [x] Defined required competencies and indicators for the Acquire level
- [x] Selected and justified assessment methods, including a tool-use audit
- [x] Scored evidence with the rubric and calculated a competency gap
- [x] Interpreted results, including overconfidence flags and red flags
- [x] Planned development and a like-for-like post-assessment

--------------------------------------------------------------------------

## 🧰 Appendix: Ready-to-Use Trainer Templates

<div class="figure">
<svg viewBox="0 0 720 230" role="img" aria-label="One-page cheat sheet with the score formula, the gap formula, the readiness index formula, and a red-flag reminder" xmlns="http://www.w3.org/2000/svg" font-family="Inter, Arial, sans-serif">
<rect x="20" y="16" width="220" height="116" rx="14" fill="#eaf3fb" stroke="#1f5c99" stroke-width="2"/>
<text x="130" y="44" text-anchor="middle" fill="#1f5c99" font-size="15" font-weight="800">📊 SCORE</text>
<text x="130" y="72" text-anchor="middle" fill="#17426e" font-size="13">0.2 × Self + 0.3 × Knowledge</text>
<text x="130" y="92" text-anchor="middle" fill="#17426e" font-size="13">+ 0.5 × Practical</text>
<text x="130" y="116" text-anchor="middle" fill="#5f6b7a" font-size="11">per competency area, scale 1–4</text>
<rect x="250" y="16" width="220" height="116" rx="14" fill="#fff8e8" stroke="#f2a900" stroke-width="2"/>
<text x="360" y="44" text-anchor="middle" fill="#b87f00" font-size="15" font-weight="800">🎯 GAP</text>
<text x="360" y="78" text-anchor="middle" fill="#17426e" font-size="15" font-weight="700">Required − Score</text>
<text x="360" y="116" text-anchor="middle" fill="#5f6b7a" font-size="11">minimum 0 · bands: 0 / 0.5 / 1.0 / above</text>
<rect x="480" y="16" width="220" height="116" rx="14" fill="#e9f9ee" stroke="#1e8e3e" stroke-width="2"/>
<text x="590" y="44" text-anchor="middle" fill="#1e8e3e" font-size="15" font-weight="800">🏁 READINESS</text>
<text x="590" y="78" text-anchor="middle" fill="#17426e" font-size="14" font-weight="700">Avg score ÷ Avg required</text>
<text x="590" y="116" text-anchor="middle" fill="#5f6b7a" font-size="11">Amira example: 2.46 ÷ 3.0 = 82%</text>
<rect x="20" y="150" width="680" height="64" rx="14" fill="#fdecea" stroke="#d93025" stroke-width="2"/>
<text x="360" y="177" text-anchor="middle" fill="#d93025" font-size="15" font-weight="800">⚠️ RED FLAG = ACT NOW, WHATEVER THE AVERAGE</text>
<text x="360" y="198" text-anchor="middle" fill="#17426e" font-size="12">Confidential data in public tools · AI-only decisions about people · No policy awareness · Self minus score ≥ 1.0</text>
</svg>
<div class="fig-cap">Figure 13: Gap assessment at a glance — a one-page trainer cheat sheet</div>
</div>

### A. Assessment Blueprint

| Competency area | Self-assessment items | Knowledge items | Scenario or work sample | Tool-use audit area |
|---|---|---|---|---|
| Human-Centred AI | | | | |
| Ethics and Data Privacy | | | | |
| AI Foundations | | | | |
| Tool Selection and Use | | | | |
| Professional Learning | | | | |

### B. Individual Scoring Sheet

| Competency area | Self (1–4) | Knowledge (1–4) | Practical (1–4) | Score | Required | Gap | Flag |
|---|---|---|---|---|---|---|---|
| Human-Centred AI | | | | | 3.0 | | |
| Ethics and Data Privacy | | | | | 3.0 | | |
| AI Foundations | | | | | 3.0 | | |
| Tool Selection and Use | | | | | 3.0 | | |
| Professional Learning | | | | | 3.0 | | |

Score = (0.2 × Self) + (0.3 × Knowledge) + (0.5 × Practical). Gap = Required − Score (minimum 0). Flag overconfidence where Self − Score ≥ 1.0.

### C. Tool-Use Audit Form (one page per learner)

| Question | Learner's answer | Trainer's note |
|---|---|---|
| Which AI tools did you use in the last month? | | |
| Which are approved by the organisation? | | |
| What tasks do you use them for? | | |
| What data do you enter? Any personal or confidential data? | | |
| How do you verify outputs? | | |
| Do you know the organisational AI policy? | | |
| Do you disclose when AI has been used? | | |

--------------------------------------------------------------------------

## 📚 Resources

### Core Tools (for trainers to demonstrate and learners to practise with)

- [ChatGPT](https://chat.openai.com) — drafting and brainstorming
- [Consensus](https://consensus.app) — evidence-based AI research with citations
- [Microsoft Copilot](https://copilot.microsoft.com) — workplace productivity
- [Perplexity AI](https://www.perplexity.ai) — sourced web search

### Learning Materials

- Organisational AI ethics guidelines (consult your HR policy library)
- Workplace AI usage policy (consult your organisation's internal policy)
- Short explainer videos on AI basics, ethics and tools (linked throughout this module)

--------------------------------------------------------------------------

## 📖 References

UNESCO. (2024). *AI Competency Framework for Teachers and Students.* United Nations Educational, Scientific and Cultural Organization.

Consensus AI. (2025). *Evidence synthesis and citation-based AI search platform.* Retrieved from https://consensus.app

Knowles, M. S., Holton, E. F., & Swanson, R. A. (2020). *The Adult Learner: The Definitive Classic in Adult Education and Human Resource Development* (9th ed.). Routledge.

OECD. (2024). *OECD AI Principles overview.* Organisation for Economic Co-operation and Development.

<div class="tip-box">
ℹ️ **Note on citations:** This reference list reflects the general source types used in the course design (UNESCO framework, adult learning theory, and AI ethics guidance). Replace with your institution's full Consensus AI bibliography and exact citation details before publishing.
</div>

--------------------------------------------------------------------------

<div class="lo-box">

### 🎓 Congratulations!

You have completed **Assessing AI Competency Gaps in HR Professionals**. You can now define the required profile, assess current knowledge and tool use, score and interpret gaps, and plan and measure improvement for the HR professionals you train. Your portfolio evidence is ready to be exported or submitted as part of your professional development record.

</div>
