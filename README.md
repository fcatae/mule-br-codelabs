# MuleSoft Codelabs Template Site

This is the base template for a MuleSoft Codelabs site. You can use this site to host a collection of Codelabs for a customer or custom workshop. Before you get started, you'll need to make sure your environment is setup. You can follow the Codelab [here](https://mulesoft-codelabs.herokuapp.com/codelabs/codelab-setup/index.html?index=..%2F..index#0) on how to get started.

## Requirements

1. [Go](https://mulesoft-codelabs.herokuapp.com/codelabs/codelab-setup/index.html?index=..%2F..index#1)
1. [Node.js and NPM](https://mulesoft-codelabs.herokuapp.com/codelabs/codelab-setup/index.html?index=..%2F..index#2)
1. [Google Codelabs as a Thing Tool](https://mulesoft-codelabs.herokuapp.com/codelabs/codelab-setup/index.html?index=..%2F..index#3)

## Setup

```

# Clone project
git clone https://github.com/djuang1/codelabs-template.git && cd codelabs-template

# Install Node modules
npm install

```

## Add Codelabs

```

# Open codelabs folder and build Codelabs page from Google Doc ID 
cd codelabs
claat export <Google Doc ID>

```

## Test

```

# Compile and host a local instance of the site that can be viewed at http://localhost:8000 
gulp serve

```

## Build

```

# Build static site pages into the  /dist folder 
gulp dist

```

# Credentials

Authorization Endpoint:

```
https://accounts.google.com/o/oauth2/auth?access_type=offline
  &client_id=<client-id>
  &redirect_uri=<redirect-url>
  &response_type=code
  &scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fdrive.readonly
  &state=unused
```

###
POST https://oauth2.googleapis.com/token
Content-Type: application/x-www-form-urlencoded

grant_type=authorization_code
&client_id=<client-id>
&client_secret=<client-secret>
&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fdrive.readonly
&code=<code>
&redirect_uri=<redirect-url>
###

 
