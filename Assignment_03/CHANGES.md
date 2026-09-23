# Assignment 03 — CHANGES

**Name:** Aye Than Tin   **Student ID:** 6705140074

## 1 · What I changed

| # | Code smell in the original | What I changed it to | OOP concept applied | How I verified behaviour was unchanged |
|---|---|---|---|---|
| 1 | Product information was stored in tuples | I created a Product class to store name, price, and category | Class / Encapsulation | I ran `python Assignment_03.py` and checked the self-test |
| 2 | Product number and quantity were stored together in lists | I created an OrderItem class with a product and quantity | Composition | I ran the program and checked the result |
| 3 | The original code used many `if/elif` statements for customer tiers | I created Customer, SilverCustomer, GoldCustomer, and PlatinumCustomer classes | Inheritance / Polymorphism | I checked the discounts and points and ran the self-test |
| 4 | The calculations were all together in one large function | I separated them into subtotal(), discount(), tax(), total(), and points() methods | Encapsulation | I compared the result with the original program |
| 5 | Numbers such as 0.07, 100, and 10 were written directly in the code | I changed them to names such as TAX_RATE, DISCOUNT_THRESHOLD, and POINTS_DIVISOR | Named constants / Clean code | I ran the self-test and got PASS |
| 6 | The old program handled the whole order in one function | I created an Order class to keep the customer, items, calculations, and receipt together | Class / Composition | I ran `python Assignment_03.py` and got PASS |

## 2 · Short reflection

I think the customer classes improved the code the most. In the old code, there were many if and elif conditions for different customer tiers. I changed them into SilverCustomer, GoldCustomer, and PlatinumCustomer classes. This helped me understand inheritance and polymorphism better. I had to be careful with the calculations and receipt format because the output had to stay the same. After fixing my errors, I ran the self-test and got PASS.

## 3 · Prompt log (Level 2 — required)

| # | My prompt to the AI | What it suggested (summary) | Accept / reject / edited | How I checked it |
|---|---|---|---|---|
| 1 | I asked AI to explain what the assignment wanted me to do because I did not understand refactoring | It explained that I needed to improve the code structure without changing the program result | Accepted | I compared the explanation with the assignment |
| 2 | I asked how to replace the magic numbers | It explained named constants such as TAX_RATE and DISCOUNT_THRESHOLD | Accepted | I checked the values with the original code |
| 3 | I asked how to create Product and OrderItem classes | It explained how the classes can store product information and quantity | Accepted and edited | I read the code and ran the program |
| 4 | I asked about the Customer classes because I did not understand inheritance and polymorphism | It explained the base Customer class and the Silver, Gold, and Platinum subclasses | Accepted and edited | I checked the discount and point rules |
| 5 | I asked how to create the Order class and calculation methods | It helped me separate subtotal, discount, tax, total, and points | Accepted and edited | I ran the self-test |
| 6 | I asked AI for help when I got indentation errors and `Order object has no attribute receipt` | It helped me find that some methods were outside the Order class because of indentation | Accepted | I fixed the indentation and ran the program again |
| 7 | I asked AI to check and correct my file because I was still getting errors | It corrected the indentation and other small mistakes in my code | Accepted and reviewed | I ran `python Assignment_03.py` and got PASS |

**Ownership statement:** By submitting, I confirm I understand and can explain the code I submitted, and this prompt log reflects my AI use.

## 4 · Before-you-submit checklist

- [yes] `python Assignment_03.py` prints **PASS**.
- [yes] Products and order items are represented with objects.
- [yes] Customer tiers use subclasses instead of repeated `if tier == ...` conditions.
- [yes] Calculation methods return values.
- [yes] Important numbers are stored as named constants.
- [yes] I completed the change table and reflection.
- [yes] I recorded my AI use in the prompt log.