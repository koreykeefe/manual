# Setting up a Ruby Environment on Ubuntu using rbenv

Tested and working as of 2/17/2022 on Ubuntu 22.04.1.

1. Update package information.
    
    ```bash
    sudo apt update
    ```

2. Install dependencies.
    
    ```bash
    sudo apt -y install git autoconf bison patch build-essential rustc libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libgmp-dev libncurses5-dev libffi-dev libgdbm6 libgdbm-dev libdb-dev uuid-dev
    ```

3. Clone rbenv into `~/.rbenv`.
    
    ```bash
    git clone https://github.com/rbenv/rbenv.git ~/.rbenv
    ```

4. Configure your shell to load rbenv. This command will close your shell session. This is required for the shell to load rbenv.
    
    ```bash
    echo 'eval "$(~/.rbenv/bin/rbenv init - bash)"' >> ~/.bashrc && exit
    ```

5. Clone ruby-build as an rbenv plugin.
    
    ```bash
    git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
    ```

6. Install the desired version of Ruby and set it globally.
    
    ```bash
    rbenv install 3.2.1 && rbenv global 3.2.1
    ```

7. Install the desired version of Rails. You do not need to do this step if you already have a Gemfile (i.e. the source code) since `bundle install` will download the required version of Rails for you.
    
    ```bash
    gem install rails -v 7.0.4.2
    ```

For more information, see the documentation: [rbenv](https://github.com/rbenv/rbenv#readme), [ruby-build](https://github.com/rbenv/ruby-build)
