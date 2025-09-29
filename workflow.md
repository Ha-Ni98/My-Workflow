# First do the concetption of the application (data base schema 'detailed with types and the prisma schema', each page detailes) and generate the front-end using ai like lovable.

# AI-Driven Full-Stack Development Workflow

This document outlines a comprehensive, three-stage workflow for building a full-stack application from an initial concept to a fully integrated product. Each phase includes a description and a ready-to-use prompt for an AI coding assistant like Cursor.

-----

-----
## 🔨 Stage 00: Project-Specific Rule Generation

**Goal:** To establish a set of project-specific rules by analyzing the existing codebase's structure and technology stack. This creates a tailored foundation for all subsequent AI-driven development.

-----

### **Phase 1: Initial Setup & Rule Generation**

**Description:** This phase involves a one-time setup to create custom rule files that reflect your project's unique architecture and dependencies. The AI will analyze your code and generate these rules for you.

#### **Step 1: Manual Setup**

Before running the prompts, prepare your rules directory:

1.  Create a `.cursor/rules` directory in your project's root if it does not already exist.
2.  Copy your base rule files (e.g., a generic `cursor-rules.mdc` or `best-practices.mdc`) into this directory. These will serve as a starting point.

#### **Step 2: Generate Project Structure Rules**

This prompt asks the AI to scan your project and create a new rule file that documents its file and folder structure.

**Cursor Prompt:**

```
Your task is to act as a software architect and document the project's structure.

**Context:**
- All source files and folders in the project.

**Instructions:**
1.  **Analyze Structure:** Scan the entire project's directory tree.
2.  **Create Structure Rule:** Generate a new rule file at `.cursor/rules/project-structure.mdc`.
3.  **Document in Rule File:** In this new file, create a rule that outlines the existing directory structure. For each major folder (e.g., `/src/components`, `/src/lib`, `/src/app`), describe its purpose and the type of files it should contain. This rule will guide all future file creation.
```

#### **Step 3: Generate Technology Stack Rules**

This prompt asks the AI to analyze your dependencies and create a rule file that outlines the tech stack and best practices for it.

**Cursor Prompt:**

```
Your task is to analyze the project's dependencies and create a technology-specific rule set.

**Context Files:**
- @package.json

**Instructions:**
1.  **Analyze Dependencies:** Thoroughly review the `dependencies` and `devDependencies` in the `package.json` file.
2.  **Create Tech Stack Rule:** Generate a new file at `.cursor/rules/tech-stack.mdc`.
3.  **Document in Rule File:** In this new file, create a rule that outlines the application's technology stack.
    -   List the main frameworks and libraries (e.g., React, Next.js, Prisma, TailwindCSS) along with their versions.
    -   For each major technology, add a subsection with key best practices and common usage patterns specific to this project.
```



## 🏛️ Stage 01: Foundational Refactor & Setup

**Goal:** To take an initial codebase, refactor it into a clean, scalable, and secure foundation, and establish the core project architecture.

-----

### **Phase 1: Codebase Analysis & Strategic Planning**

**Description:** The AI performs a deep scan of the entire initial codebase, compares it against a set of global rules (architecture, security, UI/UX) and a database schema, and produces a detailed action plan for the foundational refactor.

**Cursor Prompt:**

```
You are an expert software architect. Your task is to analyze an entire codebase and create a detailed refactoring plan.

**Context Files:**
- @best-practices-security.mdc
- @ui-ux.mdc
- @architecture.mdc
- @database-schema.md

```

-----

### **Phase 2: Strategic Sprint Planning**

**Description:** The AI takes the master action plan from the previous phase and decomposes it into a sequence of small, logical, and test-driven sprints, creating a clear roadmap for the development team.

**Cursor Prompt:**

````
Your task is to act as a project manager and create a detailed sprint plan.

**Context File:**
- @/docs/plans/plan-stage-001.md

````

-----

### **Phase 3: Sprint Execution Protocol**

**Description:** The AI enters an execution loop, implementing the sprints one by one. For each sprint, it will write code, refactor, test, update documentation, and then report back, waiting for a "next" command before proceeding.

**Cursor Prompt:**

```
You are now in sprint execution mode. Your task is to implement the **next available sprint**.

**Context Files:**
- @/docs/plans/sprints-stage-001.md
- @/docs/plans/plan-stage-001.md
- All global rule files (.mdc) and schema (.md)

```

-----

## ✨ Stage 02: Iterative Feature Implementation (Per-Page)

**Goal:** To build out the application's pages feature-by-feature using a functional front-end with type-safe mock data. This stage is a repeatable loop for each page.

-----

### **Phase 1: Page Feature Analysis & Planning**

**Description:** The AI analyzes a specific page's requirements from a markdown file and creates a detailed action plan for implementing its features, components, and mock data needs.

**Cursor Prompt:**

```
You are a front-end developer planning a new page feature.

**Context Files:**
- @/docs/pages/<pageName>-details.md  // e.g., dashboard-details.md
- @/types/
- All global rule files (.mdc)

```
-----

### **Phase 2: Page-Specific Sprint Planning**

**Description:** The AI takes the page-specific action plan and breaks it down into a sequence of sprints for building out that single page's functionality.

**Cursor Prompt:**

```
Your task is to create a sprint plan for a specific page feature.

**Context File:**
- @/docs/plans/plan-stage-02-page-<pageName>.md

```

-----

### **Phase 3: Page Sprint Execution Protocol**

**Description:** The AI executes the page-specific sprints, building the front-end components and powering them with type-safe mock data, then waits for the next command.

**Cursor Prompt:**

```
You are now in page-feature execution mode. Implement the **next available sprint** for the current page.

**Context Files:**
- @/docs/plans/sprints-stage-02-page-<pageName>.md
- @/docs/plans/plan-stage-02-page-<pageName>.md
- @/types/

```

-----

-----

## 🔗 Stage 03: Back-End & Full-Stack Integration

**Goal:** To build the back-end API and services, then replace all front-end mock data with live API calls to create a fully operational application.

-----

### **Phase 1: Back-End & Integration Planning**

**Description:** The AI analyzes the Prisma schema, back-end rules, and the front-end's mock data usage to create a master plan for building the API and integrating it.

**Cursor Prompt:**

```
You are a full-stack architect planning the final integration of an application.

**Context Files:**
- @prisma.schema
- @back-end.md
- The entire front-end codebase, specifically looking for mock data usage.

```

-----

### **Phase 2: Integration Sprint Planning**

**Description:** The AI decomposes the master integration plan into a logical series of sprints, prioritizing the construction of back-end endpoints before moving on to front-end integration.

**Cursor Prompt:**

```
Your task is to create the final sprint plan for full-stack integration.

```

-----

### **Phase 3: Integration Sprint Execution Protocol**

**Description:** The AI executes the final sprints, building API endpoints and replacing front-end mock data with live API calls until the application is fully integrated.

**Cursor Prompt:**

```
You are now in final integration mode. Implement the **next available sprint**.

**Context Files:**
- @/docs/plans/sprints-stage-03-integration.md
- @/docs/plans/plan-stage-03-integration.md
- The entire codebase.

```

