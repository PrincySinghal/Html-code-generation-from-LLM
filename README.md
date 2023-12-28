# Html-code-generation-from-LLM


### Objective: 
Fine-Tuning and Evaluating a Falcon 7B Model for HTML Code Generation. 

### Dataset:
Used https://huggingface.co/datasets/ttbui/html_alpaca dataset which contains:
Size of data: 636 rows 
1. Instructions- user prompts (textual) 
2. Input-Further information needed as per the instruction could be html code or data points (textual+code) 
3. Response- empty 
4. Output- expected HTML code


### Process (steps and challenges) 
1. Model selection
2. Dataset Preparation and Preprocessing 
3. Model Fine tuning script(setting hyperparameters and choosing fine tuning techniques and regularization) 
4. Model Evaluation
5. API development to serve the model

### Challenges and Errors encountered with resolutions 




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
1. BLEU score: 

2. Generated HTML output:
Original vs Fine tuned model

3. Fine tuned model's outputs' evaluate_html score: 


### Future Scope 





