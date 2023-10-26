# Quiz questions


This is only a "quiz" in the loosest sense that it's asking questions whose
answers will be part of your grade. Please use *any resources you want*, as
long as you list those resources (e.g. peers, websites, etc.)


## Navigating logs


1. What is the SHA for the last commit made by Prof. Xanda on this repo?
(For this and future questions, the first 5 characters is plenty.)


The SHA is 9b257


2. What is the SHA for the last commit associated with line 9 of this file?


The SHA is d1d83316


Source: Stack Overflow, https://stackoverflow.com/questions/8435343/retrieve-the-commit-log-for-a-specific-line-in-a-file.


3. What did line 12 of this file say in commit d1d83?


Line 12 said: I should really finish writing this.


Source: Boston University, https://www.bu.edu/tech/files/2019/06/Git_CheatSheet.pdf.


4. What changed between commit e474c and 82045?
The lines gross_sort = lambda x : int(x["Gross"]) and top_five = rows[:-6:-1] were added.


## Predicting merges

Assume at the start of each of these three questions that your
branch for switching to a top-10 list was called `top_ten`
and your branch generalizing to any number of movies was called `top_N`.
Predict the behavior of these three possible operations - you don't
have to provide a full `diff` but you should describe at a high level
what changes would happen.

These questions are supposed to be separate paths, not cumulative;
for example, you should *not* assume that the operations of 5 were run
before 6. When testing outcomes later in the lab, you should make sure to
revert back to the state of the branch before you started these questions.

5. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test
git merge top_N
```
When you run the first command, you are switching to the test branch. When you run
the second command, you merge top_N with the current branch (test).

Source: https://www.geeksforgeeks.org/git-merge/

6. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout top_ten
git merge test
```

When you run the first command, you switch to the top_ten branch. When you run the second command, 
you merge test with top_ten.

7. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test
git rebase top_ten
git rebase top_N
```
When you run the first command, you switch to the test branch. When you run the next command, you incorporate changes from current branch (test) onto top_ten. Same thing with the third command.

Source: https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase#:~:text=Rebase%20is%20one%20of%20two,has%20powerful%20history%20rewriting%20features.
