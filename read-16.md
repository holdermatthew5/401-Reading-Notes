## Web Scraping

Web scraping is an action performed by code which gethers information from any website you choose. To do this we only need the requests module.
The information pulled must be altered to meet the needs of our app. To do this we have BeautifulSoup4.
BeautifulSoup4 can take in an unparsed html file make it human readable and extract information to be used in the app.
Every site has the right to ban web scrapers or just shut them down in order to keep their own site functioning properly, but most don't care. Check with the site terms and conditions and privacy policy to find whether they have any restrictions against scraping.
Web scraping starts at the website. the desired elements must be inspected to find what types of tags/classes/ids/etc we need to narrow our results down to. This can be done by finding the content you want onscreen, opening the elements page in the console, clicking on the arrow in a box icon at the top left of the console and finally clicking on the content you want. When hovered over the content should provide us with a brief summary of information about the element including any attributes and the element tag type.
Once we've found the content we want we only need to devise an algorithm that collects it.