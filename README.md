# 🎬 Movie Recommendation System using Neo4j Graph Database

## 📌 Project Overview
This project implements a graph-based movie recommendation system using **Neo4j** as the backend database. The system provides personalized movie suggestions by leveraging relationships between movies, actors, directors, genres, and user interactions. The frontend is built with modern web technologies (HTML5, CSS3, JavaScript) to create an interactive user experience.

---

## 🏫 Institution
**International University of Sarajevo**  
Course: Introduction to Database Management (Project II)  
Professor: Dr. Ali Abd Almisreb  
Students: Asja Bašović, Sara Avdić, Hatidža Imamović, Farah Mašić, Lana Hasanbegović  
Date: May 27, 2025

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Neo4j** | Graph database for storing and querying connected data |
| **HTML5** | Structure and semantics of the web application |
| **CSS3** | Styling, layout, and responsive design |
| **JavaScript** | Frontend interactivity and API communication |
| **Cypher Query Language** | Querying graph data in Neo4j |
| **VS Code** | Development environment |
| **Neo4j Desktop** | Local database management and visualization |

---

## 📊 Database Design

### Nodes:
- **Movie**: Contains attributes like `title`, `year`, `rating`, `director`, `star`, etc.
- **Genre**: Represents movie genres (e.g., Action, Comedy, Drama)
- **Company**: Production companies
- **User**: Users with `userID`, `username`, `email`, `hashed password`

### Relationships:
- `ACTED_IN` – Actor to Movie
- `DIRECTED` – Director to Movie
- `BELONGS_TO_GENRE` – Movie to Genre
- `PRODUCED_BY` – Movie to Company
- `LIKES` / `DISLIKES` – User to Movie

---

## 🔧 Implementation Highlights

### 1. **Data Preparation**
- Dataset sourced from [Kaggle Movie Industry Dataset](https://www.kaggle.com/datasets/danielgrijalvas/movies)
- Filtered to 100 movies for manageability
- CSV files prepared for nodes and relationships
- Synthetic user data generated for testing

### 2. **Graph Schema**
- Nodes: Movie, Genre, Company, User
- Relationships: ACTED_IN, DIRECTED, BELONGS_TO_GENRE, LIKES, DISLIKES
- Uniqueness constraints on IDs (movieID, userID)

### 3. **Web Application Features**
- Movie search and filtering
- Detailed movie pages
- User authentication (register/login)
- Like/Dislike interactions
- Personalized recommendation dashboard

### 4. **Recommendation Logic**
- Graph-based traversal using Cypher queries
- Recommendations based on:
  - User's liked movies
  - Shared genres/actors/directors
  - Popularity and ratings

### 5. **Security**
- Passwords hashed before storage
- Input validation on frontend and backend
- Role-based access control (admin vs. user)
- No plaintext credentials stored

---

## 🚀 How to Run Locally

### Prerequisites:
- Neo4j Desktop installed
- Modern web browser
- Basic web server (e.g., Live Server in VS Code)

### Steps:
1. **Import Data into Neo4j:**
   - Open Neo4j Desktop
   - Create a new database
   - Use `LOAD CSV` Cypher commands to import nodes and relationships

2. **Launch Frontend:**
   - Open the project folder in VS Code
   - Start a live server (e.g., using the "Live Server" extension)
   - Open `index.html` in your browser

3. **Connect Frontend to Neo4j:**
   - Configure the Neo4j JavaScript driver in `script.js`
   - Update connection credentials (URI, username, password)

---

## 📈 Scalability & Performance
- Graph model designed for efficient traversal
- Indexes on frequently queried properties (movieID, userID)
- Modular frontend and backend for easy scaling
- Neo4j's native graph processing handles complex relationships efficiently

---

## 🔮 Future Enhancements
- Integrate real-time data from streaming APIs
- Implement collaborative filtering
- Add machine learning for predictive recommendations
- Deploy to cloud (e.g., Neo4j Aura, Heroku, Netlify)
- Mobile-responsive design improvements

---

## 📚 References
- Neo4j Documentation & Blogs
- MDN Web Docs, CSS-Tricks, JavaScript.info
- Research papers on recommender systems and graph databases
- Kaggle dataset: "Movie Industry" by Daniel Grijalva

---

## 👥 Team Contribution
- **Asja Bašović, Sara Avdić, Hatidža Imamović, Farah Mašić, Lana Hasanbegović**
- Work included: data preprocessing, database design, frontend development, recommendation logic, testing, and documentation.

---

## 📄 License
Educational project for academic purposes at International University of Sarajevo.

---

*Built with ❤️ using Neo4j, HTML, CSS & JavaScript.*
