# Stage 01: Phase 03 - Sprint Execution Protocol

With a detailed sprint plan in `/docs/plans/sprints-stage-001.md`, it is time to begin implementation. This phase establishes a rigorous, human-in-the-loop protocol for executing each sprint, ensuring that every change is tested, documented, and aligned with the project's goals.

-----

### 🎯 Objective

To systematically execute each sprint defined in `sprints-stage-001.md`, following a strict protocol of implementation, testing, and documentation. The final goal is to produce a fully refactored, secure, and functional codebase with a complete typing system and updated project documentation.

-----

### 📁 Context & Inputs

  * **The Sprint Plan:** `/docs/plans/sprints-stage-001.md`
  * **The Action Plan:** `/docs/plans/plan-stage-001.md`
  * **Global Rules & Schema:** All `.mdc` and `.md` files.
  * **The Codebase:** The entire source code of the project.

-----

### 🔁 The Sprint Execution Loop

You will now operate in a tight cycle for **each sprint**, one by one. You will only proceed to the next sprint after receiving a confirmation command (e.g., `"next"`).

#### Step 1: Select & Review

  * **Select the Sprint:** Open `/docs/plans/sprints-stage-001.md` and identify the first sprint that is not marked as complete. This is your current mission.
  * **Full Context Refresh:** Before writing any code, re-read `plan-stage-001.md`, the global rule files, and any parts of the codebase relevant to the sprint's tasks (identified by tags like `#auth`, `#ui`, etc.).

#### Step 2: Implement & Test

  * **Execute Tasks:** Complete every task listed in the current sprint's scope. Write real, working logic—no placeholders.
  * **Refactor & Integrate Types:** Your implementation must adhere to the global rules. This includes creating and integrating a robust typing system in a new `/types` folder based on `database-schema.md`.
  * **Test As You Go:** Perform all `[🧪 TEST]` actions specified in the sprint plan.
  * **Maintain Quality:** Fix all linter errors, TypeScript warnings, and console issues as they appear. Do not introduce regressions.

#### Step 3: Update Documentation

  * **Mark Sprint Progress:** Update the current sprint's status in `/docs/plans/sprints-stage-001.md` to ✅ **Complete**.
  * **Reflect Changes:** Update `plan-stage-001.md` to reflect the completed tasks.
  * **Log New Information:** If new issues were discovered, add them to a `bugs.md` file. If ideas for features were deferred, add them to an `incomplete-features.md` file.

#### Step 4: Report & Wait

  * **Submit a Sprint Report:** Provide a clear, structured markdown summary of your work for the completed sprint. Use the template below.
  * **PAUSE:** After submitting your report, you must **wait** for user confirmation before beginning the next sprint.

-----

### 📝 Sprint Report Template

```markdown
## ✅ Sprint [Number] Complete: [Sprint Name]

### Tasks Implemented
- [x] [Task 1 name] (#tag)
- [x] [Task 2 name] (#tag)
- [...]

### Testing & Verification
- `[✔ TEST]` [Test case 1] passed successfully.
- `[✔ TEST]` [Test case 2] passed successfully.
- Console and linter are clean.
- No regressions were introduced.

### Docs Updated
- ✅ `/docs/plans/sprints.md`
- ✅ `/docs/plans/plan-stage-001.md`

### Notes & Considerations
- [Mention any important decisions, edge cases handled, or new blockers found.]
```

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

1.  A fully **refactored codebase** that is secure, user-friendly, well-structured that strictly adheres to the globale rules.
2.  **Strict type and data conformity**, ensuring all data structures, API payloads, and state management objects adhere to the interfaces declared in the `/types` folder and the `database-schema.md`.
3.  **Updated documentation**, including the completed `sprints-stage-001.md` and `plan-stage-001.md` files, accurately reflecting the final state of the codebase.