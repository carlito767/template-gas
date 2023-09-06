# template-gas

Template for Google Apps Script project.

## Tech stack

- [Docker](https://www.docker.com/)
- [Node.js](https://nodejs.org/)
- [pnpm](https://pnpm.io/)
- [clasp](https://github.com/google/clasp)
- [Jest](https://jestjs.io/)

## Develop with containers

- Install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Install [Visual Studio Code](https://code.visualstudio.com/)
- Install [Docker extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)
- Install [Dev Containers extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

See also:

- [Docker extension for Visual Studio Code](https://code.visualstudio.com/docs/containers/overview)
- [Developing inside a Container using Visual Studio Code Remote Development](https://code.visualstudio.com/docs/remote/containers)

## Clasp

- Enable the Google Apps Script API: https://script.google.com/home/usersettings

![Enable Apps Script API](https://user-images.githubusercontent.com/744973/54870967-a9135780-4d6a-11e9-991c-9f57a508bdf0.gif)

- Login:

```sh
clasp login
```

- Create **src** folder and create/clone your project:

```sh
mkdir src
clasp clone "1u-jqvFWtxsQE1Db_CqaWKc3jpDTXDWFFDUVOlloHlk0EmZ8MWtK3MJIk" --rootDir src
```

In this example **1u-jqvFWtxsQE1Db_CqaWKc3jpDTXDWFFDUVOlloHlk0EmZ8MWtK3MJIk** is script id.

- Push/Pull modications

```sh
clasp push
clasp pull
```
