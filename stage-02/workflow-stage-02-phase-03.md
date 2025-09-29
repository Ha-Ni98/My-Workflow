# Stage 02: Phase 03 - Page Sprint Execution Protocol

With a detailed sprint plan for the page, it is time to build the features. This phase executes each sprint sequentially to deliver a fully functional front-end page powered by type-safe mock data.

-----

### 🎯 Objective

To systematically execute each sprint from the page's sprint plan, following a strict protocol of implementation, testing, and documentation to deliver a functional, high-quality page that is ready for UI/UX validation.

-----

### 📁 Context & Inputs

  * **The Page Sprint Plan:** e.g., `/docs/plans/sprints-stage-02-page-dashboard.md`.
  * **The Page Action Plan:** e.g., `/docs/plans/plan-stage-02-page-dashboard.md`.
  * **Global Rules & Schema:** All relevant `.mdc` and `.md` files.
  * **The Codebase:** The entire source code of the project.

-----

### 🔁 The Sprint Execution Loop

You will operate in a tight cycle for **each sprint**, one by one. You will only proceed to the next sprint after receiving a confirmation command (e.g., `"next"`).

#### Step 1: Select & Review

  * **Select the Sprint:** Open the page's sprint plan and identify the first sprint not marked as complete.
  * **Full Context Refresh:** Re-read the page's action plan, the global rule files, and any relevant code before starting implementation.

#### Step 2: Implement & Test

  * **Execute Tasks:** Complete every task in the current sprint.
  * **Use Mock Data:** For any data required by the new components or features, create and use **mock data**. This data must be stored appropriately (e.g., in a `/mocks` folder) and **must** strictly conform to the interfaces defined in the `/types` folder.
  * **Test As You Go:** Perform all `[🧪 TEST]` actions specified in the sprint plan to validate UI and functionality.
  * **Maintain Quality:** Fix all linter errors, warnings, and console issues immediately.

#### Step 3: Update Documentation

  * **Mark Sprint Progress:** Update the current sprint's status in the page's sprint file to ✅ **Complete**.
  * **Reflect Changes:** Update the page's action plan to reflect the completed tasks.

#### Step 4: Report & Wait

  * **Submit a Sprint Report:** Provide a structured markdown summary of your work using the standard template.
  * **PAUSE:** After submitting your report, you must **wait** for user confirmation before beginning the next sprint.

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

Upon completion of all sprints for the page:

1.  **An updated codebase** with the new page and all its features fully implemented on the front-end.
2.  **Type-safe mock data** created and integrated to power the new page's components.
3.  **Updated documentation**, including the completed sprint and plan files for the page, accurately reflecting the new state of the codebase.