# 🤖 ChatBot Project

Welcome to the SIH_Chatbot Project! This is a simple yet powerful chatbot built using Python, TensorFlow, and Natural Language Processing (NLP) techniques. The bot learns from a set of predefined intents and responds accordingly, making it a great starting point for creating more advanced conversational agents. 🚀


## 📝 Features
- **Intent Recognition**: The bot identifies user intent from input messages.
- **Interactive Responses**: Responds dynamically with a variety of answers.
- **Easy Training**: Train your bot with your custom intents and patterns.
- **Simple Integration**: Easily modify the bot to suit your specific needs.


## 📁 Project Structure
- `trainer.py` - Script to train the chatbot model using intents data.
- `chatbot.py` - Main script to run the trained chatbot.
- `intents.json` - JSON file containing intents, patterns, and responses.
- `words.pkl` & `classes.pkl` - Saved word and class data used for the model.
- `chatbot_model.h5` - Trained chatbot model file.


## 🚀 Getting Started

Follow these steps to get the bot up and running:

### 1. **Clone the Repository**

First, clone this repository to your local machine:

```bash
git clone https://github.com/your-username/chatbot-project.git
cd SIH_Chatbot
```

### 2. **Install Dependencies**

Ensure you have Python installed (preferably Python 3.7+). Then, install the required dependencies using pip:

```bash
# Create a virtual environment (optional but recommended)
python -m venv chatbot-env
source chatbot-env/bin/activate  # On Windows use: chatbot-env\Scripts\activate

# Install required libraries
pip install numpy tensorflow nltk
```

### 3. **Set Up NLTK**

NLTK requires some initial data setup. Run the following commands in your Python environment:

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

### 4. **Prepare the Data**

Before training, make sure your `intents.json` file is correctly formatted. Here’s a quick look at its structure:

```json
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Hello", "Hi", "Hey there", "Howdy"],
      "responses": ["Hello!", "Hi there!", "Greetings!", "Hey! How can I help you?"]
    },
    {
      "tag": "goodbye",
      "patterns": ["Bye", "See you later", "Goodbye"],
      "responses": ["Goodbye!", "See you soon!", "Have a nice day!"]
    }
  ]
}
```

### 5. **Train the Bot 🏋️**

To train the chatbot, run the `trainer.py` script. This script will preprocess the data, create the model, and save it for future use.

```bash
python trainer.py
```

Once training is complete, you should see the message **"Done"**, and the trained model will be saved as `chatbot_model.h5`.

### 6. **Run the Chatbot 🤖**

After training, run the `chatbot.py` script to start the chatbot:

```bash
python chatbot.py
```

Type your message when prompted, and watch the bot respond intelligently! 🎉

---
## 🛠️ Customization Tips
- **Adding Intents**: Modify `intents.json` to add more intents, patterns, and responses.
- **Training Parameters**: Adjust training parameters such as epochs and batch size in `trainer.py` to fine-tune the model performance.
- **Bot Behavior**: Customize the response selection logic in `chatbot.py` for more personalized interactions.


## 📜 License
Feel free to modify and use this project for your personal or commercial projects. Contributions are welcome!


## 💡 Contributing
If you have suggestions or improvements, please create a pull request or open an issue. Let's make this bot smarter together! 😊

---
