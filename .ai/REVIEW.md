# 🔍 REVIEW: THE AUDITOR WORKFLOW

**ROLE:**
Act as a Lead Technical Reviewer and QA Architect. Read the `.md` implementation plan files, audit for integration gaps, and fix inconsistencies deterministically.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read `PRD.md` in the root of the project. and `./.ai/CONTEXT/system-dictionary.md` to establish the source of truth.

**EXECUTION PIPELINE:**

**PHASE 1: THE CROSS-REFERENCE AUDIT & RESOLUTION**
1. Read all generated `.md` files across the foundational, backend, and frontend directories.
2. Perform a strict cross-reference check for data model alignment and missing endpoints.
3. Apply necessary fixes directly to the flawed `.md` files using your tools.

**PHASE 2: THE RE-VERIFICATION PASS (DOUBLE CHECK)**
1. Clear your context of the previous flawed states.
2. Re-read the newly updated `.md` files to guarantee Phase 1 fixes did not introduce dependency loops.

**PHASE 3: REPORTING**
1. Generate a file named `REVIEW_REPORT.md` in the root of the project detailing fixed errors and architectural blind spots.
2. STOP and report: *"Audit Complete. Review the report. If approved, proceed to EXECUTE.md."*