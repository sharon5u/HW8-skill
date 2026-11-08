# Plain-English Code Explainer

## Skill

The skill explains code step by step, describes the inputs, outputs, and also important functions in everyday language that is more readable to a beginner. The skill also defines technical terms with simple descriptive examples that are easy to understand by any level of user knowledge. The motivation is that I often need to ask an agent "please help me explain this portion of the code in a easy way," or in other forms where I request an explanaion of the code that the AI agent generated for my projects. Therefore, the skill is triggered when the user input requests such as “explain this code” or “help me understand this function.”

## MCP server

The MCP server tool finds files requested by the user by searching filenames within a local folder chosen. It then reads a selected file and returns its contents with line numbers so the AI can explain it using the skill we implemented. The motivation for this MCP server is that some times the code files can be too big or separated to copy and paste by the user. I often request AI to help me explain "What does the css file do for my project 1 assignment." 

## Setup (AI assisted with code writing)

Use Python 3.10+; from this toolkit folder:

```sh
python3 -m venv .venv
.venv/bin/python -m pip install -r local-code-files/requirements.txt
mkdir -p .agents/skills
cp -R skills/plain-english-explain .agents/skills/
```

Merge the following into your Codex configuration, replacing all machine-specific paths:

```toml
[mcp_servers.local-code-files]
command = "/ABSOLUTE/PATH/plain-english-explainer/.venv/bin/python"
args = ["/ABSOLUTE/PATH/plain-english-explainer/local-code-files/server.py"]

[mcp_servers.local-code-files.env]
CODE_ROOT = "/ABSOLUTE/PATH/project-to-explain"
```

Check registration and restart the client if necessary. Ask: “Use local-code-files to find calculator.py, then use $plain-english-explain to explain it.” Confirm actual tool calls in the transcript.


## AI use
For this homework, I mainly used AI to first explain how skills and MCP server interact before starting the assignment. I then asked AI to draft the rules for the skill and then do personalized edits by my self. I specifically used AI to help me understand why I had two skill.md files and later understood that they serve different purposes, one for the main skill and other for the checker. 
