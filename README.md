# Chat Template Formatter using Python

This project involves creating a utility function in Python that formats text into structured chat templates using specific handlebars tags. The utility function uses the pyparsing library to achieve this.

## Objective

The goal of this project is to create a utility function that takes input text and formats it into structured chat templates with user and assistant roles, as well as special commands.

## Background

In a chat system, conversations are represented using handlebars templates:
- User Role: {{#user}} ... {{/user}}
- Assistant Role: {{#assistant}} ... {{/assistant}}
- Assistant Commands: {{gen ... }}

## Requirements

1. Identify and format segments using pyparsing library.
2. Wrap text within user tags ({{#user}} ... {{/user}}).
3. Wrap {{gen ... }} commands with assistant tags.
4. Ensure single {{gen ... }} command per assistant segment.
5. Add {{gen 'write' }} if not present at assistant's completion.

## Usage

1. Install the required library:
    pip install pyparsing
   
3. Clone the repository and navigate to the project directory.

4. Run the utility function to format chat templates:
```python
from chat_formatter import format_chat_template

input_text = "Hello! {{gen 'greet'}} How can I assist you?"
formatted_output = format_chat_template(input_text)
print(formatted_output)

Test Cases
The project includes test cases to ensure the function's accuracy. You can modify and extend the provided test cases in the test_cases.py file.

Example
Input:
Tweak this proverb to apply to model instructions instead. Where there is no guidance{{gen 'rewrite'}}

Output:
{{#user}}Tweak this proverb to apply to model instructions instead.{{/user}} Where there is no guidance {{#assistant}}{{gen 'rewrite'}}{{/assistant}}
