Install nvm. Foundry runs on node, a type of javascript. We’re going to install the Node Version Manager to handle all of the node stuff for us.

`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash`

then

`source ~/.bashrc`

Ensure nvm is installed:

`command -v nvm should output nvm`

Install the latest version of node:

`nvm install node`

Ensure node is installed:

`node --version`
