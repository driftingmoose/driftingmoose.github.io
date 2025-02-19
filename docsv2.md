---
title: Code Buddy v2.0.3
layout: home
nav_order: 10
---

## Documentation for Code Buddy for Unity v2.0.3

If you have any questions - [join our Discord](https://discord.gg/JdsepFhEeX) to contact support

### Create OpenAI API key

1. Sign in or sign up to OpenAI [https://platform.openai.com/](https://platform.openai.com/)
2. Go to [https://platform.openai.com/organization/api-keys](https://platform.openai.com/organization/api-keys) and create an API key with all permissions. CodeBuddy needs it to initialize and use the assistant.

### Initialization

1. Go to Edit->Project Settings…->Code Buddy
2. Paste your API key in the “OpenAI API Key” field
3. Choose the model and press the Initialize button

![Settings](/assets/v2/settings%20full%20assistant.png)

If the “Buddy is ready!” message appears you are good to go.

### Settings

Key
: Definition

OpenAI API Key
: Your API key.[^1]

Base URL
: URL for the OpenAI API or proxy server.

Test connection
: Runs a series of tests to make sure your credentials work with the specified server.

Use Custom Model
: If checked you will be able to specify any name of a model in the new text field. Useful when working with proxies or for specific model versions.

Model
: The model used for the assistant.
Please note that free accounts support only gpt-4o-mini and gpt-3.5-turbo models.
o1 and o3 models available only with “Use Completions” option.|

Include Editor Folder
: Add the content of the “Editor” folders into the project context.
By default, Code Buddy ignores any editor extension code to optimize requests, but this option allows you to work with editor extensions as well.

Ask Where to Save
: If selected, Code Buddy will ask you where to save new files. If not, all files will be saved in the default script folder.

Default script folder
: Default folder for saving new scripts.

Instructions
: Main prompt for the model.

Temperature
: Defines randomness of the response. It is recommended to leave it at a minimum for consistency.

Use Completions
: Force Code Buddy to use Completions API instead of assistants and threads. This option is used for work for some proxies ([https://api.pawan.krd/](https://api.pawan.krd/) for ex.) or if you don’t want to create any assistants on your profile.
It is recommended not to use it if possible. Assistants API is much more efficient and cheaper than the Completions API.

Initialize
: Press to initialize the assistant[^2], or re-initialize it after a model change.

Reset
: Reset all settings to the default state
(does not remove assistant from OpenAI account)


[^1]: Your API key is stored encrypted in the Project Settings.
[^2]: Code Buddy creates a new assistant for every project.

### Generate new scripts

To open Code Buddy go to Window -> Code Buddy -> Code with Buddy

<img align="right" src="assets/v2/buddy empty window.png" width=300>

It is very straightforward:

- “Send” button launches generation
- Paperclip button allows you to attach scripts to the chat
- “+” button starts new conversation
- “History” shows list of all chats

<br clear="right"/>

Write the instructions and hit “Send”.

<img align="right" src="assets/v2/hello world.png" width=300>

“Save” button will save code to the Default script
folder or open the Save File dialogue so you can
choose where to put the new script in your project
if Ask where to save selected in the settings.

If you have selected game object in your Hierarchy
“Save and Add” button will appear. It automatically
adds script to the selected object after saving.

“Copy” - copies code into the buffer.
It is most useful when generating only partial
changes and not whole class.

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
3. Drag-n-drop desired script to the message
field or attach it by pressin paperclip button

Add instructions and hit Send.

When generation is complete, if you are happy with
the result hit “Update” and that’s it.

<br clear="right"/>

<img align="right" src="assets/v2/update item.png" width=300>

Alternatively, with default instructions Buddy should
ask you to provide him with the source code, if there
is none in the previous conversation.

<br clear="right"/>

If you have any more questions you can ask them at our [Discord](https://discord.gg/JdsepFhEeX)