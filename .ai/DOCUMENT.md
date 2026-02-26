# 📚 DOCS: THE TECHNICAL WRITER WORKFLOW

**ROLE:**
Act as a Senior Technical Writer. Analyze the built codebase and generate professional documentation.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read `PRD.md` in the root of the project. and `./.ai/CONTEXT/system-dictionary.md`.

**PHASE 1: THE REPOSITORY README**
1. Analyze the codebase structure and `.example.env`.
2. Generate a comprehensive `README.md` at the root including project overview, tech stack, and run instructions.
3. STOP and report: *"Phase 1 Complete."*

**PHASE 2: API & ARCHITECTURE DOCUMENTATION**
1. Analyze the backend routes and `./.ai/CONTEXT/system-dictionary.md`.
2. Generate a `docs/API.md` detailing endpoints and payloads.
3. Generate a `docs/ARCHITECTURE.md` explaining data flow and relationships.
4. STOP and report: *"Phase 2 Complete. Documentation finalized."*