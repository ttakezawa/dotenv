# dotenv
Eval an env file and execute a command. This script is implemented by bash, so it can expand a shell-format expression of the form `$VARIABLE`, `${VARIABLE}` or `$(command-list)`.

# Install

Fetch the script, chmod +x dotenv and put it somewhere in your PATH.

For example:

```sh
sudo curl -o /usr/local/bin/dotenv -L https://raw.githubusercontent.com/ttakezawa/dotenv/master/dotenv && sudo chmod +x /usr/local/bin/dotenv
```

# Usage

Create your env file.

Example env file:

```sh
VAR1=Hello
VAR2=${USER}
VAR3=$(ls | wc -l)
```

Use dotenv.

```sh
dotenv .env sh -c 'echo "$VAR1 $VAR2. Current directory has $VAR3 entries."'
```
