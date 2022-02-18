# <p style="text-align: center; font-size: 25px;">Sharing Hands Cooperative Union (SHCU)</p>

Sharing Hands Cooperative Union (SHCU) is a credit union firm located in Little Rock, Arkansas. It's a group of people who are pooled into a community of 12 people each who contribute a guaranty deposit (an equivalent of the monthly savings) and monthly contributions making 13 times in a year. Each person in a community is paired with the person adjacent to them as in a wall clock (3-9, 6-12 etc) thereby making every person in the community pool half of their annual contribution twice in a year and once in 6 months. The system charges a percentage deduction of 10% from the annual contribution. This is saved towards the perks and benefits of members of the credit union society. A member can decide to take his/her annual contribution based on circumstances or financial difficulties the person is going through and an appointment must be scheduled for that to be granted. Members can take interest free loans on completion of a 2 year cycle and the longer each member stays the higher the benefits and perks.

On registration of a user, A guaranteed deposit must be paid to confirm a user agreement to being a member. A pool number and a community is assigned. The system emails you a receipt of your registration and details of your pairee and account information (which consists of dates, 2 months in each halves of the year when you and your pairee will be pooling).

The system updates payment for each user (member)	 via payment gateway (stripe, square etc) and a receipt is generated and email are sent accordingly for confirmation

If a user decides to take his contribution prior to his/her pooling date for any unforeseen reason, a contract is created and payment is made from the guaranteed deposit. A user can only take this benefit once in a year

The system pays out a maximum of two pool loans bi monthly.

Each month (27th - 31st), a reminder is sent to members to pay their contribution.

A welcome message is sent to a new member on completion of his/her registration.

* Notes

  * Guaranty Deposit - The amount a member deposit, at the beginning of every contribution
  * ICU (Total Guarantee Deposit for a community) - Anyone member of a community can pool from here bimonthly and refund on getting paid, must be their quota
  * Community - A community consists of twelve people
  * members to pool twice with their pairee (opposite) in a year
  * members can take interest free loans

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SHCU Activity Diagram</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SHCU Overview (Context) Use Case Diagram</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SHCU Use Case Description</p>

| Use Case ID         |                                                                                                                                                                                       |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use Case Name       | SHCU user registration                                                                                                                                                                |
| Actors              | User                                                                                                                                                                                  |
| Brief Description   | The use case describes the process of registering on the SHCU / new user being a member.                                                                                              |
| Basic Course        | 1. &emsp;The user registers on SHCU website.<br> 2. &emsp;The user fills requested data on the website.<br> 3. &emsp;The user pays a guarantee deposit.<br> 4. &emsp;The user is redirected to the dashboard.                                                                                                                                                                                  |
| Alternative Courses | 1. &emsp;                                                                                                                                                                             |
| Others              | Any comments                                                                                                                                                                          |

<br>

| Use Case ID         |                                                                                                                                                                                       |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use Case Name       | Assign pool number and community                                                                                                                                                      |
| Actors              | SHCU System                                                                                                                                                                           |
| Brief Description   | The use case describes the process of assigning pool numbers and community to a user.                                                                                                 |
| Basic Course        | 5. &emsp;The system confirms payment of guarantee deposit on confirmation of registration.<br> 6. &emsp;The system generates pool numbers (user and pairee) and community.<br> 7. &emsp;The system sends receipt of payment to the user via email and sms.<br> 8. &emsp;The system redirects user to dashboard page.                                                                             |
| Alternative Courses | 9. &emsp;If payment is not confirmed, display payment not confirmed message.                                                                                                          |
| Others              | Any comments                                                                                                                                                                          |

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SHCU Class Diagram</p>

| USER                   | COMMUNITY            | RECEIPT        | POOL               | PAYMENT            |
| ---------------------- | ---------------------|----------------| -------------------|--------------------|
| +id                    | +id                  | +id            | +id                | +id                |
| +sequence              | +communityNumber     | +receiptNumber | +amount            | +amount            |
| +firstname             | +communityName       | +amount        | +userRef           | +forMonth          |
| +lastname              | +slug                | +modeOfPayment | +receiptId         | +modeOfPayment     |
| +username              | +description         | +userRef       | +timestamps        | +receiptNumber     |
| +email                 | +address             | +poolId        |                    | +photo             |
| +password              | +location            | +paymentId     |                    | +userRef           |
| +phone                 | +averageContribution | +timestamps    |                    | +receiptId         |
| +role                  | +timestamps          |                |                    |  +timestamps       |
| +poolMonth             |                      |                |                    |                    |
| +poolMonthNumber       |                      |                |                    |                    |
| +poolPaireeMonth       |                      |                |                    |                    |
| +poolPaireeMonthNumber |                      |                |                    |                    |
| +userCommunityNumber   |                      |                |                    |                    |
| +communityId           |                      |                |                    |                    |
| +timestamps            |                      |                |                    |                    |
|                        |                      |                |                    |                    |
| +register()            |                      |                | +canPool()         | +generateReceipt() |
| +login()               |                      |                | +pool()            |                    |
| +logout()              |                      |                | +generateReceipt() |                    |
| +getMe()               |                      |                |                    |                    |
| +forgotPassword()      |                      |                |                    |                    |
| +resetPassword()       |                      |                |                    |                    |
| +updateDetails()       |                      |                |                    |                    |
| +updatePassword()      |                      |                |                    |                    |
| +assignCommunity()     |                      |                |                    |                    |
