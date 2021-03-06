# Install Ruby on Linux


You need to do all the following steps in a Terminal. If you don't know
how to open a Terminal, please ask an instructor to show you.

If you run into errors at any step please call in an
instructor to help diagnose the installation issue.

1. Install git, wget, and some other dependencies. These steps may take
   a while.

    For Ubuntu or Linux Mint:

    ```text
    sudo apt-get update  
    sudo apt-get install -y git wget zlib1g-dev libssl-dev libreadline-dev sqlite3 libsqlite3-dev
    ```

    For Fedora:

    ```text
    sudo yum update   
    sudo yum install -y git wget zlib1g-dev libssl-dev libreadline-dev sqlite3 libsqlite3-dev
    ```

2. Check out rbenv into `~/.rbenv`.

    ```text
    cd
    git clone git://github.com/sstephenson/rbenv.git .rbenv
    ```

3. Add `~/.rbenv/bin` to your `$PATH` for access to the `rbenv`
   command-line utility.

    ```text
    echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
    ```

    **Linux Mint and Ubuntu 10.10**: Modify your `~/.bashrc` file instead of `~/.bash_profile`.  
    **Zsh**: Modify your `~/.zshenv` file instead of `~/.bash_profile`.

4. Add rbenv init to your shell to enable shims and autocompletion.

    ```text
    echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
    ```

    **Linux Mint and Ubuntu 10.10**: Modify your `~/.bashrc` file instead of `~/.bash_profile`.  
    **Zsh**: Modify your `~/.zshenv` file instead of `~/.bash_profile`.

5. Restart your shell so the path changes take effect. You can now begin using rbenv.

    ```text
    exec $SHELL
    ```

6. Install ruby-build.

    ```text
    mkdir -p ~/.rbenv/plugins
    cd ~/.rbenv/plugins
    git clone git://github.com/sstephenson/ruby-build.git
    source ~/.bash_profile
    ```

7. Install the latest Ruby. This may take a while.

    ```text
    rbenv install 1.9.3-p194
    ```

8. You should do this any time you install
   different version of Ruby or a Ruby gem that provides a command-line command. 

    ```text
    rbenv rehash
    ```

9. Set the global version of Ruby to be used in all shells.

    ```text
    rbenv global 1.9.3-p194
    rbenv shell 1.9.3-p194
    ```


10. Close an re-open your terminal and confirm Ruby is installed properly

    ```text
    ruby -v
    ```

    You should get something similar to `ruby 1.9.3p194 (2012-04-20
    revision 35410) [i616-linux]` If you see something different please
    call in an instructor to help diagnose the installation issue.

11. Install Rails and other supporting gems

    ```text
    gem install bundler rails heroku
    ```

Congratulations, you now have the Ruby development environment up and
running. Now go forth and do something awesome with it!



[« Back to Installfest](/ruby_from_scratch)

