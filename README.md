# TamperMonkey PowerToys
Here is a TamperMonkey script template that enables custom keyboard shortcuts on any page.

## Features
### On the fly URL detection
TamperMonkey used to load if the page URL matches a given pattern on page load. But if the page URL is modified programatically without reloading the page, TamperMonkey's script is not reloaded.

This scripts looks at window.location.href dynamically (hence it's a kind of meta script that applies to multiple pages)

### Page patterns
Keyboard shortcuts are defined for a given page pattern (even if the script is unique across multiple URLs as explained above)

### Customizable shortcut engine
Add your shortcut easily nthe shortcut maps. Target shortcut functions can be invoked with parameters !

## How to configure
### Global match
Configure the @match line in the headers : it should be the common part of all the URLs you want to impact.

### Invocation functions
Add function you would like to invoke on a shortcut. You can have parameters as well, as long as
* parameters are constant
* or parameters are valid if evaluated once on page load
* or parameters are evaluated on the fly (using eval)

### Url groups
Define a set of unique constants to identify the different URL targets

### Url Patterns
For each URL target, add a URL pattern that will be evaluated dynamically (the @match replacement)

### Target function and parameters
in the map below, for each URL group and pattern, define a map of shortcut / target, where target is a pair "invoked function / array of parameters"

## Example
In the example available from the repo, whe have 2 page groups : Google and others. We also have different shortcuts for each - on Google ZZT adds page title into clipboard, on any website ZZU sets URL into clipboart


Have fun :) 
