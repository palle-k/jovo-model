# Jovo Model: Google Assistant

Learn how to turn the Jovo Model into a Conversational Actions model for Google Assistant.

* [Introduction](#introduction)
* [Using the Google Assistant Jovo Model with the Jovo CLI](#using-the-google-assistant-jovo-model-with-the-jovo-cli)
* [Using the Google Assistant Jovo Model npm Package](#using-the-google-assistant-jovo-model-npm-package)

## Introduction

Google Assistant Conversational Actions are a new way to build Google Actions that don't require [Dialogflow](./dialogflow.md) as NLU service. You can either manage the language models via API (what the [Jovo CLI](https://www.jovo.tech/marketplace/jovo-cli) is doing during deployment) or in the Actions Builder console, which offers a graphical user interface.

Learn more about the structure in the [official Conversational Actions documentation](https://developers.google.com/assistant/conversational/build/conversation?tool=sdk). The Jovo Model can be translated into this structure by using the [`jovo build` command](https://www.jovo.tech/marketplace/jovo-cli/build) ([see below](#using-the-google-assistant-jovo-model-with-the-jovo-cli)) or the npm package ([see below](#using-the-google-assistant-jovo-model-npm-package)).


## Using the Google Assistant Jovo Model with the Jovo CLI

By using the [`jovo build` command](https://www.jovo.tech/marketplace/jovo-cli/build), you can turn your Jovo Model files in the `models` folder in your Jovo project into Conversational Action specific files.

Make sure that you remove the `dialogflow` part in your `project.js` file. There is no need to specify an `nlu` as the built-in service is used.

```javascript
// Before
googleAction: {
    nlu: 'dialogflow',
  },

// After
googleAction: {
  },
```

After successfully running `jovo build`, you can find the files inside the `platforms/googleAction` folder.

## Using the Google Assistant Jovo Model npm Package

Install the package like this:

```sh
$ npm install jovo-model-google --save
```

You can learn more about all the Jovo Model features here: [Using the Jovo Model npm Packages](http://jovo.tech/marketplace/jovo-model#using-the-jovo-model-npm-packages).