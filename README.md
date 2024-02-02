# rebase-test

Trying rebase workflow (disallowing non-rebased merges) to see if many open pull requests will all be invalid if one is merged.
Will branch protection apply to me, even though I created the repo?
topic newline
topic newline
topic newline
topic newline
nnewline
even
more newline
more newline
more newline
Main is adding two lines. Editing line 7, will cause conflict?

Updating main, making feat1 non mergable?.

main new overlap 19
main new overlap 19
I am main, this is the proper 20
I am topic, this is row 20
topic edit on 19
topic write on 13

Main re-writing on 21 again

main write on 21


Results:
I found that it's only editing the same line  which gives merge conflicts.
Feature branch editing line 20 and main adding a new line on 10 does not cause merge conflict, even though feature didn't think its edit was line 21.
git is smart with line add/remove.
"Require linear commit history" branch protection rule does not "force rebase". Squash commit is also linear history, as if a feature branch's commits were just added on top of main.
A good workflow is probably best off rebasing feature branch locally to main and repeating manual testing with newer main, then continue to PR. Lack of merge conflicts does not guarantee functional code.
