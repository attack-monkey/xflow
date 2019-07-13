# xflow
POC for using an experimental branch in gitflow..

Create an X branch locally. If you push to remote - add your name to it.

Having an X branch allows you to work ahead on features while other features are in review. X branch is like a speculation of what develop will be at the time a new feature goes up for review.

That way when feature 1 gets approved, feature 2 will be waiting and the diff will be from the current dev branch.

It's not a mgic bullet - since if a change is made to a feature in review, any future features not yet on develop will need to have the changes 'merged-up'.

Merge-up means to merge the previous feature into the next feature, which continues until there are no more outstanding features. Now merge the latest feature branch into X - bringing it up to date with the changes.

> Note that some changes will cause conflicts - which is fine. This is to be expected because the previous story changed, and you have presumably made more changes on top of that. Carefully review what changes you want. You may want both and then do a refactor. You may want to keep the latest change.

Whenever a change occurs to dev - merge dev to X to keep it in sync.

When you create a PR for a feature, also merge straight into X - since this is the speculation that the feature has already been merged. Now branch off of X.

If you have another feature ready to PR but you want to wait for #1 - no problem - just push to #2 branch - but don't PR. Then again merge #2 into X, since we are speculating that this will be develop.

Now when #1 gets approved, you can immediately put #2 up for review.
