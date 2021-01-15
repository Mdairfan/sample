# sampleimport mysql.connector

"""this is multi level 
comment"""
# python and mysql connectivity
mydb = mysql.connector.connect(host="localhost", user="root", passwd="Nmpnmp@1299", database="car")

# assigning cursor to variable
mycursor = mydb.cursor()

# calling execute function to run any mysql command
mycursor.execute("select Name from car_info")

# fetching all data from Name coloum
myresult = mycursor.fetchall()

for row in myresult:
    print(row)
