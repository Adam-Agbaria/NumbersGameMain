Numbers Game

Welcome to Numbers Game, a multiplayer game where players compete to choose the best number based on a strategic calculation. This repository contains all components of the game, including the Flask server, Web frontend, Android Host App, and Android Library.

📌 Project Overview

The game follows these rules:

Players join the game by scanning a QR code from the Android host app.

Each player picks a number between 0 and 100.

The average of all chosen numbers is calculated and multiplied by 0.8.

The player whose number is closest to this result wins the round.

The game continues for multiple rounds, and the player with the most round wins is the overall winner.

🛠️ Project Components

1️⃣ Flask Server (Backend)

Manages game sessions

Handles player connections and game logic

Stores results and tracks winners

Provides REST API endpoints for the frontend and mobile app

2️⃣ Web Frontend (Game UI for Players)

Players enter their name and game ID to join a game

Displays a waiting screen until the game starts

Players submit numbers within a time limit

Displays round results and the overall winner

3️⃣ Android Host App

Allows the game host to create and manage games

Generates a QR code for players to scan and join

Provides a 'Start Game' button to begin the game

Includes an 'End Round' button to control game rounds

4️⃣ Android Library

Encapsulates server logic for easy integration into mobile apps

Another Android app is included to demonstrate the library’s usage

🚀 Getting Started

1️⃣ Clone the Repository

git clone https://github.com/YourUsername/NumbersGame.git
cd NumbersGame

📦 Flask Server (Backend)

📌 Prerequisites

Python 3.x

Flask

Flask-CORS

🔧 Installation & Setup

cd backend
pip install -r requirements.txt
python app.py

The Flask server is deployed on Vercel, update the URL in the frontend and mobile app accordingly.

🌐 Web Frontend (Player UI)

🔧 Setup

cd frontend
npm install
npm run build
vercel --prod

Access the game at your Vercel deployment URL.

🎮 Player Flow

Enter name and game ID

Wait for the host to start the game

Choose a number when the game starts

See round results and final winner

📱 Android Host App

📌 Prerequisites

Android Studio

Java/Kotlin

🔧 Setup

Open the android-host-app folder in Android Studio

Sync Gradle dependencies

Build and run the app on a device or emulator

🎮 Host Features

Create a game (generates a game ID)

Generate QR code for player entry

Start the game

Manually end rounds

📦 Android Library

🔧 Setup

Add the Android Library module to your project

Include the library dependency in your app:

dependencies {
    implementation project(':numbers-game-library')
}

📡 Usage Example

GameClient client = new GameClient("https://your-vercel-deployment-url");
client.createGame();
client.joinGame("PlayerName", gameId);
client.submitNumber(42);

🤝 Contributing

Fork this repository

Clone the repo: git clone https://github.com/YourUsername/NumbersGame.git

Create a branch for your feature: git checkout -b feature-name

Commit your changes: git commit -m "Added new feature"

Push your branch: git push origin feature-name

Open a Pull Request 🎉

📜 License

This project is licensed under the MIT License.

🎯 Roadmap & Future Enhancements

✅ Basic game logic implemented

✅ Web and Android integration

🔄 Enhance UI/UX for the web frontend

🔄 Add a real-time leaderboard

🔄 Improve game analytics and stats tracking

📧 Contact

For questions or suggestions, feel free to reach out!

📩 Email: agbariaadam@yahoo.com

🔗 LinkedIn: Adam Agbaria

🌍 GitHub: Adam-Agbaria

🚀 Happy Gaming! 🎮

