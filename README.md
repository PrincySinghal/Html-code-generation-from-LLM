# Html-code-generation-from-LLM


### Objective: 
Fine-Tuning and Evaluating a Falcon 7B Model for HTML Code Generation. 

### Dataset:



### Process (steps and challenges) 
1. Model selection
2. Dataset Preparation and Preprocessing 
3. Model Fine tuning script(setting hyperparameters and choosing fine tuning techniques and regularization) 
4. Model Evaluation
5. API development to serve the model

### Challenges and Errors encountered with resolutions 


### List of hyperparameters that can be tweaked during training: 
learning_rate: 0.0002
train_batch_size: 2
eval_batch_size: 8
seed: 42
gradient_accumulation_steps: 2
total_train_batch_size: 4
optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
lr_scheduler_type: cosine
lr_scheduler_warmup_ratio: 0.03
training_steps: 320

### Results 
Model link- https://huggingface.co/PrincySinghal991/falcon-7b-sharded-bf16-finetuned-html-code-generation
![W B Chart 12_29_2023, 1_15_47 AM](https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/48e6f73a-5ec9-4116-afd3-2fa68ebd867e)
<img width="403" alt="image" src="https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/21b88108-3fc1-403f-b861-e66f76f24d9b">
![W B Chart 12_26_2023, 6_52_15 PM](https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/a77847dc-db45-452e-a626-df40d36bbdd4)
![W B Chart 12_26_2023, 6_52_26 PM](https://github.com/PrincySinghal/Html-code-generation-from-LLM/assets/87893594/e7bed244-3d21-4d38-b7c1-64139491446d)




### Further Steps 


### Key learnings 


