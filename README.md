# Unit1-project
Customer Coffee Quiz
print("Welcome to the Coffee Quiz! Let's find your perfect drink!\n")

coffee_type = input("How do you like your coffee: H for hot, I for iced, or B for blended? ")
print(f"You like your coffee {coffee_type} excellent choice!")

flavor_choice = input("What flavor do you like: 1 for Caramel, 2 for Vanilla, or 3 for Mocha? ")
print(f"You like the flavor {flavor_choice} yummy choice!")

size = input("What's your preferable size: S for small, M for medium, or L for large? ")
print(f"You like your coffee size {size}.")
whip = input("Would you like whipped cream? (Yes or No): ")
print(f"Your whipped cream choice is {whip}")
sweetness = input("Do you like sweet coffee or the taste of coffee more? (Sweet or Unsweet): ")
print(f"You like your coffee {sweetness}.")
#flavor choice
if flavor_choice == "1":
    flavor = "Caramel"
    print("You chose Caramel")
elif flavor_choice == "2":
    flavor = "Vanilla"
    print("You chose Vanilla")
elif flavor_choice == "3":
    flavor = "Mocha"
    print("You chose Mocha")
else:
    flavor = "House Blend"
    print("You didnt select any flavors above hinting that you might just like the natural taste of coffee")

#ask size
if size == "S":
    size_text = "Small"
    print("Size small is selected")
elif size == "M":
    size_text = "Medium"
    print("Size medium is selected")
elif size == "L":
    size_text = "Large"
    print("Size large is selected")
else:
    size_text = "Regular"
    print("You did not select a size hinting that you would like just a regular size")

#ask for drink size
if sweetness == "sweet" and coffee_type == "B":
    # Blended sweet drinks
    if flavor_choice == "1":  # Caramel
        print(f"\nYou'd love a {size_text} Caramel Frappuccino!")
    elif flavor_choice == "2":  # Vanilla
        print(f"\nYou'd enjoy a {size_text} Vanilla Bean Frappuccino!")
    elif flavor_choice == "3":  # Mocha
        print(f"\nA {size_text} Mocha Frappuccino would be perfect for you!")
    else:
        print(f"\nA {size_text} Sweet Blended Coffee would hit the spot!")

elif coffee_type == "H" and sweetness == "sweet":
    # Sweet hot coffee options
    if whip == "yes":
        print(f"\nYou'd love a {size_text} Hot {flavor} Latte with Whipped Cream — warm and cozy!")
    else:
        print(f"\nYou'd love a {size_text} Hot {flavor} Latte — the perfect balance of heat and sweetness!")

elif coffee_type == "H" and sweetness == "unsweet":
    # Unsweet hot coffee
    print(f"\nYou prefer the bold flavor of coffee. Try a {size_text} Brewed {flavor} Coffee!")

elif coffee_type == "I" and sweetness == "unsweet":
    print(f"\nYou might enjoy a {size_text} Plain Iced Latte — smooth and simple!")

elif coffee_type == "I" and sweetness == "sweet":
    print(f"\nYou'd love a {size_text} Iced {flavor} Latte — refreshing and flavorful!")

else:
    print(f"\nYou've got a unique taste! Try a custom {size_text} {flavor} drink next time!")

if whip == "yes":
    print("Don't forget the whipped cream on top!")

print("\nThanks for taking the Coffee Quiz!")
