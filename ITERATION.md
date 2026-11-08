# Iteration

During my fist rounds of testing, MCP server was not able to find or extract the correct files. "File not found". 
My diagnosis is that the MCP server is not looking at the right place. 
I changed CODE_ROOT in ~/.codex/config.toml to /Users/sharon.wu/Desktop/CMU, allowing searches across my desktop CMU folder instead of simply the folder for this homework. The fix successfully allowed MCP connection to find hw6_protein.py and confirmed it was readable. 