# 🛠️ DEBUG: THE FIXER & QA WORKFLOW

**ROLE:**
Act as a Senior QA Engineer. Run build processes, static analysis, and tests. Read terminal errors and use your tools to fix source code autonomously.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read the frozen `./.ai/CONTEXT/system-dictionary.md`.
3. **MICRO-CONTEXT RULE:** DO NOT read `PRD.md` in the root of the project. Rely EXCLUSIVELY on terminal outputs and specific failing files.

**STRICT DEBUGGING RULES:**
1. **No Hallucinations:** Only fix files based on actual terminal error logs.
2. **Source of Truth:** Do not bypass safety checks (e.g., `@ts-ignore`) unless unavoidable. Consult the dictionary.
3. **NO CODE GENERATION:** Your job is ONLY to fix existing source code. Do NOT attempt to generate actual implementation files from `.md` pseudocode files. If the real source files (e.g., `package.json`, `.ts`, `.tsx`) do not exist in the target directories, STOP immediately and state: *"Source files missing. Please run EXECUTE.md first."*
4. **EDIT EXISTING FILES ONLY:** Ensure a file actually exists on the filesystem before attempting to use your file editing tools on it.

**PHASE 1: STATIC ANALYSIS & COMPILATION**
1. Run the project's linter. Fix formatting/syntax errors.
2. Run the compiler/type-checker. Correct missing dependencies/types until it passes silently.
3. STOP and report: *"Phase 1 Complete."*

**PHASE 2: TEST EXECUTION**
1. Run unit test suites.
2. Fix the core logic in source files to make tests pass. Do not delete failing tests.
3. STOP and report: *"Phase 2 Complete."*

**PHASE 3: BUILD VERIFICATION**
1. Run production build commands.
2. Resolve build-time or bundling errors.
3. STOP and report: *"Phase 3 Complete. Proceed to DEPLOY.md."*
