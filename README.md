# Roll Bot for GroupMe

## Requirements:

  * GroupMe account
  * Heroku account

# Bot Commands<a name="commands"></a>
All commands can start with "!" or "/"

/roll (range 1 - 100):
    
    /roll

/roll xdy (rolls y sided dice x times):

    /roll 1d20

/roll min max (range min - max):

    /roll 5 500

# Get bot up and running<a name="deploy"></a>

## Deploy to Heroku:

Be sure to log into heroku, using your heroku credentials, then click the link below.

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Next, create a GroupMe Bot:

Go to:
https://dev.groupme.com/session/new

Use your GroupMe credentials to log into the developer site.

Once you have successfully logged in, go to https://dev.groupme.com/bots/new

Fill out the form to create your new bot:

  * Select the group where you want the bot to live
  * Give your bot a name
  * Paste in the url to your newly deply heroku app
    * `http://your-app-name-here.herokuapp.com/`
  * (Optional) Give your bot an avatar by providing a url to an image
  * Click submit

## Add your Bot ID to your Heroku app:

Go here to see all of your Heroku apps and select the one you just created before:

https://dashboard-next.heroku.com/apps

On your app page, click settings in the top navigation:

On your app's setting page, find the Config Vars section and click the Reveal Config Vars button:

Then click edit:

Fill out the form to add an environment variable to your app:

  * In the "key" field type: BOT_ID
  * In the "value" field paste your Bot ID that you copied in the previous steps
  * Click the save button

## Test the bot

Go to GroupMe and type "/cool guy" in the group where your bot lives to see it in action.

# Run locally
## Pull the code to your local machine

Within terminal, change directory to the location where you would like the files to live, then run this command:

    $ heroku git:clone -a YOUR_APP_NAME_HERE

And then change directory into the new folder

    $ cd YOUR_APP_NAME_HERE

## Configure your local BOT_ID environment variable

Open the file `.env` from your local files in your text editor of choice.
Find where it says "YOUR_BOT_ID_HERE" and replace it with the ID of your new bot.

    BOT_ID="YOUR_BOT_ID_HERE"

## Start the server

To test your bot locally, open terminal and run the following command to start a local server.

    $ foreman start

Then navigate to `http://127.0.0.1:5000/` in a browser.

