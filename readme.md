
# GPT Real-Time Defense Against Adversarial Prompts

1️⃣ It uses functions calling  attempting to generate the first 30 words of a  regular response then returns "True" or "False" for objectionable content based on the initial words of the response.
2️⃣ regular reSponse is generated simultaneously with the objectionable response detection but only printed if there is no objectionable response

 🚀 It uses concurrency to manage both generations simultaneously

This is an effort to save on token usage while trying to detect of GPT response is objectionable as this implementation only uses the first 30 words of a response for detection and in real time. 

❗  (not tested thoroughly by any means)

⭐ Please give it a star if you think the idea is worthy 

This project leverages OpenAI's GPT models specific focus on defending against "adversarial prompts." Adversarial prompts can be used to manipulate the system into generating undesired content, and this Python script attempts to alleviate this concern by detecting potential objectionable content. This implementation tries to detect objectionable responses which might be generated by an "Adversarial prompt" and detects it with minimal token usage(30 words of the response) with "Functiona calling", returns a "True" "False" Boolean for objectionable content.

## Features
- **Response Generation:** Utilizes the GPT models to create intuitive responses.
- **Defense Against Adversarial Prompts:** Employs a system to check the first 30 words of a response to determine whether the content is objectionable, as part of the system's defense mechanism.
- **Concurrency Support:** Makes use of ThreadPoolExecutor for efficient parallel processing.
- **Streamed Output:** Allows real-time monitoring of response generation.

## Requirements
- Python 3.6 or higher
- OpenAI Python package
- termcolor package

## Usage
Simply run the main script:
```bash
python main.py
```
Then, enter your text when prompted. The script will generate a response and perform a check to ensure that it's not objectionable, safeguarding against adversarial attempts to manipulate the response.

## Understanding the Code
- `check_objectionable_response`: A function that communicates with the GPT model to check for objectionable content and prevent adversarial manipulation.
- `regular_response`: A function that gets the regular response from the GPT model.
- `main`: The main function that coordinates both tasks and provides the final output.

## Additional Resources
- **YouTube Channel:** Learn how to build AI-powered apps with GPT on [EchoHive's YouTube Channel](https://www.youtube.com/@echohive).
- **Website:** Search over all "building with GPT" videos and find code download links at [EchoHive Live](https://www.echohive.live/).
- **LLM Paper Summarizer:** Summarizes every new paper related to "large language models" from arXiv automatically every hour. Visit [LLM Papers](https://llmpapers.up.railway.app/).
- **Support:** If you want to support MY efforts, you can do so through [Patreon](https://www.patreon.com/echohive42).

