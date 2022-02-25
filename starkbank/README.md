# <p style="text-align: center; font-size: 25px;">StarkBank (StarkBank)</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">StarkBank Activity Diagram</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">StarkBank Overview (Context) Use Case Diagram</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">StarkBank Use Case Description</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">StarkBank Models</p>

| userModel              | primaryAccountModel   | savingsAccountModel   | primaryTransactionModel | savingsTransactionModel | recipientModel       | appointmentModel |
| ---------------------- | ----------------------|-----------------------| ------------------------|-------------------------|----------------------|------------------|
| +id                    | +id                   | +id                   | +id                     | +id                     | +id                  | +id              |
| +username              | +primaryAccountNumber | +savingsAccountNumber | +description            | +description            | +username            | +date            |
| +firstname             | +accountBalance       | +accountBalance       | +type                   | +type                   | +accountNumber       | +location        |
| +lastname              | +userRef              | +userRef              | +status                 | +status                 | +type                | +description     |
| +email                 | +timestamps           | +timestamps           | +amount                 | +amount                 | +description         | +isConfirmed     |
| +password              |                       |                       | +availableBalance       | +availableBalance       | +userRef             | +userRef         |
| +phone                 |                       |                       | +userRef                | +userRef                | +timestamps          | +timestamps      |
| +role                  |                       |                       | +primaryAccountId       | +savingsAccountId       |                      |                  |
| +password              |                       |                       | +date                   | +date                   |                      |                  |
| +isEnabled             |                       |                       | +timestamps             | +timestamps             |                      |                  |
| +primaryAccountId      |                       |                       |                         |                         |                      |                  |
| +savingsAccountId      |                       |                       |                         |                         |                      |                  |
| +resetPasswordToken    |                       |                       |                         |                         |                      |                  |
| +resetPasswordExpire   |                       |                       |                         |                         |                      |                  |
| +timestamps            |                       |                       |                         |                         |                      |                  |
|                        |                       |                       |                         |                         |                      |                  |
| +register()            |                       |                       |                         |                         | +getRecipients()     |                  |
| +login()               |                       |                       |                         |                         | +getRecipient()      |                  |
| +logout()              |                       |                       |                         |                         | +createRecipient()   |                  |
| +getMe()               |                       |                       |                         |                         | +updateRecipient()   |                  |
| +forgotPassword()      |                       |                       |                         |                         | +deleteRecipient()   |                  |
| +resetPassword()       |                       |                       |                         |                         |                      |                  |
| +updateDetails()       |                       |                       |                         |                         |                      |                  |
| +updatePassword()      |                       |                       |                         |                         |                      |                  |

<br><br><br>

# <p style="text-align: center; font-size: 25px;">StarkBank Class Diagram</p>