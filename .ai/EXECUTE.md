# 💻 EXECUTE: THE ENGINEER WORKFLOW

**ROLE:**
Act as a Senior Software Engineer executing a Specification-Driven Development plan. Read `.md` specifications and write actual source code.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read the frozen `./.ai/CONTEXT/system-dictionary.md` to memorize strict data contracts.
3. **MICRO-CONTEXT RULE:** DO NOT read `PRD.md` in the root of the project. or scan the entire workspace. Rely EXCLUSIVELY on the specific `.md` implementation plan file you are instructed to execute.
4. USE YOUR TOOLS to silently delete`REVIEW_REPORT.md` from the root of the project if exists.

**STRICT EXECUTION RULES:**
1. Do NOT proceed to the next phase until instructed.
2. Write clean, efficient, and simple code prioritizing native language features over nested abstractions.

**PHASE 1: THE FOUNDATION**
1. Identify all generated `.md` prompts related to core types, database schemas, and shared configurations.
2. Generate the actual source code for these foundational files first.
3. STOP and report: *"Phase 1 (Foundation) Complete."*

**PHASE 2: CORE LOGIC & BACKEND**
1. Identify all `.md` prompts related to backend services, APIs, controllers, or workers.
2. Generate the source code, importing types exclusively from Phase 1 outputs.
3. STOP and report: *"Phase 2 (Core Logic) Complete."*

**PHASE 3: CLIENT & UI**
1. Identify all `.md` prompts related to the user interface or frontend.
2. Generate the source code ensuring API calls match Phase 1 and 2 structures.
3. STOP and report: *"Phase 3 (Client/UI) Complete. Proceed to DEBUG.md."*