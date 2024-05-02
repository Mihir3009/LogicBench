# LogicBench: Towards Systematic Evaluation of Logical Reasoning Ability of Large Language Models

You may want to check out our paper - [Towards Systematic Evaluation of Logical Reasoning Ability of Large Language Models](https://arxiv.org/abs/2404.15522)

We comprehensively evaluate the logical reasoning ability of LLMs on 25 different reasoning patterns spanning over propositional, first-order, and non-monotonic logics. To enable systematic evaluation, we introduce LogicBench, a natural language question-answering dataset focusing on the use of a single inference rule. We conduct detailed analysis with a range of LLMs such as GPT-4, ChatGPT, Gemini, Llama-2, and Mistral using chain-of-thought prompting. Experimental results show that existing LLMs do not fare well on LogicBench; especially, they struggle with instances involving complex reasoning and negations. We believe that our work and findings facilitate future research for evaluating and enhancing the logical reasoning ability of LLMs.

## Data Release

Please see `./data` folder to access the LogicBench dataset.

**Licence:** MIT License

**Scope of the dataset:** As shown below, LogicBench covers 25 inference rules/reasoning patterns spanning propositional, first-order, and non-monotonic logic.

<img src="logic_types.png" align="center" data-canonical-src="logic_types.png" width="600" height="315" />

We introduce two versions of our proposed dataset: LogicBench(Eval) and LogicBench(Aug). LogicBench(Eval) is a high-quality human-verified evaluation dataset, whereas LogicBench(Aug) is only a synthetically augmented version for training purposes. LogicBench(Eval) consists of two types of tasks: (1) Binary Question-Answering (BQA), and (2) Multiple Choice Question-Answering (MCQA).

```data/``` contains both versions of the dataset and is distributed in the folder as follows:

    ├── ...
    ├── data
        ├── LogicBench(Aug)
        │   ├── first_order_logic
        │   ├── nm_logic
        │   └── propositional_logic
        └── LogicBench(Eval)
            ├── BQA
            |   ├── propositional_logic
            |   ├── first_order_logic
            |   └── nm_logic
            └── MCQA
                ├── propositional_logic
                ├── first_order_logic
                └── nm_logic
            

In all these folders, the JSON file corresponding to each inference rule is formatted as below:

### JSON file format for LogicBench(Eval) - BQA

```JSON
{
    "type": "str",
    "axiom": "str",
    "samples": [
        {
            "id": "int",
            "context": "str",
            "qa_pairs": [
                {
                    "question": "str",
                    "answer": "str"
                },
                {
                    "question": "str",
                    "answer": "str"
                }
            ]
        },
        {
            "id": "int",
            "context": "str",
            "qa_pairs": [
                {
                    "question": "str",
                    "answer": "str"
                },
                {
                    "question": "str",
                    "answer": "str"
                }
            ]
        }
    ]
}
```

### JSON file format for LogicBench(Eval) - MCQA

```JSON
{
    "type": "str",
    "axiom": "str",
    "samples": [
        {
            "id": "int",
            "context": "str",
            "question": "str",
            "choices": "dict"
            "answer": "str"
        },
        {
            "id": "int",
            "context": "str",
            "question": "str",
            "choices": "dict"
            "answer": "str"
        }
    ]
}
```

## BibTeX Entry and Citation Info ##

If you are using our dataset, please cite our paper:

```bibtex
@article{parmar2024towards,
  title={Towards Systematic Evaluation of Logical Reasoning Ability of Large Language Models},
  author={Parmar, Mihir and Patel, Nisarg and Varshney, Neeraj and Nakamura, Mutsumi and Luo, Man and Mashetty, Santosh and Mitra, Arindam and Baral, Chitta},
  journal={arXiv preprint arXiv:2404.15522},
  year={2024}
}
```

## Stay tuned for ...

- Huggingface version of LogicBench dataset for easy access
- Release of source code for data generation, inference and analysis 
