firstyear = (11,7,2019)
lastyear = (11,8,2022)
dateofYear = 0
dateofMonth = 0
date = 0

#tính số ngày giữa 2 năm
for i in range (firstyear[2],lastyear[2]):
    if (firstyear[2]==lastyear[2]):
        dateofYear = 0
    else:
        if ((i%4 == 0) and (i% 100 != 0) or (i % 400 ==0)):
            dateofYear +=366
            
        else:
            dateofYear +=365
            
#Tính số ngày giữa 2 tháng
a = [31,28,31,30,31,30,31,31,30,31,30,31]
if ((firstyear[2]%4 == 0) and (firstyear[2]% 100 != 0) or (firstyear[2] % 400 ==0)):
    a[1] = 29
if (firstyear[1] > lastyear[1] ):
    for i in range (lastyear[1],firstyear[1]):
        dateofMonth -= a[i-1]
else:
    for i in range (firstyear[1],lastyear[1]):
        dateofMonth += a[i-1]
#tính khoảng cách giữa 2 ngày
date = lastyear[0] - firstyear[0] + 1
tong = dateofYear + dateofMonth + date
print("Khoang cach giua 2 ngay la:", tong," ngay")

 
    
