# CodingAgency

CodingAgency is a structured Markdown-based AI workflow that turns a
`PRD.md` into a fully generated, reviewed, executed, debugged, deployed,
and documented project.

It works through a sequence of specialized agent instruction files
designed to operate with strict execution rules and minimal output.

------------------------------------------------------------------------

## 📂 Project Structure

To use CodingAgency, your project must follow this structure:

```
/your-project
│
├── ai/
│   ├── AI_SYSTEM_RULES.md
│   ├── START.md
│   ├── REVIEW.md
│   ├── EXECUTE.md
│   ├── DEBUG.md
│   ├── DEPLOY.md
│   └── DOCUMENT.md
│
└── PRD.md
```

### Requirements

-   Place the `ai` folder in the **root** of your project.
-   Place your project specification file `PRD.md` in the **root** of
    your project.

------------------------------------------------------------------------

## 🚀 How It Works

The workflow is sequential and must be executed in order.

### Step 1 --- START

Run the following prompt in your AI environment:

Read AI_SYSTEM_RULES.md and then execute START.md. I remind you of your
most critical directive: ZERO CHAT OUTPUT. Use your tools to create the
files silently and respond to me ONLY with the list of created files. No
echoes or previews.

------------------------------------------------------------------------

### Step 2 --- REVIEW

After START completes, execute:

Read AI_SYSTEM_RULES.md and then execute REVIEW.md.

------------------------------------------------------------------------

### Step 3 --- EXECUTE

Read AI_SYSTEM_RULES.md and then execute EXECUTE.md.

------------------------------------------------------------------------

### Step 4 --- DEBUG

Read AI_SYSTEM_RULES.md and then execute DEBUG.md.

------------------------------------------------------------------------

### Step 5 --- DEPLOY

Read AI_SYSTEM_RULES.md and then execute DEPLOY.md.

------------------------------------------------------------------------

### Step 6 --- DOCUMENT

Read AI_SYSTEM_RULES.md and then execute DOCUMENT.md.

------------------------------------------------------------------------

## 🧠 Philosophy

-   The PRD is the single source of truth.
-   Each stage operates with strict role separation.
-   Output must be controlled and intentional.
-   Automation first. Conversation second.

------------------------------------------------------------------------

## ⚡ Usage

1.  Create your project.
2.  Add the `ai` folder at the root.
3.  Add your `PRD.md` at the root.
4.  Paste the START prompt.
5.  Let the agents build.

That's it.
