#  Machine Learning — Decision Tree Classification Models

### 📘 Programming Assignment
This repository contains implementations and analysis of three Decision Tree algorithms — **ID3**, **CART**, and **C4.5** — including their complexity and overfitting/underfitting behavior.

---

## 🔹 Analysis of ID3 Model

### **Complexity**
- **Time Complexity:** O(m × n log n), where *m* = number of attributes and *n* = number of records  
- **Worst Case:** O(m × n²) when all attributes are evaluated at every node  
- **Space Complexity:** O(n × m) for storing feature values, entropy calculations, and recursive structures  
> Overall efficient for small to medium datasets, but performance decreases for large data due to repeated entropy computation.

### **Overfitting**
ID3 often overfits because it splits until all leaves are pure, learning noise in the training data. Pruning or limiting tree depth can reduce overfitting.

### **Underfitting**
Underfitting occurs when the tree is too shallow or important features are ignored. Balancing tree depth helps maintain generalization.

---

## 🔹 Analysis of CART Model

### **Complexity**
- **Time Complexity:** O(m × n log n) for categorical features  
- **Worst Case:** O(m × n²) when all attributes are scanned at each node  
- **Space Complexity:** O(n × m) for storing nodes (≈ 2n–1) and temporary subsets  
> Overall, CART is efficient but can be computationally heavier for very large datasets.

### **Overfitting**
CART overfits when the tree grows too deep, fitting noise in training data. It can be controlled using pruning or parameters like `max_depth`.

### **Underfitting**
Occurs when the tree is too simple or restricted, missing patterns in data. Allowing deeper trees or relaxed splitting criteria helps.

---

## 🔹 Analysis of C4.5 Model

### **Complexity**
- **Time Complexity:** O(m × n log n), with *m* attributes and *n* samples  
- **Worst Case:** O(m × n²) due to repeated entropy and gain ratio calculations  
- **Space Complexity:** O(n × m) for subset storage and recursion  
> Efficient for small to medium datasets with balanced trade-off between accuracy and computation.

### **Overfitting**
C4.5 may overfit by fully purifying leaves without pruning, leading to high training accuracy but lower test performance. Controlled pruning helps mitigate this.

### **Underfitting**
Rare, since C4.5 explores most attribute splits. Underfitting only happens if tree depth is restricted or pruning is excessive.

---

### 👩‍💻 Author
**Happy Kumari**    
NIT Silchar
