---
name: self-reflection-thought
description: Forces the Agent to think smarter using a 3-step self-reflection workflow (Draft -> Reflect -> Revise) before delivering the final response.
globs: ["*"]
---

# Multi-Step Self-Reflection Skill (Draft-Reflect-Revise)

When a user requests to solve a complex logical problem, write code for a new feature, or debug a system error, DO NOT immediately reply with the first solution that comes to mind. You must strictly adhere to the following cognitive workflow.

## Mandatory Cognitive Workflow

Every complex response you generate must progress through 3 distinct phases and be explicitly displayed within your thought process (or inside a `<thinking>` block):

### Step 1: Draft
*   Quickly generate an initial solution, a rough code draft, or a foundational approach to address the user's request.
*   **Goal:** Establish a baseline solution framework as fast as possible.

### Step 2: Reflect (Review & Critique)
Act as an extremely rigorous Principal Engineer to scrutinize the initial draft from Step 1. Ask yourself the following critical questions:
*   *Logic:* Are there any unhandled edge cases? Are there any potential security vulnerabilities?
*   *Performance:* Is this code/solution optimized for memory allocation and execution time complexity?
*   *Context:* Does this break any existing architecture in the user's project? Did you misunderstand any implicit requirements or underlying goals?

### Step 3: Revise (Refactor & Refine)
*   Utilize all the logical flaws, missing details, and negative feedback identified in Step 2 to refactor, rebuild, or fine-tune your draft.
*   **Goal:** Output a final response that is clean, highly optimized, and thoroughly vetted.

---

## Response Template

To demonstrate your transparent reasoning process to the user, format your final output using the following visual structure:

### 🧠 System Thinking

#### 📝 [1. DRAFT] Initial Concept / Rough Draft
*(Write your initial approach or raw code block here)*

#### 🔍 [2. REFLECT] Code Review & Critique
*   **Identified Weaknesses:** ...
*   **Unhandled Edge Cases:** ...
*   **Performance / Security Risks:** ...

#### 🚀 [3. REVISE] Final Optimized Solution
*(Provide the ultimate code snippet or response after resolving all issues identified in Step 2)*
