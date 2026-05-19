# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline

# ---------------- LINE GRAPH ----------------

x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]

# Create a line graph
plt.plot(x, y, label="Line Graph", color="blue", marker="o")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Simple Line Graph")
plt.show()


# line 1 points
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]

# plot line 1 and line 2 points in same graph
plt.plot(x1, y1, label="line 1", color="red")
plt.plot(x2, y2, label="line 2", color="green")

# plot the points in above graph
plt.scatter(x1, y1, color="red")
plt.scatter(x2, y2, color="green")

plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Two Line Graph")
plt.show()


# fill between
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]

plt.plot(x_values, y_values)
plt.fill_between(x_values, y_values, color="lightblue", alpha=0.5)
plt.title("Fill Between Graph")
plt.show()


# interpolate data using cubic spline
x = np.array([1,2,3,4,5,6,7,8,9,10])
y = np.array([2,4,5,7,8,8,9,10,11,12])

x_new = np.linspace(x.min(), x.max(), 300)
spl = make_interp_spline(x, y, k=3)
y_smooth = spl(x_new)

plt.plot(x_new, y_smooth)
plt.title("Smooth Curve")
plt.show()


# ---------------- BAR GRAPH ----------------

values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]

# Create bar graph
plt.bar(names, values, color='orange')
plt.xlabel("Names")
plt.ylabel("Values")
plt.title("Bar Graph")
plt.show()


c1 = ['red', 'green', 'blue', 'yellow', 'purple']

# plot a bar chart
plt.bar(names, values, color=c1)
plt.show()


df = sns.load_dataset("tips")

avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()

plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')

plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()


# ---------------- SCATTER PLOT ----------------

x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]

# Create scatter plot
plt.scatter(x_values, y_values)
plt.title("Scatter Plot")
plt.show()


# x-axis values
x = [1,2,3,4,5,6,7,8,9,10]
# y-axis values
y = [2,4,5,7,6,8,9,11,12,12]

# plot scatter with parameters
plt.scatter(x, y, label="stars", color="green", marker="*", s=30)

# labels
plt.xlabel("X Axis")
plt.ylabel("Y Axis")

# title and legend
plt.title("Scatter Plot with Stars")
plt.legend()
plt.show()


# ---------------- PIE CHART ----------------

# defining labels
activities = ['eat', 'sleep', 'work', 'play']
# portion covered by each label
slices = [3, 7, 8, 6]
# color for each label
colors = ['r', 'y', 'g', 'b']

# plot pie chart
plt.pie(slices, labels=activities, colors=colors, autopct='%1.1f%%', startangle=90)
plt.title("Pie Chart")
plt.show()
```
<img width="532" height="387" alt="image" src="https://github.com/user-attachments/assets/6d521533-53a4-4f83-88d2-2cbeb4091927" />




<img width="621" height="377" alt="image" src="https://github.com/user-attachments/assets/c9827a49-c954-4257-ba73-b1db10278d20" />


<img width="570" height="357" alt="image" src="https://github.com/user-attachments/assets/20591ae6-f983-4af8-8054-5a6484299f67" />

<img width="483" height="368" alt="image" src="https://github.com/user-attachments/assets/d76431b3-0e06-4f8e-8ac2-435c9767d4c8" />


<img width="546" height="370" alt="image" src="https://github.com/user-attachments/assets/c129953c-180d-4752-aa4e-7829651d3787" />

<img width="537" height="347" alt="image" src="https://github.com/user-attachments/assets/f67890af-3222-4326-a41a-169a248ef26c" />

<img width="680" height="467" alt="image" src="https://github.com/user-attachments/assets/51e1bf4a-634e-4dab-ac25-63ff5e8245ee" />


<img width="541" height="362" alt="image" src="https://github.com/user-attachments/assets/50d494bf-848d-464e-849e-6f25683241e3" />

<img width="533" height="376" alt="image" src="https://github.com/user-attachments/assets/64e11330-c214-4ef2-b8e6-6be095d50b07" />



<img width="418" height="341" alt="image" src="https://github.com/user-attachments/assets/07b3cbe8-153f-4a35-9a0c-4adfaca89208" />

# Result:
Thus the data visualization using matplot library is successfully executed.

