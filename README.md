# VEML
Vector Embedding Markup Language - markup language designed specifically for annotating and structuring data related to vector embeddings. This could be used to represent, exchange, or store vector embeddings in a structured way that's easily readable by both humans and machines.
## How the idea was born
Running [IngestAI](https://ingestai.io) project since February 2023 we faced a lot of issues from thousands of our users. Almost all of these issues were connected with the dataset structure and ability to influence on the vector search results.

Main issues we collected from users:

-⚡ All users wish to have ability to manipulate with embedding process: to exclude some parts ot the text from embedding requests, etc.
-2. Almost every user wanted to see not just chunk text, beautyful HTML-markup for their AI search results.
-3. Most of users wanted to add additional information to chunks, like links, images, links to the YouTube videos, etc.
## VEML Markup
VEML file is saved in JSON format and consists of following structure:
1. "html": an array of pure HTML code of a chunks to make it presentable for the users.
2. "tokens": an array of pure texts part that will be embedded
3. "vectors": an array of embeddings for every chunk (can be empty if chunk was disabled)
4. "meta": an array of meta information for every chunk, consists of strings, that have such strcture: key:value, ex. link:https://wikipedia.com

You can see the structure of VEML file in schema.json file in this repository, and also you can see examples in the examples folder.

# Benefits
The implementation of VEML offers numerous advantages, such as:

1. Standardization: VEML provides a standardized format for pre-processing and editing vector embeddings.
2. Interoperability: It ensures better interoperability among different applications and systems that utilize vector embeddings.
3. Extensibility: Just like XML, VEML has the potential to be extensible, allowing users to add new tags and attributes to represent additional properties or metadata associated with the vector embeddings.
5. Machine Readability: A well-defined markup language would also be easily parseable by ML, ensuring efficient processing and manipulation of vector embeddings by various software applications.

## VEML Editor
We understand that developing a markup without an app that supports it, is not a good idea, so we created open-source tool called [Embedditor](https://embedditor.ai). You can download it from Github or Docker and run it on your local server to start working with the VEML files and editor.
