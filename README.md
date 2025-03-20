# Prac
def budget_expenses():
    s = int(input("Enter the salary: "))
    if s<0:
         s = s*(-1)
    b = int(input("Enter your monthly Budget: "))
    if b<0:
         b = b*(-1)
    g = int(input("Enter your expenditure on Groceries: "))
    if g<0:
         g = g*(-1)
    return s

def bills():
        e = int(input("Amount of Expenditure on Electricity: "))
        if e<0:
             e = e*(-1)
        w = int(input("Amount of Expenditure on Water: "))
        if w<0:
             w = w*(-1)
        g = int(input("Amount of Expenditure on LPG Gas: "))
        if g<0:
             g = g*(-1)
        credit_card = 0
        print("Do you have Credit Card Bills: ")
        print("1.Yes")
        print("2.No")
        key = int(input())
        if key == True:
            credit_card = int(input("Amount of Credit Card Expenses: "))
        print("Do you have EMI: ")
        Emi = 0
        print("1.Yes")
        print("2.No")
        key_1 = int(input())
        if key_1 == True:
            Emi = int(input("Amount of EMI Expenses: "))
        print(f"Electicity : {e}\nWater Bill : {w}\nGas Bill: {g}")
        print(f"Crredit Card : {credit_card}\nEMI : {Emi}")
        sum = e+w+g+credit_card+Emi
        return sum
def accomodation():
    rent = int(input("Enter house rent: "))
    boo = int(input("Do you have Shop\n1.Yes\n2.No\n"))
    s_rent = 0
    if boo:
         s_rent = int(input("Enter Shop Rent: "))
    print(f"House Rent: {rent}\nShop Rent: {s_rent}")
    su = rent+s_rent
    return su

def maintenance():
     v = int(input("Enter Vehicle Expenses: "))
     h = int(input("Enter house expenses: "))
     e_d = int(input("Amount for Electronics Maintenance: "))
     print(f"Vehicle: {v}\nHouse Expenses: {h}\nAmount for Electronics: {e_d}")
     sums = v+h+e_d
     return sums

def extras():
     fee = int(input("Will you pay fee this month:\n1.Yes\n2.No\n"))
     f = 0
     if fee==1:
          f = int(input("Enter Fees: "))
     sh = int(input("Shopping??\n1.Yes\n2.No\n"))
     shop = 0
     if sh==1:
          shop = int(input("Enter Shopping Expenses: "))
     print(f"Fees: {f}\nShopping: {shop}")
     ri = f + shop
     return ri

print("Budget and Savings:")
a = budget_expenses()
b = bills()
c = accomodation()
d = maintenance()
e = extras()
w = b+c+d+e
print(f"Total Expenses = {w}") 
print(f"Savings = {a-w}")

