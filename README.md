This is my personal bash and neovim setup. 
Feel free to use it aswell.

#Git autocompleteion:
In .bashrc on line 109, there is a source of the __git_complete. This has to be included in your .bashrc, if it complains of __git_complete does not exist.
This error happens because the use of __git_complete happens before the git autocomplete file has been sourced.

#TODO:
- Make neovim installation automatic
    - each part (vim and bash) should be optional

optional tools: <br>
npm install -g typescript-language-server typescript <br>
sudo apt install ranger <br>
pip install tldr <br>

lazygit:
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | \grep -Po '"tag_name": *"v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/download/v${LAZYGIT_VERSION}/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit -D -t /usr/local/bin/
