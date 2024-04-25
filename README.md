# LogicBench: Towards Systematic Evaluation of Logical Reasoning Ability of Large Language Models

Recently developed large language models (LLMs) have been shown to perform remarkably well on a wide range of language understanding tasks. But, can they really "reason" over the natural language? This question has been receiving significant research attention and many reasoning skills such as commonsense, numerical, and qualitative have been studied. However, the crucial skill pertaining to "logical reasoning" has remained underexplored. Existing work investigating this reasoning ability of LLMs has focused only on a couple of inference rules (such as modus ponens and modus tollens) of propositional and first-order logic. Addressing the above limitation, we comprehensively evaluate the logical reasoning ability of LLMs on 25 different reasoning patterns spanning over propositional, first-order, and non-monotonic logics. To enable systematic evaluation, we introduce LogicBench, a natural language question-answering dataset focusing on the use of a single inference rule. We conduct detailed analysis with a range of LLMs such as GPT-4, ChatGPT, Gemini, Llama-2, and Mistral using chain-of-thought prompting. Experimental results show that existing LLMs do not fare well on LogicBench; especially, they struggle with instances involving complex reasoning and negations. Furthermore, they sometimes tend to prioritize parametric knowledge over contextual information and overlook the correct reasoning chain. We believe that our work and findings facilitate future research for evaluating and enhancing the logical reasoning ability of LLMs.

## Data Release

**Licence:** MIT License

**Huggingface URL for LogicBench:** https://huggingface.co/datasets/cogint/LogicBench-v1.0

**Scope of the dataset:** As shown below, LogicBench covers 25 inference rules/reasoning patterns spanning propositional, first-order, and non-monotonic logic.

<img src="logic_types.png" align="center" data-canonical-src="logic_types.png" width="600" height="315" />
