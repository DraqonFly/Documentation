
## 1. Interactive Git Rebase

		git rebase --interactive HEAD~6
		git rebase --interactive HEAD~abcdef

	pick abcdef		//holder of squashed commits 
	squash abcde2	//change action on commit to squash
	squash abcde3	//change action on commit to squash
	squash abcde4	//change action on commit to squash
	squash abcde5	//change action on commit to squash
	squash abcde6	//change action on commit to squash

## 2. Change commit message of squashed commit 

		git commit --amend
	  	git commit --ammend -m "message..."

## 3. Available actions on rebase

	git rebase --abort 		// reset changes and undo rebase
	git rebase --edit-todo	// rechange actions on commits
	git rebase --continue   // continue (solve merge conflicts)

## 4. Push Changes made by rebase

	git add

	git push --force 						// no merge conflicts
    git push origin HEAD:master --force 	// merge conflicts but push anyway 