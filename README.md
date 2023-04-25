# CustomValidation Prototype
This code defines a CustomValidation prototype that keeps track of the list of invalidity messages for an input and the validity checks needed for that input. It performs the validity checks and sends feedback to the front end.

The CustomValidation prototype contains several methods:

- addInvalidity: Adds an error message to the list of invalidities.
- getInvalidities: Returns all the invalidities joined by a period and a newline.
- checkValidity: Performs the validity checks for the input based on the validity checks array passed to it. If any check fails, it adds an invalidity message to the list of invalidities and updates the requirement element's class.
- checkInput: Calls checkValidity for the input node and sets its custom validity according to whether there are any invalidities.
- registerListener:  Registers a keyup event listener on the input node to call checkInput.

## Validity Checks
There are four arrays of validity checks, one for each input: usernameValidityChecks, passwordValidityChecks, passwordRepeatValidityChecks, and emailValidityChecks. Each array is comprised of three elements:

- isInvalid(): A function that determines if the input fulfills a particular requirement.
invalidityMessage: The error message to display if the field is invalid.
- element: The element that states the requirement.

## Setup CustomValidation
For each input, the code sets up a CustomValidation object with the corresponding validity checks array and registers a listener on the input node.

## Event Listeners
When the submit button or the form is submitted, the validate function is called, which calls checkInput for each input to update their validity state.
