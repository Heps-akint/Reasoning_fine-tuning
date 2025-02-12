# Fine-Tuning a Language Model for Mathematical Reasoning

This project documents my journey in fine-tuning a pre-trained language model to enhance its mathematical reasoning capabilities. The primary goal was to experiment with model customization techniques to improve performance on specific tasks, thereby deepening my understanding of natural language processing and model training processes.

## Project Overview

The project involved fine-tuning the [Microsoft Phi-3-mini-4k-instruct](https://huggingface.co/microsoft/Phi-3-mini-4k-instruct) model using a subset of the GSM8K dataset, which is widely used for mathematical reasoning tasks. The fine-tuning process aimed to enable the model to generate step-by-step solutions to mathematical problems, thereby enhancing its reasoning abilities.

## Motivation

The motivation behind this project was to explore the process of adapting large language models to specific tasks through fine-tuning. By focusing on mathematical reasoning, I aimed to understand the challenges and intricacies involved in training models to perform domain-specific tasks effectively.

## Dataset

I utilized a subset of the [GSM8K dataset](https://huggingface.co/datasets/gsm8k), specifically the first 100 examples from the training set. This dataset is commonly used for benchmarking mathematical reasoning in language models.

## Fine-Tuning Process

1. **Model Preparation**: Loaded the pre-trained Phi-3-mini-4k-instruct model and configured it for fine-tuning using the Low-Rank Adaptation (LoRA) technique to optimize training efficiency.

2. **Data Formatting**: Each example from the dataset was formatted into a chain-of-thought prompt, encouraging the model to generate step-by-step solutions.

3. **Training**: The model was trained over multiple epochs, with training parameters such as learning rate and batch size carefully selected to ensure effective learning.

4. **Evaluation**: Post-training, the model's performance was evaluated by generating solutions to mathematical problems and assessing the coherence and correctness of the reasoning steps.

## Challenges Encountered

Throughout the project, I encountered several challenges:

- **Configuration Errors**: Faced issues related to missing configuration names during dataset loading, which were resolved by specifying the appropriate dataset configurations.

- **Model Output Handling**: Managed errors related to model outputs not containing expected keys, such as 'loss', by adjusting the training loop and model configurations.

- **Resource Management**: Addressed warnings related to resource usage, such as the incompatibility of `use_cache=True` with gradient checkpointing, by modifying model settings accordingly.

## Results

The fine-tuned model demonstrated improved capabilities in generating step-by-step solutions to mathematical problems. Training metrics indicated a decrease in loss over successive epochs, suggesting effective learning.

## Future Work

Building upon this foundational work, future endeavors could include:

- **Expanding the Dataset**: Utilizing a larger and more diverse dataset to further enhance the model's reasoning capabilities.

- **Hyperparameter Optimization**: Experimenting with different hyperparameters to optimize model performance.

## Acknowledgements

I would like to acknowledge the developers of the [Phi-3-mini-4k-instruct model](https://huggingface.co/microsoft/Phi-3-mini-4k-instruct) and the contributors to the [GSM8K dataset](https://huggingface.co/datasets/gsm8k) for providing the foundational tools and data that made this project possible.

---

*Note: This project was conducted for personal learning and experimentation purposes.* 
