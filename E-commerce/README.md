# E-commerce Product Recommendation System

A Python-based recommendation engine that suggests products to users based on their purchase history and ratings, similar to Amazon's "Customers Also Bought" feature.

## 📝 Description

This project implements a collaborative filtering recommendation system for e-commerce products. It analyzes user purchase patterns and ratings to suggest products that users might be interested in purchasing.

### How It Works

1. **Data Collection**: 
   - Collects user purchase history and product ratings
   - Each user can rate products from 1-5 stars
   - Sample data includes computer accessories like laptops, monitors, mice, etc.

2. **Recommendation Process**:
   - Creates a user-product matrix from purchase data
   - Uses collaborative filtering to find similar products
   - Calculates recommendation scores using cosine similarity
   - Suggests products based on user's previous purchases

### Features

- Generates personalized product recommendations
- Analyzes user-product interaction patterns
- Visualizes purchase patterns through heatmaps
- Provides basic evaluation metrics

## 🚀 Installation

1. Clone this repository
2. Ensure you have Python installed
3. Install required packages:
```bash
pip install pandas numpy scikit-learn seaborn matplotlib
```

## 💻 Usage

Run the main script in Google Colab or Jupyter Notebook:
```python
# Import and run the system
from recommendation_system import main
main()
```

### Example Output
```
Creating sample e-commerce data...

Sample of purchase data:
   UserID        Product  Rating
0  User_1        Monitor       3
1  User_1     Power Bank       5
2  User_1         Laptop       2

Top recommended products:
Webcam: Score = 3.54
Mouse: Score = 3.49
USB Drive: Score = 3.41
```

## 🛠️ Technologies Used

- Python 3.x
- pandas: Data manipulation
- NumPy: Numerical computations
- scikit-learn: Similarity calculations
- seaborn/matplotlib: Visualization

## 📊 System Performance

- Successfully processes data for 5 users and 10 products
- Average recommendation relevance score: 3.5+
- Average system rating: 3.10 out of 5

## 🔄 Future Improvements

1. Add more sophisticated recommendation algorithms
2. Implement content-based filtering
3. Add real-time recommendation updates
4. Scale system for larger datasets
5. Add user interface for easier interaction

## 📚 What I Learned

- Implementing collaborative filtering algorithms
- Working with user-item matrices
- Calculating similarity between products
- Handling and analyzing user rating data
- Creating meaningful visualizations of recommendation patterns

## 👤 Author

Emmanuel Victor 
- GitHub: https://github.com/victor22-gif/victor-career-website.git
- LinkedIn: https://www.linkedin.com/in/victor-emmanuel-534043298?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
