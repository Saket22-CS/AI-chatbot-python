# 🤖 Chatbot with Python and Machine Learning

This project demonstrates how to build an intelligent chatbot using **Python**, **TensorFlow**, and **Natural Language Processing (NLP)**. The chatbot is trained to respond to various user queries based on predefined intents.

---

## 🧠 Features

- NLP-based intent recognition using `nltk`
- Neural Network classifier using `TensorFlow / Keras`
- Interactive terminal chat interface
- Easily customizable intent dataset (`intents.json`)
- Persistence using model/tokenizer/encoder saving
- Lightweight Flask integration possible (for future deployment)

---

## 🗂️ Folder Structure

```

📁 chatbot-ml/
│
├── intents.json              # Intents dataset (patterns + responses)
├── chatbot.ipynb             # Jupyter notebook with all training code
├── tokenizer.pickle          # Saved tokenizer for inference
├── label\_encoder.pickle      # Saved label encoder
├── chat\_model/               # Saved TensorFlow model
└── README.md                 # You're reading this!

````

---

## 🧰 Requirements

Install the required packages:

```bash
pip install tensorflow==2.3.1
pip install nltk==3.5
pip install colorama==0.4.3
pip install numpy==1.18.5
pip install scikit-learn==0.23.2
pip install Flask==1.1.2
````

---

## 📝 How It Works

1. **Data Preparation**

   * Load and process the `intents.json` file.
   * Use `LabelEncoder` to encode intent tags.
   * Tokenize and pad text using Keras tokenizer.

2. **Model Training**

   * Create a simple feed-forward neural network with:

     * Embedding Layer
     * GlobalAveragePooling1D
     * Dense Layers
   * Train for 500 epochs.

3. **Model Saving**

   * Save the trained model (`chat_model`)
   * Save the tokenizer and label encoder for inference.

4. **Chat Function**

   * Load saved model and tokenizer.
   * Predict intent of the user's message.
   * Reply with an appropriate response.

---

## 🧪 Example Interaction

```shell
User: Hi
ChatBot: Hello!

User: What is your name?
ChatBot: I'm RISHU, your virtual assistant.

User: I forgot my password
ChatBot: Please click 'Forgot Password' on the login page to reset it.

User: quit
```

---

## 🗃️ Customizing Intents

You can add or modify intents inside `intents.json` like:

```json
{
  "tag": "greeting",
  "patterns": ["Hello", "Hi", "Hey"],
  "responses": ["Hi there!", "Hello!", "Hey!"]
}
```

Don't forget to re-train the model after editing!

---

## 🚀 Future Improvements

* Add support for multiple languages
* Integrate with Flask API
* Deploy on web/mobile
* Contextual conversation memory

---

## 💡 Credits

Built using:

* [TensorFlow](https://www.tensorflow.org/)
* [Scikit-Learn](https://scikit-learn.org/)
* [NLTK](https://www.nltk.org/)
* [Keras](https://keras.io/)

---

## 📜 License

This project is for educational purposes and is open-source. Feel free to fork and improve!
