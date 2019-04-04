# The problem
A billing system allows an e-commerce SaaS company to keep track of transaction fees to charge to the clients of the company, the merchants, who sell products through the e-commerce platform.


The merchants register product sales and for each sale transaction the e-commerce SaaS company will charge the merchants a small fee.


When a merchant subscribes to the platform, can choose a subscription plan, every plan has a specific transaction fee:
* Basic plan, with a transaction fee of 2% 
* Medium plan, with a transaction fee of 1%
* Full plan, with a transaction fee of 0.5%


At any given moment, a Merchant can update its subscription plan, for example: if a Merchant started with a Basic plan, can upgrade to Medium or Full, or if a Merchant started with a Medium plan can downgrade to Basic plan, etc.


The e-commerce SaaS company charges the merchants and sends a bill to them every month, For a given merchant and month, the e-commerce platform calculates the bills to send to the merchant, with the summary of sales and their corresponding fees.


## Bill specification
A bill for a given merchant and month, includes the sum of transaction amounts, and the sum of the fees to charge the merchant. Any previous debt or credit from previous months of the Merchant's balance account is included too.

The subtotal of the bill is equal to the sum of fees, plus previous credits, minus previous debt.

The total of the bill is equal to the subtotal, plus 21% for VAT (IVA).

When a merchant pays a bill, the e-commerce SaaS company register the payment and updates the balance account for the merchant.

### Discount rules
* A bill paid during the first 30 days after generated has a 2% discount on the total of the bill, appliable as credit for the next Bill. 


# The goals
Given:
* Merchant M1, with subscription plan Basic
* Merchant M2, with subscription plan Medium
* Merchant M3, with subscription plan Full
* Product P1, part of Merchant's M1 catalog
* Product P2, part of Merchant's M2 catalog
* Product P3, part of Merchant's M3 catalog

Create a model for the following features using Java / Kotlin:


## Mandatory features
* Update a Merchant's plan (upgrade/downgrade)
* As a Merchant, register the sale of a given product
* Get the Bill for a given Merchant and business month, following the above specification of the Bill


## Bonus features
* Update a Merchant's contact info: name, email, phone, address
* Pay a given Bill


## Add RESTful services
And for all the features you modeled in Java / Kotlin (mandatory and/or bonus): 
* Provide REST endpoints for all above features
* Write a server application that exposes the REST APIs. The application must be written in Java or Kotlin, and a REST framework of choice.
* Document the REST APIs, either statically in a README file, or using an automatic documentation tool.
* Document how to compile the code and run the created application.


# Expected deliverable 
You don't need to complete all the objectives, but as a minimum you should provide the class model, REST endpoint and documentation of the mandatory features. The more complete solution you provide the better for us to evaluate your skills!


## Publish your work
1. Create a public repository in GitHub, BitBucket, Gitlab, etc. to share your solution.
2. Try to commit each step of your process so we can follow your thought process.
3. Include documentation that you consider important, of any decision made about the design and implementation.
