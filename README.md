i# README
## This is the README for the vscode plugin for cornet
-------------------

This folder contains a VSCode extension that do BPMN checks for cornet. Currently, it does the following checks:

- very basic xml syntax check (via a modified version of node-htmlparser in BpmnCompiler)
- js lint check (via BpmnCompiler)
- basic bpmn rules check (via Engine.validate)


The code for the extension is in the 'client' folder. It uses the 'vscode-languageclient' node module to launch the language server.

The language server is located in the 'server' folder. 


# How to run locally
* `npm install` to initialize the extension and the server
* `npm run compile` to compile the extension and the server
* open the `cornet-vscode-lsp` folder in VS Code. In the Debug viewlet, run 'Launch Client' from drop-down to launch the extension and attach to the extension.
* create a file `test.txt`, and type `typescript`. You should see a validation error.
* to debug the server use the 'Attach to Server' launch config.
* set breakpoints in the client or the server.

# Warning or Error Message
| Message and Description  | 
| ------------------------ |
| **Message** Warning: [ex] Change process id to something meaningful [Process_1]<br> **Cause** Expect a more meaningful name for bpmn:process |
| **Message** Error: [ex] Cannot find processId (maybe not a BPMN file) <br> **Cause** `id` of bpmn:process should be set. The default value is Process_n. |
| **Message** Error: [ex] scriptFormat must be defined <br> **Cause** `Script Format` should be set for those section that type is `script`. Only `javascript` is supported for `Script Format`.
| **Message** Error: [ex] scriptFormat 'xscript' does not support <br> **Cause** Only `javascript` is supported for `Script Format`.

