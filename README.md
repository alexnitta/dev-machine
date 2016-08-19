# dev-machine
How I like to set up my computer for software development

##Mac OS Applications
* [Chrome] (https://www.google.com/chrome/browser/desktop/)
  * [Vimium] (https://vimium.github.io/)
    * Disable Vimium on Gmail: In Chrome, click Chrome > Preferences > Extensions, then scroll to Vimium and click Options. Click Show Advanced Options at the bottom of the screen. Find the field titled 'Characters used for link hints' and remove the 'f' character to avoid accidentally hitting a link after you invoke Vimium. Click Save Options at the bottom of the screen.
* [Sublime Text 3] (https://www.sublimetext.com/3)
  * Install [Package Control] (https://packagecontrol.io/installation) for Sublime
  * Use Package Control to install the following:
    1. Charcoal theme
    2. SublimeLinter
    3. SublimeLinter-contrib-eslint 
    4. babel
  * Set Sublime preferences by copying from this repo at `config/preferences-sublime-settings`, then in Sublime go to Preferences / Settings - User, paste text and save file
  * After you have installed Node (see below), create a build system in Sublime for Node. Copy from this repo at `config/node.sublime-build`, then in Sublime go to Tools > Build System > New Build System, delete the default code, and paste the text. Close the file, and when asked whether you want to save, click Save. Rename the file to `Node.sublime-build`.
* [iTerm 2] (https://www.iterm2.com/) - Set preferences: Profiles > Default > Colors > Color Presets... Pastel (Dark Background)
* [XCode] (https://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12)

##Command Line Utilities
* Git  
  * Use the GUI to [install Git] (https://git-scm.com/download/mac)
  * Copy from this repo at `config/dot-gitconfig`. Open `~/.gitconfig` and paste the text. Replace `Your Name` and `your@email.com`, close and save the file.
* Homebrew 
  * `$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
* Node 
  * `brew install node`
* Python 
  * `$ brew install python libjpeg`
  * `$ export PATH=/usr/local/bin:/usr/local/share/python:$PATH`
* Ruby 
  * `$ brew install ruby`
  * `$ gem install nokogiri premailer`
* Less 
  * `$ npm install less less-plugin-clean-css -g`
* Tmux 
  * `$ brew install tmux`
* NVM 
  * `$ npm install -g nvm`
* virtualenv 
  * `pip install virtualenv`

##Config Files

* Bash Profile
  * `$ cd ~` `$ touch .bash_profile`
  * Copy raw text from this repo at: `config/dot-bash_profile`
  * `$ nano .bash_profile` 
  * `Command-V` `Ctrl-x` `Enter` 
  * `$ source .bash_profile`

* Set up `subl` command
  * `$ ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`

* Set up SSH key for GitHub
  * `$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` (use a secure passphrase)
  * `eval "$(ssh-agent -s)"`
  * `$ ssh-add ~/.ssh/id_rsa`
  * [Add SSH Key to your GitHub account] (https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

