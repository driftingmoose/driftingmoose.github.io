---
title: Code Buddy v2.0.3
layout: home
---

## Code Buddy for Unity v2.0.3

If you have any questions - [join our Discord](https://discord.gg/JdsepFhEeX) to contact support

Documentation for v1.1 is here

### Create OpenAI API key

1. Sign in or sign up to OpenAI https://platform.openai.com/
2. Go to https://platform.openai.com/organization/api-keys and create an API key with all permissions. CodeBuddy needs it to initialize and use the assistant.

### Initialization

1. Go to Edit->Project Settings…->Code Buddy
2. Paste your API key in the “OpenAI API Key” field
3. Choose the model and press the Initialize button

![Settings](/assets/v2/settings%20full%20assistant.png)

If the “Buddy is ready!” message appears you are good to go.

### Settings

Key
: Definition

| OpenAI API Key | Your API key. * |
| Base URL | URL for the OpenAI API or proxy server. |
|Test connection|Runs a series of tests to make sure your credentials work with the specified server.|
|Use Custom Model|If checked you will be able to specify any name of a model in the new text field. Useful when working with proxies or for specific model versions.|
|Model|The model used for the assistant.
Please note that free accounts support only gpt-4o-mini and gpt-3.5-turbo models.
o1 and o3 model available only with “Use Completions” option.|

Include Editor Folder
Add the content of the “Editor” folders into the project context.
By default, Code Buddy ignores any editor extension code to optimize requests, but this option allows you to work with editor extensions as well.
Ask Where to Save
If selected, Code Buddy will ask you where to save new files. If not, all files will be saved in the default script folder.
Default script folder
Default folder for saving new scripts.
Instructions
Main prompt for the model.
Temperature
Defines randomness of the response. It is recommended to leave it at a minimum for consistency.
Use Completions
Force Code Buddy to use Completions API instead of assistants and threads. This option is used for work for some proxies (https://api.pawan.krd/ for ex.) or if you don’t want to create any assistants on your profile.
It is recommended not to use it if possible. Assistants API is much more efficient and cheaper than the Completions API.
Initialize
Press to initialize the assistant**, or re-initialize it after a model change.
Reset
Reset all settings to the default state
(does not remove assistant from OpenAI account)


 *Your API key is stored encrypted in the Project Settings.
           **Code Buddy creates a new assistant for every project.

