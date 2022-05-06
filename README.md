# Better Git Commits

This is everything you need to know about having better Git commit messages.


## Rules

I listed 10 rules for having a professional commit message.

### 1. Meaningful messages:

The first and most important rule for a Git commit message is this! Each commit message must have a complete, meaningful and independent description. Commit message has to be valuable for its readers. As a reader, when I looked at the Git's log of your repository, All the commits messages must be clear for me and I be known about the changes of each commit, just by a simple looking!

I prepared some examples of bad commit messages and I explained why they are bad, so look at these:


❌ `First commit`

🔷 **Why it's bad?**
> It's not important for the reader to known about the number of commits in the commit message. Because he/she can just check Git logs. 
> you should inform the reader that exactly what happened
> 
✅ git commit -m 'feat: initialize project and download project dependencies'


❌ `Add some codes`

🔷 **Why it's bad?**
> When you works on a codebase, you can **add**, **delete** or **modify** the codes and there is not any other option! So, it has not any benefit for the reader! You must say what you added!

❌ `Refactoring and cleaning codes`

🔷 **Why it's bad?**
> How can I be informed that which section of the codebase had been modified? Or how can I guess what type of refactoring had been applied on codebase? Your commit message have to include the answer of these questions in self!

❌ `Bug resolved`

🔷 **Why it's bad?**
> Which bug is resolved? Have to the reader guess the bug?! Of course no, so please explain what bug is resolved explicitly.

❌ `I added a new feature`

🔷 **Why it's bad?**
> According to the previous examples, here we haven't any clear vision about the modifications of codebase! Btw, there is no need to use pronoun at the first of this commit message. Git saves that who is the author of each commit by self and we haven't do a duplicated action!


### 2. Neither Long nor Short:

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


### 3. Use Imperative Mood:

When you want to write a commit message, suppose you give Git an order. Do not ask or inform Git! Just command directly!

For example, suppose you implemented a function that can transform the characters of a text into the upper case characters.

❌ `Implementing a function that transform letters to upper case.`

❌ `I added a function to transforming letters to upper case.`

❌ `A function to transforming letters to upper case has been added.`

✅ `Implement a function to transform letters to upper case.`


### 4. Avoid Writing Details:

This rule complements the `Neither Long nor Short` rule. No need to write everything and details.
Remember always, you must tell `What` and `Why` something added/removed/modified in the codebase, not `How`! Also, no need to write the bit or low-priority modifications.

For example, assume you want to refactor a function named getUser in your codebase. After refactoring it, you notice that the related file has an unused variable inside itself, so you decide to remove it. When you want to commit your changes, there is no need to write something like this:

❌ `Refactor the 'getUser' function and delete an unused variable in its related file.`

Why is it not necessary to refer to the delete variable? Because it wasn't the primary goal of this commit. It was a minor modification that we could fix along with another commit. Of course, you can delete this unused variable in a separate commit, or maybe you want to make a new task for your project to find all unused variables and remove them all in a commit!

I prefer this one:

✅ `Refactor the 'getUser' function.`


### 5. Conceptual Prefixes:

This one is an optional offer for your commit messages but can make them very readable and powerful. According to the added modifications in the codebase in your commit, you can use a suitable and matched prefix for its message. In most cases, prefixes are used at the first of commit messages.

Here is a list of the most usable prefixes that I often see in software teams:

* `[BUGFIX]`: For resolving any bug and issue from the codebase.
* `[TEST]`: For writing any type of tests (Unit / End-to-End / UserStory / Integration / Regression / ...)
* `[FEATURE]`: For adding a new feature and implementation
* `[REFACTOR]`: For improving current codes for any purpose like better readability, performance, etc.
* `[UPDATE]`: For updating libraries and dependencies, also updating current features by documentation.
* `[BASE]`: For installing new libraries and dependencies and setting up the infrastructures of the codebase, like configuring the project and its packages.
* `[DOCS]`: For adding or modifying the documentations.

The above cases are only some offers for you so, there isn't any force to using them. You can have your own!

🔑 *The text of your prefixes can be lowercase. Please follow a fixed rule. For example, if you want to write your prefixes in lowercase, write them all in lowercase forever in the related repository.*


### 6. Emoji? Please No!

Recently I'm seeing developers use emojis in commit messages. In my opinion, it's not a good practice! Say Why? Because of two reasons:

* That they don't have a clear message.
* Emojis have specific Unicode, maybe we have a terminal that doesn't support those Unicode, so we can't see any emoji in our terminal.

One of my colleagues disagreed with me about case one. She believed that each emoji has a special meaning, and we can use them in our commit messages. I asked her to give an example. She showed the emoji of a worm (🐛) and said that everybody knows that this emoji refers to a bug! I asked her what should be used for features, refactoring, testing, and ...? She introduced a website to me and said they provide lots of emojis and have a unique meaning for all of them.

It's the address of that website: [Gitmoji](https://gitmoji.dev)

I disagree with my colleague because this website is not a reference for git commits! It's not the product of a famous company with high-level standards! Only one tasteful person has presented some emojis and has written explanations for each of them according to his taste. That and no more!
One day, if terminals support showing images, I can create a website for using images in the commit messages! For example, I can provide the picture of a scared man and say that refers to a bug! It's not standard :)


### 7. Referral Prefixes:

This case is similar to `Conceptual Prefixes` with a main different: The *Conceptual Prefixes* have a straight and clear messages for their reader and directly say their content. But the *Referral Prefixes* point to a external description, like a task on Jira, a card on Trello, an issue on Gitlab or anything else! *Referral Prefixes* usually be used in the large teams and teams that they used Scrum methodology.

For using a referral prefix, there are some common styles that I list:

* `[#<CARD-NUMBER>]`, `[#<ISSUE-NUMBER>]` or `[#<TASK-NUMBER>]`
* `[<CARD-NUMBER>]`, `[<ISSUE-NUMBER>]` or `[<TASK-NUMBER>]`
* `(<CARD-NUMBER>)`, `(<ISSUE-NUMBER>)` or `(<TASK-NUMBER>)`


An examples of the above cases:

* `[#217] Resolve the bug of 'fetchUsers' function that causes some users be missed`

> [#217] at the first of this commit can refer to task number 217. It's no matter what tasks manager you are using. You can always use these referral prefixes to point to your tasks/cards/issues.


🔑 *You can use both **Conceptual Prefixes** and **Referral Prefixes** together. It relates to your decision.*

I list examples of usage of conceptual prefixes and referral prefixes side each other:


* `[#REFACTOR](217) Use Array's methods like 'forEach' and 'map' instead of simple 'for' and 'while' loops in the codebase`

* `[REFACTOR-217] Use Array's methods like 'forEach' and 'map' instead of simple 'for' and 'while' loops in the codebase`

* `[#217][REFACTOR] Use Array's methods like 'forEach' and 'map' instead of simple 'for' and 'while' loops in the codebase`


🔑 *The above examples are just some template and they are not a rule. You can use them in any other styles.*


### 8. Separate References to The Codes and Specialized Terms

Sometimes commit messages to contain references to variables, functions, methods, classes, and specialized terms. Whenever you need to write a specialized term or the name of a variable/function/method/class or anything similar, wrap its name in a couple of backticks or quotation marks. It helps the reader detect that the wrapped word is different from others and is a reference to the codebase.


❌ `Upgrade Jest and React Testing Library to the latest versions`

✅ `Upgrade 'Jest' and 'React Testing Library' to the latest versions`

❌ `Use for-in loop instead of for-of loop inside calculatePrice function`

✅ `Use 'for-of' loop instead of 'for-in' loop inside the 'calculatePrice' function`

### 9. Extra Tips

* Write your messages just in English! Not any other language.

* Don't put dot (`.`) at the end of your messages.

❌ `Install 'Redux' and 'Redux Toolkit' libraries.`

✅ `Install 'Redux' and 'Redux Toolkit' libraries`


* Capitalize the first letter of the commit message.

❌ `write integration test for 'Settings' module`

✅ `Write integration test for 'Settings' module`


* Wrap lines at 72 characters. (Always there exist exceptions)

* Don't use urls in the messages.

### 10. Have a Coherent Log!

If you have a tour in the log of lots of the famous repositories, you can see a lot of differences between commit messages. For example, some of them have prefixes, and some don't. Some of them include emojis, some of them no. Some start with a capitalized letter, some of them no, etc. It usually happens because teams and persons don't follow typical rules. Always have a complete and clear guideline for yourself and your team. By doing it, you can prevent having inconsistent commit messages.

You can use some external tools and linters for double-checking the commits. Linters and these external tools, ensure that no commit message will conflict with the rules you applied. They force you and your team members to follow the rules.


**If this repository helped you, don't forgive getting a star ;)**
