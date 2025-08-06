
# 🎥 Movie Recommender System

This is a **content-based movie recommender system** built using Python and Streamlit that suggests the top 5 similar movies based on a selected title. It uses **cosine similarity** on preprocessed movie metadata and is optimized for fast performance using **Pickle** for serialization.


---

## 🔎 Project Overview

The project enables users to:

- Select any movie from a dropdown list.
- Get **5 instant recommendations** of similar movies.
- View suggestions in a clean, interactive **Streamlit web app**.
- Experience low-latency performance using precomputed similarity scores.

This app can be further extended with TMDB posters, genre filters, and hybrid recommendation logic (collaborative + content-based).

---

## Example Output
<img width="1912" height="921" alt="image" src="https://github.com/user-attachments/assets/df3fad67-15d0-402a-adad-acfb4f8c4cef" />

## 🛠️ My Contributions

 **Data Handling & Preprocessing:**
- Loaded and processed a movie metadata dataset.
- Engineered features (overview, genres, keywords, cast, crew) for similarity computation.
- Cleaned and transformed text data to build a unified "tags" column.

 **Model Development:**
- Applied **TF-IDF vectorization** (or CountVectorizer depending on version).
- Calculated **cosine similarity** between movies based on tags.
- Validated recommendation quality by checking semantic closeness of results.

 **Performance Optimization:**
- Serialized the movie DataFrame and similarity matrix using **Pickle**.
- Reduced runtime latency and improved app responsiveness.

 **Streamlit Frontend:**
- Built a responsive UI for movie selection and result display.
- Integrated dropdowns, buttons, and custom formatting using Streamlit components.
---

## 💻 Technologies Used

- **Python** (core logic)
- **Streamlit** (web framework)
- **Pickle** (for data serialization)
- **Pandas** & **NumPy** (data handling)
- **Scikit-learn** (similarity calculation)
- **Cosine Similarity** (ML model logic)

---

## 🗂️ Project Structure

```bash
movie-recommender/
├── main.py               # Streamlit app logic
├── movies.ipynb          # Notebook for feature engineering and similarity matrix creation
├── movie_list.pkl        # Serialized movie DataFrame
├── similarity.pkl        # Serialized similarity matrix
└── README.md             # You are here!
```
## 🧠 How the Recommendation Works
You select a movie title from the dropdown.

The app fetches its index in the DataFrame.

Cosine similarity scores are calculated with all other movies (precomputed).

Top 5 most similar movies (excluding the selected one) are fetched.

The list is displayed in the Streamlit interface.
