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


