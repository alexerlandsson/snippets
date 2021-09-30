# Input Text

Basic styling for input text elements.

## Base

```html
<label for="input-base">Base</label>
<input type="text" placeholder="Lorem ipsum" id="input-base" />
```

## E-mail

Uses `autocapitalize="none"` to prevent automatic capitalize on touch keyboards.

```html
<label for="input-email">E-mail</label>
<input type="email" placeholder="Lorem ipsum" id="input-email" autocapitalize="none" name="email" autocomplete="email"/>
```

## Autocomplete attributes

List of attributes used for various autocompletion.

### Name

| name | autocomplete |
|---|---|
| name fname mname lname | name (full name) given-name (first name) additional-name (middle name) family-name (last name) |

### Email

| name | autocomplete |
|---|---|
| email | email |

### Address

| name | autocomplete |
|---|---|
| address city region province state zip zip2 postal country | For one address input: street-address For two address inputs: address-line1 , address-line2 address-level1 (state or province) address-level2 (city) postal-code (zip code) country |

### Phone

| name | autocomplete |
|---|---|
| phone mobile country-code area-code exchange suffix ext | tel |

### Credit Card

| name | autocomplete |
|---|---|
| ccname cardnumber cvc ccmonth ccyear exp-date card-type | cc-name cc-number cc-csc cc-exp-month cc-exp-year cc-exp cc-type |
