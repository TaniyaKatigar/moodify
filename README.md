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
   - Fetches 15 songs matching that genre  
   - Populates the playlist automatically  
5. User gets a **clickable Spotify playlist link** 🎧  

---

## 🚀 Getting Started (Local Setup)

### 1. Clone the repo
git clone https://github.com/TaniyaKatigar/moodify.git
cd moodify

### 2. Create a Virtual Environment
python -m venv venv
venv\Scripts\activate   # On Windows

source venv/bin/activate  # On Mac/Linux

### 3. Install Dependencies
pip install -r requirements.txt

### 4. Set up Environment Variables
Create a .env file in the root directory and add:
### Spotify API
SPOTIFY_CLIENT_ID=your_spotify_client_id
SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
SPOTIFY_REDIRECT_URI=http://127.0.0.1:5000/callback
### Gemini API
GEMINI_API_KEY=your_gemini_api_key
### Flask Secret
FLASK_SECRET_KEY=super_secret_key
### Gemini API
GEMINI_API_KEY=your_gemini_api_key
### Flask Secret
FLASK_SECRET_KEY=super_secret_key

### 5. Run MindsDB (locally)
Make sure you have a running MindsDB instance:

docker run -p 47334:47334 mindsdb/mindsdb

Train or connect your mood_to_genre_model in MindsDB.

### 6. Start the Flask Server
python app.py

Go to 👉 http://127.0.0.1:5000


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
