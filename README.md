# QR-Code-Generator
Generates a list of QR Codes based on a particular CSV file.

Firstly, import the necessary modules:

```
import csv
import os
import pyqrcode
import png
```

Next, create an empty list and then initialize inputs from User-end. Create a new directory so as to save your QR Codes into it:

```
os.makedirs(''+folder_name+'')
```

Read the CSV File & Append the values into an empty list:

```
f = open(''+csv_file_name+'')
csv_f = csv.reader(f)

for row in csv_f:
  student_r_num.append(row[0])
```

Finally, pass each value from the list to generate the QR Codes:

```
for i in range(len(student_r_num)):
    qr_code = pyqrcode.create(''+c_code+'_'+student_r_num[i]+'')
    qr_code.png(''+student_r_num[i]+'.png', scale=6)
```
