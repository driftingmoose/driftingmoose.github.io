<!-- ---
title: Getting Started (print)
layout: home
nav_order: 10
--- -->

# Getting Started

You can find latest documentation online at [https://docs.driftingmoose.com/](https://docs.driftingmoose.com/).

If you have any questions - [join our Discord](https://discord.gg/JdsepFhEeX) to contact support.

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/DI0LMVRDQ2k?si=mGKqlxre5ww-vrmS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen> </iframe> -->

## Table of contents

- [Quick start](#quick-start)
- [Configure AI providers](#configure-ai-providers)
  - [OpenAI](#openai)
  - [Ollama](#ollama)
  - [DeepSeek](#deepseek)
  - [Gemini](#gemini)
  - [Claude](#claude)
- [Settings overview](#settings)

## Quick start

1. Go to Edit->Project Settings…->Code Buddy
2. Choose AI provider and [configure it](#configure-ai-providers)
3. Open Code Buddy by selecting Window -> Code Buddy -> Code with Buddy.
4. Make your first request

## Configure AI Providers

### OpenAI

#### Create OpenAI API key

1. Sign in or sign up to OpenAI [https://platform.openai.com/](https://platform.openai.com/)
2. Make sure you have an active balance on the account, and top up it if necessary.
3. Go to [https://platform.openai.com/organization/api-keys](https://platform.openai.com/organization/api-keys) and create an API.

#### Configure Code Buddy

1. Go to **Edit->Project Settings…->Code Buddy**
2. Paste your API key in the “OpenAI API Key” field
3. Choose the model

![Settings](/assets/v25/settingsfilled.png)

You are ready to go! [Start creating new scripts.](#generate-new-scripts)

### Ollama

#### Install and configure Ollama

1. Install Ollama from the official website [https://ollama.com/download](https://ollama.com/download)
2. After installation is complete install at least one model using website [https://ollama.com/search](https://ollama.com/search) or using Terminal with command `ollama run <model_name>`. For example, to install the llama 3.2 model, use the command `ollama run llama3.2`.

You can read more about using Ollama [here](https://github.com/ollama/ollama/blob/main/README.md).

#### Configure Code Buddy

1. After model download is finished make sure Ollama is running and go to Code Buddy settings in **Edit->Project Settings…->Code Buddy**.
2. In the **Provider:** dropdown choose Ollama.
3. Press **Refresh** button.
4. The newly installed model should appear in the **Model:** dropdown.

![Ollama Settings](/assets/v25/ollama%20settings.png)

### DeepSeek

#### Create DeepSeek API key

1. Go to [https://platform.deepseek.com/](https://platform.deepseek.com/) and sign up or login to your account.
2. Make sure you have a positive balance on the account.
3. Create a new API key at the page [https://platform.deepseek.com/api_keys](https://platform.deepseek.com/api_keys).

#### Configure Code Buddy

1. Go to **Edit->Project Settings…->Code Buddy**
2. Select **DeepSeek** from **Provider:** drop down list.
3. Paste your API key in the "DeepSeek API Key" field.
4. Choose the model from the list.

![DeepSeek Settings](/assets/v25/settings%20deepseek.png)

### Gemini

#### Create Gemini API key

1. Go to [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) and press **Create API key**.
2. Follow the instructions in case you will need to create Google Cloud project.
3. Copy your key.

#### Configure Code Buddy

1. Go to **Edit->Project Settings…->Code Buddy**
2. Select **Gemini** from **Provider:** drop down list.
3. Paste your API key in the "Gemini API Key” field.
4. Choose the model from the list.

To get the latest list of available models, press **Refresh model list** button next to the dropdown.

![Gemini Settings](/assets/v27/gemini-settings.png)

### Claude

#### Create Claude key

1. Go to [https://console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys) and **Create key**.
2. Choose project and name the key.
3. Copy your key.

#### Configure Code Buddy

1. Go to **Edit->Project Settings…->Code Buddy**
2. Select **Claude** from **Provider:** drop down list.
3. Paste your API key in the "Claude API Key" field.
4. Choose the model from the list.

To get the latest list of available models, press **Refresh model list** button next to the dropdown.

![Claude Settings](/assets/v27/claude-settings.png)

## Settings

This is the full list of available settings. Final set that you will see on the settings page will slightly differ depending on the currently selected provider.

API Key
: Your API key for selected provider.[^1]

Base URL
: URL for the provider or proxy server.

Refresh button
: Refreshes list of available models.

Test connection button
: Runs a series of tests to make sure your credentials work with the specified server.

Use Custom Model
: If checked you will be able to specify any name of a model in the new text field. Useful when working with proxies or for specific model versions.

Model
: The model used for the assistant.

Context size (for Ollama)
: The size of the context window used to generate the next token. Bigger numbers will require more RAM to run models.

Max tokens (for Claude)
: The maximum number of tokens to generate before stopping. Each model has it's own maximum value so please check the [Claude documentation](https://docs.anthropic.com/en/docs/about-claude/models/all-models#model-comparison-table).

Instructions
: Main prompt for the model.

Include Editor Folder
: Add the content of the “Editor” folders into the project context.
By default, Code Buddy ignores any editor extension code to optimize requests, but this option allows you to work with editor extensions as well.

Excluded Folders
: List of folders to exclude from the context.

Ask Where to Save
: If selected, Code Buddy will ask you where to save new files. If not, all files will be saved in the default script folder.

Default script folder
: Default folder for saving new scripts.

Reinitialize project cache
: Clear localy cached data about the project

Temperature
: Defines randomness of the response. It is recommended to leave it at a minimum for consistency.

Clear History
: Clears all chat history for all providers.

Reset
: Reset all settings to the default state
(does not remove assistant from OpenAI account)

[^1]: Your API key is stored encrypted in the Project Settings.

<!-- You can find more details about how code buddy works under the hood in [this article](/how-code-buddy-works.html). -->

If you have any more questions you can ask them at our [Discord](https://discord.gg/JdsepFhEeX)
