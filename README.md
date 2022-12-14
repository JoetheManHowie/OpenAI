# OpenAI
A beginner guide to the python api for openai. Please find a module of the code demomstrated in these tutorials [here](https://github.com/JoetheManHowie/pyai).

OpenAI is an amazing machine learning technology that can generate responses in the form of text, images, or code all from plain text descriptions, called the prompt. The plain text description can be as basic or hyperspecific as you like; with up to 1000 characters in the prompt. 


## Overveiw:

This repo is meant to get you started with the basics of the openai python api. There are two main jupyter notebook tutorials:

1. GettingStarted--TextCompletion.ipynb
2. GettingStarted--ImageGeneration.ipynb



The openai has three main use cases:

1. Generating text documents (essays, summaries, cover letters, proposals, book and paper outlines, news articles, lists, recipes, etc.) 
2. Generating images
3. Generate code (any language)

Both text and code generation are done with `openai.Completion`, and image generation is done with `openai.Image`.

For a module with class versions of these notebooks [see the repo pyai](https://github.com/JoetheManHowie/pyai).

### Installation and Setup:

To run the jupyter-notebook you will need to pip install the openai library

`pip install --upgrade openai`

This is also in the jupyter notebooks as well.

import the openai library as:

`import openai as oai`

To use the AI, make an account at [the openai website](https://beta.openai.com). Then go to the [API keys page](https://beta.openai.com/account/api-keys) and generate a secret key.

There are ways to set you key privately that are not (yet) addressed in these tutorials. Save your private key, and enter it when prompted by the notebooks.
Please feel free to contribute a guide on setting the api key on your local machine, or for multiple clients.

To set your key in python use `oai.api_key = <your_key>`




### TextCompletion

This notebook reviews the basics of the python api for text completion.

`Completion` is the class from `oai` that lets us generate text from a prompt with the method `create`.

Ex: `response = oai.Completion.create(model="text-davinci-003", prompt=<text_prompt>)` where `<text_prompt>` is the plain text instructions for the AI.


Try using it to: write a cover letter, write a essay, write a program (in any programming language), write a poem, write a speak, write a resume, create a recipe, generate a list of names, etc. 


### ImageCompletion

This notebook reviews the bacis of the python api for image generation.

`Image` is the class from `oai` that lets us generate images from a prompt with the method `create`.

Ex: `image_resp = oai.Image.create(prompt=<image_prompt>)` where `<image_prompt>` is the plain text instructions for the AI.

Try using it to: design a logo, create a van gogh painting (or a different artist painting), generate images of cats, draw a landscape (just type a country or city name), draw a map, etc

