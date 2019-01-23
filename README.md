# About the Mozilla TechSpeakerBot
The mtsbot takes care of some of the online chores of the Mozilla TechSpeakers and provides integrations with GitHub's services. There is a big variety of tasks it is involved in (or, will be, in the future).

## CFPs
One of the important duties of mtsbot is taking care of the rather ambitious syncing of services required for running the CFP calendar integrations.

The mtsbot tracks direct messages on the [@mozTechCFPs](https://twitter.com/moztechcfps) Twitter account and ensures the CFP suggestions end up in a GitHub issue over at the [`conf-db`](/techspeakers/conf-db/issues) repository. Admins can further detail the scraped information and ask mtsbot for its inclusion in the CFP calendar. Here are the usable commands (only usable by users with sufficient privileges):

* `preview` - based on the current state of the issue and data contained, how will the CFP calendar entry/tweet look like? Can also be used to warn for missing mandatory data (e.g. if the conference CoC was not provided).
* `add` - take the data from the issue and add it into the calendar. mtsbot may refuse to add the event to the tracked events if some non-optional data is missing - in this cases it will report back and ask for the data to be completed.
* `highlight` - similar to `add`, except mtsbot will tweet about the new CFP calendar addition while adding the event to the calendar.
* `discard` - mtsbot will not add the event to the calendar and close the issue. The people maintaining and curating the TechSpeakers calendar may choose freely to not include events without further explanation. Closing the issue without telling mtsbot to add the event to the calendar has the same effect as this command.
