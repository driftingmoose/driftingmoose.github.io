---
title: Code Buddy Documentation
layout: home
nav_order: 1
---

# Code Buddy Documentation

You can find latest documentation online at [https://docs.driftingmoose.com/](https://docs.driftingmoose.com/).

If you have any questions - [join our Discord](https://discord.gg/JdsepFhEeX) to contact support.

## Table of contents

- [Start with OpenAI](#start-with-openai)
- [Start with Ollama](#start-with-ollama)
- [Start with DeepSeek](#start-with-deepseek)
- [Settings](#settings)
- [Main operations](#main-operations)

## Start with OpenAI

### Create OpenAI API key

1. Sign in or sign up to OpenAI [https://platform.openai.com/](https://platform.openai.com/)
2. Make sure you have an active balance on the account, and top up it if necessary.
3. Go to [https://platform.openai.com/organization/api-keys](https://platform.openai.com/organization/api-keys) and create an API key with all permissions. CodeBuddy needs it to initialize and use the assistant.

### Configure Code Buddy

1. Go to **Edit->Project Settings…->Code Buddy**
2. Paste your API key in the “OpenAI API Key” field
3. Choose the model
4. If you use **OpenAI Assistant** - press the Initialize button

![Settings](/assets/v25/settingsfilled.png)

You are ready to go! [Start creating new scripts.](#generate-new-scripts)

## Start with Ollama

### Install and configure Ollama

1. Install Ollama from the official website [https://ollama.com/download](https://ollama.com/download)
2. After installation is complete install at least one model using website [https://ollama.com/search](https://ollama.com/search) or using Terminal with command `ollama run <model_name>`. For example, to install the llama 3.2 model, use the command `ollama run llama3.2`.

You can read more about using Ollama [here](https://github.com/ollama/ollama/blob/main/README.md).

### Configure Code Buddy

1. After model download is finished make sure Ollama is running and go to Code Buddy settings in **Edit->Project Settings…->Code Buddy**.
2. In the **Provider:** dropdown choose Ollama.
3. Press **Refresh** button.
4. The newly installed model should appear in the **Model:** dropdown.

![Ollama Settings](/assets/v25/ollama%20settings.png)

You are ready for [code generation](#generate-new-scripts).

## Start with DeepSeek

### Create DeepSeek API key

1. Go to [https://platform.deepseek.com/](https://platform.deepseek.com/) and sign up or login to your account.
2. Make sure you have a positive balance on the account.
3. Create a new API key at the page [https://platform.deepseek.com/api_keys](https://platform.deepseek.com/api_keys).

### Configure Code Buddy

1. Go to **Edit->Project Settings…->Code Buddy**
2. Select **DeepSeek** from **Provider:** drop down list.
3. Paste your API key in the DeepSeek API Key” field.
4. Choose the model from the list.

![DeepSeek Settings](/assets/v25/settings%20deepseek.png)

You are ready to [create your first script](#generate-new-scripts)

## Settings

This is the full list of available settings. Final set that you will see on the settings page will slightly differ depending on the currently selected provider.

OpenAI API Key
: Your OpenAI API key.[^1]

DeepSeek API Key
: Your DeepSeek API key.[^1]

Base URL
: URL for the provider or proxy server.

Refresh button
: Refreshes list of available Ollama models.

Test connection button
: Runs a series of tests to make sure your credentials work with the specified server.

Use Custom Model
: If checked you will be able to specify any name of a model in the new text field. Useful when working with proxies or for specific model versions.

Model
: The model used for the assistant. o1 and o3 models are available only with the “OpenAI Completions” option.

Context size
: The size of the context window used to generate the next token. Bigger numbers will require more RAM to run models.

Instructions
: Main prompt for the model.

Include Editor Folder
: Add the content of the “Editor” folders into the project context.
By default, Code Buddy ignores any editor extension code to optimize requests, but this option allows you to work with editor extensions as well.

Ask Where to Save
: If selected, Code Buddy will ask you where to save new files. If not, all files will be saved in the default script folder.

Default script folder
: Default folder for saving new scripts.

Temperature
: Defines randomness of the response. It is recommended to leave it at a minimum for consistency.

Use Completions
: Force Code Buddy to use Completions API instead of assistants and threads. This option is used for work for some proxies ([https://api.pawan.krd/](https://api.pawan.krd/) for ex.) or if you don’t want to create any assistants on your profile.
It is recommended not to use it if possible. Assistants API is much more efficient and cheaper than the Completions API.

Initialize
: Press to initialize the assistant[^2], or re-initialize it after a model change.

Clear History
: Clears all chat history for all providers.

Reset
: Reset all settings to the default state
(does not remove assistant from OpenAI account)


[^1]: Your API key is stored encrypted in the Project Settings.
[^2]: Code Buddy creates a new assistant for every project.

## Main operations

### Generate new scripts

To open Code Buddy go to Window -> Code Buddy -> Code with Buddy.

<img align="right" src="assets/v2/buddy empty window.png" width=300>

It is very straightforward:

- “Send” button launches generation
- Paperclip button allows you to attach scripts to the chat
- “+” button starts new conversation
- “History” shows a list of all chats

<br clear="right"/>

Write the instructions and hit “Send”.

<img align="right" src="assets/v2/hello world.png" width=300>

“Save” button will save the code to the Default script
folder or open the Save File dialogue so you can
choose where to put the new script in your project
if **Ask where to save** selected in the settings.

If you have selected a game object in your Hierarchy
the “Save and Add” button will appear. It automatically
adds a script to the selected object after saving.

“Copy” - copies code into the buffer.
It is most useful when generating only partial
changes and not the whole class.

<br clear="right"/>

### Edit script

<img align="right" src="assets/v2/update item attach.png" width=300>

You can edit existing scripts with Code Buddy.
There are 3 options:
1. Open the context menu for the MonoBehaviour
in the inspector and select
“Edit Script with Buddy”.
2. Right-click on the script in the Project panel
and select “Edit Script with Buddy”.
3. Drag-n-drop the desired script to the message
field or attach it by pressing the paperclip button

Add instructions and hit Send.

When generation is complete if you are happy with
the result hit “Update” and that’s it.

<br clear="right"/>

<img align="right" src="assets/v2/update item.png" width=300>

Alternatively, with default instructions, Buddy should
ask you to provide him with the source code, if there
is none in the previous conversation.

<br clear="right"/>

You can find more details about how code buddy works under the hood in [this article](/how-code-buddy-works.html).

If you have any more questions you can ask them at our [Discord](https://discord.gg/JdsepFhEeX)