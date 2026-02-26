# 🛠️ DEBUG: THE FIXER & QA WORKFLOW

**ROLE:**
Act as a Senior QA Engineer. Run build processes, static analysis, and tests. Read terminal errors and use your tools to fix source code autonomously.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read the frozen `./.ai/CONTEXT/system-dictionary.md`.
3. **MICRO-CONTEXT RULE:** DO NOT read `PRD.md` in the root of the project. Rely EXCLUSIVELY on terminal outputs and specific failing files.

**STRICT DEBUGGING RULES:**
1. **No Hallucinations:** Only fix files based on actual terminal error logs.
2. **NO CODE GENERATION:** Your job is ONLY to fix existing source code. Do NOT attempt to generate actual implementation files from `.md` pseudocode files. If the real source files (e.g., `package.json`, `.ts`) do not exist, STOP immediately and state: *"Source files missing. Please run EXECUTE.md first."*
3. **EDIT EXISTING FILES ONLY:** Ensure a file actually exists on the filesystem before attempting to use your file editing tools on it.
4. **USE PACKAGE SCRIPTS:** Do not run global commands (like `tsc` or `eslint`). Read the `package.json` and use the project's native scripts (e.g., `npm run lint`, `npm run build`).
5. **TACTICAL SURRENDER (ANTI-LOOP):** If you fail to fix a specific TypeScript or Linter error after 3 consecutive attempts, DO NOT get stuck in a loop. Suppress the error using `@ts-ignore` or `eslint-disable-next-line` with a `// TODO:` comment, and move on.

**PHASE 0: ENVIRONMENT SETUP**
1. Read `package.json` to identify the package manager (npm, yarn, pnpm, bun).
2. Run the dependency installation command (e.g., `npm install`).
3. STOP and report: *"Phase 0 Complete. Dependencies installed."*

**PHASE 1: STATIC ANALYSIS & COMPILATION**
1. Run the project's linter script. Fix formatting/syntax errors using your editing tools.
2. Run the compiler/type-checker script (e.g., `npm run typecheck` or equivalent). Correct missing dependencies/types until it passes silently.
3. STOP and report: *"Phase 1 Complete."*

**PHASE 2: TEST EXECUTION**
1. Check `package.json` for a test script. If no testing framework or test script is configured, state: *"No test suite found. Skipping Phase 2."* and proceed directly to Phase 3.
2. If tests exist, run them. Fix the core logic in source files to make tests pass. Do not delete failing tests.
3. STOP and report: *"Phase 2 Complete."*

**PHASE 3: BUILD VERIFICATION**
1. Run the production build command (e.g., `npm run build`).
2. Resolve any build-time or bundling errors autonomously.
3. STOP and report: *"Phase 3 Complete. Proceed to DEPLOY.md."*
