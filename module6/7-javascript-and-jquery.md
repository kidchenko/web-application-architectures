# Javascript and jQuery

### Javascript and Browser security

- Client-side JavaScript opens up the possibility for authors to deliver malicious scripts to the browser
- Browser guard against this using two strategies
    - Javascript code is run in a sandbox that only allows web-related actions to be performed, not general-purpose programming task (no writing to disk, creating files, etc.)
    - Javascript code is constrained by the same origin policy - scripts from one website do not have access to information such as usernames, passwords, or cookies form other websites

### jQuery

- jQuery supports the notion of unobtrusive JavaScript – the separation of behavior from document structure. With unobtrusive JavaScript, you never embed any JavaScript expressions or statements within the body of an HTML document, either as attributes of HTML elements (such as onclick) or in script blocks
- The jQuery developers placed a high priority on ensuring that it worked consistently across all major browsers
- The focus in jQuery is on retrieving elements from HTML pages, and performing operation on them
- The returned elements are actually “wrapped” with additional functions (methods), and these elements are therefore referred to as the wrapped set. Available methods: **api.jquery.com**
- Many of the jQuery methods also return a wrapped set, so it’s
common to chain methods in jQuery
