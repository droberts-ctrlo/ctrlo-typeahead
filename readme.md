# @ctrlo/typeahead

Basic typeahead module using Twitter's typeahead.js

## Usage

```javascript
const builder = new TypeaheadBuilder();

builder
    .withInput($input) // The control to use as a typeahead - required
    .withCallback((suggestion) => {console.log(suggestion)}) // Callback for when an item is selected - required
    .withName("typeahead") // The name for the typeahead - required
    .withAjaxSource(url) // url (String) for the source to fetch the options for the typeahead -required
    .withAppendQuery(true) // whether to append the query to the above url (optional, default true)
    .withData(data) // any data to be sent with the request - this option will clear the dataBuilder setting and is mutually exclusive
    .withMapper((input)=>output) // The mapping function to use - see @ctrlo/mapper package for options
    .withDefaultMapper() // use the default mapper - see @ctrlo/mapper package for options
    .withDataBuilder((data)=>result) // Function to map the data to input - this will clear the data setting and is mutually exclusive
    .withMethod('GET') // request method to use when retrieving data - optional (defaults to 'GET')
    .build()
```
