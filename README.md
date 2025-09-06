# 🎵 Moodify – AI-Powered Mood-based Playlist Generator

Moodify is an AI-powered web app that generates **Spotify playlists based on your mood**.  
It uses **Google Gemini AI** to classify emotions from text, **MindsDB** to map moods to music genres, and the **Spotify API** to create personalized playlists in real time.  

---

## ✨ Features
- 🔑 **Spotify OAuth Login** – securely connect your account  
- 🧠 **Gemini Integration** – classifies user mood into one of 12 emotions  
- 🎶 **MindsDB-powered Recommendations** – maps detected mood → music genre  
- 📀 **Spotify Playlist Generator** – automatically creates a playlist and fills it with songs    

---

## 🛠️ Tech Stack
- **Backend:** Flask (Python)  
- **Frontend:** HTML + TailwindCSS  
- **AI/ML:** Google Gemini API, MindsDB  
- **Music Data:** Spotify Web API  

---

## ⚙️ How It Works
1. User enters how they feel → *“I’m stressed but hopeful.”*  
2. Gemini API → classifies text into an **emotion** (e.g., *relaxation*).  
3. MindsDB → maps mood to a **genre** (e.g., *chill*).  
4. Spotify API →  
   - Creates a private playlist for the user  
   - Fetches songs matching that genre  
   - Populates the playlist automatically  
5. User gets a **clickable Spotify playlist link** 🎧  

---

## 🚀 Getting Started (Local Setup)

### 1. Clone the repository
git clone https://github.com/your-username/moodify.git

cd moodify

### 2. Create a Virtual Environment
python -m venv venv

source venv/bin/activate   # Linux/Mac

venv\Scripts\activate      # Windows


### Install dependencies:

pip install -r requirements.txt

### 3. Create a Spotify Developer App

- Go to Spotify Developer Dashboard
- Log in with your Spotify account.
- Click Create an App.

Fill in:

- App Name: Moodify
- App Description: Playlist generator based on mood
- Redirect URI: http://127.0.0.1:5000/callback
- Save the app.

👉 Copy your Client ID and Client Secret from the app settings.

### 4. Get a Gemini API Key

- Visit Google AI Studio
- Sign in with your Google account.
- Generate a Gemini API key.
- Copy the key.

### 5. Configure .env File

In the project root, create a file named .env with the following content (replace with your own values):

SPOTIFY_CLIENT_ID=your_spotify_client_id
SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
SPOTIFY_REDIRECT_URI=http://127.0.0.1:5000/callback

GEMINI_API_KEY=your_gemini_api_key

MINDSDB_HOST=http://127.0.0.1:47334

FLASK_SECRET_KEY=some_secret_key

👉 You can copy from .env.template (provided in repo) and fill in your details.

### 6. Run the App
python app.py

The app will be available at:
👉 http://127.0.0.1:5000

### 8. Login with Spotify

- Open the app in your browser.
- Click Login with Spotify.
- Approve permissions.
- Enter your mood → playlist will be created in your Spotify account 🎶


### 📸 Screenshots
### Homepage
<img width="464" height="604" alt="ss1" src="https://github.com/user-attachments/assets/1ed0aa89-8d46-42fe-9eda-3fa0f97ab65c" />

### User Input about mood
<img width="495" height="412" alt="ss2" src="https://github.com/user-attachments/assets/b9eff7f5-1ea5-47b8-b984-af897408d8e1" />

### Mood Detection
<img width="414" height="281" alt="ss3" src="https://github.com/user-attachments/assets/699566eb-5e40-4e6c-81de-af9a475b0f64" />

### Spotify Playlist Generation based on the mood detected
<img width="1278" height="605" alt="ss4" src="https://github.com/user-attachments/assets/6797dfc7-2b08-4e65-bcf2-aca71a67e7b0" />


### 🧑‍💻 My Contribution to MindsDB
This project was built as part of my contribution to MindsDB.
- Used MindsDB’s SQL interface for AI-powered mood → genre mapping
- Demonstrated how MindsDB simplifies ML integration into real-world apps
- Integrated MindsDB with Spotify & Gemini to create an end-to-end AI application

### 👩‍🎓 About Me
Hi! I’m Taniya Katigar 👋
🎓 Diploma Student in AI & ML
🤖 Aspiring Data Scientist, passionate about building impactful AI solutions
💡 Actively contributing to MindsDB Open Source

🌐 LinkedIn: www.linkedin.com/in/taniya-katigar-a731bb360
