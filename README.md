# Florida Animal Cruelty Case Tracker

## Overview

The Florida Animal Cruelty Case Tracker is a real-time, collaborative web application designed to monitor and visualize active animal cruelty cases across the state of Florida. This platform aims to increase public awareness, transparency, and advocacy by providing a centralized, user-friendly dashboard.

The application is built with modern web technologies, including a live Firebase Firestore database for real-time updates and an interactive map powered by Leaflet.js. Users can not only view and filter existing case data but also contribute by submitting new cases, which become instantly visible to all users.

## Live Demo

A live, functional version of this application is available for interaction. *(Note: Link would go here in a real GitHub project)*

## Key Features

- **Real-Time Database:** Utilizes Google Firebase Firestore to ensure all case data is live and updates instantly for all users.
- **Interactive Map:** Displays the geographic distribution of cases across Florida using Leaflet.js. Map markers are clickable, providing quick case summaries and a link to detailed views.
- **Collaborative Case Submission:** Users can submit new cases through a simple form. Submissions are added to the database in real-time and marked as "Pending Review."
- **Advanced Filtering & Search:** Cases can be filtered by county, status, or incident date. A dynamic search bar allows filtering by defendant name or case number.
- **Data Visualization:** Interactive charts powered by Chart.js provide a visual breakdown of cases by county and status.
- **Responsive Design:** The UI is built with Tailwind CSS for a seamless experience on desktops, tablets, and mobile devices.
- **Guidance for Action:** Includes a modal with clear, actionable information on how to officially report suspected animal cruelty to the correct Florida authorities.

## Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (ES6 Modules)
- **Database:** Google Firebase Firestore (Real-time, NoSQL)
- **Mapping:** Leaflet.js
- **Charting:** Chart.js
- **Styling:** Tailwind CSS

## Project Setup

To run this project locally, you will need to have a Google Firebase account.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/florida-animal-cruelty-tracker.git](https://github.com/your-username/florida-animal-cruelty-tracker.git)
    cd florida-animal-cruelty-tracker
    ```

2.  **Firebase Configuration:**
    - Create a new project in your [Firebase Console](https://console.firebase.google.com/).
    - In your project, create a new Web App.
    - Go to **Project Settings** > **General**. Under "Your apps", find the web app you created.
    - Select the **Config** option to get your Firebase configuration object. It will look like this:
      ```javascript
      const firebaseConfig = {
        apiKey: "AIza...",
        authDomain: "your-project-id.firebaseapp.com",
        projectId: "your-project-id",
        storageBucket: "your-project-id.appspot.com",
        messagingSenderId: "...",
        appId: "..."
      };
      ```
    - This project is designed to work with environment variables provided by a host (like the one you're using). You would typically place this config in a secure file or environment variable. For simple local testing, you can modify the `index.html` script section to use your config directly, but **do not commit your keys to a public repository.**

3.  **Enable Firestore:**
    - In the Firebase console, go to the **Firestore Database** section.
    - Click **Create database**.
    - Start in **test mode** for easy local development. This will allow open read/write access. **For a production application, you must set up proper security rules.**
    - The application is designed to automatically seed the database with initial data on the first run if the `cases` collection is empty.

4.  **Run the Application:**
    - Since this is a vanilla HTML/JS project, you can open the `index.html` file directly in your browser. For best results and to avoid CORS issues with modules, it's recommended to use a simple local server. If you have Python installed:
      ```bash
      # For Python 3
      python -m http.server
      ```
    - Open your browser and navigate to `http://localhost:8000`.

## Contributing

Contributions are welcome and encouraged! Please see the `CONTRIBUTING.md` file for guidelines on how to report bugs, suggest features, and submit pull requests.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
