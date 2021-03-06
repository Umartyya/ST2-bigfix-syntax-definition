# ST2-bigfix-syntax-definition

*NOTE: I no longer work at IBM, so this is stagnant. I no longer use relevance on a daily basis so I am not privy to any changes in syntax.*

## Description

This is a user-defined syntax definition for the Relevance language. Relevance is one of the proprietary languages used by IBM Endpoint Manager (IEM), formerly known as Bigfix.

## Why? Nobody uses this..

Well, I do in my job <sup>[No longer true. See note above.]</sup>. Since there isn't a proper fixlet debugger, which is a Windows-only GUI application, in my development OS of choice (OS X), and I use ST2 a lot for development, I decided to hack this up. It's pretty much a work in progress.

There is a command-line debugger in for unix-like OSes, but there's no fancy shmancy colors. I like colors.

## Installation

- In the menu, navigate to Preferences-Browse Packages. In OS X, the preferences menu is a sub-menu under "Sublime Text 2" menu.
- Copy over the file bigfix_relevance.tmLanguage to the User folder there.

  In OS X, the exact folder is /Users/<username>/Library/Application Support/Sublime Text 2/Packages/User.

  In Windows, the exact folder is C:\Users\<username>\AppData\Roaming\Sublime Text 2\Packages\User.
  
  Not sure for Linux distros.

- Restart Sublime Text 2.
- Bigfix Relevance syntax should be available in the menu under View-Syntax. Opening *.qna files in Sublime Text 2 should automatically use that syntax as well.

## Building from source

The steps below attempt to complement the steps from [Sublime Text documentation](http://docs.sublimetext.info/en/latest/extensibility/syntaxdefs.html). For more information, please read the Sublime Text docs.

- Install the AAAPackageDev package in Sublime Text 2.
- In the menu, navigate to Tools-Packages-Package Development-New Syntax Definition. A new YAML template should be created in a new tab.
- Copy over everything in bigfix_relevance.YAML-tmLanguage EXCEPT THE UUID FIELD.
- To build, hit Cmd+B (not sure for the shortcut for other OSes). Or in the menu, navigate to Tools-Build.
- Restart Sublime Text 2 (though sometimes not necessary).

## Bugs / Known Issues

None at the moment.

The scope names might not make sense. One of the tips I got when googling about what scope names I can use is to model it after a language I often use. Since I like and use Ruby, I just tried to fit it to Ruby's scope names, just to get good colourization.
