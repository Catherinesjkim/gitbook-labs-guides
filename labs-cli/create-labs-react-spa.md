# Create a Labs React SPA

The React SPA generator is used by the [Labs CLI](https://github.com/Lambda-School-Labs/gitbook-labs-guides/tree/99d50db2598c8781016ceb9b1449fd8d3338d396/labs-cli/cli-basics/README.md) to generate greenfield SPA applications or add components.

## Installation

The Labs React SPA generator is installed as a dependancy for the labs CLI, which is a nodejs application and can be installed with the following command:

`npm i -g @lambdalabs/labs`

Running this command will install the following npmjs module and all associated Labs generators that have been published:

[@lambdalabs/labs](https://www.npmjs.com/package/@lambdalabs/labs)

To see all the arguments and options visit the npmjs site for [Labs SPA Generator](https://www.npmjs.com/package/@lambdalabs/generator-spa)

## Create app from the CLI

Now lets create a new application entirely from the CLI. This app will use the following info:

* \[Arg\] Project Name: `LabsPT12-ExpressGroomer-Team-C`
  * this should be the Labs team name
* \[Opt\] Program: `Labs`
* \[Opt\] Team has DS team members: `No`
* \[Opt\] github repo url: `https://github.com/LambdaLabs/labspt12-expressgroomer-team-c-fe.git`
  * this should be the same url you would clone from

Now lets plug that info into the `labs` CLI command:

`labs @lambdalabs/spa LabsPT12-ExpressGroomer-Team-C --program=labs --hasDS=false --repoUrl=https://github.com/LambdaLabs/labspt12-expressgroomer-team-c-fe.git`

All [options](https://www.npmjs.com/package/@lambdalabs/generator-spa#prompts--options) have been statisfied so the `labs` CLI will start working doing the following work:

* generate Labs SPA folder structure
* generate Labs SPA files for CRA app, page component examples and other

  utility modules/components.

* Update the package.json with Labs approved base config and libraries
* run `npm install`
* Initialize git repo
  * `git init`
  * rename the default branch to `main`
  * make initial commit
  * add github url as remote `origin`
  * push repo to github

Phew 😅, that's a lot.

## Same outcome, different UX

So now lets try creating the same app using the Prompts UX:

We'll use the same info as above except for the following:

* \[Arg\] Project Name: `LabsPT12-ExpressGroomer-Team-B`
* \[Opt\] github repo url: `https://github.com/LambdaLabs/labspt12-expressgroomer-team-b-fe.git`

So lets run the `labs` CLI.

`labs @lambdalabs/spa LabsPT12-ExpressGroomer-Team-B`

You will now need to answer the following prompts:

![Labs CLI Prompt UX](../.gitbook/assets/labs-cli-spa-prompt-1.png)

Choose `Labs` which should be highlighted by default. This will set the `--program` option. Onto the next prompt.

![Labs CLI Prompt UX](../.gitbook/assets/labs-cli-spa-prompt-2.png)

Answer `n` or `no` to set the `--hasDS` option as false.

![Labs CLI Prompt UX](../.gitbook/assets/labs-cli-spa-prompt-3.png)

Here we enter the entire `git` url to the repo. It should end with a `.git`

And away we go. The CLI should now be taking the exact same actions as mentioned above.

