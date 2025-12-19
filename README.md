# Python-Project
shop = {
    "apple": 30,
    "banana": 10,
    "milk": 50,
    "egg":8,
    "cheese":40,
    "yougurt":50,
    "bread":30,
    "coffee":12,
    "tea":15,
    "juice":25,
    "pantry":25,
    "orange":35,
    "pineapple":35,
    "biscuits":50

}

cart = []

print("Welcome to the Shop")

print("Available items:")
for item in shop:
    print(item, ":", shop[item])

while True:
    name = input("Enter item name: ")

    if name not in shop:
        print("Item not available")
        continue

    quantity = int(input("Enter quantity: "))

    price = shop[name]

    cart.append((name, quantity, price))

    choice = input("Do you want to add more items? (yes/no): ")
    if choice == "no":
        break

print(" BILL")
print("Item  Qty  Price  Amount")

total = 0
for item in cart:
    name, qty, price = item
    amount = qty * price
    total = total + amount
    print(name, qty, price, amount)

print("Total Amount =", total)
print("Thank you for shopping!")
