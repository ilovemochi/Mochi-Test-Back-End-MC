<h1 align="center">
    <img alt="logo Mochi" src="logo-purplehorizontal.png" />
    <br>
    Mochi Aptitude Test
    <br>
</h1>

<h4 align="center">
Welcome to your aptitude test
</h4>
<p align="center">
&nbsp;&nbsp;
  <a href="#test-objective">Test objective</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#how-use">How use</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#information_source-how-to-use">How test</a>&nbsp;&nbsp;
</p>

## :wrench: Test Objective

<p>
This test aims to measure the candidate's technical capabilities and find out if they are in accordance with the developer profile that Mochi is looking for.

Your object is the following
</p>

<br>

## :rocket: Technologies

You can use the following technologies to complete this test:

- [Node 14 (ES6+)](https://nodejs.org/en/)
- [VS Code][vc] and [ESLint][vceslint]
- [Typescript](https://www.typescriptlang.org/)
- [AWS](https://aws.amazon.com/)
  - [DynamoDB](https://aws.amazon.com/dynamodb/?nc2=type_a)
  - [Lambda](https://aws.amazon.com/lambda/?nc2=type_a)
  - [SES](https://aws.amazon.com/ses/)
  - [SQS](https://aws.amazon.com/sqs/)
  - [S3](https://aws.amazon.com/s3/)
  - [API Gateway](https://aws.amazon.com/api-gateway/)
  - [Auth0](https://auth0.com/partners/amazon-web-services)
  

# To make a commit must be used a following rule:

`git commit -m "*type*: commit-message"`

- Where type is: [ `build`, `chore`, `ci`, `docs`, `feat`, `fix`, `perf`, `refactor`, `revert`, `style`, `test` ]
- And commit-message must be written in lower-case.

## Coding Conventions

- All other Interfaces should be CamelCase version of the name of the function or object
- Only add the prefix I if there is no other Choice
  - e.g - Function `addStyles() => {}`
  - e.g - Interface `interface AddStyles {}`
- Do not use the type any, opt for unknown.
- Limit the use of classes but instead opt for pure single purpose functions.
- Rely on composability to deal with complexity
- Prefer Async/Await syntax over .chain with then.catch
- Rely on utility functions by ramda for immutability, composability and clarity
- Immutability

  ```ts
  // BAD PRACTICE
  // Mutates the object
  const obj = { removeMe: '😭', keepMe: '😊' };
  obj.removeMe = null;
  delete obj.removeMe;
  // obj === { keepMe: '😊' }

  // BETTER BUT NOT IDEAL
  // Immutable but not declarative
  // Pollutes the execution context with variable key
  const objTwo = { removeMe: '😭', keepMe: '😊' };
  const { removeMe, ...updatedObj } = objTwo;
  // objTwo === { removeMe: '😭', keepMe: '😊' }
  // updatedObj = { keepMe: '😊' }

  // IDEAL
  // Immutable and declarative
  const objThree = { removeMe: '😭', keepMe: '😊' };
  const removeKey = R.omit(['removeMe']);
  const updatedObjTwo = removeKey(objThree);
  // objThree === { removeMe: '😭', keepMe: '😊' }
  // updatedObjTwo = { keepMe: '😊' }
  ```

- Pure single purpose functions
- Composability

## :warning: Requisites

## :information_source: How To Use

```bash
#  Fork & Clone this repository
$ git clone https://github.com/Nicasiomarques/mochi-test

# Go into the repository
$ cd mochi-test

```

## All Rights Reserved for Mochi Noir, LDA

[nodejs]: https://nodejs.org/
[vc]: https://code.visualstudio.com/
[vceditconfig]: https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig
[vceslint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
