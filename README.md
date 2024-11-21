# C++ Developer Technical Assessment
**Duration:** 4 hours  
**Level:** Junior (0-2 years experience)

## 👋 Introduction
Hi there! This is a practical coding exercise to assess your C++ skills. Don't worry - we're not expecting perfect code, just a demonstration of your problem-solving approach and coding style. The task involves working with financial market data, but no prior finance knowledge is required.

## 🎯 What You'll Build
You'll create a program that processes market data (think of it as stock price updates). The program will:
- Read price updates from a file
- Calculate some basic statistics
- Store and retrieve the data efficiently

## 📝 Tasks Breakdown

### Task 1: Building the Basic Structure (1 hour)
Create a class to hold market data with these simple fields:
```cpp
class MarketTick {
    string symbol;     // Stock symbol like "AAPL" (max 20 chars)
    double price;      // Current price, e.g., 150.25
    int volume;        // Number of shares traded
    uint64_t timestamp; // When this happened (Unix timestamp in seconds)
};
```

What to implement:
- ✅ Constructors to create new MarketTick objects
- ✅ Ways to get and set the values (getters/setters)
- ✅ Basic checks (price can't be negative, etc.)
- ✅ Ways to compare two MarketTicks (for sorting)

### Task 2: Data Processing (2 hours)
Create a class that can:
1. Store multiple price updates for different stocks
2. Calculate these values:
   - VWAP (Average price weighted by volume)
   - Highest and lowest prices in a time range
   - Moving average (average of last N prices)

Here's what these calculations mean:
```
VWAP = Σ(Price × Volume) ÷ Σ(Volume)
Example: 
- Update 1: $100 × 50 shares = $5000
- Update 2: $101 × 100 shares = $10100
VWAP = $15100 ÷ 150 = $100.67

Moving Average (last 3 prices):
Prices: 100, 101, 102, 103, 104
3-point moving average at end: (102 + 103 + 104) ÷ 3 = 103
```

### Task 3: File Handling and Testing (1 hour)
Make your program:
1. Read data from CSV files like this:
```csv
symbol,price,volume,timestamp
AAPL,150.25,100,1637142400
MSFT,290.50,200,1637142400
AAPL,150.50,150,1637142460
```

2. Write results to a file
3. Include basic tests to make sure everything works

## 🛠️ Technical Requirements
- Use C++11 or newer
- Use standard C++ containers (vector, map, etc.)
- Handle errors gracefully
- Write clean, well-commented code

## ⭐ Bonus Points (Optional)
If you finish early, you could:
- Make it safe for multiple threads to use
- Add timing measurements to see how fast it runs

## 📊 How We'll Evaluate
- 25% - Is the code well-organized and easy to understand?
- 30% - Good use of C++ features (containers, classes, etc.)
- 20% - How well does it handle errors and edge cases?
- 15% - Is performance considered?
- 10% - Are there good tests?

## 🚀 Getting Started
Here's some starter code:
```cpp
class MarketTick {
public:
    // Constructor - create a new market tick
    MarketTick(std::string symbol, double price, int volume, uint64_t timestamp) {
        // TODO: Implement this
    }
    
    // Add your other methods here
};

class MarketDataProcessor {
public:
    // Add a new price update
    void addTick(const MarketTick& tick) {
        // TODO: Implement this
    }
    
    // Calculate VWAP for a symbol
    double calculateVWAP(const std::string& symbol) {
        // TODO: Implement this
        return 0.0;
    }
    
    // Calculate moving average
    double calculateSMA(const std::string& symbol, int n) {
        // TODO: Implement this
        return 0.0;
    }
};
```

## 📫 How to Submit
1. Share your code via:
   - GitHub repository link (preferred)
   - Zip file with your code

2. Include a README file that explains:
   - How to build and run your code
   - Any important decisions you made
   - Any assumptions you made

3. Include some test data and example outputs

## 💡 Tips for Success
- Start with the basics and get them working before adding advanced features
- Comment your code to explain your thinking
- Don't worry if you can't finish everything - we're interested in your approach
- Ask questions if anything is unclear!

## 🤔 Questions?
If anything's unclear, please don't hesitate to ask for clarification. Good luck!