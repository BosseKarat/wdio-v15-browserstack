# wdio-browserstack

* install dependecies

* To run test: npm run wdio


# Steps to reproduce the issue

Every version below 9.14.0 is working. 

    "@wdio/browserstack-service": "^9.14.0",
    "@wdio/cli": "^9.14.0",
    "@wdio/local-runner": "^9.14.0",
    "@wdio/mocha-framework": "^9.14.0",
    "@wdio/spec-reporter": "^9.14.0",
    "undici": "^7.10.0"

If these versions are installed instead:

    "@wdio/browserstack-service": "^9.15.0",
    "@wdio/cli": "^9.15.0",
    "@wdio/local-runner": "^9.15.0",
    "@wdio/mocha-framework": "^9.15.0",
    "@wdio/spec-reporter": "^9.15.0",
    "undici": "^7.10.0"

Running your tests using Browserstack will not work and the error below is displayed. The ECONNRESET error indicates that the connection was forcibly closed by the remote server. This could be a problem related to me using a VPN. I am unable to test this without using a VPN so it would be greatly appreciated if debugging is done with that in mind. 

PR:https://github.com/webdriverio/webdriverio/pull/14493
or 
PR:https://github.com/webdriverio/webdriverio/pull/13938

ERROR @wdio/runner: Error: WebDriverError: Request failed with error code ECONNRESET when running "https://hub-cloud.browserstack.com/wd/hub/session" with method "POST" and args "{"capabilities":{"alwaysMatch":{"bstack:options":{"os":"Windows","osVersion":"10","projectName":"ProjectName","buildName":"BuildName + 2025-06-02T19:37:50.237Z","sessionName":"SessionName","seleniumVersion":"4.20.0","debug":"true","networkLogs":"true","consoleLogs":"verbose","wdioService":"9.14.0","testhubBuildUuid":"w2r1zeonfgfkv5s6jglfha1vvyxtronsablkhwtk","buildProductMap":{"observability":true,"accessibility":null,"percy":false,"automate":true,"app_automate":false}},"browserName":"chrome","browserVersion":"latest","webSocketUrl":true,"unhandledPromptBehavior":"ignore"},"firstMatch":[{}]}}"