# tickett.py
code
#  python.py
  
  
adult_price = 20
child_price = 15
concession_price = 17.50
total_sales = 0
  
while True:
    new_sale = input("Is there a new ticket sale? (yes/no): ")
    if new_sale.lower() == "no":
        break

        adult_tickets_sold = 0
        child_tickets_sold = 0
        concession_tickets_sold = 0

        total_tickets_sold = 0
  
    while True:
        try:
            adult_tickets = int(input("Number of adult tickets: "))
            child_tickets = int(input("Number of child tickets: "))
            concession_tickets = int(input("Number of concession tickets: "))
            if adult_tickets < 0 or child_tickets < 0 or concession_tickets < 0:
                raise ValueError
            if adult_tickets == 0 and child_tickets == 0 and concession_tickets == 0:
                raise ValueError
            break
        except ValueError:
            print("Invalid input. Please enter a non-negative integer.")
  
    sale_total = adult_tickets * adult_price + child_tickets * child_price + concession_tickets * concession_price
    total_sales += sale_total
    print(f"Total due: <img src="https://latex.codecogs.com/gif.latex?{sale_total:.2f}&quot;)

print(f&quot;Total%20sales:"/>{total_sales:.2f}")
print(f"Adult tickets sold: {adult_tickets}")
print(f"Child tickets sold: {child_tickets}")
print(f"Concession tickets sold: {concession_tickets}")
