Project Prompt I Created:

Description

CardVault is a small business that specializes in buying, selling, and tracking trading cards from games like Pokémon, Magic: The Gathering, and Yu-Gi-Oh. The business operates both in-store and online, requiring an efficient database system to manage its inventory, customer purchases, and employee transactions.

CardVault wants to track its inventory to ensure that each card’s brand, name, and price are stored. Each card has a Card ID that represents the card type, for example a Base Set Charizard would have the ID of CHA001. Cards are also organized into their respective sets, with each set’s name and release date being tracked. A card can belong to only one set, but a set can have any number of cards associated with it. 

They also need to track every order, including its date and total price. Each order is associated with one and only one customer, but a customer can place multiple orders. CardVault also tracks employee first and last names and which orders they process to maintain accurate personnel records. Employees can process multiple orders or no orders, but each order is processed by only one employee.

CardVault keeps track of every customer’s first and last name, phone number (phone numbers can be shared), and membership status. For members, CardVault tracks the date they joined.

Finally, some trading cards have evolutions, meaning they can transform into another card within the same game. A card may evolve into zero, one, or many other cards (its evolutions). Similarly, a card may evolve from zero, one, or many other cards (its pre-evolutions). For example: A Charmander card evolves into Charmeleon (1 evolution) and evolves from 0 other cards (it’s a base form).

ERD Model: ![Screenshot 2025-04-28 094701](https://github.com/user-attachments/assets/f0cee107-a123-414d-ad5a-1a9abdeb36c5)

Conversion

CORDER(OID, ODate, OPrice, EID, CNum)
CARD(CID, CName, CBrand, CCondition, CPrice, SID)
EMPLOYEE(EID, EF, EL)
CSET(SID, SName, SDoR)
CUSTOMER(CNum, CF, CL)
MEMBER(MJoinDate, CNum)
DETAIL(OQty, OID, CID)
EVOLUTION(CID1, CID2)
CPHONE(CPhone, CNum)

