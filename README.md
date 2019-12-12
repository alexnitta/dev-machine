# dev-machine
How I like to set up my computer for software development in JavaScript and Python

## Mac OS Applications
* [Chrome](https://www.google.com/chrome/browser/desktop/)
  * Use [Sign In to Chrome](https://www.google.com/chrome/browser/signin.html) when you set up Chrome for the first time. Next time you need to set up a new machine, install Chrome and sign in, and your extensions and preferences will automatically sync up.
  * [Vimium](https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=en)
    * In Chrome, click Chrome > Preferences > Extensions, then scroll to Vimium and click Options.
      * Make sure `https?://mail.google.com/*` is listed in Excluded URLs and keys so that Vimium is disabled in Gmail.
      * Click Show Advanced Options at the bottom of the screen. Find the field titled 'Characters used for link hints' and remove the `f` character to avoid accidentally hitting a link after you invoke Vimium (by typing `f`). Click Save Options at the bottom of the screen.
  * [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en)
  * [React DevTools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
  * [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en)
  * [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=en)
* [Visual Studio Code](https://code.visualstudio.com/)
  * Install [Setting Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) extension and sync all other settings from GitHub gist. In the Extensions marketplace, search for the `shan.code-settings-sync` identifier.
* [iTerm 2](https://www.iterm2.com/)
  * Set preferences: Profiles > Default > Colors > Color Presets... Pastel (Dark Background)
  * Add [Shell Integration](https://iterm2.com/documentation-shell-integration.html)
* [p4Merge](https://www.perforce.com/downloads/visual-merge-tool)
  * Follow instructions here, under **External Merge and Diff Tools**: [Customizing Git: Git Configuration](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)
  * Note that you may need to `sudo chmod +x /usr/local/bin/extMerge` and `sudo chmod +x /usr/local/bin/extDiff`
* [XCode](https://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12)
* [Cyberduck](https://cyberduck.io/?l=en)


## Command Line Utilities
* Git
  * Use the GUI to [install Git](https://git-scm.com/download/mac)
  * Copy from this repo at `config/dot-gitconfig`. Open `~/.gitconfig` and paste the text. Replace `Your Name` and `your@email.com`, close and save the file.
* Homebrew
  * `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
* Node
  * `brew install node`
* NVM
  * See: [https://github.com/creationix/nvm](https://github.com/creationix/nvm)
  * Once you've installed NVM and Sublime Text 3, make sure to set a default alias so that Sublime uses NVM when launching Node: `nvm alias default v<version_number>`. This will help avoid issues where Sublime can't find your linters or lint configs, even if you installed them globally.
* Python
  * `brew install python libjpeg`
  * `export PATH=/usr/local/bin:/usr/local/share/python:$PATH`
  * `pip install --upgrade pip`
* Ruby
  * `brew install ruby`
  * `gem install nokogiri premailer`
* Less
  * `npm install less less-plugin-clean-css -g`
* Tmux
  * `brew install tmux`
* virtualenv
  * `pip install virtualenv`
* black - for automatically formatting Python code, like prettier.js
  * `pip install black` for the CLI
  * `pip install black[d]` for the local black server
* core-utils
  * `brew install coreutils` (includes gsplit for splitting files)

## Config Files

* Bash Profile
  * `cd ~` `touch .bash_profile`
  * Copy raw text from this repo at: `config/dot-bash_profile`
  * `nano .bash_profile`
  * `Command-V` `Ctrl-x` `Enter`
  * `source .bash_profile`

* Set up SSH key for GitHub
  * `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` (use a secure passphrase)
  * `eval "$(ssh-agent -s)"`
  * `ssh-add ~/.ssh/id_rsa`
  * [Add SSH Key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

* [Set up Keybase.io, GPG & Git to sign commits on GitHub](https://github.com/alexnitta/keybase-gpg-github)
