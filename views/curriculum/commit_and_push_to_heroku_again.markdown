# Commit and Push to Heroku, Again
## Goals
We just made some awesome changes. Let's push them so our friends can play with it.

## Steps
Type this in the terminal:

```text
git add .
git commit -m "Added votes"
git push heroku master
heroku run rake db:migrate
```

## Explanation
We commit our changes, push them out and run the remote migration... By this time it should be fairly old hat.

## Extra Credit
If you already tried working with the [Rails console](extra_credit/04_console),
why not [add some pagination](extra_credit/05_pagination)?

## Next Step
Go on to [Setting the Default Page](setting_the_default_page)
