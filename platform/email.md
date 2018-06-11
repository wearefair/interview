Coding challenge or existing code?
==================================

The coding challenge is optional if you already have some code that you're proud of and can share with us.

Existing code
-------------

If you have existing code, please follow these guidelines:

* Include a link to the hosted repository (e.g. Github, Bitbucket...). We cannot review archives or single files.
* The repo should include a README that follows the [recomendation below](#readme). Please make sure to include a high-level overview of what the code is doing.
* Ideally, the code you're providing:
  * Has been written by you alone. If not, please tell us which part you wrote and are most proud of in the README.
  * Is leveraging web technologies.
  * Is deployed and hosted somewhere, or trivial to run locally (fully Dockerized).

Readme
------

Regardless of whether it's your own code or our coding challenge, write your README as if it was for a production service. Include the following items:

* Description of the problem and solution.
* How to invoke your API
* Reasoning behind your technical choices, including architectural.
* Trade-offs you might have made, anything you left out, or what you might do differently if you were to spend additional time on the project.
* Link to to the hosted application where applicable.


How we review
-------------

Your application will be reviewed by at least two of our engineers.  We do take into consideration your experience level.

**We value quality over feature-completeness**. It is fine to leave things out provided you call them out in your project's README. The goal of this code sample is to help us understand what you consider production-ready code. You should consider this code ready for final review before deploying to production.

The aspects of your code we will assess include:
* **Architecture**: how clean is the separation between the API (view) and the internals?
* **Clarity**: does the README clearly and concisely explains the problem and solution? Are technical tradeoffs explained?
* **Correctness**: does the application do what was asked? If there is anything missing, does the README explain why it is missing?
* **Code quality**: is the code simple, easy to understand, and maintainable?  Are there any code smells or other red flags? Is the coding style consistent with the language's guidelines? Is it consistent throughout the codebase?
* **Security**: are there any obvious vulnerabilities?
* **Testing**: how thorough are the automated tests? Will they be difficult to change if the requirements of the application were to change? Are there some unit and some integration tests?
	* We're not looking for full coverage (given time constraint) but just trying to get a feel for your testing skills.
* **UX**: Is the API intuitive and easy to use?
* **Technical choices**: do choices of libraries, databases, architecture etc. seem appropriate for the application?

Bonus point (those items are optional):

* **Scalability**: will technical choices scale well? If not, is there a discussion of those choices in the README?
* **Production-readiness**: does the code include monitoring? logging? proper error handling?


Coding Challenge Guidelines
===========================

Please organize, design, test, document and make your code runnable (ex: via Docker) as if it were
going into production, then send us a link to the hosted repository (e.g.
Github, Bitbucket...).


Functional spec
---------------

The UX/UI is totally up to you. If you like, get creative and add additional
features a user might find useful!

### Email Service

Create a service that accepts the necessary information and sends emails. It
should provide an abstraction between two different email service providers.
If one of the services goes down, your service should quickly failover to
the secondary provider without affecting your customers.

Example Email Providers:

* [SendGrid](https://sendgrid.com/user/signup) - [Simple Send Documentation](https://sendgrid.com/docs/API_Reference/Web_API/mail.html)
* [Mailgun](http://www.mailgun.com) - [Simple Send Documentation](http://documentation.mailgun.com/quickstart.html#sending-messages)
* [SparkPost](https://www.sparkpost.com/) - [Developer Hub](https://developers.sparkpost.com/)
* [Amazon SES](http://aws.amazon.com/ses/) - [Simple Send Documentation](http://docs.aws.amazon.com/ses/latest/APIReference/API_SendEmail.html)

All listed services are free to try and are pretty painless to sign up for, so
please register your own test accounts on each (omit your credentials, we will provide our own when we run your project).


Technical spec
--------------

There is no one-size-fits-all technology. Good engineering is about
using the right tool for the right job, and constantly learning about them.
Therefore, feel free to mention in your `README` how much experience you have
with the technical stack you choose, we will take note of that when reviewing
your challenge.

Here are some technologies we are more familiar with:

* Python
* JavaScript
* Ruby
* Go
* Java
* Clojure
