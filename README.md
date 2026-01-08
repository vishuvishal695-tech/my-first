# my-first
expense tracker using ,dictionalr , for and whileloop,sets
#EXPENSE TRACKER CODE
Expenseslist=[] # list of expnses in the form of dictionary 
print("welcome to expense tracker")


while True:
    print("===MENU===")
    print("1.Add expenses")
    print("2.View expenses")
    print("3.View total expenses")
    print("4.Exit")

    choice=int(input("Please enter your choice : "))
#1.Add Expenses
    if(choice ==1):
      Date=input("Please eneter the date : ")
      Category=input("Enter the Category(food, travel , shopping,etc) :")
      Discription=input("Give details : ") 
      Amount=float(input("Eneter the amount :"))

      Expenses={
        "Date":Date,
        "Category":Category,
        "Discription":Discription,
        "Amount":Amount
        }
      Expenseslist.append(Expenses)
      print("expenses added succesfully")

#2.VIEW ALL EXPENSES
    elif(choice ==2):
        if(len(Expenseslist)==0):
            print("No expensese added ,kindely go back and add expenses ")
        else:
          print("This is your expenses so far")
          count=1
          for eachexpenses in Expenseslist:
              print(f"expense Number {count} ->{eachexpenses["Date"]},{eachexpenses["Category"]},{eachexpenses["Discription"]},{eachexpenses["Amount"]}")
              count= count+1 
            

#3.VIEW TOTAL EXPENSES
    elif(choice==3):
        total=0
        for eachexpenses in Expenseslist:
          total= total+eachexpenses["Amount"]
       
          print("\n Total Expenses=", total)
       
#4.EXIT
    elif(choice==4):
        print("thank you for using expense tracker")
        break

    else:
       print("THANKYOU FOR USING EXPENSE TRACKER")
