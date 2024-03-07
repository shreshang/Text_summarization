# Text Summarization Model 
Text summarization is the process of distilling large amounts of text into shorter, coherent versions while retaining the most important information. This process aims to provide a concise representation of the original text, making it easier and quicker for readers to grasp the main points without having to go through the entire document.

I have tried to create a model that can provide us the summary of the poems which i have saved in the dataset.

The dataset contains 2 folders named as "forms" and "topics"

The forms folder contains files of different kinds of peotric forms such as verse, lyrics, etc.

The topics folder contains of different kinds of themes of poetry such as murder, animals, etc.

# Recommended Runtime 
GPU is best suited for such tasks as it can generate faster results. 

# Installations 
```python
!pip install transformers
!pip install sentencepiece
!pip install gensim
!pip install spacy
!pip install sumy
!pip install nltk
!pip install -U spacy
!python -m spacy download en_core_web_sm
``` 

# Usage

1. First, initialize the model and tokenizer by running the provided code snippet:
```python
!pip install transformers
from transformers import AutoModel, AutoTokenizer

model_name = "facebook/bart-large-cnn"
model = AutoModel.from_pretrained(model_name)
tokenizer = AutoTokenizer.from_pretrained(model_name)
```

2. Next, use the provided code to summarize your text and try to make a function to clean the text.
```python
summarizer = pipeline("summarization", model=model_name)

def clean_text(text):
    # your logic here
    return(....)
```
3. Now define function to summarize text
```python 
def summarize_text(text):
    # your logic here
    return(....)
```
4. Define folder containing text files
```python
folder_path = "folder_path_here"
```
5. Iterate over files in your folder 
```python 
for filename in os.listdir(folder_path):
    if filename.endswith(".txt"):
        # your logic here
        print () # use this statement to print your final summary
```
