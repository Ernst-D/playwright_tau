# 🎭 Playwright with JavaScript - Test Automation University
This repo contain all the examples in this course.

## Table of Contents

- ```Chapter 2``` Branch: Writing Your First Script
- ```Chapter 3``` Branch: Debugging and Tooling
- ```Chapter 4``` Branch: Element State 
- ```Chapter 5``` Branch: Managing a Virtual Keyboard
- ```Chapter 6``` Branch: Interacting with Mouse Events
- ```Chapter 7``` Branch: Taking a Screenshot  
- ```Chapter 8``` Branch: Recording videos
- ```Chapter 9``` Branch: Emulating a device
- ```Chapter 10``` Branch: Integration with Jest
- ```Chapter 11``` Branch: Visual Testing
- ```Chapter 12``` Branch: Playwright CLI
- ```Chapter 13``` Branch: Page Object Model


## - ```Chapter 2``` Branch: Writing Your First Script

TBA.

## - ```Chapter 3``` Branch: Interacting with Elements

Previously, we wrote our first Playwright-Test spec. It was simple, but even in a simple script something can go wrong. 

We need a thing which could help us to inspect every step of our test script.

There are **four** ways you can debug your tests:
   
1. Using JavaScript Debug Terminal: 
    
    Lets add new variable which will contain text content of title. 
    Then go to "Run and Debug" tab, open JS Debug Terminal, 
    put breakpoint on line with `expect` statement  and run script once more with `npx playwright test --project="chromium" --headed`. 
    When execution comes to the `expect` statement - debugger will stop program and you will be able to go through the code.

2. Using Playwright Inspector:
    
    Run your script with environment variable `PWDEBUG=1`. 
    
    Windows - `$env:PWDEBUG=1; npx playwright test --project="chromium" --headed`.

    Unix - `PWDEBUG=1 npx playwright test --project="chromium" --headed`. 

    With this variable, Playwright-CLI will open inpsector in the beggining and you will be able step over the code by clicking specific button (put screenshot here, I don't know).

3. Using Playwright TraceViewer:

    Edit playwright config: set `trace: "on"` property. Run script with `npx playwright test --project="chromium" --headed`. 
    After test run there will be folder `test-results` with `trace.zip`. Copy relative path to `trace.zip` and run `npx playwright show-trace`. Example: `npx playwright show-trace ./test-results/first-basic-test-chromium/trace.zip`. It will open TraceViewer where you can inspect the insights of your test.


4. Using [Web version of TraceViewer](https://trace.playwright.dev/). 

    The same as the local version, but you can drop `trace.zip` to web app. Useful when you need to show some insights to non-technical people or open CI results. 



# Resources

- https://playwright.dev/ 
- https://jestjs.io/
- https://applitools.com/blog/top-playwright-questions-answered/#:~:text=Playwright%20is%20a%20relatively%20new,testing%20for%20today's%20web%20apps
- https://applitools.com/
- https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing 
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions
- https://www.selenium.dev/documentation/en/guidelines_and_recommendations/page_object_models/
- https://github.com/microsoft/playwright#-playwright
