# Book Recommender System Using Machine Learning

This project is a **Book Recommender System** built using **machine learning techniques**. The system provides personalized book recommendations based on user-selected input. It uses a collaborative filtering approach and displays recommended books along with their cover images.

## Features
- **Book Recommendation**: Suggests books similar to the one selected by the user.
- **Book Covers**: Displays the cover images of the recommended books.
- **Interactive UI**: Built with Streamlit for an intuitive user interface.
- **Efficient Search**: Leverages a pre-trained KNN model to find the nearest neighbors for recommendations.

---

## How It Works
1. **Model**:
   - A pre-trained KNN (K-Nearest Neighbors) model is used to calculate similarity between books.
   - The model is loaded from a serialized file using `pickle`.

2. **Data**:
   - Book titles, ratings, and pivot tables are preprocessed and stored as serialized files (`book_names.pkl`, `final_rating.pkl`, `book_pivot.pkl`).
   - Covers are fetched using URLs stored in the dataset.

3. **Recommendation Process**:
   - The user selects a book from a dropdown menu.
   - The system retrieves similar books using the trained KNN model.
   - It fetches the corresponding book covers from the dataset and displays them.

---

## Installation
### Prerequisites
- Python 3.7 or higher

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Chukwuemeka-James/Books-Recommender-System-Using-Machine-Learning.git
   cd Books-Recommender-System-Using-Machine-Learning
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

---

## Files in the Repository
- **`artifacts/`**:
  - Contains the serialized model and data files:
    - `model.pkl`: Pre-trained KNN model.
    - `book_names.pkl`: List of all book names.
    - `final_rating.pkl`: Preprocessed rating data.
    - `book_pivot.pkl`: Pivot table for collaborative filtering.

- **`app.py`**:
  - Main application file for the Streamlit UI.

---

## How to Use
1. Launch the app using the command:
   ```bash
   streamlit run app.py
   ```
2. Select a book from the dropdown menu.
3. Click **"Show Recommendation"**.
4. View the recommended books and their covers in a visually appealing layout.