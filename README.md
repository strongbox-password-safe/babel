
# Strongbox Babel
This is the repository for contributing to translation and localisation for Strongbox. Please read the CONTRIBUTIONS.md file before you contribute. 

**Note**: It is no small task as there are upwards of 6,000 words in the project, so please only take this on if it something you feel you can do a good job on and bring to completion. I don't want to release a localised Strongbox which is only half way there, Thanks!
# How to contribute for your Language
If you'd like to have Strongbox translated into your language and are willing to do so under the terms of the MIT licence then please follow the steps below:

1. Get in touch with me (support@strongboxsafe.com) or simply open an issue above and we can discuss.

2. Once you're happy with your contribution, create a review request, then submit a pull request with your changes. I'll review and make sure they won't crash or otherwise cause any trouble with the Strongbox.

3. If you come across any issues, or problems with existing contributions, or if you can't find a particular string then just create and issue here in this repository and hopefully we can resolve things quickly and amicably.

4. All going well, I should be able to take the work you've contributed here and integrate it into the main app.

# Hints, Tips & FAQ for Contributors
 - Start with **StrongBox/Localizable.strings** - it's the biggest one and you'll have almost all expressions/terms to decide on the best translation. You can then keep these terms consistent across the code base. For example, will you use 'Unlock' or 'Open'?

 - You can use the **Machine Translate** button to speed things up (It's not perfect but sometimes it can be uncannily accurate)
 - **Strange Strings** (e.g. "m9o-ET-lXK" or "nKD-uE-qBB") - These are either strings from XCode Interface builder or test placeholder strings. Feel free to ignore all of these. GitLocalize doesn't do a brilliant job or parsing the original XCode generated strings files.
 - **Empty Files** - There are some empty files with nothing to translate at all. This is fine, they're just auto generated, feel free to ignore. e.g.
    - StrongBox/SelectItem.strings    
    - StrongBox/LaunchScreen.strings
- **Some strings you can skip**, e.g. Licences (There is a copy of the MIT licence in the About screen and other copyright notices). I'll try collect a list of these strings and remove them from the process

 - If you **miss** some strings, don't worry! Everything will be fine, it's not the end of the world you can always see it in the app after a release, and come back and change it later.
 - It is helpful to have the App available in front of you for context
 
 ### GitLocalize Bugs
GitLocalize does appear to have some bugs. It's not a perfect tool, but it does help get the job done. If you have a lot of entries which are separated on multiple pages the percentage progress bar works for the current page only (e.g. if page 1 is not ready yet and you are finished all entries on page 2 - it already shows 100% on page 2 at first). Only after switching pages the overall progress gets updated.

If you already translated an entry, then edit it again, click on machine translate (in case something changes) and finally click on cancel you’d see at first that everything is correct. But in reality the latest machine translated text was saved, which can lead to wrong translation (you’ll see the saved value, if you reload the page).

The same problem is happening when you click into an empty entry, machine translate it and click on cancel. At first you'd see your grey and untranslated text, so you could probably think that everything is fine, but after refreshing the page, you’ll see that machine translated text.

In short it helps to refresh regularly.

### Determining Context
Sometimes you'll need to see the context where the strings are used, for better understanding the appropriate localisation. Unfortunately this is a little bit difficult but here is something you can try

- Tap the 'See content on Github' in Gitlocalize button which will open it as the original Strings file.
- Find the string you're interested in by search for it
e.g.  https://github.com/strongbox-password-safe/babel/blob/master/StrongBox/CreateDatabaseOrSetCredentials.strings
- You should be able to search for this in the original source code project here: https://github.com/strongbox-password-safe/Strongbox

But if you can't find it, don't worry, just let me know and I'll try to find it for you. In some cases it may be best to continue translation and worry about it after a release, where you can look for it or spot it in app. This is fine too. Considering how many strings there are in the project, it will be hard to get it right first time.

# Caution
Some caution is required only in a couple of cases, these are related to programmatic or escape characters described below. Unfortunately **Machine Translate** is not very careful or good at this, so that's when you really need to look out. 
I will run a couple of checks anyway before integration into Strongbox so just do your best.

### Format Strings
These look something like below (they begin with a percentage sign) and are used in code to insert parameters into a string programmatically, e.g. **"25 days remaining"** might look like **"%d days remaining"** in the strings file.

    %@
    %d
    %ld
    %f
    %s
    %c

### Quotes
Because strings are delimited by double quotes (i.e. ") any strings that include double quotes need to have that character specially escaped. This is done by using a backslash (i.e. \\"). So for example the string:

    Noam said "Colorless green ideas sleep furiously"

looks like the following when escaped properly:

    "Noam said \"Colorless green ideas sleep furiously\""

This will be obvious enough in context.

### Line Breaks
Line breaks are another area where you need to be careful. Line breaks are encoded as "\\n", and often there can be multiple within a string, e.g.

    "Hi,\nThis is a multiline string!\n\nThanks for your help!\n-Mark"

which will be rendered as:

    Hi,
    This is a multiline string!
    
    Thanks for your help!
    -Mark

# Language Contributors
Below is a list of the contributors for various languages so far.

- German
    - @Slummi
- Russian
    - @xatage
- Ukrainian
    - @a-polivanchuk
- Chinese
    - Help welcome
- French
    - Help welcome
- Italian
    - Help welcome
- Japanese
    - Help welcome
- Portuguese
    - Help welcome
- Spanish
    - Help welcome

Don't see your language? Get in touch!
-Mark



