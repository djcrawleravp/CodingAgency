# 🚀 DEPLOY: THE DEVOPS & RELEASE WORKFLOW

**ROLE:**
Act as a Senior DevOps Engineer. Securely deploy the debugged codebase to the target environment and generate operational scripts.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read `./.ai/CONTEXT/infrastructure-setup.md` to understand the deployment strategy and teardown commands.

**STRICT DEPLOYMENT RULES:**
1. **Zero Logic Changes:** Do not modify application source code.
2. **Secret Management:** Never hardcode secrets. Map production variables properly.
3. **Conditional Execution:** You must strictly follow either Phase 2 OR Phase 3 based on the existence of `setup.sh`. Never run both.

**PHASE 1: PRE-FLIGHT & PATH DECISION**
1. Verify build artifacts exist.
2. Confirm required CLI tools are installed and authenticated.
3. Check if `setup.sh` exists in the root of the project.
4. STOP and report: *"Phase 1 Complete. `setup.sh` [exists / does not exist]. Proceeding to the corresponding phase."*

**PHASE 2: FIRST-TIME DEPLOY & SCRIPT GENERATION (If `setup.sh` DOES NOT exist)**
1. Execute commands to create infrastructure based on setup files and run database migrations.
2. Execute the raw final deployment commands.
3. Run a `curl` command to verify the live service responds with 200 OK.
4. **ONLY AFTER SUCCESS:** Read `./.ai/CONTEXT/infrastructure-setup.md` and silently create `setup.sh` in the root.
5. The script MUST be an interactive Bash script with EXACTLY these 3 options:
   - **1) Deploy / Update:** Execute the standard build and deploy commands.
   - **2) Fresh Deploy:** Execute teardown commands, followed immediately by fresh provisioning and deployment.
   - **3) Undeploy:** Execute teardown/destroy commands to completely remove infrastructure.
6. Ensure options 2 and 3 include a strict safety confirmation (`[y/N]`). Make the script executable (`chmod +x setup.sh`).
7. STOP and report: *"Phase 2 Complete. First deploy successful and 'setup.sh' generated. Proceed to DOCUMENT.md."*

**PHASE 3: SUBSEQUENT DEPLOYS (If `setup.sh` ALREADY exists)**
1. Do NOT run raw provisioning or deployment commands manually.
2. Execute `./setup.sh` and use option **1) Deploy / Update**.
3. Run a `curl` command to verify the live service responds with 200 OK.
4. STOP and report: *"Phase 3 Complete. Update deployed via 'setup.sh'. Proceed to DOCUMENT.md."*
