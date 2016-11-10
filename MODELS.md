Here we a list a few rules for models and their relationship that a project must follow.

# Contact
- **id**: required `int`
- **first_name**: required `string`, max: 20 chars
- **last_name**: optional `string`
- **age**: optional `int`, range: 18~99

# Address
- **id**: required `int`
- **street**: required `string`, max: 20 chars
- **number**: optional `int`, min: 1
- **line_2**: optional `string`
- **postal_code**: required `string` (different countries might use punctuation or even letters in the postal code)
- **country**: required `string`, fixed length: 2 chars (optionally this could be verified to be part of a list, like an ENUM field)

# The relationship
`contact 1..n address`
> The relational field was purposely left behind as the implementer might want to implement this in a document-based approach instead, leaving addresses as sub-documents of a contact.

# Validations
Some fields were specifically set to have the said format to enforce some validation rules on the API. For instance, the age sets a specific minimum and maximum values, while the address may contain a number that should be a positive integer - although sometimes used with letters in the real world. Some other fields have required maximum length.
Date fields were out as many languages have no specific format for this and could lead to a deviation of the original purpose, spending time on actually verifying if the date has a valid format instead of focusing on the API.
