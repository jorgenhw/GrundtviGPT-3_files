<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://i.imgur.com/t8mSDQS.png">
    <img src="https://i.imgur.com/t8mSDQS.png" alt="Logo" width=200 height=200>
  </a>
  
  <h1 align="center">GrundtviGPT-3</h1> 
  <h2 align="center"><i>Finetuning GPT-3 on Lyrics Generation</i></h2> 
  <h3 align="center">Cognitive Science Bachelor's 2023</h3>


  <p align="center">
    Jørgen Højlund Wibe & Niels Aalund Krogsgaard
  </p>
</p>

<!-- ABOUT THE PROJECT -->
## About the project

In this project, we will be finetuning the GPT-3 Davinci model on a lyrics generation task. The lyrics are from the Danish songbook named "Højskolesangbogen" which contains around 600 songs of cultural significance to Denmark. GPT-3 (Generative Pre-trained Transformer 3) is a state-of-the-art language model developed by OpenAI that can generate human-like text. By finetuning GPT-3 on a specific task, we can fine-tune its capabilities to perform that task more effectively.

## Requirements

* A machine with a GPU (we used Google Colab: a virtual notebook environment that executes code on virtual machines with GPU)
* Python 3.6 or higher
* The OpenAI API key (you can apply for one here: https://beta.openai.com/)

## Set up
1. Clone this repository:

```
git clone https://github.com/jorgenhw/GrundtviGPT-3
cd GrundtviGPT-3
```

2. Install the required packages:
```
pip install -r requirements.txt
```
3. Set up the OpenAI API key:
```
export OPENAI_API_KEY=your_api_key
```
## Data
We will be using a dataset of song lyrics as our training data. You can use any dataset of song lyrics that you like, or you can scrape lyrics from the internet. Make sure to preprocess the data and save it in a .txt file.

## Finetuning
1. Choose the GPT-3 model that you want to use for finetuning. You can find a list of available models and their sizes here.

2. Fine-tune the model on your dataset using the OpenAI API:

```
openai train \
  --model-engine gpt2 \
  --model-size medium \
  --dataset dataset.txt \
  --num-epochs 10 \
  --output-path model.bin
```

Replace medium with the size of the model that you have chosen, and dataset.txt with the path to your dataset.

## Evaluation
Evaluate the performance of the finetuned model by generating lyrics and comparing them to a sample of the training data. You can also use metrics such as perplexity and BLEU score to quantitatively evaluate the model.

## Conclusion
In this project, we have successfully finetuned the GPT-3 model on a lyrics generation task. You can further improve the performance of the model by using a larger dataset, increasing the number of training epochs, or fine-tuning on a specific artist or genre.

## Contact

Feel free to contact the authors, [Emil Jessen](https://github.com/emiltj) or [Johan Horsmans](https://github.com/johanHorsmans) for any questions regarding the scripts.
You may do so through our emails ([Emil](mailto:201807525@post.au.dk), [Johan](mailto:201810219@post.au.dk))
<br />




The two files in this folder contains instructions on how to replicate the results found in the paper: GrundtviGPT-3: Lyric
generation by a Large Language Model.

These results are part of an exam projekt in Cultural Data Science at Aarhus University, 2022.

Authors:
Jørgen Højlund Wibe
Niels Aalund Krogsgaard
