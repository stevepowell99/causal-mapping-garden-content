---
date: 2025-05-27
---

Many evaluators and other professionals think that "summarise this document" is an easy task for an AI. Here I'm going to present a general framework to help explain that it isn't, and why that matters.

## Task evaluation framework 

### What is a task

First, let's clearly define what we mean by a "task." A task consists of:

1. **Task Description** (essential): States the objective, for example, 
	1. Summarize this document.
	2. Evaluate this program (based on this documentation).
	3. Plan an excellent follow-up to this project
	4. Tell me a joke about a parrot and a robot
	5. What is the square root of 16?
	6. Cat: Is this picture a picture of a cat?
	7. Watsan: Does this page mention water and sanitation programming?
	8. Crossword: Solve this cryptic crossword puzzle and explain why it fits the clue (one answer possible)
	9. Title: Think of a great title for this report (may answers possible)
    Some tasks such as the last two require additional material, in which case we need the next component: 
2. **Input Dataset** (optional, depending on the task): The materials, such as documents or images, that the AI must process.
 
3. **Examples or Training Data** (optional): Materials provided to illustrate desired outputs or to train the AI.
    
4. **Evaluation Criteria** (optional, with default): A more or less explicit written statement to say in advance how the solution will be judged. By default the criterion is simply: does the answer fulfil the task, yes or no.
        
### Evaluation procedure

- The AI's response must be a discrete, clearly defined output such as yes/no or a picture or a page of text.
    
- The response will be evaluated by a diverse panel of individual raters with relevant expertise. Tasks or types of tasks in which raters agree have hight **inter-rater reliability**.
- Evaluation could also include robustness (see the HELM evaluation approach): How well the model performs under perturbations or changes in the input (e.g., typos, paraphrasing).

To understand why tasks differ so widely in their difficulty, we use a simple 2x2 matrix defined by two key dimensions:

- **Algorithmic: We know how to get it:** Tasks range from having known, algorithmic solutions (decidable) to no known algorithmic solutions (undecidable).
    
- **Evaluable: We'll know it when we've got it**: Tasks range from having clearly defined, objective criteria to ambiguous, subjective criteria.

Undecidable problems with high IRR are called insight problems in psychology.

Solvers can improve IRR by adding their working / traceability [[!700 Retraceable, reconstructable, operationalisable]]

But what if the raters are gullible and taken in by a false explanation?

What if the response is a python program plus a proof that it works?

Here is our evaluation difficulty matrix:

|                 | Easy / high IRR   | Evaluable               | Hard / low IRR                              |
| --------------- | ----------------- | ----------------------- | ------------------------------------------- |
| **Undecidable** | Cryptic crossword |                         | Plan an excellent follow-up to this project |
| **Algorithmic** | Watsan, Cat       | Summarise this document |                                             |
| **Decidable**   | Simple arithmetic |                         | ????                                        |



For example, arithmetic tasks like "add two numbers" are clearly defined and algorithmically solvable, placing them in the "easy evaluation" quadrant. A simple computer program can solve it. 

Conversely, "summarize this document" typically falls into the "hardest evaluation" category because it involves subjective judgment and no known definitive algorithm.

One kind of task which doesn't fit are so-called **wicked problems** (problems so ill-defined that stakeholders can't even agree on the issue itself).

the **agreement-certainty matrix**, which classifies tasks based on the clarity of goals and certainty of methods to achieve them.

In a follow-up blog post, we will explore practical approaches to breaking down challenging tasks into simpler, more manageable ones. But for now, recognizing why tasks like "summarize this document" are inherently complex is a crucial first step for evaluators considering the use of AI.

