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
3. **ANTI-LAZINESS RULE:** You must process EVERY SINGLE `.md` file belonging to the current phase. Do not skip any file. If you hit an output limit, STOP and ask the user to type "continue" to finish the remaining files. Do NOT falsely claim completion if files are still pending.

**PHASE 1: THE FOUNDATION**
1. Identify all generated `.md` prompts related to core types, database schemas, and shared configurations.
2. **INVENTORY:** Count exactly how many `.md` files you found for this phase.
3. Generate the actual source code for these foundational files. 
4. **VERIFY & ANTI-LOOP:** Check the filesystem. Did you create a source code file for *every* `.md` file counted? If you fail to find or process a specific file after 2 attempts, SKIP IT, report it as skipped, and MOVE ON. Do NOT repeat the same search command endlessly.
5. STOP and report: *"Phase 1 (Foundation) Complete. Processed [X] files. Skipped [Y] files."*
6. **CREATE & RENAME (DO NOT EDIT):** Assume the target source code files DO NOT EXIST YET. You MUST use your file creation tool (e.g., `write_to_file`, `create_file`) to physically create them on the disk. Do NOT use file editing/modifying tools. **CRITICAL:** You must strip the `.md` extension from the target file name. For example, if the blueprint/prompt is `apps/client-web/package.json.md`, you MUST create the real source file exactly as `apps/client-web/package.json`.
7. **EFFICIENT INVENTORY:** When identifying `.md` files for a phase, DO NOT execute dozens of individual search queries. Use a single directory listing tool or run a single terminal command (e.g., `find . -type f -name "*.md"`) to map all available specification files AT ONCE.
8. **TRANSLATE, DO NOT COPY:** You are strictly forbidden from copying the raw markdown prompt content into the final source files. You must TRANSLATE the pseudocode into actual, fully implemented, and functional code. Remove all metadata headers (like "Purpose:", "Dependencies:", or "PSEUDOCODE"). The final created file MUST contain ONLY valid syntax for the target language (e.g., valid TypeScript or valid JSON) and absolutely no markdown conversational text.
9. **IGNORE DEPENDENCY ERRORS (BLIND EXECUTION):** Do NOT attempt to install packages, run package managers (e.g., `npm install`), or fix TypeScript/Linter "missing module" errors. The workspace dependencies have not been installed yet. Your ONLY job is to write the raw code. Ignore all IDE error highlights, red squigglies, and compilation warnings. Dependency resolution is explicitly reserved for the DEBUG phase.

**PHASE 2: CORE LOGIC & BACKEND**
1. Identify all `.md` prompts related to backend services, APIs, controllers, or workers.
2. **INVENTORY:** Count exactly how many `.md` files you found for this phase.
3. Generate the source code, importing types exclusively from Phase 1 outputs.
4. **VERIFY & ANTI-LOOP:** Check the filesystem to ensure no file was skipped. If stuck on a file after 2 attempts, SKIP IT and move on.
5. STOP and report: *"Phase 2 (Core Logic) Complete. Processed [X] files. Skipped [Y] files."*

**PHASE 3: CLIENT & UI**
1. Identify all `.md` prompts related to the user interface or frontend.
2. **INVENTORY:** Count exactly how many `.md` files you found for this phase.
3. Generate the source code ensuring API calls match Phase 1 and 2 structures.
4. **VERIFY & ANTI-LOOP:** Check the filesystem. If stuck on a file after 2 attempts, SKIP IT and move on.
5. STOP and report: *"Phase 3 (Client/UI) Complete. Processed [X] files. Skipped [Y] files. Proceed to DEBUG.md."*
