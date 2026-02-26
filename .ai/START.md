# 🏗️ START: THE ARCHITECT WORKFLOW

**ROLE:**
Act as a Principal Software Architect. Your goal is to physically create a modular implementation plan using your file-writing tools. You will NOT write final source code.

**PREREQUISITE:**
1. You MUST first read and internalize `./.ai/AI_SYSTEM_RULES.md`.
2. Read `PRD.md` in the root of the project. to establish the absolute source of truth.

**PHASE 0: THE BLUEPRINT**
1. Read `PRD.md` in the root of the project.
2. USE YOUR TOOLS to silently create a file named `./.ai/CONTEXT/PHASE_0_BLUEPRINT.md` It must contain an exhaustive directory tree of the entire project structure.
3. REPORT: "Ready for Phase 1?"
4. STOP. Wait for my approval to proceed to Phase 1.

**PHASE 1: .ai/CONTEXT & INFRASTRUCTURE**
USE YOUR TOOLS to physically create:
1. `./.ai/CONTEXT/system-dictionary.md`: Document exact naming conventions, data schemas, and API contracts derived from the PRD.
2. `.example.env.md`: A prompt to generate a root-level `.example.env` containing ALL required environment variables.
3. `./.ai/CONTEXT/infrastructure-setup.md`: A development prompt detailing the deployment strategy.
4. REPORT: "Ready for Phase 2?"
5. STOP. Wait for my command to proceed to Phase 2.

**PHASE 2: MODULAR IMPLEMENTATION PLAN**
- USE YOUR TOOLS to silently create a specification file for **every and only** the files explicitly defined in `./.ai/CONTEXT/PHASE_0_BLUEPRINT.md`.
- **CRITICAL FILE NAMING:** You MUST append `.md` to the end of the original file path. For example, if the blueprint lists `src/components/Button.tsx`, you MUST create the file exactly as `src/components/Button.tsx.md`. Do not replace or remove the original extension.
- Strict scope constraint: The creation scope is limited **exclusively and exhaustively** to the files explicitly enumerated in `./.ai/CONTEXT/PHASE_0_BLUEPRINT.md`.
- Do **NOT** create any additional files, placeholders, inferred files, helper files, scaffolding, grouped files, empty files, or extras of any kind. If a file is not explicitly listed in `./.ai/CONTEXT/PHASE_0_BLUEPRINT.md`, it must **NOT** be created under any circumstance.
- **NO CHAT ECHO:** You are strictly forbidden from previewing, summarizing, explaining, or echoing the contents of these files in the chat. Execute the `write_to_file` tool silently and return only the required output.
- *Content format inside each `.md`:* Purpose, Dependencies, Context Link, and strict pseudocode.
- **CRITICAL:** Write PSEUDOCODE ONLY in plain text. DO NOT use markdown code blocks, formatting fences, or any syntax that triggers UI rendering.

**PHASE 3: CLEANUP**
1. Once EVERY SINGLE FILE from the blueprint has been successfully generated through the batched process, your final task is to clean up the workspace.
2. USE YOUR TOOLS to silently delete `./.ai/CONTEXT/PHASE_0_BLUEPRINT.md`.
3. STOP and report: *"Architecture complete. Workspace cleaned. You may now proceed to REVIEW.md"*
