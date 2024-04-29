while True:
    tcls=int(input("Enter Total Class Conducted: "))
    tpre=int(input("Enter Total Class Attented: "))
    times = -1
    
    if tpre > tcls:
        print ("Bruhhh!! How is your attended class greater than total class..Just How?????\n")
    else:
        result = tpre/tcls*100
        result = round(result, 2)
        print(f"Attendance Percentage is {result}%", end=' , ')

        if result <75:
            print("Which is below 75%")
            while result < 75:
                result = tpre/tcls*100
                tpre += 1
                tcls += 1
                times += 1
        else:
            print ("Which is Awesome. \n")

        if times == 1:
            print (f"You will need to attend {times} class to attain 75% Attendance.\n")

        elif times <= 0:
            print ("")
        else:
            print(f"You need to attend {times} classes to attain 75% Attendance.\n")