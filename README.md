# Telegram Meets AI: Integrating ChatGPT into Telegram

## Features

- Recognize audio provided from telegram bot by the user and convert the audio to text. 
- Invoke the GPT API in-order to fetch the response for the question. 
- Collect the response and convert the response to user's local language as audio as well in text
- Provide the audio and text as the answer to the users question in telegram chat.


## Link to the demo video
- [Demo Run Video](https://drive.google.com/file/d/1-zzhYMba1PwMX0E2EknqGsSohmn7FEL-/view?usp=drive_link)
- [Self Introduction Video](https://drive.google.com/file/d/1w22MnHGOSBhX4x00ExNbsvuqm40x9UN5/view?usp=drive_link)


## Steps to use the application:

1. Obtain the following keys and replace with the respective genarated key in the **config.yml** (since the service is not hosted on ANY paid cloud servers) :-
    1.1 Get the OpenAI keys (used to invoke GPT for querying)
    - Reference guide: https://www.howtogeek.com/885918/how-to-get-an-openai-api-key/
    
    1.2 Get the [Telegram Bot key](https://core.telegram.org/api/obtaining_api_id) (used to create the chat bot on the Telegram app)
    
    1.3 Get the Bhashini API key (used to invoke voice synthesis and text translation)
    - Reference guide: https://www.aisupersmart.com/ai-tools-directory/bhashini-ai/

    Your config.yml file should look something like:
    ```sh
    OPENAI:
      API_KEY: <your-OpenAI-API-key-as-generated-in-step-1.1>
    TELEGRAM:
      TOKEN: <your-Telegram-Bot-key-as-generated-in-step-1.2>
    BHASHINI:
      HEADERS:
        ulca-api-key: <generated-ucla-api-key-in-step-1.3>
        user-id: <generated-user-id-key-in-step-1.3>
        inference-api-key: <generated-inference-key-in-step-1.3>
    ```

2. Install the following code dependencies:
    ```sh
    pip install -r requirements.txt
    ```
3. Run the application:
    ```sh
    python Bot.py
    ```
