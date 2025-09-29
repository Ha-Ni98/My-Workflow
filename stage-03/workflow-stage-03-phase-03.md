# Stage 03: Phase 03 - Integration Sprint Execution Protocol

This is the final execution phase. You will work through the integration sprints to build the back-end services and connect the front-end, transforming the application from a prototype into a fully operational full-stack product.

-----

### 🎯 Objective

To systematically execute each sprint from the integration plan, resulting in a complete set of back-end services and a fully integrated application where the front-end exclusively uses the back-end API for all data operations.

-----

### 📁 Context & Inputs

  * **The Integration Sprint Plan:** `/docs/plans/sprints-stage-03-integration.md`.
  * **The Integration Action Plan:** `/docs/plans/plan-stage-03-integration.md`.
  * **All Project Files:** The entire codebase, rules, and schema files.

-----

### 🔁 The Sprint Execution Loop

You will operate in the established cycle for **each sprint**, waiting for user confirmation (`"next"`) before proceeding.

#### Step 1: Select & Review

  * **Select the Sprint:** Open the integration sprint plan and identify the next sprint to be executed.
  * **Full Context Refresh:** Re-read the relevant parts of the integration plan, the `prisma.schema`, `back-end.md`, and the front-end components that will be affected.

#### Step 2: Implement & Test

  * **Execute Back-End Tasks:** If the sprint involves API work, build the endpoints, services, and database logic according to the rules in `back-end.md`. Test endpoints directly.
  * **Execute Front-End Tasks:** If the sprint involves integration, **remove all corresponding mock data and files**. Replace them with live API calls. Implement state management for loading, success, and error states.
  * **Maintain Quality:** Keep the codebase clean of linting errors, warnings, and console logs.

#### Step 3: Update Documentation

  * **Mark Sprint Progress:** Update the current sprint's status in `/docs/plans/sprints-stage-03-integration.md` to ✅ **Complete**.
  * **Reflect Changes:** Update the master integration plan to reflect the completed tasks.

#### Step 4: Report & Wait

  * **Submit a Sprint Report:** Provide a structured markdown summary of your work.
  * **PAUSE:** Wait for the user's "next" command.

-----

### 🧠 Guiding Principles: The 10 Commandments

1.  **Understand First:** No blind coding.
2.  **Don't Break Things:** Prioritize stability.
3.  **No Placeholders:** Real, working logic only.
4.  **Lint Must Be Clean.**
5.  **Console Must Be Silent.**
6.  **Stick to the Scope:** Log extra ideas elsewhere.
7.  **Test What You Build.**
8.  **Update All Docs.**
9.  **Report with Clarity.**
10. **Wait for "next".**

-----

### ✅ Expected Outputs

Upon completion of all sprints:

1.  A complete set of **back-end services and API endpoints**, built according to the project's rules.
2.  A **fully integrated application** where the front-end exclusively uses the back-end API for all data operations, with no remaining mock data.
3.  **Updated documentation**, including the completed sprint and plan files, accurately reflecting the final, full-stack state of the codebase.