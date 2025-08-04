🧠 Spam Detector – Full Stack Web App with Machine Learning
This project is a **spam message detection system** built using:
* A **Flask API backend** with a trained **Naive Bayes model**
* A **React frontend** for real-time message input
* **Docker support** for easy deployment

 🚀 Features
* Input any text message and check if it's **spam or not**
* Pretrained model using **TF-IDF vectorization** and **Naive Bayes**
* Clean and simple **React interface**
* Fully containerized using Docker

 🧩 Tech Stack
* 🐍 Python (Flask)
* 📦 scikit-learn, pandas, pickle
* 🌐 React.js (frontend)
* 🐳 Docker
* 🧠 Machine Learning (Multinomial Naive Bayes)

 🏗 Project Structure
├── backend/
│   ├── app.py               # Flask backend app
│   ├── train_model.py       # Model training script
│   ├── spam_model.pkl       # Trained ML model (generated)
│   ├── vectorizer.pkl       # TF-IDF vectorizer (generated)
│   └── Dockerfile           # Backend Docker config
│
├── frontend/
│   ├── App.js               # Main React component
│   ├── App.css              # Styling
│   └── ...                  # Other React files (if any)
│
├── docker-compose.yml       # For full stack deployment
└── README.md                # Project documentation

 🧪 How It Works

1. **Model Training**:
   * Run `train_model.py` to train a spam classifier using a labeled dataset.
   * It saves the model (`spam_model.pkl`) and TF-IDF vectorizer (`vectorizer.pkl`).
2. **Backend (Flask)**:
   * Loads the trained model and exposes a `/predict` API endpoint.
   * Receives messages from the frontend and returns spam prediction.
3. **Frontend (React)**:
   * Simple UI for users to enter a message.
   * Sends the message to the backend and displays the prediction.

🐳 Running the App (with Docker Compose)
Step 1: Build and Run
```bash
docker-compose up --build
```
This will:
* Build and start the Flask backend on `http://localhost:5000`
* Start the React frontend on `http://localhost:3000`
> 📝 Ensure the React frontend calls the backend at `/predict` correctly. In production, use relative URLs or environment configs.

💡 Example

**Input**: "Congratulations! You won a free cruise. Click here!"

**Output**: 🚨 Spam Message Detected!

📄 License
This project is intended for educational/demo purposes. Feel free to use and adapt with attribution.
<img width="1484" height="728" alt="image" src="https://github.com/user-attachments/assets/a49beb17-56b0-4ff6-b3b3-e1d4f73134ae" />

<img width="1601" height="899" alt="image" src="https://github.com/user-attachments/assets/ae61f897-7ebc-40aa-a9c8-5f69952a3a5d" />
