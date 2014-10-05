# HTML Forms

### Form Submission – GET Request

URL encoding works as follows — the form data is separated from the URI by a “?”, each name/value pair is separated by “&”, and each name is separated from its value by a “=” (“unsafe” characters, e.g., “/” and “&”, are escaped).

### Form Submission – GET Request

- The GET method should be used when a form is idempotent (i.e., it does not cause side effects). E.g., if the form data is used to search a database, there are no side effects.
- You should not send sensitive data in a form using the GET method — the sensitive data will end up in the URL and anyone monitoring the network traffic can see it.
- The GET method should not be used if there is a large amount of form data, or if the form data contains non-ASCII characters or binary data.
- The GET method cannot be used if the form contains a file upload control — files cannot be passed in the URL.

### Form Submission – POST Request

- If the server-side processing associated with the form causes side effects, e.g., modification of a database, subscription to a service, etc., then the POST method should be used.
- Furthermore, if the form data is sensitive, the HTTPS protocol should be established, so that the form data will be encrypted in the message body before it is sent to the server.


### Form Submission Process

1. The user agent running in the browser identifies the successful controls, and builds a form data set — a sequence of control-name/current-value pairs for the successful controls.
2. The form data set is encoded by the user agent according to the content type specified in the enctype attribute of the form element.
    - application/x-www-form-urlencoded — this is the default, form data is encoded as name-value pairs.
    - multipart/form-data — form data is encoded as a message, with a separate part for each control.
    - text/plain — form data is encoded as plain text.
3. The user agent submits the encoded data set to the processing agent running on the server side using the HTTP protocol method specified by the action attribute in the form.


### Form Controls

- Form controls are specified using an input or select element that must appear in the content section of the form element, i.e., between the <form> and </form> tags.
- The name of a control is specified using the name attribute.
- A control has an initial value and a current value, both of which are character strings. The current value is first set to the initial value, but may change according to user supplied input.

### Form Controls – Buttons

- Button controls are specified using either the button element or the input element. The type attribute, which should always be specified (as different browsers have different defaults for the type), has three possible values:
    - submit – Causes the form to be submitted.
    - reset – Causes the form to be reset, i.e. all controls are assigned their initial values.
    - button – Creates a push button, that typically has a client-side script associated with it through the event attribute. When the button is pressed and released, the associated script is executed.
- With the input element, the type attribute may be specified as image.
- This creates a graphical submit button. The src attribute specifies the URL of the image file that will decorate the button.

### Form Controls – Checkboxes, Radio Buttons

- Checkboxes and radio buttons are specified using the input element.
- These are essentially “on/off” switches that can be toggled by the user.
- Several of these controls can share the same control name.
- A switch is “on” when the control element’s checked attribute is set.
- When a form is submitted, only the “on” checkbox and radio button controls are treated as successful.
- If several radio button controls share the same name, they are treated as mutually exclusive. I.e., when one is switched “on” all of the others with the same name are switched “off.”
- Multiple checkboxes with the same name may simultaneously be switched “on” in a form.