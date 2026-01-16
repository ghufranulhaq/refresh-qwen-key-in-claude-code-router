# Refresh Qwen Key in Claude Code Router
Updated (v3)

## Pre-requisites
- Qwen CLI should be installed. see command [here](qwen.md)
- Claude Code should be installed. see command [here](claude-code.md)
- Claude Code Router should be installed. see command [here](claude-code.md)
- config.json file of Claude Code Router should contain values according to Qwen. Just copy paste the provided config file in claude code router folder.

## Generate new API key of Qwen
Run this command to generate a new api key of qwen
```
qwen --auth-type qwen-oauth
```

The above command generates a new key. You can now exit Qwen.

## Copy Qwen API key to Claude Code Router
Make sure you have "copy_qwen_apikey_v3.py" file in current directory or any other appropriate directory.
This python script will copy Qwen key to Router's config file.
Run the script 
```
Enter command:
python3 copy_qwen_apikey_v3.py

Expected Output: (similar to the following)

Updated api_key for provider: qwen
Successfully updated api_key(s) in 
/Users/ghufran/.claude-code-router/config.json
with access token from 
/Users/ghufran/.qwen/oauth_creds.json
```

## Start CCR Router
Run this command
```
ccr start
```

Leave this terminal open

## Start Claude Code (using Qwen)
Open a new terminal and run command
```
ccr code
```
