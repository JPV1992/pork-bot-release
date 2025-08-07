# pork-bot-release
The release repository for the Twitch Chat Bot "PorkBot"

# PorkBot the Twitch Chat Bot Wonder!

PorkBot is a  C# .NET chat bot designed to run locally on a streamers machine and sit in their twitch channel to provide a wide variety of different functionalities.

Currently the only commands available are relating to creating, storing, editing and retrieving quotes users can add to a SQLite database, but more functionality is planned for the future so stick around!

## Setup

To setup PorkBot, carry out the following:

1. Download/Extract and double click the PorkBot.exe
2. If it asks for administrator permissions to run click yes
3. A console window should appear, on first setup it will ask you to enter YOUR twitch username. Enter it and press enter
4. It should then give you a URL to click to authorise PorkBot for your account. Either click it, or copy the link into a browser.
5. Sign into your twitch account and authorise
6. Go back to the console window and press enter.
7. It should then connect to chat. Any errors will appear in red text.
8. When it's fully connected and set up, it should have a message of "Successfully registered Event Sub Listeners. Now subscribed to channel.chat.message."

To close the console down at any point just click in the window and press Ctrl+C

**IMPORTANT:** - PorkBot will post messages to the channel under the twitch account of the authorised user

## Commands

Currently PorkBot is released with the quote functionality added and more features to come! The existing commands are:

Command | Syntax | Description
----------- | ------- | -----------
**Commands** | *!commands* | Should lead back to this discord post or an image link of it for reference
**AddQuote** | *!addQuote user quoteText* | Add's a quote to the database for that user with the text supplied after the username. A response message confirms the creation of the quote along with it's ID in the database to be recalled later.
**EditQuote** | *!editQuote user quoteId newQuoteText* | Edits an existing quote, replacing the old quote text with the newly supplied quote text
**DeleteQuote** | *!deleteQuote user quoteId* | Deletes the quote with the users quote based on the id supplied
**Quote** | *!quote user quoteId* | Gets a quote from the specified user, with the specific ID
**QuoteCount** | *!quoteCount user* | Gets the total number of quotes in the database for the specified user
**QuoteList** | *!quoteList user* | Gets a list of every existing quote ID for the specified user
**RandomQuote (any quote in the DB)** | *!randomQuote* | Gives a random quote from any user in the database
**RandomQuote (specific user)** | *!randomQuote user* | Gives a random quote from the specified user
