# Stage 03: Phase 01 - Back-End & Integration Planning

This is the final stage of development, focusing on building the back-end and connecting it to the front-end. This first phase is dedicated to creating a comprehensive plan for both the API construction and the systematic removal of all mock data.

-----

### 🎯 Objective

To analyze the application's data models (`prisma.schema`), back-end requirements, and the front-end's mock data usage to produce a complete, actionable plan for building the API and performing the full-stack integration.

-----

### 📁 Context & Inputs

  * **Codebase:** The finalized front-end project from Stage 02.
  * **Back-End Schema:** `prisma.schema` (The single source of truth for data models).
  * **Back-End Rules:** `back-end.md` (Rules for API design, error handling, auth, etc.).
  * **Global Rules & Types:** All `.mdc` rule files and the `/types` folder.

-----

### 🪜 Steps

#### Step 1: Full-Stack Analysis

  * **Analyze the Schema:** Deeply scan the `prisma.schema` to understand every model, field, and relation. This forms the foundation for the API.
  * **Scan for Mock Data:** Intelligently scan the entire front-end codebase to identify every file and component that currently uses mock data. Catalog what data is being mocked and where.
  * **Review Back-End Rules:** Absorb all guidelines from `back-end.md` to ensure the plan adheres to the required architectural patterns.

#### Step 2: Define the API & Integration Strategy

  * **Map API Endpoints:** Based on the Prisma models and front-end needs, define all required API endpoints. Specify the HTTP method, URL, purpose, and the data model it interacts with for each endpoint.
  * **Map Mock Data to Endpoints:** Create a clear mapping that links each instance of mock data in the front-end to the specific API endpoint that will replace it.

#### Step 3: Generate the Integration Action Plan

  * **Create the Plan File:** Synthesize all analysis into a new master plan for this stage: `/docs/plans/plan-stage-03-integration.md`.

  * **Structure the Plan:** Organize the plan into two distinct parts:

    1.  **Part 1: API Construction Blueprint:** A detailed list of every API endpoint to be built.

          * **Example Entry:**
              * **Endpoint:** `POST /api/tasks`
              * **Model:** `Task`
              * **Description:** Creates a new task for the logged-in user.
              * **Auth:** Required.
              * **Payload:** `{ title: string, content: string }`
              * **Returns:** `{ id, title, content, authorId, ... }`

    2.  **Part 2: Front-End Integration Checklist:** A component-by-component guide for replacing mock data.

          * **Example Entry:**
              * **File:** `/src/components/TaskList.tsx`
              * **Action:** Remove `mockTasks.ts` import.
              * **Integration:** Implement a data-fetching hook (e.g., `useSWR` or `React Query`) to call `GET /api/tasks`.
              * **State Handling:** Add loading, success, and error states to the component's render logic.

-----

### ✅ Expected Outputs

  * A detailed, two-part action plan: **`/docs/plans/plan-stage-03-integration.md`**.
  * A list of any potential conflicts or ambiguities between the front-end's data needs and the `prisma.schema`.

-----
