# Realtimemedianfinder
This is a console based project which is built in java

# 📊 Running Median Finder Using Two Heaps (Java)

## 📌 Project Overview

The **Running Median Finder** is a Java-based console application that calculates the median of a stream of integers dynamically as numbers are entered.

Instead of sorting the entire collection every time a new number arrives, the application uses two Priority Queues (Heaps) to efficiently maintain the median.

The approach divides the numbers into two halves:

- **Max Heap:** Stores the smaller half of the numbers.
- **Min Heap:** Stores the larger half of the numbers.

By balancing these two heaps after every insertion, the median can be calculated efficiently without sorting the complete dataset.

## 🚀 Features

- **Dynamic Input:** Accepts numbers continuously from the user.
- **Real-Time Median:** Calculates the median after every insertion.
- **Two-Heap Approach:** Uses a Max Heap and Min Heap to maintain sorted halves.
- **Automatic Balancing:** Maintains the size difference between the heaps.
- **Heap Visualization:** Displays the contents of both heaps after each insertion.
- **Input Validation:** Handles invalid inputs without terminating the application.
- **Interactive Console:** Supports the `exit` command to stop execution.

## 🛠️ Technologies Used

- Java
- PriorityQueue
- Max Heap and Min Heap
- Java Collections Framework
- Object-Oriented Programming (OOP)

## 🧠 Algorithm Explanation

The application uses two heaps to maintain the running median.

### 1. Max Heap (Lower Half)

Stores the smaller half of the input numbers.

- The largest element of the lower half stays at the root.
- Provides quick access to the maximum element of the lower half.

### 2. Min Heap (Upper Half)

Stores the larger half of the input numbers.

- The smallest element of the upper half stays at the root.
- Provides quick access to the minimum element of the upper half.

### 3. Heap Balancing

After inserting a number:

1. If the number is smaller than or equal to the maximum of the lower half, insert it into the Max Heap.
2. Otherwise, insert it into the Min Heap.
3. Balance the heaps to ensure the Max Heap has either the same number of elements as the Min Heap or exactly one extra element.

### 4. Median Calculation

- If both heaps contain an equal number of elements, the median is the average of their root elements.
- If the Max Heap contains one extra element, its root is the median.

## 📂 Project Structure

```text
Running-Median/
│
├── RunningMedian.java
└── README.md
```

## ▶️ How to Run

**Step 1: Clone the repository**

```bash
git clone <your-repository-url>
```

**Step 2: Navigate to the project directory**

```bash
cd Running-Median
```

**Step 3: Compile the Java file**

```bash
javac RunningMedian.java
```

**Step 4: Execute the application**

```bash
java RunningMedian
```

## 💻 Sample Execution

```text
Enter number (or 'exit'): 5
Max Heap (Left): [5]
Min Heap (Right): []
Current Median: 5.0

Enter number (or 'exit'): 2
Max Heap (Left): [2]
Min Heap (Right): [5]
Current Median: 3.5

Enter number (or 'exit'): 8
Max Heap (Left): [5, 2]
Min Heap (Right): [8]
Current Median: 5.0

Enter number (or 'exit'): 10
Max Heap (Left): [5, 2]
Min Heap (Right): [8, 10]
Current Median: 6.5

Enter number (or 'exit'): exit
Exiting...
```

## ⏱️ Time and Space Complexity

Let N represent the total number of elements inserted.

| Operation | Time Complexity |
|---|---|
| Insert a number | O(log N) |
| Balance heaps | O(log N) |
| Retrieve median | O(1) |
| Display heaps | O(N) |

**Overall Space Complexity:** O(N), since both heaps store all inserted elements.

## 🎯 Learning Outcomes

- Understanding the Running Median problem.
- Implementing Max Heap and Min Heap using Java PriorityQueue.
- Understanding heap insertion and deletion operations.
- Learning how to balance two heaps efficiently.
- Applying data structures to solve streaming-data problems.
- Optimizing median calculation without repeatedly sorting an array.

## 🔮 Future Enhancements

- Develop a graphical interface using HTML, CSS, and JavaScript.
- Visualize heap operations step by step.
- Add support for reading numbers from files.
- Display the median progression using a graph.
- Extend the application to handle larger data streams.

## 👨‍💻 Author

**Bharath Chandra**

