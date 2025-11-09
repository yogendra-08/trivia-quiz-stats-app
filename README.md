# 🎯 Trivia Quiz Stats App

> Test your knowledge with live trivia questions and track your performance with advanced statistics

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

---

## 📖 About The Project

**Trivia Quiz Stats App** is an interactive desktop application that brings the excitement of trivia quizzes right to your computer. Built with Python, this application fetches real-time questions from the Open Trivia Database API and provides detailed statistical analysis of your performance using industry-standard data science libraries.

### ✨ Key Highlights

- 🌐 **Live API Integration** - Thousands of questions across 25+ categories
- 📊 **Statistical Analysis** - Mean, Median, Mode calculations using SciPy
- 💾 **Data Persistence** - Quiz history stored and analyzed with Pandas
- 🎨 **Beautiful GUI** - Clean, modern interface built with Tkinter
- 📈 **Performance Tracking** - Track your progress over time
- 🎓 **Educational** - Perfect for learning Python, APIs, and data analysis

---

## 🚀 Features

### Quiz Features
- ✅ **25+ Categories** - General Knowledge, Science, History, Sports, and more
- ✅ **3 Difficulty Levels** - Easy, Medium, Hard
- ✅ **Customizable** - Choose 5-20 questions per quiz
- ✅ **Real-time Feedback** - Instant answer validation
- ✅ **Progress Tracking** - See your current position in the quiz

### Statistical Features
- 📊 **Mean Score** - Average performance across all quizzes
- 📊 **Median Score** - Middle value of all your scores
- 📊 **Mode Score** - Your most frequently achieved score
- 📊 **Accuracy Rate** - Overall percentage of correct answers
- 📊 **Performance Trends** - Best and worst scores
- 📊 **Quiz History** - View recent attempts with details

### Technical Features
- 🔄 **Error Handling** - Graceful handling of network issues
- 💾 **CSV Storage** - All data stored in easy-to-access format
- 🧪 **Modular Design** - Clean, maintainable code structure
- 📱 **Responsive UI** - Smooth user experience

---

## 🛠️ Technologies Used

| Technology | Purpose | Version |
|------------|---------|---------|
| **Python** | Core programming language | 3.8+ |
| **Tkinter** | GUI framework | Built-in |
| **Requests** | HTTP library for API calls | 2.31.0 |
| **Pandas** | Data manipulation and storage | 2.1.0 |
| **SciPy** | Statistical calculations (Mode) | 1.11.0 |
| **NumPy** | Numerical operations | 1.25.0 |

---

## 📋 Prerequisites

Before running this project, make sure you have:

- **Python 3.8 or higher** installed
- **pip** (Python package manager)
- **Internet connection** (for fetching quiz questions)
- **Basic Python knowledge** (if you want to modify the code)

---

## 🔧 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/trivia-quiz-stats-app.git
cd trivia-quiz-stats-app
```

### Step 2: Create Virtual Environment (Recommended)

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Run the Application

```bash
python main.py
```

---

## 📦 Project Structure

```
trivia-quiz-stats-app/
│
├── main.py                 # Main GUI application (Entry point)
├── quiz_app.py            # Quiz logic and API handler
├── stats_manager.py       # Statistical analysis module
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── LICENSE               # MIT License
├── .gitignore           # Git ignore rules
│
├── data/
│   └── quiz_history.csv  # Stores all quiz attempts (auto-generated)
│
└── assets/              # Screenshots and images (optional)
    └── .gitkeep
```

---

## 🎮 How to Use

### 1️⃣ Launch Application
Run `python main.py` to start the app. You'll see the main menu.

### 2️⃣ Start a Quiz
- Click **"Start Quiz"**
- Select your preferred category (or choose "Any Category")
- Choose difficulty level (Easy/Medium/Hard)
- Set number of questions (5-20)
- Click **"Start Quiz"** to begin

### 3️⃣ Answer Questions
- Read each question carefully
- Select one of the four options
- Click **"Submit Answer"**
- Get instant feedback (Correct ✅ or Incorrect ❌)
- Continue until quiz completion

### 4️⃣ View Results
- See your final score percentage
- Review correct vs incorrect answers
- Check time taken
- Get performance feedback

### 5️⃣ Track Statistics
- Click **"View Statistics"** from main menu
- See comprehensive performance metrics:
  - Mean, Median, Mode scores
  - Overall accuracy
  - Best and worst performances
  - Recent quiz history

---

## 📊 API Information

This project uses the **Open Trivia Database API**:

- **API URL:** https://opentdb.com/
- **Documentation:** https://opentdb.com/api_config.php
- **Free to use** - No API key required
- **Rate Limit:** 1 request per 5 seconds
- **Question Types:** Multiple Choice
- **Categories:** 24 different categories
- **Difficulties:** Easy, Medium, Hard

### Available Categories:
- General Knowledge
- Books, Film, Music
- Television, Video Games
- Science & Nature, Computers
- Mathematics, Mythology
- Sports, Geography, History
- Politics, Art, Celebrities
- Animals, Vehicles, Comics
- And more...

---

## 💡 Code Modules Explained

### 1. `main.py` - GUI Application
**Purpose:** Main application interface and user interaction

**Key Components:**
- `QuizGUI` class - Main application controller
- `show_main_menu()` - Display home screen
- `show_quiz_setup()` - Quiz configuration window
- `show_quiz_window()` - Question display interface
- `show_results()` - Score and performance display
- `show_statistics()` - Statistical analysis window

### 2. `quiz_app.py` - Quiz Logic
**Purpose:** Handle API requests and quiz functionality

**Key Components:**
- `QuizApp` class - Quiz controller
- `fetch_questions()` - Get questions from API
- `get_current_question()` - Retrieve active question
- `check_answer()` - Validate user's answer
- `calculate_percentage()` - Compute score
- `get_quiz_summary()` - Generate results data

### 3. `stats_manager.py` - Statistics Module
**Purpose:** Manage data storage and statistical analysis

**Key Components:**
- `StatsManager` class - Statistics controller
- `save_quiz_result()` - Store quiz data to CSV
- `calculate_mean_score()` - Compute average (NumPy)
- `calculate_median_score()` - Find middle value (NumPy)
- `calculate_mode_score()` - Most frequent score (SciPy)
- `get_statistics_summary()` - Complete stats overview

---

## 🧪 Testing

### Manual Testing
1. **Test API Connection:**
   ```bash
   python quiz_app.py
   ```

2. **Test Statistics Module:**
   ```bash
   python stats_manager.py
   ```

3. **Test Full Application:**
   ```bash
   python main.py
   ```

### Test Checklist
- [ ] Application launches without errors
- [ ] Can fetch questions from API
- [ ] Can select different categories
- [ ] Can answer questions and see feedback
- [ ] Results page displays correctly
- [ ] Statistics calculate properly
- [ ] Data saves to CSV file
- [ ] Can view quiz history

---

## 🐛 Troubleshooting

### Common Issues

**1. Module Not Found Error**
```
Error: No module named 'pandas'
```
**Solution:** Install dependencies
```bash
pip install -r requirements.txt
```

**2. API Connection Error**
```
Error: Failed to fetch questions
```
**Solution:** 
- Check your internet connection
- Try again (API might be temporarily down)
- Verify API URL is accessible

**3. CSV File Error**
```
Error: Permission denied
```
**Solution:**
- Make sure `data/` folder exists
- Check write permissions
- Close any programs using the CSV file

**4. Tkinter Not Found**
```
Error: No module named 'tkinter'
```
**Solution:**
- Tkinter comes with Python, reinstall Python
- On Linux: `sudo apt-get install python3-tk`

---

## 📈 Future Enhancements

Planned features for future versions:

- [ ] 🕐 Timer for each question
- [ ] 🏆 Leaderboard system
- [ ] 👥 Multiplayer mode
- [ ] 📊 Data visualization with charts
- [ ] 📄 Export statistics as PDF
- [ ] 🎨 Theme customization
- [ ] 🔊 Sound effects
- [ ] 🌍 Multiple language support
- [ ] ☁️ Cloud data synchronization
- [ ] 📱 Mobile responsive design

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


---

## 🙏 Acknowledgments

- [Open Trivia Database](https://opentdb.com/) - For providing free trivia questions API
- [Python Software Foundation](https://www.python.org/) - For Python programming language
- [Tkinter](https://docs.python.org/3/library/tkinter.html) - For GUI framework
- [Pandas](https://pandas.pydata.org/) - For data manipulation
- [SciPy](https://scipy.org/) - For statistical functions
- [NumPy](https://numpy.org/) - For numerical operations


---

## ⭐ Show Your Support

If you found this project helpful, please give it a ⭐ on GitHub!

---

## 📸 Screenshots

*(Add screenshots of your application here)*

### Main Menu
![Main Menu](assets/main_menu.png)

### Quiz Interface
![Quiz](assets/quiz_interface.png)

### Statistics Dashboard
![Statistics](assets/statistics.png)

---

<div align="center">


[Report Bug](https://github.com/yourusername/trivia-quiz-stats-app/issues) · [Request Feature](https://github.com/yourusername/trivia-quiz-stats-app/issues)

</div>