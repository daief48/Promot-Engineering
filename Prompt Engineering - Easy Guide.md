# 📘 Prompt Engineering — The Easy Guide

*A short, simple book for beginners. Read it in 10 minutes, use it forever.*

---

## 1. What is a Prompt?

A **prompt** is simply what you type to an AI.

The AI knows nothing about your wishes until you tell it.

> 🍳 **Think of the AI like a chef.**
> If you say *"make food"* — you might get anything.
> If you say *"make spicy chicken biryani for 2 people"* — you get what you want.

---

## 2. What is Prompt Engineering?

**Prompt Engineering = writing instructions so the AI doesn't have to guess.**

```
Good prompt  →  Good answer
Bad prompt   →  Guessing  →  Wrong answer
```

---

## 3. The Golden Rule

> ### ⭐ Don't make the AI guess. If it's important — say it.

**❌ Weak prompt:**
```
Make a login system.
```
The AI must guess: Which language? Which database? Which fields? What response?

**✅ Strong prompt:**
```
Build a login API using Laravel and Sanctum tokens.
Return JSON with the user and token.
Do not change any existing code.
```
Now the AI has nothing to guess.

---

## 4. The 6 Building Blocks of a Good Prompt

| Block | Question it answers |
|---|---|
| **Role** | Who should the AI act as? |
| **Task** | What should it do? |
| **Context** | What does it need to know? |
| **Requirements** | What MUST be included? |
| **Constraints** | What must NOT happen? |
| **Output** | How should the answer look? |

**All 6 together:**
```
ROLE:        You are a senior Laravel developer.
TASK:        Fix the login API.
CONTEXT:     Laravel 12 + MySQL + React frontend. Sanctum is used.
REQUIREMENTS: Valid login returns a token. Wrong password returns 401.
CONSTRAINTS: Do not change the database. Do not touch registration.
OUTPUT:      1. The problem  2. Fixed code  3. How to test it
```

> 💡 Simple question? Skip the structure. Complex task? Use all 6.
> **Structure matters more than length.**

---

## 5. Five Techniques That Improve Any Prompt

### 1️⃣ Be specific
```
❌ Make my website better.
✅ Improve the dashboard UI: better spacing, larger text on mobile, faster loading.
```

### 2️⃣ Give context
```
❌ Fix the bug.
✅ Fix the login API bug. It returns 500 on a wrong password.
   It should return 401 instead.
```

### 3️⃣ Show an example (the few-shot trick)
Showing beats explaining. One example teaches the pattern:
```
Rewrite messages in a polite, professional tone.

Example:
Input:  "i can't come today"
Output: "Hi, I'm feeling unwell today, so I won't be able to come in."

Now rewrite:
Input:  "i will be late tomorrow"
```

### 4️⃣ Set boundaries (constraints)
This protects your project — the AI only touches what you allow:
```
Only modify the login page.
Do not touch the backend, database, or other pages.
```

### 5️⃣ Define "done"
Tell the AI what success looks like:
```
Done means: valid login returns a token,
wrong password returns 401, nothing else changes.
```

---

## 6. Zero-Shot vs One-Shot vs Few-Shot

| Technique | Examples given | Use when |
|---|---|---|
| **Zero-shot** | 0 | The task is common and clear |
| **One-shot** | 1 | You want a specific style or format |
| **Few-shot** | 2+ | The pattern is complex — classify, format, code style |

```
Zero-shot:  "Translate this to English."
Few-shot:   "Here are 3 translation examples. Follow this style.
             Now translate this one."
```

> Like teaching a junior developer: **tell them → show them once → show them several times.**

---

## 7. Copy-Paste Template

```
ROLE:
You are a [expert type].

TASK:
[One clear action + target.]

CONTEXT:
[Project, tech stack, what already exists.]

REQUIREMENTS:
- [Must do 1]
- [Must do 2]

CONSTRAINTS:
- [Must NOT do 1]
- [Must NOT do 2]

OUTPUT:
1. [Plan]  2. [Code/answer]  3. [How to test/use it]
```

---

## 8. Common Mistakes to Avoid

| Mistake | Fix |
|---|---|
| ❌ "Make it better" | ✅ Say *what exactly* to improve |
| ❌ No context | ✅ Tell it the stack and what exists |
| ❌ No boundaries | ✅ Say what it must NOT touch |
| ❌ Contradictions ("change nothing" + "add a feature") | ✅ One clear direction |
| ❌ Very long prompt full of useless info | ✅ Only relevant details |

---

## 9. The Whole Book in One Line

> **Tell the AI what to do, what it needs to know, what not to touch, and what the result should look like — then let it work.**

*Simple task → simple prompt. Complex task → structured prompt.*

🎯 **Practice:** Take this bad prompt and fix it using the 6 blocks:
> *"Make a website for my app."*

---
*End of guide. Master these basics and you're ahead of 90% of AI users.* 🚀
10. Task Decomposition

Breaking a large task into smaller tasks.

Instead of:

Build my entire application.

Use:

1. Analyze requirements
2. Design architecture
3. Design database
4. Design API
5. Build backend
6. Build frontend
7. Test
8. Optimize
11. Step-by-Step Reasoning

How to ask AI to reason through difficult problems without relying on vague instructions like “think harder.”

12. Structured Output

Controlling output using:

Markdown
Tables
JSON
XML
Lists
Code blocks
Schemas
Templates

Example:

Return the result in this JSON structure:

{
  "problem": "",
  "cause": "",
  "solution": "",
  "code": ""
}
🟠 LEVEL 3 — Advanced Prompting
13. Chain-of-Thought Concepts
Reasoning prompts
When reasoning helps
When it doesn't
Asking for concise reasoning summaries
Avoiding unnecessary reasoning output
14. Self-Consistency

Ask the model to consider multiple possible approaches and select the strongest one.

15. Self-Critique

Have AI review its own output.

First create the solution.

Then review your solution for:
- Bugs
- Security problems
- Missing requirements
- Performance issues

Finally provide the corrected version.
16. Reflection

AI evaluates its previous response and improves it.

17. ReAct-Style Reasoning

Combining:

Reason → Act → Observe → Continue

Important for AI agents and tool-using systems.

18. Prompt Chaining

One prompt's output becomes the next prompt's input.

Requirements
   ↓
Architecture
   ↓
Database
   ↓
API
   ↓
Frontend
   ↓
Testing
🔵 LEVEL 4 — Context & Large Projects
19. Context Window

Understand:

Tokens
Context window
Input tokens
Output tokens
Token limits
Context overflow
20. Token Optimization

How to reduce unnecessary tokens while preserving useful information.

21. Context Compression

Turning a huge conversation/project into a compact useful summary.

22. Long-Context Prompting

Working with:

Large documents
Large codebases
Requirements
Logs
API documentation
23. Project Context

How to tell AI about:

Project
├── Tech stack
├── Architecture
├── Database
├── Coding standards
├── Business rules
├── Existing features
└── Restrictions
24. Persistent Instructions

Creating reusable instructions for your projects.

🟣 LEVEL 5 — Coding Prompt Engineering

This will be especially important for you because you use AI for development.

25. Code Generation Prompts
Laravel
React
React Native
Node.js
Next.js
Prisma
SQL
26. Code Debugging Prompts

How to provide:

Error
Stack trace
Relevant code
Environment
Expected behavior
Actual behavior
27. Code Review Prompts
Review this code for:
- Bugs
- Security vulnerabilities
- Performance
- Maintainability
- Laravel best practices
28. Refactoring Prompts
29. Feature Development Prompts
30. Architecture Prompts
31. Database Design Prompts
32. API Design Prompts
33. Testing Prompts
Unit tests
Feature tests
Integration tests
Edge cases
34. Security Prompts
Authentication
Authorization
SQL injection
XSS
CSRF
API security
Data validation
🔴 LEVEL 6 — AI-Assisted Software Development
35. AI Coding Workflow

How to work with:

Claude
ChatGPT
Cursor
Antigravity
VS Code AI
GitHub Copilot
36. AI Coding Agent Prompts

How to tell an AI agent:

Analyze → Plan → Implement → Test → Fix → Report

37. Repository-Level Prompting

Give AI understanding of an entire project rather than individual files.

38. Existing Codebase Modification

Very important:

Do not rewrite existing functionality.
Only modify the requested feature.
39. Safe Code Changes

How to prevent AI from unnecessarily changing:

Backend
Database
APIs
Existing UI
Authentication
Business logic
40. Debugging Workflow

A professional AI debugging loop:

Error
 ↓
Reproduce
 ↓
Analyze
 ↓
Identify root cause
 ↓
Fix
 ↓
Test
 ↓
Regression check
🟤 LEVEL 7 — Prompt Engineering for UI/UX
41. UI Generation Prompts
42. UX Design Prompts
43. Design System Prompts
44. Responsive Design Prompts
45. Mobile UI Prompts
46. Animation Prompts
47. Landing Page Prompts
48. Dashboard Prompts
49. Component-Level Prompts
50. Design Refinement Prompts

For example:

Don't change the functionality.

Only improve:
- Typography
- Spacing
- Colors
- Cards
- Buttons
- Responsive layout
🟧 LEVEL 8 — Prompt Engineering for Business
51. Requirement Analysis
52. PRD Generation
53. User Stories
54. Acceptance Criteria
55. Business Logic
56. Workflow Design
57. Competitor Analysis
58. Market Research
59. Product Strategy
60. Business Model Generation

Example:

Convert these rough client requirements into:

1. Functional requirements
2. Non-functional requirements
3. User roles
4. User workflows
5. Admin workflows
6. Edge cases
7. Acceptance criteria
🟨 LEVEL 9 — Prompt Engineering for AI Agents

This is where prompt engineering becomes much more powerful.

61. What is an AI Agent?
62. Agent Instructions
63. Tool Calling
64. Tool Selection
65. Agent Planning
66. Memory
67. State Management
68. Multi-Step Tasks
69. Agent Guardrails
70. Agent Error Recovery
71. Human-in-the-Loop
72. Multi-Agent Systems

Example:

Research Agent
      ↓
Analysis Agent
      ↓
Planning Agent
      ↓
Coding Agent
      ↓
Testing Agent
🟦 LEVEL 10 — RAG & Knowledge-Based Prompting
73. What is RAG?
74. Embeddings
75. Vector Databases
76. Retrieval
77. Context Injection
78. Document Chunking
79. Semantic Search
80. RAG Prompt Design
81. Grounded Responses
82. Citation-Based Answers
83. Handling Missing Information

Important instruction:

If the answer cannot be supported by the provided context,
say that the information is unavailable.
Do not invent information.
🟥 LEVEL 11 — Prompt Security

Very important if you're building AI applications.

84. Prompt Injection
85. Indirect Prompt Injection
86. Jailbreaks
87. Instruction Conflicts
88. Data Leakage
89. System Prompt Protection
90. Tool Abuse
91. Agent Security
92. Input Sanitization
93. Output Validation
94. AI Safety Guardrails
🟪 LEVEL 12 — Prompt Evaluation

A professional prompt isn't just written—it is tested.

95. Prompt Testing
96. Prompt Evaluation
97. Accuracy
98. Consistency
99. Relevance
100. Hallucination Detection
101. Regression Testing
102. A/B Testing Prompts
103. Evaluation Datasets
104. LLM-as-a-Judge
105. Prompt Versioning
🟩 LEVEL 13 — Production Prompt Engineering
106. System Prompts
107. Developer Instructions
108. User Prompts
109. Prompt Templates
110. Dynamic Prompts
111. Variables

Example:

You are a {role}.

User:
{name}

Task:
{task}

Context:
{context}
112. Prompt Management
113. Prompt Version Control
114. Cost Optimization
115. Latency Optimization
116. Reliability
117. Fallback Strategies
⚫ LEVEL 14 — Multimodal Prompt Engineering
118. Image Prompting
119. Image Analysis
120. Screenshot Analysis
121. PDF Analysis
122. Audio Prompting
123. Video Prompting
124. Vision + Text
125. Image + Code
126. UI Screenshot → Code
🚀 LEVEL 15 — Advanced AI Product Engineering

Eventually you'll learn how prompting fits into real AI products.

127. LLM APIs
128. Function Calling
129. Structured Outputs
130. Streaming
131. Tool Use
132. RAG Pipelines
133. AI Agents
134. Memory Systems
135. Multi-Agent Architecture
136. AI Workflow Automation
137. AI Product Architecture
138. LLM Cost Management
139. Production Monitoring
140. AI Evaluation Systems
🎯 The Learning Path I'd Recommend for You

Since you're already a web developer and use AI coding tools, I wouldn't teach you prompt engineering like a complete beginner.

I'd use this progression:

PHASE 1
Prompt Fundamentals
        ↓
PHASE 2
Prompt Structure
        ↓
PHASE 3
Advanced Prompting
        ↓
PHASE 4
Coding Prompts
        ↓
PHASE 5
AI Coding Agents
        ↓
PHASE 6
Context Engineering
        ↓
PHASE 7
RAG
        ↓
PHASE 8
AI Agents
        ↓
PHASE 9
Prompt Security
        ↓
PHASE 10
Evaluation
        ↓
PHASE 11
Production AI Systems

And we'll learn it practically, not just theoretically.

For example, you'll eventually be able to take a requirement like:

“Make an admin panel similar to my previous renewable project, but type = 9.”

and transform it into a professional AI-development prompt containing:

Context → Objective → Existing System → Requirements → Business Rules → Constraints → Technical Requirements → UI Requirements → Edge Cases → Acceptance Criteria → Implementation Rules → Testing → Final Report

That is the level of prompt engineering that will be genuinely useful for your Laravel/React/Node/AI projects.

Next lesson: Lesson 1 — How LLMs actually understand prompts + Anatomy of a Professional Prompt.