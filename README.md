
# Strongbox Babel
This is the repository for contributing to translation and localisation for Strongbox. Please read the CONTRIBUTIONS.md file before you contribute. 

**Note**: It is no small task as there are upwards of 6,000 words in the project, so please only take this on if it something you feel you can do a good job on and bring to completion. I don't want to release a localised Strongbox which is only half way there, Thanks!
# How to contribute for your Language
If you'd like to have Strongbox translated into your language and are willing to do so under the terms of the MIT licence then please follow the steps below:

1. Get in touch (support@strongboxsafe.com) or simply open an issue here and we can discuss.

2. I will add you to the Crowd In system and you can begin translating

3. If you come across any issues, or problems with existing contributions, or if you can't find a particular string then just create and issue here in this repository and hopefully we can resolve things quickly and amicably.

4. Once you've completed and all going well, your work will be waiting for a Pull Request and I should be able to take this work integrate it into the main app.

# Hints, Tips & FAQ for Contributors
 - Start with **StrongBox/Localizable.strings** - it's the biggest one and you'll have almost all expressions/terms to decide on the best translation. You can then keep these terms consistent across the code base. For example, will you use 'Unlock' or 'Open'?

 - **Empty Files** - There are some empty files with nothing to translate at all. This is fine, they're just auto generated, feel free to ignore. e.g.
    - StrongBox/SelectItem.strings    
    - StrongBox/LaunchScreen.strings
- **Some strings you can skip**, e.g. Licences (There is a copy of the MIT licence in the About screen and other copyright notices). I'll try collect a list of these strings and remove them from the process

 - If you **miss** some strings, don't worry! Everything will be fine, it's not the end of the world you can always see it in the app after a release, and come back and change it later.
 - It is helpful to have the App available in front of you for context
 
### Determining Context
Sometimes you'll need to see the context where the strings are used, for better understanding the appropriate localisation. Unfortunately this is a little bit difficult but here is something you can try:

- You should be able to search for this in the original source code project here: https://github.com/strongbox-password-safe/Strongbox

- If you can't find it, don't worry, just let us know and I'll try to find it for you. In some cases it may be best to continue translation and worry about it after a release, where you can look for it or spot it in app. This is fine too. Considering how many strings there are in the project, it will be hard to get it right first time.

# Caution
Some caution is required only in a couple of cases, these are related to programmatic or escape characters described below. We will run a couple of checks anyway before integration into Strongbox so just do your best.

### Format Strings
These look something like below (they begin with a percentage sign) and are used in code to insert parameters into a string programmatically, e.g. **"25 days remaining"** might look like **"%d days remaining"** in the strings file.

    %@
    %d
    %ld
    %f
    %s
    %c
    
These need to stay in the same order also, you cannot change something like "%@ blah %d" to "%d blah %@" as that would cause a crash.

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
Below is a list of the contributors for various languages completed so far.

- Chinese - GY & Attis
- French - Charles-Ivan Chesneau
- German - @Slummi
- Italian - Marco Ermini
- Russian - Wishes to remain anonymous
- Spanish - Wishes to remain anonymous
- Swedish - Jari Häkkinen
- Ukrainian - Artem Polivanchuk

Don't see your language? Get in touch to help out.
-Mark



