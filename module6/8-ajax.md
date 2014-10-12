# AJAX

### What is Ajax

- Ajax was originally an acronym that stood for Asynchronous JavaScript and XML (AJAX).
- XMLHttpRequest (XHR) is an API available to the browser viaJavaScript. It’s used to send asynchronous HTTP requests to a web server and then load the server response data back into the script.
- In spite of the name, any text data can be retrieved from the server, not just XML. Nowadays, it’s common to retrieve JavaScript Object Notation (JSON), HTML, JavaScript or plain text data.

### Ajax, jQuery & Rails

- The jQuery library provides a full suite of Ajax capabilities (see: http://api.jquery.com/category/ajax/).
- The $.ajax() method is used to initiate an asynchronous HTTP (Ajax) request.
- An unobtrusive javascript adapter for jQuery, called jquery_ujs, is automatically provided in Rails. Using this adapter, forms and links that have the attribute: `data-remote="true"` will be submitted using jQuery’s ajax method, i.e., using $.ajax(). In Rails, you set this attribute using `remote :true` Ex.

```ruby
<%= form_for([@post, Comment.new], remote: true) do |f| %>
```