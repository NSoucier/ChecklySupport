# Checkly Monitoring-as-code: Customer CLI Boilerplate

## About this repository 
This repository contains a working example of the Checkly CLI. It contains a folder titled `__checks__` where all of the API Checks and Playwright-powered Browser Checks live. This repository shows how you can use the Checkly CLI in a monitoring as code (MaC) workflow. We are using the https://checklyhq.com website as a monitoring target.

## Run locally

Install dependencies:

```bash
npm install
```

Login to your personal Checkly account:

```bash
npx checkly login
```

Write new API Checks and Playwright-powered Browser Checks in the `__checks__` folder.

Optionally, export checks from your Checkly account and add to the `__checks__` folder. This can be done by following steps below:
- Navigate to your account home.
- Click on the vertical ellipsis of your desired check.
- Click “Export to code”, then the “Download all files” button near the bottom of the pop up.
- Move this downloaded file to the previously created `__checks__` folder where your other tests live.


Run the command below to execute your tests. This  will look for `.check.js` and `.spec.js` files in the `__checks__` directory and execute them.

```bash
npx checkly test
```
  
Run the command below to deploy your checks to your Checkly account, attach alert channels, and run them on a 10 minute schedule. Now you have your app monitored around the clock. Navigate to your Checkly account home page to view all of your tests. 

```bash
npx checkly deploy
```

## Adding email alerts
To receive emails when your checks fail, please navigate to the alerts section in your Checkly account, or follow this link: https://app.checklyhq.com/alerts/settings/channels/new/email

## Integrating checks to your CI/CD pipeline
Depending on your preferred platform, please click on the corresponding link below to view step-by-step instructions to integrate Checkly into your CI/CD pipeline:
- Overview of Checkly integration: https://www.checklyhq.com/docs/cicd/
- GitHub Actions: https://www.checklyhq.com/docs/cicd/github-actions/
- Jenkins: https://www.checklyhq.com/docs/cicd/jenkins/
- GitLab CI: https://www.checklyhq.com/docs/cicd/gitlabci/
- Vercel: https://www.checklyhq.com/docs/cicd/vercel/
- GitHub deployments: https://www.checklyhq.com/docs/cicd/github/

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
| `npx checkly login`  | Log in to your Checkly account                   |
| `npx checkly test`   | Dry run all the checks in your project           |
| `npx checkly deploy` | Deploy your checks to the Checkly cloud          |
| `npx checkly --help` | Show help for each command.                      |

[Check the docs for the full CLI reference](https://www.checklyhq.com/docs/cli/command-line-reference/).

## Questions?

Check [our CLI docs](https://www.checklyhq.com/docs/cli/), the [main Checkly docs](https://checklyhq.com/docs) or 
join our [Slack community](https://checklyhq.com/slack).
For additional questions or clarification, please reach out to me via email at name@email.com.
# ChecklySupport
