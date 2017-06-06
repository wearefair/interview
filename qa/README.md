# QA Engineer Take Home Excercise

Create an Test Suite to externally validate the following:

Using a ruby based test framework test against credit-test.herokuapp.com.

The application is meant to work like this:

A line of credit product.  This is like a credit card except theres no card.
It should work like this:

  - Have a built in APR and credit limit
  - Be able to draw ( take out money ) and make payments.
  - Keep track of principal balance and interest on the line of credit
  - APR Calculation based on the outstanding principal balance over real number of days.
  - Interest is not compounded, so it is only charged on outstanding principal.
  - Keep track of transactions such as payments and draws on the line and when
    they occured.
  - 30 day payment periods.  Basically what this means is that interest will not be
    charged until the closing of a 30 day payment period.  However, when it is charged,
    it should still be based on the principal balance over actual number of days outstanding
    during the period, not just ending principal balance.

Couple of Scenarios how it would play out:

Scenario 1:

Someone creates a line of credit for $1000 and 35% APR.

They draws $500 on day one so their remaining credit limit is $500 and their balance is $500.
They keep the money drawn for 30 days.  They should owe $500 * 0.35 / 365 * 30 = 14.38$ worth
of interest on day 30.  Total payoff amount would be $514.38

Scenario 2:

Someone creates a line of credit for $1000 and 35% APR.

They draw $500 on day one so their remaining credit limit is $500 and their balance is $500.
They pay back $200 on day 15 and then draws another 100$ on day 25.  Their total owed interest on
day 30 should be 500 * 0.35 / 365 * 15 + 300 * 0.35 / 365 * 10 + 400 * 0.35 / 365 * 5  which is
11.99.  Total payment should be $411.99.



# Specific requirements

1. Test the scenarios described above and validate that the final numbers are correct.

1. Test some negative cases where a user tries to break the system

1. Log any bugs or defects the system has

1. Suggest improvements to address the found defects




