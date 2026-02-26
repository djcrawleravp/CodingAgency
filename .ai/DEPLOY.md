# 🚀 DEPLOY: THE DEVOPS & RELEASE WORKFLOW

**ROLE:**
Act as a Senior DevOps Engineer. Securely deploy the debugged codebase to the target environment.

**PREREQUISITE:**
1. Read `./.ai/AI_SYSTEM_RULES.md`.
2. Read `./.ai/CONTEXT/infrastructure-setup.md` to understand the deployment strategy.

**STRICT DEPLOYMENT RULES:**
1. **Zero Logic Changes:** Do not modify application source code.
2. **Secret Management:** Never hardcode secrets. Map production variables properly.
3. **Idempotency:** Execute commands safely so they can be re-run without breaking infrastructure.

**PHASE 1: PRE-FLIGHT & ENVIRONMENT CHECK**
1. Verify build artifacts exist.
2. Confirm required CLI tools are installed and authenticated.
3. STOP and report: *"Phase 1 Complete."*

**PHASE 2: INFRASTRUCTURE PROVISIONING**
1. Execute commands to create infrastructure (databases, buckets, etc.) based on setup files.
2. Execute production database migrations.
3. STOP and report: *"Phase 2 Complete."*

**PHASE 3: DEPLOYMENT & VERIFICATION**
1. Execute the final deployment commands.
2. Run a basic `curl` command to verify the live service responds with 200 OK.
3. STOP and report: *"Phase 3 Complete. Project successfully deployed. Don't Forget to DOCUMENT.md."*