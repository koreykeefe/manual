# Install NVM, Node, and Angular CLI on Ubuntu

```shell
sudo apt install curl
```

```shell
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
```

Close and reopen the terminal for NVM to take effect!

```shell
nvm install --lts
```

The latest LTS version of Node is recommended

> To install a specific version of Node
> 
> ```shell
> nvm install <version>
> ```

```shell
nvm use <version>
```

```shell
npm install @angular/cli
```

> To install a specific version of Angular
> 
> ```shell
> npm install @angular/cli@<version>
> ```
