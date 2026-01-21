# Refresh Qwen Key in Claude Code Router
Updated (v4)

## Pre-requisites
- Qwen CLI should be installed. see command [here](qwen.md)
- Claude Code should be installed. see command [here](claude-code.md)
- Claude Code Router should be installed. see command [here](claude-code.md)
- config.json file of Claude Code Router should contain values according to Qwen. Just copy paste the provided config file in claude code router folder.
- Thy python script file copy_qwen_apikey.py file should be available in your home directory.


## Generate new API key of Qwen and Update it in Claude Code Router
Run this command 

```
qwen --auth-type qwen-oauth -p "hi" && python3 ~/copy_qwen_apikey.py && ccr restart && ccr code
```

This command will do these things in one go.
1.⁠ ⁠Regenerate Qwen API key
2.⁠ ⁠⁠Copy Qwen key to Claude Code router
3.⁠ ⁠⁠ccr restart
4.⁠ ⁠⁠Open Claude Code by running command “ccr code”

Note: I have used it in MacOS, it worked well. I am sure it will work in Linux too. and I think it will work in Git Bash and WSL too, if you are using any of them in windows.

