If you're new to Python, here's a step-by-step guide to running the script:

1. **Install Python**:
   - If you haven't already, download and install Python from [python.org](https://www.python.org/downloads/).
   - During installation, make sure to check the box that says "Add Python to PATH." This allows you to run Python from the command line.

2. **Setting Up a Virtual Environment (Recommended)**:
   - It's a good practice to use virtual environments to avoid potential conflicts between packages.
   - Open a terminal or command prompt.
   - Navigate to the directory where you want your project (and the script) to be.
   - Create a virtual environment:
     ```
     python -m venv myenv
     ```
   - Activate the virtual environment:
     - On Windows:
       ```
       .\myenv\Scripts\activate
       ```
     - On macOS and Linux:
       ```
       source myenv/bin/activate
       ```

3. **Install Required Libraries**:
   - With the virtual environment activated (you'll see `(myenv)` on the command line if it's active), install the required libraries:
     ```
     pip install whisper openai dotdev
     ```
    - `whisper`: A library used for audio transcription, provided by OpenAI.
    - `openai`: The OpenAI Python client library, which allows you to interact with the OpenAI API for various AI models including GPT-3.
    - `dotenv`: A Python package that reads key-value pairs from a `.env` file and can set them as environment variables.
    - `os`: A standard library in Python that provides a way to perform OS-dependent functions such as reading or writing environment variables.
     The 'os' module is part of the standard library of Python, so you do not need to install it separately. It comes pre-installed with Python and provides a way of using operating system dependent functionality like reading or writing to a filesystem, manipulating paths, and more.
     
     You can use it directly in your scripts without any additional installation steps. Just make sure you have Python installed on your system, and you can import and use os directly.

4. **About the Script**:
   
   This script integrates Whisper for audio transcription and OpenAI for text summarization, along with saving the results to a text file. The code is commented in everyline so that it can be easely understood.

   An importand notes:

   - To learn to work with whisper library please go to https://github.com/openai/whisper
   - The script is using "gpt-4-1106-preview" model, since it uses a context window of 128,000 tokens.

        In the realm of natural language processing (NLP) and particularly with models like GPT (Generative Pretrained Transformer), a "context window" or "context length" refers to the maximum number of tokens (words or pieces of words) that the model can consider at once when generating text or understanding input.

        For a context window of 128,000 tokens:

        Token Definition: Tokens are not necessarily whole words; they can also be parts of words, especially in languages like English where you can have smaller sub-word units (like prefixes or suffixes) that are meaningful. The way tokens are defined depends on the tokenizer used to process text into a format the model understands.

        Window Size: A context window of 128,000 tokens is exceptionally large. Most earlier models, like GPT-2 or even GPT-3, had much smaller context windows (GPT-3, for instance, has a context window of 2048 tokens). A context window this large would allow the model to generate or analyze long documents without losing context, which is essential for maintaining coherence over long passages of text.

        Implications for Processing: Being able to consider 128,000 tokens at once means the model could handle very lengthy inputs, such as complete books, extensive reports, or long conversations, without needing to truncate them. This would be particularly useful for tasks that require a deep understanding of long-form content.

        Technical Challenges: Handling such a large context window would likely pose significant memory and computational challenges. It would require a lot of resources to process, which is one of the reasons why many language models operate with smaller context windows.

        Use Cases: With a context window of this size, you could expect the model to perform tasks that involve long narratives or content with complex structure without losing track of earlier parts of the text. It could be useful in applications like summarizing whole novels, conducting legal reviews of entire contracts, or analyzing long scientific articles.


    Please check: https://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbo

5. **Run the Script**:
   - Go back to your terminal or command prompt.
   - Navigate to the directory where you saved your script, if you're not already there.
   - Run the script:
     ```
     python record_audio.py
     ```
   - The script will execute, and when it finishes, you should see the file of the summary in the summaries folder.

6. **Deactivate the Virtual Environment**:
   - Once you're done working on your project, you can deactivate the virtual environment by simply typing:
     ```
     deactivate
     ```
