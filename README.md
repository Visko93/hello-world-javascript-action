# Hello world javascript action

This action prints "Hello World" or "Hello" + the name of a person to greet to the log.
>pt - Essa é uma github action que imprime "Hello World" ou "Hello + nome fornecido" caso haja um input no log. 

## Inputs

### `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.
>**REQUIRED** Nome da pessoa que será cumprimentada

## Outputs

### `time`

The time we greeted you.
>O horário do ação.

---
## Build

```Bash
  # I used @zeit/ncc to build
  npm i -g @zeit/ncc

  ncc build index.js
  rm -rf node_modules && npm install

  git add action.yml dist/index.js node_modules/*
  git commit -m "Use zeit/ncc"
  git tag -a -m "My first action release" v1
  git push --follow-tags
 ```
[@zeit/ncc](https://github.com/vercel/ncc)
## Example usage

uses: actions/hello-world-javascript-action@v1.1
with:
  who-to-greet: 'Mona the Octocat'