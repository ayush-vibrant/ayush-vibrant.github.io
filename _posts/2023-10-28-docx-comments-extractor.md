# Extracting comments from DOCX files: A python solution

Few days ago, I was fine-tuning LLMs on documents filled with comments, strikethroughs, and edits. I couldn't find the right tool to get the data in correct format, so I created a Python script.


This script allows users to extract comments and their associated text from a DOCX file. 

The output can be presented in multiple formats, and the script provides the option to include additional details such as the author's name and timestamp.


## Features

- Extract comments and the text they are associated with. It handles parent-child relationships of comments too.
- Display in original, enhanced, or JSON format.
- Option to include the author's name and timestamp of the comment.

### [Github Repository](https://github.com/ayush-vibrant/docx-comments-extractor) can be found here. 