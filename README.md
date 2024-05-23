# Overview

This repository is the final report for CS274. In this repository, I have my:
#### -Report for my project
#### -Powerpoint for my project
#### -Dataset used for my project
#### -Code used for my project

# Report

This report is attached as a .pdf file.

# Powerpoint
This powerpoint is attached as a .pptx file.

# Dataset
This dataset is a subset of an original dataset. The original dataset can be found at: https://nijianmo.github.io/amazon/index.html
The current dataset in this repository is already pre-processed

# Code
This code is sourced from: https://github.com/anord-wang/LLM4REC

Navigate to the LLM4REC/src folder and install the required libraries. This requires a python version of Python 3.11.5
-pip install -r requirements.txt

Since the Vision Models are not incorporated into the actual code, you don't have to install the Vision Model. If you want to test the Vision Model out:
-pip install ultralytics
You can simply run vision.py to test the Vision Model. This would require adding a main into this file.
Add
```
def main():
  predict('insert image location here', #epochs)

if __name__ == "__main__":
  main()
```

Training of this project isn't necessary, but if you want to run the training.py file, you must change some locations in the training.py file.
Change
#### -server_root: your root for LLM4REC.
#### -local_root: location to save models.
After changinging these parameters, you can run python training.py --dataset 'location of luxury dataset' --lambda_V 1   

Fine-tuning is after this step. This step requires a lot of parameter changing, if you ran the training step.
This file uses embeddings created from the Training step, so if you have run the training step, it is necessary to change all of the embeddings.
If you did not run the training step, you do not have to change anything and can run with my embeddings.
You can run fine-tuning: python finetuning.py --dataset 'location of luxury dataset' --lambda_V 1
