A command-line inventory and point-of-sale simulation written in Python. A manager stocks the store, then a customer browses it, builds a cart, redeems loyalty points, and gets a printed receipt.

Features:

Manager interface

  Add products with a name, price, quantity, condition grade (1–5), and loyalty point value
  Rejects duplicate product names (case-insensitive)
  Validates every field: prices must be numeric, quantities and point values must be non-negative integers, condition must fall between 1 and 5
  Edit any field of a product after entering it, with repeated edits allowed until you're done

Customer interface

  Search the catalogue by product name
  See stock levels, price, and condition before buying
  Cannot buy more of an item than is in stock
  Running cart total displayed between purchases
  Repeated purchases of the same item are merged into a single cart line

Checkout

  Loyalty points are randomly seeded at launch (0–500) for demo purposes
  Each point is worth $0.15 off the final total
  Purchases that are fully covered by points are free, and payment is skipped
  Otherwise the customer enters a payment amount and change is calculated
  A formatted receipt prints the itemised cart, subtotal, points discount, total, and change
