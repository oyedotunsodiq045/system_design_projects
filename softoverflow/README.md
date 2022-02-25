# <p style="text-align: center; font-size: 25px;">SoftOverflow (SoftOverflow)</p>

A simple and convenient way to ask anything, anywhere. It’s way better than pen and paper.
You can also say a simple clone of Stackoverflow, but an API. <a href="https://softoverflow.glitch.me/" target="_blank">docs</a>, <a href="https://github.com/oyedotunsodiq045/softoverflow" target="_blank">github</a>, <a href="https://documenter.getpostman.com/view/3890015/TVYQ1ZNY" target="_blank">postman</a>

<table>
  <tr>
    <th>Note</th>
    <th></th>
  </tr>
  <tr>
    <td>URL</td>
    <td>https://softoverflow.glitch.me</td>
  </tr>
  <tr>
    <td>URL</td>
    <td>https://softoverflow.herokuapp.com</td>
  </tr>
</table>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SoftOverflow Activity Diagram</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SoftOverflow Overview (Context) Use Case Diagram</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SoftOverflow Use Case Description</p>

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SoftOverflow Models</p>

| USER          | QUESTION        | ANSWER           | RATING          |
| ------------- | ----------------|------------------| ----------------|
| +id           | +id             | +id              | +id             |
| +name         | +question       | +solution        | +rating         |
| +email        | +categories     | +isSolution      | +questionRef    |
| +role         | +averageRating  | +questionRef     | +userRef        |
| +password     | +userRef        | +userRef         | +timestamps     |
| +timestamps   | +timestamps     | +timestamps      |                 |
|               |                 |                  |                 |
| +register()   |+getQuestions()  |+getAnswers()     |+getRatings()    |
| +login()      |+getQuestion()   |+getAnswer()      |+getRating()     |
| +logout()     |+askQuestion()   |+answerQuestion() |+rateQuestion()  |
| +getMe()      |                 |                  |                 |
| +getUsers()   |                 |                  |                 |
| +getUser()    |                 |                  |                 |

<br><br><br>

# <p style="text-align: center; font-size: 25px;">SoftOverflow Class Diagram</p>