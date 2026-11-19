# Dart OOP Assignment: Kigali Bus Card

**Name:** Hiba Omer Ahmed Zayed
**Student ID:** 25996/2024

## My numbers
- D = 96, L = 6
- Starting balance = 1960 RWF
- Bus fare = 296 RWF
- Student discount = 16%

## Output of main.dart
Topped up 2000 RWF
Paid 296 RWF
Owner: Hiba Omer Ahmed Zayed | Balance: 3368 RWF
Student discount: 47 RWF
Paid 249 RWF
Owner: Hiba Omer Ahmed Zayed | Balance: 1711 RWF
Student card: 16% off

## Part 1: Why no setter for balance?
Having no setter for the balance protects it from being changed randomly. We only change the balance through specific methods like `topUp` and `pay` which contain rules to ensure the transaction is valid.

## Part 2: What does ~/ do?
The `/` operator performs division and returns a double (e.g., 40.29). The `~/` operator performs integer division and returns only the whole number without decimals (e.g., 40). We use `~/` to calculate the discount in whole RWF.

## Part 4: Bug table
| Bug | The line | Why it is wrong (your words) | Your fix |
| :--- | :--- | :--- | :--- |
| **1** | `String _brand; int _battery;` | Fields need a starting value (null safety). | Added `= ''` and `= 0`. |
| **2** | `SmartPhone(...) {` | It doesn't call the parent constructor using `super`. | Added `: super(brand, battery)` |
| **3** | `@override`<br>`void restart()` | The parent `Phone` class doesn't have a `restart` method. | Removed `@override`. |
| **4** | `'Restarting $system'` | Missing the `_` or the variable name is wrong. | Changed to `'Restarting $_system'`. |
| **5** | `print(p.battery());` | `battery` is a getter, not a method, so no `()`. | Changed to `print(p.battery);` |
| **Not a bug** | `Phone p = new Phone(...);` | Using `new` is optional in Dart and perfectly fine. | (none) |

## Part 5
My prediction: 1 then 6.
Real output: 1 then 6.
Was I right? Yes.