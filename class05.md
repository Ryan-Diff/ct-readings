## Web Scraping JavaScript (https://www.scrapingbee.com/blog/web-scraping-javascript/)
* Request, Axios, and Superagent are examples of HTTP clients that work with node and JS
* You will need something to interpret the results of the data you scrape, and doing it manually can be tough. An HTML parser can help if you use regular expressions to look for a match. 
* Cheerio is a light weight and efficient library that uses JQuery on the server. It will not run css, javascript or render any dom elements.
* You might use Cheerio to fetch the dom element, then use text() to get the text
* JSDOM (npm install jsdom axios) can be used to interact with websites automatically and do things like click and manipulate the DOM, this can create a bot that goes around interacting with web sites.
* Puppeteer (npm install puppeteer) is a hight level API that controls a headless version of chrome. It can take screenshots or generate PDFs of pages, generate pre-rendered content, or automate user interactions (keyboard inputs, form submissions, navigation, etc)
* Nightmare (install nightmare) is another option for a high level browser automation
* To scrape and not get blocked you need to look more like a user to the target and less like a robot.
* The first thing to watch out for is the headers on your request.
* One option is to use a headless version of chrome, this will behave exactly like the browser. Selenium and Puppeteer are the two most common drivers for Headless Chrome
* Transport Layer Security (TLS) can give you away, you need to copy variables that are used typically in a given combination
* You also need to emulate human behavior with proxy servers making multiple fast requests to come from different locations. The TOR network hides traffic well, but is often blocked or slow due to the rerouting it does. 
* Captchas might need to be solved with something like 2Captchas or DeathByCaptchas
* Requesting certain patterns or at certain rates can raise automated suspicion to your scraping

## MDN - QuerySelector
* querySelector() returns the first element that matches the specified selector.
* Syntax: element = document.querySelector(selectors);
* The selectors must be a valid CSS selector string
* The match returns as an object

## MDN - QuerySelectorAll
* querySelectorAll() returns an static array of all the elements that match the specific selector.
* Syntax: elementList = parentNode.querySelectorAll(selectors);
* The selectors must be a valid CSS selector string
* The matches can be accessed like an array
