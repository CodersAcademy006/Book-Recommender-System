# BookWise: Book Recommender System

BookWise is a modern, web-based Book Recommendation System that helps users discover their next favorite read. It leverages collaborative filtering and popularity-based algorithms to suggest books based on user input, and presents recommendations in a visually appealing, responsive interface.

---

## Features

- **Landing Page:**
  - Modern hero section with a call-to-action.
  - Top 50 most popular books displayed with cover, author, votes, and rating.
  - Responsive, visually rich Bootstrap 4 design.

- **Recommendation Page:**
  - Search for book recommendations by entering a book you like.
  - Personalized recommendations using collaborative filtering.
  - Each recommendation shows book cover and author.
  - Consistent, premium UI/UX.

- **Navigation & Footer:**
  - Clean navbar for easy navigation.
  - Footer with copyright and branding.

---

## Tech Stack

- **Backend:** Python (Flask)
- **Frontend:** HTML5, CSS3, Bootstrap 4, Google Fonts
- **Data:** Preprocessed book metadata and ratings (pickled files)
- **Deployment:** Ready for Heroku/Render/other cloud platforms

---

## Project Structure

```
Book-Recommender-System/
├── app.py                  # Main Flask application
├── requirements.txt        # Python dependencies
├── templates/
│   ├── index.html          # Landing page
│   └── recommend.html      # Recommendation page
├── books.pkl               # Book metadata (pickled)
├── popular.pkl             # Popular books data (pickled)
├── pt.pkl                  # Pivot table for recommendations (pickled)
├── similarity_scores.pkl   # Precomputed similarity matrix (pickled)
├── book-recommender-system.ipynb # Data processing notebook
├── Procfile                # For deployment
└── README.md               # Project documentation
```

---

## How It Works

1. **Landing Page:**
   - Shows the top 50 books based on popularity (votes & rating).
   - Data is loaded from `popular.pkl` and displayed in a grid of cards.

2. **Recommendation Page:**
   - User enters a book they like.
   - The system finds similar books using collaborative filtering (cosine similarity on a pivot table of users/books).
   - Recommendations are displayed with cover and author.

3. **Backend Logic:**
   - All data is preprocessed and stored as `.pkl` files for fast loading.
   - Flask handles routing and rendering of templates.

---

## Setup & Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/codersacademy006/Book-Recommender-System.git
   cd Book-Recommender-System
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the app:**
   ```bash
   python app.py
   ```
4. **Open in browser:**
   - Visit `http://127.0.0.1:5000/`

---

## Data Files

- `books.pkl`: Book metadata (title, author, image, etc.)
- `popular.pkl`: Top 50 popular books (used for landing page)
- `pt.pkl`: Pivot table (users x books) for collaborative filtering
- `similarity_scores.pkl`: Precomputed similarity matrix for fast recommendations

---

## Screenshots

### Landing Page
![Landing Page](https://user-images.githubusercontent.com/placeholder/landing-page.png)

### Recommendation Page
![Recommendation Page](https://user-images.githubusercontent.com/placeholder/recommend-page.png)

---

## Deployment

- The app is ready for deployment on Heroku, Render, or any cloud platform supporting Python/Flask.
- Use the provided `Procfile` for Heroku deployment.

---

## Customization

- You can update the look and feel by editing the Bootstrap and CSS in `index.html` and `recommend.html`.
- To use your own data, replace the `.pkl` files with your processed datasets.

---

## License

This project is licensed under the MIT License.

---

## Credits

- Book cover images and metadata: [Open Library](https://openlibrary.org/), [Goodreads](https://goodreads.com/) (if used)
- UI: Bootstrap 4, Google Fonts
- Developed by [Your Name]

---

## Contact

For questions or suggestions, open an issue or contact the maintainer.
