# RasaChatbotProject - Chatbot Documentation

## Overview
This document serves as a comprehensive guide for setting up and using a multilingual Rasa chatbot. This chatbot is designed to understand and interact in multiple languages, providing a dynamic conversational experience.


## Requirements
- Python 3.8 or above
- Visual Studio Code (VSCode)


## Setting up the Environment
### Create a Virtual Environment
- **Command:** python -m venv myenv

### Activate the Virtual Environment
- **For Windows:** myenv\Scripts\activate


## Installing Rasa
1. **Ensure the virtual environment is active.**
2. **Install Rasa via pip in VSCode's terminal:** pip install rasa

## Verifying Rasa Installation
- **Command:** rasa –version

## Creating a New Rasa Project
- **Command:** rasa init

## Training the Model
- Ensure necessary changes in the code are made before training.
- **Command:** rasa train

## Using Rasa
- **Command:** rasa shell

For more advanced configurations and features, refer to [Rasa's official documentation](https://rasa.com/docs/rasa/).


## Understanding Rasa Files

### Data Folder
Contains three files: `nlu.yml`, `rules.yml`, and `stories.yml`.

#### nlu.yml
- **Intent Definitions:** Describes user intentions.
- **Training Data:** Provides examples for each intent.
- **Intent Synonyms:** Handles different phrasings for the same intent.

#### rules.yml
- **Rule Definitions:** Outlines sequences of dialogue steps.
- **Conditions and Actions:** Specifies bot responses to user inputs.
- **Fallback Rules:** Manages unrecognized user intents.

#### stories.yml
- **Story Definitions:** Narrates specific conversation flows.
- **User Inputs:** Details intent names and entity values.
- **Bot Responses:** Defines bot's reactions to inputs.

### domain.yml
Defines chatbot behavior including intents, entities, responses, and slots.

### config.yml
Configures NLU and Core models, detailing pipelines and language models.

### Pipelines
- **WhitespaceTokenizer**: Splits user input into tokens.
- **RegexFeaturizer**: Finds patterns for additional features.
- **LexicalSyntacticFeaturizer**: Extracts syntactic features.
- **CountVectorsFeaturizer**: Converts text into numerical representation.
- **DIETClassifier**: Performs intent classification and entity recognition.
- **EntitySynonymMapper**: Consolidates entity variations.
- **ResponseSelector**: Chooses the best response from a set.

The configuration in `config.yml` significantly impacts chatbot performance and should be tailored to your specific needs. This file is essential during both the training and the inference phases of your Rasa project.






