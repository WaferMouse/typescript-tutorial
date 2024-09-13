# typescript-tutorial

As we are going to be moving our codebase to TypeScript, it's important that everyone understands how to begin a TypeScript project.

## Starting the project

To begin, open VS Code and open a new folder as a project. Now run the following command in your terminal to initialize a node project:

```shell
npm init
```

You'll also need to install TypeScript:

```shell
npm install -g typescript
```

Now you'll need to create some files and folders. You want to recreate the following structure. `package.json` will already exist, we'll deal with that in a moment.

```
.
├── src
│   └── main.ts
├── package.json
└── tsconfig.json
```

## Configuring

Now edit package.json. You'll need to add the `dev` script, as well as the `devDependencies` block as below. You'll also have to edit `main`:

```json
{
  "name": "tstut",
  "version": "1.0.0",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "node src/main.js"
  },
  "devDependencies": {
    "typescript": "^5.5.3",
    "typescript-eslint": "^8.0.1"
  },
  "author": "",
  "license": "ISC",
  "description": ""
}
```

Now you want to paste the following into `tsconfig.json`. This sets up a TypeScript project.

```json
{
    "compilerOptions": {
        "target": "es6"
    }
}
```

## Hello, World!

Now, paste the following Hello World into `main.ts`:

```ts
let message: string = 'Hello, World!';

console.log(message);
```

## Compilation

We're ready to compile! Because we already setup `tsconfig.json`, compiling is as easy as:

```shell
tsc
```

You'll now have a `main.js` in your `src` directory. That contains the JavaScript code that was generated from your TypeScript! Let's run it in the terminal:

```shell
npm run dev
```

Amazing! You have a project setup to begin experimenting with TypeScript.

## Further work

Now it's time to experiment. You already know JavaScript, so we won't teach you how to code, but we will point out a few useful resources:

[TypeScript for JavaScript Programmers](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)

[TypeScript Cheat Sheets](https://www.typescriptlang.org/cheatsheets/)

Where you go from here is up to you!

🐟
