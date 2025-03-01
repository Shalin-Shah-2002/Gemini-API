# Setting Up Your Gemini API Key

To use this project, you need to set up your own **Gemini API Key** and store it securely in a `.env` file.

## Steps to Get Your Gemini API Key
1. **Go to Google AI Platform:**  
   Visit [Google AI Platform](https://ai.google.dev/) and sign in with your Google account.

2. **Create an API Key:**  
   - Navigate to the API key section.
   - Generate a new API key.
   - Copy the generated key.

## Setting Up the `.env` File
1. **Create a `.env` file** in the root directory of your project.
2. **Add the following line to store your API key:**
   ```
   GEMINI_API_KEY=your_api_key_here
   ```
   Replace `your_api_key_here` with your actual Gemini API key.

## Install Required Packages
Before running the project, make sure to install the necessary dependencies. Run the following command:
```sh
npm i @google/generative-ai@^0.22.0 axios@^1.8.1 cors@^2.8.5 dotenv@^16.4.7 express@^4.21.2 gemini-api@file:
```

## Using the Live API
This API is live and can be accessed at:
**Endpoint:** `https://gemini-api-gjrq.onrender.com/generate`

### Sending a POST Request
Use your favorite API tool (e.g., Postman, Insomnia) to send a POST request with the following JSON format:
```json
{
  "prompt": "Generate a structured exercise plan of Deadlift with the following details. Ensure the response follows the exact format mentioned below:\n\nResponse Format:\n``\n**Exercise Name:** \n**Description:** \n**Recommended Reps:**\n- **Beginners:** \n- **Intermediate:** \n- **Professional:** \n``"
}
```

## Important Notes
- **Do NOT share your `.env` file** or commit it to version control (e.g., GitHub). Add `.env` to `.gitignore`.
- If you accidentally expose your API key, **revoke it immediately** and generate a new one.

## Using the API Key in Your Code
In your application, you can load the API key from the environment variables like this:
```python
import os
GEMINI_API_KEY = os.getenv("GEMINI_API_KEY")
```

By following these steps, you can securely use the Gemini API in your project. 🚀

