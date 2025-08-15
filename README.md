# BYOD AI Workshop

## Machine Learning and You: A Whirlwind Tour

Location:
RFP 214 / 215

John Fink (McMaster University)

Tim Ribaric (Brock University)

10:00 AM to 12:00 AM

Large Language Models have exploded in popularity in the past 2 years prompting the creation of new and exciting ways to do research. It is now possible to use AI to gather insights and develop rich insights into data without being a full fledged data scientist. This workshop will begin with a tour through the Library Carpentry Machine Learning for Librarians curriculum before delving into the hands-on portion where learners will experiment with running different models and environments on their own computers. Participants will learn about the wide variety of options that exist outside of the narrow range of popular tools that find themselves in the news, and learn about the wide world of machine learning, from edge computing on microcontrollers to sophisticated language models running on supercomputers.



## Setup

Due to the fact that working that models uses rather large files we'll try to download them directly from the platform or from this tutorial website. We don't want to spend most of our time together just looking at download progress bars.

### Please Install

[GPT4ALL](https://www.nomic.ai/gpt4all) - This will be the client program that we run on your laptop. This will run the different models that we will experiment with.
There are many different platforms that help you run an LLM on your local machine. ([Jan](https://jan.ai/) is a good one to try next.) The reason we are using GPT4ALL is that is has built in [Retrieval Augmented Generation](https://elibtronic.github.io/AIL_Database/items/ail_026.html) built in.

### Download Data Set

Please download the [zip](https://github.com/elibtronic/BYOD_AI_Workshop/raw/refs/heads/main/GPT4ALL_Workshop/DataSet.zip) file of of the data that we are going to use for the RAG portion of the workshop. You can leave it in your Downloads directory for now. The [data Set](data/) - A collection of reviews about different Spider Man movies ranking at different scores. (Data orginally from [Kaggle](https://www.kaggle.com/datasets/okancan/spiderman-movies-imdb-reviews)) The data is split up into two files:

- `Spidey_Bad/` - Ten reviews that ranked the movie a 1 out of 10
- `Spider_Good/` - Ten reviews from the dataset that ranked the movie at a perfect 10.

### Download Model Files

To demonstrate the differences between various LLM options we are going to try running some lower end models. We'll start with these but as the session goes on we can explore different ones. Once you click on the links look for the __Download__ button on the page. You can leave the files in your download directory.

[Model 1 - Qwen2.5-0.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct-GGUF/blob/main/qwen2.5-0.5b-instruct-q4_0.gguf) -  A super lightweight model that only clocks in at 450 MB!

[Model 2 
Llama-3.2-1B-Instruct](https://huggingface.co/bartowski/Llama-3.2-1B-Instruct-GGUF/blob/main/Llama-3.2-1B-Instruct-Q5_K_M.gguf) - The smallest version of Meta's Llama model (about 900 MB) that will produce good enough results for our experimenting. 

### Shared notes for the session

This following Google [document](https://docs.google.com/document/d/1p4ZSZS-qhJLDydX17YzSCCV6oxTFaYX9fQ4v2YlcxBg/edit?usp=sharing) will be our shared notes location for the workshop. Please feel free to drop any comments / questions in this document as we proceed during the session. Feel free to answer the questions of others if you know the answer. Feel free to add silly comments to this document as well.


## Agenda


|||
|---|----|
|1000|Introductory [Presentation](presentation.pdf) |
|1030|Multiple Models running locally|
|1115|Adding Data & Retrieval Augmented Generation|
|1145|Concluding Discussion and Wrap-up|

### Actvity 1 - Installing GPT4All and load in Model Files

We are using [GPT4All](https://www.nomic.ai/gpt4all) as it is a simple GUI that has all of the generative AI functions put together in an easy to use interface.

- Start __GPT4ALL__
- Open Settings > Application > Download Path
- Open a Finder / Explore window to this directory and copy in the two Model files you downloaded

### Activity 2 - Adjusting model parameters

To tweak the individual models we are going to adjust some parameters to see what they do

- System Prompt
- Suggested FollowUp Prompt
- Temperature

### Activity 3 - Two models answering the same thing

We are going to explore asking the same question of two different models to see what difference in results we can get. First we'll try with _Qwen_, then with _LLama_.

### Activity 4a - Does RAG Affect your Results


We will use the _Local Docs_ feature of GPT4All to create a basic Retrieval Augemented Generation system. Once we do that we'll ask our models the same questions about Spider-Man movies to see if the results are different. Make two local docs locations for the two datasets:

Dataset #1 - 10 Reviews of _Spiderman: Into the Spiderverse_ that ranked the movie a 10 out of 10. Save all of these files in a directory called `spidey_good_reviews` in your Downloads directory.

Dataset #2 - 10 Review of _Spiderman: Into the Spiderverse_ that ranked the movie 1 out of 10. Save all of these files in a directory called `spidey_bad_reviews` in your Downloads directory.


### Activity 4b - Does RAG Affect your Results

Trying asking _Qwen_ 

```
Is Spider-Man into the Spider-Verse a good movie?
``` 

With `spidey_good_reviews` enabled in for _Local Docs_ and again with `spidey_bad_reviews`.

### Activity 4c - Does RAG Affect your Results

Let's try the RAG experiement again, this time with the _Meta Llama_ model


### Actvity 5 - Your Own RAG

Find a few document about something that you know a good deal about. Create a _Local Docs_ of those documents and run your different models against them.

### Activity 6 - Other models

Check out [Hugging Face](https://huggingface.co/) to see all of the different models that are available for you to use. Share any with the class that you find interesting.


## Further Reading

- [Intro to AI for GLAM from Library Carpentry](https://carpentries-incubator.github.io/machine-learning-librarians-archivists/)



