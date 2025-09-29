# Stage 01: Phase 01 -  Codebase Analysis & Strategic Planning

This document outlines the first phase of an AI-driven development workflow. The primary goal is to take an initial codebase, perform a deep analysis against established standards, and generate a comprehensive, prioritized action plan for refactoring and development.

-----

### 🎯 Objective

To transform an initial, potentially raw codebase into a clear, actionable engineering plan. This phase involves a deep scan of the entire project, cross-referencing it with architectural rules and data schemas, and producing a strategic "war map" that guides all subsequent development efforts towards a robust and scalable MVP.

-----

### 📁 Context & Inputs

For this phase, you will be provided with the following:

  * **Global Rules:**
      * `best-practices-security.mdc`: Security guidelines, best practices, and rules.
      * `ui-ux.mdc`: UI/UX principles, component standards, and user flow requirements.
      * `architecture.mdc`: Rules for folder structure, state management, and code organization.
  * **Data Structure:**
      * `database-schema.md`: A complete description of the database tables, columns, and relationships.
  * **Codebase:**
      * The entire initial source code of the project.

-----

### 🪜 Steps

#### Step 1: Codebase Deep Scan & Internal Mapping

Your first task is to build a complete understanding of the project's current state and document it.

  * **Intelligently scan every file** in the provided codebase—frontend, backend, configurations, data models, and scripts. As you read, construct a comprehensive internal graph of the system's components and their interactions.
  * **Use internal tags** to classify all logic and entities. This creates a searchable mental map.
    ```
    #auth, #api, #ui, #data, #admin, #infra, #realtime, #testing, #core-logic, #jobs, #middleware, #services, #routes, #graphql, #cache, #scripts
    ```
  * **Track and tag the following specifically:**
      * 🧱 **Project Layout:** Folder structure, entry points, build configurations.
      * 🔌 **API & Backend:** REST endpoints, GraphQL schemas, RPC calls, custom handlers.
      * 🧩 **Modules & Components:** The purpose, props, state, and connections of each UI and logic module.
      * 🔐 **Authentication:** Login flows, token handling, session management, roles, and permissions.
      * 💾 **Data Layer:** Database connections (e.g., Postgres, Supabase), storage services, and data access patterns.
      * 🔁 **Core User Flows:** Onboarding, dashboards, payments, and other critical user journeys.
      * 🌐 **External Services:** All SDKs and third-party API integrations.
      * 🧪 **Developer Tooling:** Test suites, scripts, migrations, and linters.
  * **Generate a structured codebase map.** Create a new file at `/docs/analysis/codebase-map.md`. This file will serve as the persistent, detailed output of your scan. For each significant file in the codebase, create a markdown entry detailing its:
      * **Purpose:** A brief, one-sentence description of the file's role.
      * **Tags:** A list of the relevant `#tags` you've assigned.
      * **Connections:** Key imports, dependencies, or API calls it makes.
      * **Key Entities:** The main functions, components, classes, or logic blocks within the file.

#### Step 2: Triage & Thematic Analysis

Using the generated `/docs/analysis/codebase-map.md` as your reference, cross-analyze your findings against the provided rule files.

  * **Identify Violations & Gaps:** Compare the codebase map against the global rules. Identify every instance of non-compliance, bug, security vulnerability, or architectural deviation.
  * **Schema & Data Integrity Check:** Cross-reference the data-related code (`#data`, `#api`) with `database-schema.md` to find missing schemas, unsafe queries, data model mismatches, and to help generate the `/types` folder.
  * **Group Findings by Theme:** Consolidate all identified issues, gaps, and necessary refactors into functional themes (e.g., `#auth`, `#ui`, `#data`). Analyze the root causes and link them to their effects (e.g., "Missing DB logic → Empty UI state → Confusing UX").

#### Step 3: Generate the Action Plan

Synthesize your analysis into a single, tactical markdown file. This document will serve as the master plan for the development team.

  * **Create the file:** `/docs/plans/plan-stage-001.md`
  * **Structure the plan** with the following sections, providing clear context, referencing specific files/functions, and using tags for clarity.
    1.  **🔥 Critical Fixes:** What is fundamentally broken or blocking core functionality? (e.g., broken login, failing API calls, critical security flaws).
    2.  **🧩 Incomplete Features:** What is half-built, UI-only, or stubbed out? For each item, specify what’s missing, what’s needed to complete it, and its dependencies (DB, API, services).
    3.  **🧼 UX & UI Gaps:** Where does the user experience fail? Document broken flows, missing loading/error states, unresponsive layouts, and awkward transitions. Prioritize onboarding, forms, and core user journeys.
    4.  **🛠 Backend & Data Layer Issues:** Where is the hidden fragility? Detail missing schemas, unsafe queries, broken data relationships, incorrect environment variables, or brittle integrations.
    5.  **♻️ Refactor Opportunities:** What needs cleanup to ensure future scalability? Identify spaghetti logic, duplicated code, dead code, and high-debt zones that will slow down future development.
    6.  **🚀 MVP Readiness Checklist:** A final, high-level checklist to track progress towards a shippable product.
        ```markdown
        - [ ] Core features are fully functional
        - [ ] No critical bugs exist in the main user flow
        - [ ] Onboarding and primary user journeys are smooth
        - [ ] Authentication and user roles are fully implemented and secure
        - [ ] Essential configurations and environment variables are properly set up
        - [ ] The development setup is clean and deployable from scratch
        ```

-----

### ✅ Expected Outputs

Upon completion of this phase, you will provide:

1.  **The Codebase Map:** The newly generated `/docs/analysis/codebase-map.md` file, which documents the complete scan.
2.  **The Action Plan:** The final, detailed `/docs/plans/plan-stage-001.md` file.
3.  **Analysis Summary:** A brief report on your triage method and the key themes you identified.
4.  **Open Questions:** A list of any ambiguities, logical uncertainties, or decisions that require stakeholder input before proceeding.

-----

### 💡 Guiding Principles

Your role is to engineer the path to a successful launch.

  * **Think like a founding engineer:** Prioritize impact and focus on what matters most.
  * **Cut the noise:** Deliver clarity, not just documentation.
  * **Maximize leverage:** Identify fixes and refactors that will provide the most value.
  * **Aim to ship:** Ensure the plan is pragmatic, actionable, and geared towards shipping a fast, safe, and scalable product.