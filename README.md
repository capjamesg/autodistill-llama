<div align="center">
  <p>
    <a align="center" href="" target="_blank">
      <img
        width="850"
        src="https://media.roboflow.com/open-source/autodistill/autodistill-banner.png"
      >
    </a>
  </p>
</div>

# Autodistill LLaMA 2 Module

> [!TIP]
> Autodistill is a framework for using large, foundation vision models to train smaller, faster models. Autodistill does not officially support distilling LLMs. This repository is an experiment.

This repository contains the code supporting the LLaMA 2 base model for use with [Autodistill](https://github.com/autodistill/autodistill).

[LLaMA 2](https://github.com/facebookresearch/llama) is an open-source Large Language Model (LLM) developed by Meta AI. You can use LLaMA 2 to label data for use in fine-tuning an LLM, or generating data for use in training another type of language model (i.e. text classifier).

## Installation

To use LLaMA 23 with autodistill, you need to install the following dependency:

```bash
pip3 install autodistill-llama-2
```

## Quickstart

```python
from autodistill_llama_2 import LLaMA

base_model = LLaMA()

result = base_model.predict("What is a cookie?")

# data must be in a JSONL file with the structure
# {"data": "[question] [answer]" }
base_model.label("./data.jsonl")
```


## License

The source code for this project is licensed under an MIT license. To use LLaMA, you must agree to Meta AI's [LLaMA 2 terms and conditions](https://ai.meta.com/resources/models-and-libraries/llama-downloads/).

## 🏆 Contributing

This module is currently experimental and not ready for external contributions. When this changes, we will update this section.
