# Searchable-Combobox-Lwc

> **_NOTE:_**  This combobox is different from the lookup component.

This a custom lightning combobox with free text in which you can pick the value from the available options or type your own value. The component's functions are very similar to the standard Subject field on the Task Object in Salesforce.

## Features
1. Type a custom value or select from a dropdown/picklist.
1. Supports keyboard navigation through the options.
1. Uses standard salesforce styles and components.
1. Allow users to set the value and add a required attribute.
1. Can be used on Salesforce Platform or LWC Open Source.

# How to use.
1. Download The code
1. Deploy the component in your org.
1. Use the component in your custom web components.

### Example Code
1. HTML File
```html
<c-searchable-combobox
    required="true"
    label="Searchable Combobox"
    options={options}
    value={value}
    onchange={handleChange}
></c-searchable-combobox>
```
2. JavaScript Controller.
```js
value = "";
options = [
	{label: "--None--", value: ""},
	{label: "Call", value: "Call"},
	{label: "Email", value: "Email"},
	{label: "Message", value: "Message"},
	{label: "Task", value: "Task"},
	{label: "Visit", value: "Visit"},
	{label: "Other", value: "Other"},
];

handleChange(event) {
	this.value = event.detail.value;
	console.log(this.value);
}
```
