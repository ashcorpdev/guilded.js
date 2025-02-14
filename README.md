<div align="center">
    <img src="https://raw.githubusercontent.com/guildedjs/guilded.js-next/main/static/readme-header.png" width="546" alt="guildedjs"/>
    <p><b>Tools for interacting with the official <a href="https://www.guilded.gg/">Guilded.gg</a> API.</b></p>  
    <br />
    <p>
        <a href="https://www.guilded.gg/i/k1ber4Jp"><img src="https://shields.yoki-labs.xyz/shields/i/k1ber4Jp?style=flat"></a>
        <img src="https://github.com/guildedjs/guilded.js/actions/workflows/ci.yml/badge.svg" alt="CI">
        <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a><br>
    </p>
</div>

## 📝 About

This repo serves as a monorepo that houses several packages, mainly the `guilded.js` package, which is a library for the Guilded API.

## 📦 Packages

-   `guilded.js` (**[GitHub](https://github.com/guildedjs/guilded.js/tree/main/packages/guilded.js#readme), [NPM](https://www.npmjs.com/package/guilded.js)**) - Main library that ties everything together. Has additional logic for caching.
-   `@guildedjs/gil` (**[GitHub](https://github.com/guildedjs/guilded.js/tree/main/packages/gil#readme), [NPM](https://www.npmjs.com/package/@guildedjs/gil)**) - Framework allowing you to build bots with ease.
-   `@guildedjs/guilded-api-types` (**[GitHub](https://github.com/guildedjs/guilded.js/tree/main/packages/guilded-api-typings#readme), [NPM](https://www.npmjs.com/package/@guildedjs/guilded-api-typings)**) - Interfacing directly with the API without using `guilded.js`? This package provides typings covering the entire API.
-   `@guildedjs/webhook-client` (**[GitHub](https://github.com/guildedjs/guilded.js/tree/main/packages/webhook-client#readme), [NPM](https://www.npmjs.com/package/@guildedjs/webhook-client)**) - Library agnostic client for interacting with webhooks.
-   `@guildedjs/rest` (**[GitHub](https://github.com/guildedjs/guilded.js/tree/main/packages/rest#readme), [NPM](https://www.npmjs.com/package/@guildedjs/rest)**) - Utility for making REST requests to the Guilded API. Includes ratelimit handling.
-   `@guildedjs/ws` (**[GitHub](https://github.com/guildedjs/guilded.js/tree/main/packages/ws#readme), [NPM](https://www.npmjs.com/package/@guildedjs/ws)**) - Utility for connecting to Guilded's WebSocket gateway and receiving events.

## 📥 Installation

<a href="https://npmjs.org/package/guilded.js"><img src="https://nodei.co/npm/guilded.js.png" alt="NPM"></a>

**Recommended that you use node v12+**

-   `npm install guilded.js`
-   `yarn add guilded.js`

## ⚡ Usage

You can find extra examples [here](https://github.com/guildedjs/examples/tree/main/examples)

```ts
const { Client } = require("guilded.js");
// import { Client } from "guilded.js";
const client = new Client({ token: "TOKEN_HERE" });

client.on("ready", () => console.log(`Bot is successfully logged in`));
client.on("messageCreated", (message) => {
    if (message.content === "test") {
        return message.reply("test indeed");
    }
});

client.login();
```

## 📃 Documentation

Documentation is viewable here: https://guilded.js.org

<!--END GETTING STARTED-->

## ✋ Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

We make use of [PNPM](https://pnpm.io/) and [Changeset](https://github.com/changesets/changesets) to manage our monorepo. It's recommended that if you plan on contributing, you use these tools.

Please run `pnpm install -r` in your local environment to properly locally symlink all the packages that depend on each other.

Please ensure your commits pass the test, lint, and build scripts.

## 🤝 Acknowledgements

[Discord.js](https://github.com/discordjs/discord.js) - Inspiration & derived work.

## ⚖️ LICENSING

> **Guilded.JS** © [zaida04](https://github.com/zaida04). All packages released under [MIT](https://github.com/guildedjs/guilded.js/blob/main/LICENSE).

Maintained by: [zaida04](https://github.com/zaida04), [Skillz4Killz](https://github.com/Skillz4Killz), [Uhuh](https://github.com/Uhuh), and [DaStormer](https://github.com/DaStormer)
