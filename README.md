# TravelBuddy: AI Travel Agent ✈️🏨

TravelBuddy is an intelligent, multi-agent AI assistant designed to simplify your travel planning. This application, built with LangGraph and Streamlit, allows you to find flights and hotels for your next trip and have the information sent directly to your email.

---

### Key Features

* **Intelligent Agent Workflow:** The application uses a stateful agent system powered by **LangGraph** to manage the travel planning process from query to email delivery.
* **Gemini-Powered AI:** It leverages the **`gemini-2.0-flash-lite`** model for both natural language understanding and for formatting the final email.
* **Real-time Information:** The agent uses tools powered by **SerpApi** to find up-to-date flight and hotel information.
* **Email Integration:** After finding travel details, the app can format the information into a professional HTML email and send it to your inbox using **SendGrid**.
* **Interactive UI:** A user-friendly interface built with **Streamlit** allows for easy input of travel queries and email details.

---

### Project Structure

This project is organized into several key components:

* **`app.py`**: The main application file that handles the Streamlit user interface, user input, and state management.
* **`agent.py`**: Defines the core agent logic using LangGraph. This file orchestrates the workflow between the AI model and the various tools.
* **`tools/`**: A directory containing the specialized tools the agent uses.
    * **`flights_finder.py`**: A tool that uses the Google Flights engine to search for flight options.
    * **`hotels_finder.py`**: A tool that uses the Google Hotels engine to search for hotel options.
* **`.env`**: A file to store your API keys and email credentials. **This file should not be committed to a public repository.**

---

### Getting Started

To get a local copy up and running, follow these steps.

#### Prerequisites

* Python 3.8 or newer
* `pip` package manager
* API keys for the following services:
    * **SerpApi**: For real-time flight and hotel searches.
    * **SendGrid**: For sending emails.
    * **Google AI Studio**: For the Gemini model.

#### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Arghadeepkar85/TravelBuddy.git]
    cd TravelBuddy
    ```

2.  **Create a virtual environment and activate it:**
    ```bash
 
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up environment variables:**
    Create a `.env` file in the root directory and add your API keys and email credentials.
    ```
    SERPAPI_API_KEY="your_serpapi_api_key"
    SENDGRID_API_KEY="your_sendgrid_api_key"
    GOOGLE_API_KEY="your_google_ai_key"
    FROM_EMAIL="sender_email@example.com"
    TO_EMAIL="receiver_email@example.com"
    EMAIL_SUBJECT="Your Travel Plan"
    ```

---

### Usage

1.  **Run the Streamlit application:**
    ```bash
    streamlit run app.py
    ```
2.  The application will open in your web browser.
3.  Enter your travel query in the text box. For example: `I want to travel to Tokyo from Madrid from 1-7 of October. Find me flights and 4 star hotels.`
4.  Click **"Get Travel Information"** to see the results.
5.  If you want to send the information via email, select **"Yes"** and fill out the email details.
6.  Click **"Send Email"** to deliver the travel plan to your inbox.

---
### Screenshots

<img width="1719" height="906" alt="Screenshot 2025-09-15 202658" src="https://github.com/user-attachments/assets/9ca2ba2b-0b3b-4b53-907a-d9a03714aae8" />

---
<img width="1238" height="824" alt="Screenshot 2025-09-15 202849" src="https://github.com/user-attachments/assets/b9904b6c-d754-4211-8766-4d94012bafc9" />

---
<img width="1151" height="729" alt="Screenshot 2025-09-15 202909" src="https://github.com/user-attachments/assets/aba31c5e-ff47-4e84-a9e6-490824b0f9d6" />

---
<img width="1828" height="809" alt="Screenshot 2025-09-15 202922" src="https://github.com/user-attachments/assets/3c38d229-9434-46e1-8aa5-eac90dcd1958" />

---



### Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---


