# CWRU Game Room Leaderboard

This project implements a Game Checkout System and Leaderboard for the CWRU Game Zone. It allows students to check out games, tracks active sessions, manages a waitlist for unavailable games, records session history, and maintains a leaderboard for game scores.

## Features

- **Game Checkout:** Students can check out available games.
- **Waitlist Management:** If a game is unavailable, students can be added to a waitlist. When a game is checked in, the next student on the waitlist for that game is automatically checked out.
- **Active Sessions Tracking:** Displays currently checked-out games and their check-in times.
- **Session History:** Records all past game sessions, including duration.
- **Leaderboard:** Tracks and displays top scores for various games, with filtering options.
- **Firebase Integration:** Uses Firebase for real-time data storage and authentication.
- **Responsive Design:** Built with Tailwind CSS for a modern and responsive user interface.

## Technologies Used

- **HTML5**
- **Tailwind CSS**
- **JavaScript (ES6+)**
- **Firebase (Firestore, Authentication)**

## Project Structure

- `index.html`: The main application for checking out and checking in games.
- `dashboard.html`: Displays the live active sessions and the game leaderboards.
- `.gitattributes`: Git configuration for line endings.

## Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ashishgoyal545/GameRoomLeaderboard.git
   cd GameRoomLeaderboard
   ```

2. **Firebase Configuration:**
   This project uses Firebase. You will need to set up your own Firebase project and update the `firebaseConfig` object in both `index.html` and `dashboard.html` with your project's credentials.

   The `firebaseConfig` object looks like this:
   ```javascript
   const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_AUTH_DOMAIN",
       projectId: "YOUR_PROJECT_ID",
       storageBucket: "YOUR_STORAGE_BUCKET",
       messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
       appId: "YOUR_APP_ID",
       measurementId: "YOUR_MEASUREMENT_ID"
   };
   ```

3. **Open in Browser:**
   Simply open `index.html` or `dashboard.html` in your web browser to use the application. No local server is strictly required for basic functionality, as Firebase handles the backend.

## Usage

### Game Checkout System (`index.html`)

- Enter a Student ID.
- Select a game from the dropdown. The dropdown shows available game counts.
- Click "Check In" to start a session.
- If a game is unavailable, the student will be added to a waitlist.
- Click "Check Out" next to an active session to end it. This will prompt for a score to be entered for the leaderboard.

### Game Zone Dashboard (`dashboard.html`)

- View "Currently Playing" to see all active game sessions.
- View "Top Scores" to see the leaderboard.
- Use the "Filter by Game" dropdown to view the leaderboard for a specific game or all games.

## Contributing

Feel free to fork the repository, make improvements, and submit pull requests.

## License

This project is open source and available under the [MIT License](LICENSE).
