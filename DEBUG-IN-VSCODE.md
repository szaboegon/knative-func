# Debugging in VS Code

## Setup

1. Create a launch configuration file in the `.vscode` foler named `launch.json`
2. Copy the following into the file:

```
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Create",
      "type": "go",
      "request": "launch",
      "mode": "exec",
      "program": "${workspaceRoot}/func.exe",
      "args": ["create", "-l", "go", "../temp/test-gofunc"]
    },
    {
      "name": "Deploy",
      "type": "go",
      "request": "launch",
      "mode": "exec",
      "program": "${workspaceRoot}/func.exe",
      "args": ["d", "-p", "../temp/test-gofunc"]
    }
  ]
}
```

You can add configurations like this for all commands you want to debug

## Start debugging

1. Run `make build` to rebuid the `func.exe` binary in the root of the project

2. Put breakpoints in your code

3. Go to the Run and Debug tab and start the debug config for the command you would like to run
