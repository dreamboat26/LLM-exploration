# Fine-tuned PHI 2 Model

This notebook showcases the process of fine-tuning the PHI 2 model using a custom dataset and specific configuration parameters. The goal is to create a task-specific model for a particular use case, leveraging the powerful capabilities of PHI 2 in natural language processing tasks.

## Overview

The notebook consists of the following key steps:

1. **Dataset Loading**: The Toxic_DPO dataset is loaded from the Hugging Face library, specifically the training split.
2. **Tokenizer Configuration**: The tokenizer is configured to handle padding using the End of Sentence token to ensure uniform token lengths.
3. **Quantization Configuration**: The model is loaded with 4-bit precision using BitsAndBytesConfig for reduced VRAM usage and quantization.
4. **LoRA Configuration**: LoraConfig is used to define the LoRA parameters for the fine-tuning process.
5. **Base Model Loading**: The base PHI 2 model is loaded with the specified configurations.
6. **Model Preparation**: The model is prepared for k-bit training using prepare_model_for_kbit_training function.
7. **Training Arguments**: Training arguments are defined, specifying parameters such as batch size, learning rate, and evaluation strategy.
8. **Supervised Fine-Tuning**: The SFTTrainer is instantiated with the model, dataset, and training arguments for supervised fine-tuning.
9. **Training**: The model is trained on the provided dataset using the configured parameters.
10. **Model Saving**: The trained model is saved for future use as the fine-tuned Toxic_Edition model.

## Getting Started

To fine-tune the PHI 2 model for a task-specific application, follow these steps:

1. **Load Dataset**: Specify the dataset to use for fine-tuning, ensuring it is compatible with the task.
2. **Configure Tokenizer**: Customize the tokenizer settings, such as padding and special tokens, as required.
3. **Set Quantization Parameters**: Adjust the quantization configurations to optimize memory usage and performance.
4. **Define LoRA Configuration**: Set the LoRA parameters based on the task requirements and model architecture.
5. **Load Base Model**: Choose the base PHI 2 model to fine-tune and load it with the specified configurations.
6. **Prepare Model**: Use the prepare_model_for_kbit_training function to prepare the model for k-bit training.
7. **Define Training Arguments**: Set the training arguments, including batch size, learning rate, and evaluation strategy.
8. **Initiate Fine-Tuning**: Instantiate the SFTTrainer with the model, dataset, and training arguments, and start the fine-tuning process.
9. **Monitor Training**: Monitor the training progress and adjust parameters if necessary for optimal performance.
10. **Save Trained Model**: Once training is complete, save the fine-tuned model for future use in the specified directory.

## Acknowledgments

This notebook leverages the capabilities of PHI 2 to facilitate fine-tuning for task-specific applications. We extend our gratitude to the developers and contributors of these libraries for their valuable contributions.

Let's embark on the journey of fine-tuning PHI 2 and creating powerful task-specific models!

