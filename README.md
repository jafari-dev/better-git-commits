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
