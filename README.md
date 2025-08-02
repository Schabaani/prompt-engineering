# prompting-engineering

## 📋 Full List of Prompting Strategies

| #   | Strategy                      | Why & When to Use                                         | How to Use It                                          | Tips for Better Prompting                     |
| --- | ----------------------------- | --------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------- |
| 1   | Zero-Shot Prompting           | Use for simple, direct tasks with no examples needed      | Provide a clear instruction                            | Keep the task concise and unambiguous         |
| 2   | Few-Shot Prompting            | Use when task benefits from examples                      | Show 2–5 examples before asking for output             | Match examples to target input format         |
| 3   | Chain-of-Thought (CoT)        | Use for multi-step reasoning or logic problems            | Add “Let’s think step by step” or show reasoning steps | Pair with few-shot for best results           |
| 4   | Tree of Thought (ToT)         | Use when multiple possible solutions exist                | Ask for multiple options + evaluation                  | Guide it with criteria for comparison         |
| 5   | ReAct (Reason + Act)          | Use in tool-using agents or when actions follow reasoning | Use format: Thought → Action → Observation → Thought   | Useful in LangChain and agentic systems       |
| 6   | Self-Ask Prompting            | Use when solving requires asking sub-questions            | Ask: “What do I need to find first?”                   | Encourage sub-task decomposition              |
| 7   | Role Prompting                | Use when tone/persona/expertise is important              | “You are a \[role]. Your task is…”                     | Be specific about audience and expectations   |
| 8   | Instruction Tuning            | Use for structured outputs (API, parsing)                 | Define expected output format                          | Use JSON, XML, or bullet structures           |
| 9   | Reflexion (Self-Critique)     | Use to improve model answers iteratively                  | Ask model to review and fix its own answer             | Run multi-round loops for refinement          |
| 10  | Deliberation Prompting        | Use for exploring multiple viewpoints or outcomes         | Ask to weigh pros/cons or explore options first        | Useful for planning, writing, debating        |
| 11  | Prompt Chaining               | Use for multi-step workflows                              | Chain outputs as inputs to next prompt                 | Keep each step modular and testable           |
| 12  | Multimodal Prompting          | Use when combining text + images/audio/video              | Upload media, then describe task in text               | Be clear on what to look for in media         |
| 13  | Few-Shot + CoT Hybrid         | Use for high-complexity tasks                             | Combine examples + reasoning steps                     | Choose relevant and high-quality examples     |
| 14  | Guided Decoding / Hints       | Use when the model struggles or needs clues               | “Here’s a hint:…” or give partial answers              | Use for tutoring, puzzles, code tasks         |
| 15  | Counterfactual Prompting      | Use for “what if” and alternative scenarios               | “What if X didn’t happen?”                             | Good for testing, creativity, analysis        |
| 16  | Constraint-Based Prompting    | Use when strict format, tone, or limits apply             | “Write a 50-word email using these phrases…”           | Use token constraints or checklist items      |
| 17  | Emotion Prompting             | Use when tone or feeling matters                          | “Write this as if you’re feeling hopeful…”             | Combine with Role Prompting for realism       |
| 18  | Time-Travel Prompting         | Use for futuristic or historical reasoning                | “Imagine you’re in year 2100…”                         | Great for creative or speculative tasks       |
| 19  | Verification Prompting        | Use to fact-check or verify model output                  | “Is this information accurate?”                        | Use with RAG or source-grounded models        |
| 20  | Prompt Inversion              | Use to test prompt sensitivity or reverse-engineer        | “Guess the prompt from this output”                    | Helpful for security and evaluations          |
| 21  | Multi-Agent Prompting         | Use when multiple agents can debate, vote, or collaborate | Prompt agents with different roles or views            | Compare outputs and choose best               |
| 22  | Socratic Prompting            | Use for teaching or exploration via questions             | Ask “why” or “how” iteratively                         | Useful in education and coaching tools        |
| 23  | Debate Prompting              | Use to explore opposing views on a topic                  | Ask two roles to argue different sides                 | Encourage final reflection or vote            |
| 24  | Memory-Based Prompting        | Use when continuity/context over time matters             | Reference prior answers explicitly                     | Combine with session memory or embeddings     |
| 25  | Recursive Prompting           | Use for deeply nested tasks or iterative refinement       | Feed answer back into model for improvement            | Great for writing, debugging, refinement      |
| 26  | Analogical Prompting          | Use to teach via analogy or metaphor                      | “Explain like a chef, teacher, artist…”                | Useful in education, persuasion, UX writing   |
| 27  | Negative Prompting            | Use to instruct what **not** to do                        | “Don’t include any technical jargon.”                  | Combine with positive constraints for clarity |
| 28  | Retrieval-Augmented Prompting | Use when model needs accurate, up-to-date info            | Combine prompt with external knowledge source          | Works best in RAG pipelines                   |
| 29  | Sandbox Prompting             | Use to simulate or test hypothetical logic flows          | “Pretend you are simulating a robot…”                  | Great for agentic simulations                 |
| 30  | Self-Improvement Prompting    | Use to evolve model performance over sessions             | “What would be a better version of this prompt?”       | Useful for building adaptive agents           |

## 🧩 Categorized Prompting Strategies

### 🧠 By Cognitive Task Type

This groups prompts by what kind of thinking they ask the model to do (e.g., reasoning, generating, evaluating).

**Reasoning & Logic:** Chain-of-Thought, Tree of Thought, ReAct, Self-Ask

**Generation & Creativity:** Zero-Shot, Few-Shot, Role Prompting

**Evaluation & Self-Improvement:** Reflexion

| Category                             | Strategies                                                                                                                                 | Why This Grouping Matters                                                                                                           |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| 🧠 **Reasoning & Logic**             | Chain-of-Thought, Tree of Thought, ReAct, Self-Ask, Socratic Prompting, Deliberation Prompting, Debate Prompting, Counterfactual Prompting | These focus on step-by-step thought, problem-solving, or decision trees. Useful for math, logic, planning, complex Q\&A.            |
| ✍️ **Generation & Creativity**       | Zero-Shot, Few-Shot, Time-Travel, Emotion Prompting, Role Prompting, Analogical Prompting, Sandbox Prompting                               | These strategies help generate content, ideas, or simulate imaginative contexts. Ideal for writing, marketing, or product ideation. |
| 🛠️ **Evaluation & Self-Improvement** | Reflexion, Verification, Prompt Inversion, Recursive Prompting, Self-Improvement Prompting                                                 | These ask the model to **analyze, critique, or improve** its own output. Useful for refining or validating model behavior.          |

### 🧱 By Structure/Complexity

This categorizes by how complex or layered the strategy is — from simple instructions to dynamic, agentic flows.

**Simple/Flat Prompting:** Zero-Shot, Few-Shot, Role Prompting, Instruction Tuning

**Multi-Step or Recursive:** Chain-of-Thought, Reflexion

**Agent-Oriented or Multi-Agent:** ReAct, Tree of Thought

| Category                             | Strategies                                                                                                 | Why This Grouping Matters                                                                                                     |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| 🧾 **Simple/Flat Prompting**         | Zero-Shot, Few-Shot, Role Prompting, Instruction Tuning, Negative Prompting, Constraint-Based Prompting    | These involve **one-pass input**, no memory, no recursion. Great for static tasks.                                            |
| 🔁 **Multi-Step or Recursive**       | Chain-of-Thought, Prompt Chaining, Recursive Prompting, Reflexion, Self-Improvement, Few-Shot + CoT Hybrid | These involve multiple rounds, feedback loops, or chaining outputs to inputs. Used in **tooling and agents**.                 |
| 🤖 **Agent-Oriented or Multi-Agent** | ReAct, Tree of Thought, Multi-Agent, Retrieval-Augmented, Memory-Based Prompting, Sandbox Prompting        | These often use **memory, tools, environments**, or simulate agent behavior. Needed for autonomous systems and orchestration. |

### 🧭 By Use Case Domain

Groups based on where and why you’d use the prompt — like education, decision-making, creativity, or automation.

**Learning & Tutoring:** Self-Ask

**Problem Solving / Critical Thinking:** Chain-of-Thought, Tree of Thought, ReAct

**Creative Content / Ideation:** Few-Shot, Role Prompting

**Automation & Tool Use:** Instruction Tuning, ReAct

| Category                                   | Strategies                                                                           | Why This Grouping Matters                                                                                         |
| ------------------------------------------ | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- |
| 🧑‍🏫 **Learning & Tutoring**                 | Socratic Prompting, Self-Ask, Guided Decoding, Analogical Prompting, Time-Travel     | These support **interactive thinking**, great for coaching, teaching, or onboarding.                              |
| 🧠 **Problem Solving / Critical Thinking** | Chain-of-Thought, Tree of Thought, ReAct, Counterfactual, Verification, Deliberation | These guide the model to **solve, analyze, and reason**, making them good for decision support or expert systems. |
| 🎨 **Creative Content / Ideation**         | Few-Shot, Emotion Prompting, Role Prompting, Sandbox Prompting, Analogical Prompting | Useful for storytelling, content generation, product copywriting, etc.                                            |
| 🧾 **Automation & Tool Use**               | Prompt Chaining, Instruction Tuning, Retrieval-Augmented, ReAct, Memory-Based        | Designed to be **repeatable, API-friendly**, or part of larger pipelines or agents.                               |

## Summery

| Property                       | Purpose of Grouping                                  |
| ------------------------------ | ---------------------------------------------------- |
| 🧠 Cognitive Task Type         | Helps decide **how the model should think**          |
| 🧱 Prompt Structure Complexity | Helps design **how the model should behave**         |
| 🧭 Use Case Domain             | Helps match prompting to **real-world applications** |

