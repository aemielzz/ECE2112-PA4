## Experiment 4
## DATA WRANGLING AND DATA VISUALIZATION
##### Amiel Elestin M. Cruz
##### 2ECE-D
## ECE BOARD EXAM PROBLEM: 
![image](https://github.com/user-attachments/assets/f854a14a-2c9c-4aef-95d7-603ac9c38a77)

First, when using pandas, it is mandatory to input "Import pandas as pd" to access pandas library

___ECE BOARD EXAM PROBLEM: Using data wrangling and data visualization technique with
storytelling, analyze the data and present different (i) data frames; and (ii) visuals using the dataset given.___

1. Create the following data frames based on the format provided:


![image](https://github.com/user-attachments/assets/c4f46f6f-8fae-469b-9cfd-c246f6465ee9)

After declaring import pandas as pd, I declared the boards as pd.read_csv('board2.csv') to read the boards file that I downloaded, and for me to use easily, I will use it to declare for my next codes. Commanding pd.read_csv(file) will automatically read the file that I downloaded in the same folder with the same format and encoded 'board2' to print the file in tabular form.

__a. Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon__


![image](https://github.com/user-attachments/assets/df1697bb-fd59-46b8-b807-678e0b0f42bb)

Based on the instructions above, the file name should be Instru, so I declared the boards.loc(to locate something) as Instru, and then the data that needs to be displayed is for students who have a grade higher than 70 in electronics, the track is constant instrumentation, and his/her hometown is Luzon. That's why I used  "(boards['Electronics']>70)" to look for students who got 70 in electronics, and I used "&" to add another condition, which is  (boards['Hometown']=='Luzon') to look for students whose hometown is Luzon and got 70 above grades in electronics. I added "&" again to add another condition, which is (boards['Track']=='Instrumentation') to look for students whose track is instrumentation. This will sort out the data, and this will show the table that contains the students whose hometown is Luzon, higher than 70 grade in electronics, and its track is instrumentation. Lastly, the tabular data should only display the name, GEAS grade, and electronics grade of the students, so I encoded this "['Name,' 'GEAS,' 'Electronics']" and encoded Instru to display the data below.

__b. Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is
constant as Mindanao and gender Female__


![image](https://github.com/user-attachments/assets/ec340855-7352-4a02-82da-c6c3e3955c9d)

In part B. for this problem, we need to get the average scores of every student. I declared boards['Average'] as the average of all the subjects I encoded "boards[['Math','Electronics','GEAS','Communication']].mean(axis=1)" to average the scores of every student's math, electronics, geas, and communication scores. I inputted mean because it would get the average and "axis=1" to find the mean of every row. I encoded boards once again to print the new table with the average of every student.

![image](https://github.com/user-attachments/assets/7974e616-1f46-4e0b-9621-38f98a3beae8)


Next, based on the instructions above, the file name should be Mindy, so I declared the boards.loc(to locate something) as Mindy then the data that needs to be displayed is for students who have an average grade higher than 55 in all subjects, her hometown is Mindanao, and her gender is female. That's why I used (boards['Hometown']=='Mindanao') To look for students who are from Mindanao and I used "&" to add another condition which is (boards['Gender']=='Female')" to look for Female students. I used "&" again to add another condition, which is  "(boards['Average']>=55)" to look for students whose average is equal to or greater than 55. This will sort out the data, and this will display the table that contains the students whose hometown is Mindanao, whose Average grades are equal to and greater than 55 grade in all the subjects, and a female. Lastly, the tabular data should only display the name, track, electronics grade, and the average grade of the students so I encoded this['Name', 'Track', 'Electronics','Average']] and I encoded Mindy to print the table.

2. Create a visualization that shows how the different features contributes to average grade. Does
chosen track in college, gender, or hometown contributes to a higher average score?

![image](https://github.com/user-attachments/assets/27a19ad2-8851-491c-a93f-ab4be6a31009)

Before I discuss problem number 2, first, I import matplotlib.pyplot as plt for us to access and for us to be allowed to use graphs and charts. Since the 2nd problem is a table or a visualization using graphs, Now I encoded plt.figure(figsize=(15, 10)) to choose the size of my bar graph. Since the question is whether the chosen track, gender, or hometown contributes to a higher average score, we will sort out and display a table for every aspect. I inputted plt.bar(boards['Hometown'], boards['Average'], color = '#98fb98') to differentiate which hometown has the highest average scores, color, and reference number to change the color to my own preference. The bar graph shows that Luzon has the highest average scores on board; the second is Visayas, and the 3rd is Luzon. Therefore, this table shows that the highest number of students who aced this exam are from Luzon. 

![image](https://github.com/user-attachments/assets/c9ddafd7-0978-4b57-9e47-a14faa8fd49f)
For the 2nd bar graph, I encoded plt.figure(figsize=(15, 10)) to choose the size of my bar graph. Since the question is whether the chosen track, gender, or hometown contributes to a higher average score, we will sort out and display a table for every aspect. I inputted plt.bar(boards['Track'], boards['Average'], color = '#98fb98') to differentiate which college track has the highest average scores, color, and reference number to change the color to my own preference. The bar graph shows that among the college tracks, microelectronics has the highest average scores on board, the second is communication, and the 3rd is instrumentation. Therefore, this table shows that the highest student who aced this exam is from Luzon, and the track he/she chose is Microelectronics. 

![image](https://github.com/user-attachments/assets/eb89959b-5be4-43f8-8845-85dc228fb2cc)
For the 3rd bar graph, I encoded plt.figure(figsize=(15, 10)) to choose the size of my bar graph. Since the question is whether the chosen track, gender, or hometown contributes to a higher average score, we will sort out and display a table of every aspect. plt.bar(boards['Gender'], boards['Average'], color = '#98fb98') to differ which Gender has the highest average scores, color, and reference number to change the color to my own preference. The bar graph shows that between males and females, the one with the highest score is a female. Therefore, this table shows that the highest student who aced this exam is from Luzon, and the track she chose is Microelectronics, and she is a female. 






