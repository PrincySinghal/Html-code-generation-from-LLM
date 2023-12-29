# Html-code-generation-from-LLMs


### Objective: 
Fine-tuning the Falcon 7B  for the task of HTML code generation. The current model was selected based on its performance on complex reasoning benchmarks such as ARC and GSM8K and its compatibility with the available computational resources.

### Dataset:
Used https://huggingface.co/datasets/ttbui/html_alpaca dataset which contains:
Size of data: 636 rows 
1. Instructions- user prompts (textual) 
2. Input-Further information needed as per the instruction could be html code or data points (textual+code) 
3. Response- empty 
4. Output- expected HTML code


### Process 
1. Model selection
2. Dataset Preparation and Preprocessing 
3. Model Fine tuning script(setting hyperparameters and choosing fine tuning techniques and regularization) 
4. Model Evaluation
5. API development to serve the model

### Challenges and Errors encountered with resolutions 
1. Understanding and implementing Parameter-Efficient Tuning (PeFT).
2. Managing the computational complexity and memory limitations of large models.
3. Ensuring reproducibility and consistency across training runs.
4. Dealing with long training times and optimizing model runtime.

### Solutions Implemented:
1. Adopting PeFT techniques like LoRA, prefix tuning, and prompt tuning.
2. Utilizing quantization and model sharding to manage memory usage.
3. Setting a random seed for train-test splitting to ensure reproducibility.
4. Implementing early stopping and learning rate scheduling to improve convergence speed.
5. Regularization techniques such as dropout and scaling factor were applied.
6. Training arguments were carefully set up to balance performance and resource usage.



### List of hyperparameters that can be tweaked during training: 
1.learning_rate: 0.0002
2. train_batch_size:
3. eval_batch_size: 8
4. seed: 42
5.gradient_accumulation_steps: 2
6.total_train_batch_size: 4
7.optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
8.lr_scheduler_type: cosine
9.lr_scheduler_warmup_ratio: 0.03
10.training_steps: 320

### Training Results
Model link- https://huggingface.co/PrincySinghal991/falcon-7b-sharded-bf16-finetuned-html-code-generation
<img width="500" alt="image" src="https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/1b43ccd7-10ad-4962-b30c-5859973b681e">
<img width="500" alt="image" src="https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/dbffede6-3aa2-42c5-8683-a2f43b8d4d1f">
<img width="600" alt="image" src="https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/21b88108-3fc1-403f-b861-e66f76f24d9b">


### Evaluation Results
1. BLEU score: 0.01782


### Current explorations: 
1. LLMS more suited for code generation
2. Hyperparamter tuning to improve low evalution score





