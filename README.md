# Repro for ElderJS + Sanity compatibility issue

I used the [ElderJS template](https://github.com/Elderjs/template/) as a base, installed `@sanity/client` and imported it from a Svelte component, `src/routes/home/Home.svelte`.

### Instructions

1. clone
2. `pnpm install` / `npm install` / `yarn install`
3. npm start
4. Open browser at `localhost:3000`
5. Your terminal should show this error:

```
TypeError [ERR_INVALID_ARG_TYPE]: The "superCtor" argument must be of type Function. Received type undefined
      at Object.inherits (util.js:146:11)
```

# Elder.js Template Project

<img src="https://img.shields.io/badge/dynamic/json?color=brightgreen&label=Node&query=engines.node&url=https%3A%2F%2Fraw.githubusercontent.com%2Felderjs%2Ftemplate%2Fmaster%2Fpackage.json" alt="node version" />

This is a project template for [Elder.js](https://elderguide.com/tech/elderjs/) apps. The template lives at https://github.com/elderjs/template and the Elder.js source is here: https://github.com/elderjs/elderjs

Here is a demo of the template: [https://elderjs.netlify.app/](https://elderjs.netlify.app/)

## Get started

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit Elderjs/template elderjs-app
cd elderjs-app
```

### Install the dependencies:

```bash
npm install # or just yarn
```

### Start Project:

```bash
npm start
```

Navigate to [localhost:3000](http://localhost:3000). You should see your app running.

### Development:

For development, we recommend running two separate terminals. One for the server and the other for rollup.

**Terminal 1**

```bash
npm run dev:server # `npm start` above starts a server, but doesn't rebuild your Svelte components on change.
```

**Terminal 2**

```bash
npm run dev:rollup # This rebuilds your svelte components on change.
```

Once you have these two terminals open, edit a component file in `src`, save it, and reload the page to see your changes.

### To Build HTML:

```bash
npm run build
```

This will build all of your html into the /public/ folder.

### What to Expect

- Nodemon is watching your files for changes. It will restart when it needs to.
- Rollup is watching your files for changes. It will restart when it needs to.
- If your `elder.config.js` has `@elderjs/plugin-browser-reload': {}` in it's plugins, your browser will automatically restart after the server restarts.
