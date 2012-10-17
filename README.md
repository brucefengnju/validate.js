# validate.js

validate.js is a lightweight JavaScript form validation library inspired by CodeIgniter.

## Features

- Validate form fields from over a dozen rules
- No dependencies
- Customizable Messages
- Supply your own validation callbacks for custom rules
- Chainable customization methods for ease of declaration
- Works in all major browsers, (even IE6!)
- Modeled off the CodeIgniter form validation API
- Set the validate event

## How to use

    var validator = new FormValidator('example_form', [{
        name: 'req',
        display: 'required',    
        rules: 'required',
        event:'focus'
    }, {
        name: 'alphanumeric',
        rules: 'alpha_numeric',
        event:'focus'
    }, {
        name: 'password',
        rules: 'required'
    }, {
        name: 'password_confirm',
        display: 'password confirmation',
        rules: 'required|matches[password]'
    }, {
        name: 'email',
        rules: 'valid_email'
    }, {
        name: 'minlength',
        display: 'min length',
        rules: 'min_length[8]'
    }], function(errors) {
        if (errors.length > 0) {
            // Show the errors
        }
    });
	
	validator.setValidateEvent('click','req');
	
## Documentation

You can view everything at https://github.com/brucefengnju/validate.js

## Plugins

jQuery: https://github.com/mahil/validate_helper
