# Better Git Commits

This is everything you need to know about having better Git commit messages.


## Rules

I listed 10 rules for having a professional commit message.

### Meaningful messages:

The first and most important rule for a Git commit message is this! Each commit message must have a complete, meaningful and independent description. Commit message has to be valuable for its readers. As a reader, when I looked at the Git's log of your repository, All the commits messages must be clear for me and I be known about the changes of each commit, just by a simple looking!

I prepared some examples of bad commit messages and I explained why they are bad, so look at these:


❌ `First commit`

🔷 **Why it's bad?**
> It's not important for the reader to be known about the number of commit in its message. Because he/she can be known about it, by has a looking to the Git's log? Also he/she couldn't have any idea about the what happen's in the codebase in this commit!

❌ `Add some codes`

🔷 **Why it's bad?**
> When you works on a codebase, you can **add**, **delete** or **modify** the codes and there is not any other option! So, it has not any benefit for the reader! You must say what you added!

❌ `Refactoring and cleaning codes`

🔷 **Why it's bad?**
> How can I be informed that which section of the codebase had been modified? Or how can I guess what type of refactoring had been applied on codebase? You commit message have to include the answer of there questions in self!

❌ `Bug resolved`

🔷 **Why it's bad?**
> Which bug is resolved? Have to the reader guess the bug?! Of course no, so please explain what bug is resolved explicitly.

❌ `I added a new feature`

🔷 **Why it's bad?**
> According to the previous examples, here we haven't any clear vision about the modifications of codebase! Btw, there is no need to use pronoun at the first of this commit message. Git saves that who is the author of each commit by self and we haven't do a duplicated action!


### Neither Long nor Short:

If you want to write a meaningful message for a commit, avoid writing lengthy descriptions. Very summarized texts too! A sign of a good commit message is a suitable length most of the time. Maybe you want to know why we should avoid long/short messages in commit messages? Well, here's an example.

Assume my friend asks me to lend him some money.

❌ `Please lend me money!`
> It's an example of a short message. When my friend tells it, I ask two pertinent questions: "How much money do you need?" and "When will you get it back?". He could make me clear about them, so there was no need to these questions.

❌ `Hey Ahmad, get on the bus as soon as it arrives at the bus station. Then go to your bank, fill out a form, and then get the money from the bank and lend me $20. I'm going to return it in three weeks.`
> This is an example of a long message. It's an example of a long message. Don't tell me how I can provide some money! Just tell me your request.

✅ `Ahmad, please lend me 20 dollars. I will return it in 3 weeks.`
> Perfect! It's that I want to hear!


🔑 *The text of your message, must be the gist of your commit.*

🔑 *If you think that you need a long text to tell the gist of your commit, probably you have a big commit that should be separated in 2 or more smaller commits.*


### Use Imperative Mood:

When you want to write a commit message, suppose you give Git an order. Do not ask or inform Git! Just command directly!

For example, suppose you implemented a function that can transform the characters of a text into the upper case characters.

❌ `Implementing a function that transform letters to upper case.`

❌ `I added a function to transforming letters to upper case.`

❌ `A function to transforming letters to upper case has been added.`

✅ `Implement a function to transform letters to upper case.`


### Avoid Writing Details:

This rule complements the `Neither Long nor Short` rule. No need to write everything and details.
Remember always, you must tell `What` and `Why` something added/removed/modified in the codebase, not `How`! Also, no need to write the bit or low-priority modifications.

For example, assume you want to refactor a function named getUser in your codebase. After refactoring it, you notice that the related file has an unused variable inside itself, so you decide to remove it. When you want to commit your changes, there is no need to write something like this:

❌ `Refactor the 'getUser' function and delete an unused variable in its related file.`

Why is it not necessary to refer to the delete variable? Because it wasn't the primary goal of this commit. It was a minor modification that we could fix along with another commit. Of course, you can delete this unused variable in a separate commit, or maybe you want to make a new task for your project to find all unused variables and remove them all in a commit!

I prefer this one:

✅ `Refactor the 'getUser' function.`
