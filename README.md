# Checkly Monitoring-as-code: Customer CLI Boilerplate

## About this repository 
This repository contains a working example of the Checkly CLI. It contains a folder titled __checks__ where all of the playwright tests and Checkly checks live. This example project shows how you can use the Checkly CLI in a monitoring as code (MaC) workflow. We are using the https://checklyhq.com website as a monitoring target.

## Run locally

Install dependencies:

```bash
npm install
```

Login to your personal account:

```bash
npm checkly login
```

Write new API Checks and Playwright-powered Browser Checks in the `__checks__` folder.

Optionally, export tests from your Checkly account and add to the `__checks__` folder.

- Running `npx checkly test` will look for `.check.js` files and `.spec.js` in `__checks__` directories and execute them.
  
- Running `npx checkly deploy` will deploy your checks to your Checkly account, attach alert channels, and run them on a 10m schedule. Now you have your app monitored around the clock.

## Adding email alerts
email alerts

## Integrating checks to your CI pipeline
CI pipeline integration

## Project Structure

This project has the basic boilerplate files needed to get you started.

```
.
├── README.md
├── __checks__
│   ├── api.check.js
│   └── homepage.spec.js
├── checkly.config.js
└── package.json
```

## CLI Commands

Run the core CLI commands with `npx checkly <command>` 

| Command              | Action                                           |
|:---------------------|:-------------------------------------------------|
| `npx checkly test`   | Dry run all the checks in your project           |
| `npx checkly deploy` | Deploy your checks to the Checkly cloud          |
| `npx checkly login`  | Log in to your Checkly account                   |
| `npx checkly --help` | Show help for each command.                      |

[Check the docs for the full CLI reference](https://www.checklyhq.com/docs/cli/command-line-reference/).

## Questions?

Check [our CLI docs](https://www.checklyhq.com/docs/cli/), the [main Checkly docs](https://checklyhq.com/docs) or 
join our [Slack community](https://checklyhq.com/slack).
For additional questions or clarification, please reach out to me via email at name@email.com.
# ChecklySupport
