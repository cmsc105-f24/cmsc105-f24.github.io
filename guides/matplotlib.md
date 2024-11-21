---
layout: default  
permalink: /guides/matplotlib  
title: Matplotlib Guide  

---

# Matplotlib Guide

This guide provides an overview of common Matplotlib features for creating visualizations in Python. For detailed documentation, refer to the [Matplotlib Official Guide](https://matplotlib.org/stable/contents.html).

---

### **1. `plot(x, y)`**
   - **Description**: Creates a line plot of `y` versus `x`.
   - **Parameters**:  
     - `x`: Sequence of x-coordinates.
     - `y`: Sequence of y-coordinates.
     - `label` (optional): Adds a label for the plot.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     x = [1, 2, 3, 4]
     y = [10, 20, 25, 30]
     plt.plot(x, y, label='Line 1')
     plt.legend()
     plt.show()
     ```

---

### **2. `scatter(x, y)`**
   - **Description**: Creates a scatter plot of `y` versus `x`.
   - **Parameters**:  
     - `x`: Sequence of x-coordinates.
     - `y`: Sequence of y-coordinates.
     - `color` (optional): Marker color.
     - `size` (optional): Marker size.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     x = [1, 2, 3, 4]
     y = [10, 20, 25, 30]
     plt.scatter(x, y, color='red')
     plt.show()
     ```

---

### **3. `bar(x, height)`**
   - **Description**: Creates a bar chart.
   - **Parameters**:  
     - `x`: Sequence of x-coordinates (categories).
     - `height`: Heights of the bars.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     categories = ['A', 'B', 'C']
     values = [10, 20, 15]
     plt.bar(categories, values)
     plt.show()
     ```

---

### **4. `hist(data, bins)`**
   - **Description**: Plots a histogram to display the distribution of data.
   - **Parameters**:  
     - `data`: Sequence of data points.
     - `bins` (optional): Number of bins for the histogram.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     data = [1, 1, 2, 3, 3, 3, 4, 5, 5]
     plt.hist(data, bins=5)
     plt.show()
     ```

---

### **5. `pie(sizes)`**
   - **Description**: Creates a pie chart.
   - **Parameters**:  
     - `sizes`: Data for the pie segments.
     - `labels` (optional): Labels for the segments.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     sizes = [10, 20, 30]
     labels = ['A', 'B', 'C']
     plt.pie(sizes, labels=labels)
     plt.show()
     ```

---

### **6. `xlabel(label)` and `ylabel(label)`**
   - **Description**: Adds labels to the x-axis and y-axis.
   - **Parameters**:  
     - `label`: Text for the axis label.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     plt.plot([1, 2, 3], [4, 5, 6])
     plt.xlabel('X-axis')
     plt.ylabel('Y-axis')
     plt.show()
     ```

---

### **7. `title(label)`**
   - **Description**: Adds a title to the plot.
   - **Parameters**:  
     - `label`: Text for the title.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     plt.plot([1, 2, 3], [4, 5, 6])
     plt.title('My Plot')
     plt.show()
     ```

---

### **8. `legend()`**
   - **Description**: Displays a legend for labeled plots.
   - **Parameters**: None (optional configuration through `loc` for position).
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     plt.plot([1, 2, 3], [4, 5, 6], label='Line 1')
     plt.legend(loc='upper left')
     plt.show()
     ```

---

### **9. `savefig(filename)`**
   - **Description**: Saves the current plot to a file.
   - **Parameters**:  
     - `filename`: Path or name of the file to save.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     plt.plot([1, 2, 3], [4, 5, 6])
     plt.savefig('my_plot.png')
     ```

---

### **10. `show()`**
   - **Description**: Displays the plot.
   - **Parameters**: None.
   - **Example**:
     ```python
     import matplotlib.pyplot as plt
     plt.plot([1, 2, 3], [4, 5, 6])
     plt.show()
     ```
