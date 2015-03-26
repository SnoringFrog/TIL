#Get List of Formulas in a Tap

When I find a new tool/script from a developer, I often check out their other work to see what they've got. Thought it'd be nice to do that with Homebrew taps too, so I looked up how to do that. 


```bash
TAP=thoughtbot/homebrew-formulae # replace with the tap you want, but make sure to add the 'homebrew-' prefix
ls $(brew --prefix)/Library/Taps/$TAP/Formula/*.rb` || ls $(brew --prefix)/Library/Taps/$TAP/*.rb
```

If you just want to see all formulas from all taps, this will print them out under their repective  dev/organization names:

```bash
for f in `\ls $(brew --prefix)/Library/Taps`; do echo $f; find $f -regex .*/.*.rb | cut -d"/" -f2- | sed "s/\/Formula\|homebrew-\|\.rb//g"; echo; done
```
(the "\" in front of `ls` is to run the default `ls` in case you have `ls` aliased to provide color, like I do, because the colors will confuse find)

[Source]
[Source]:http://stackoverflow.com/questions/25334787/homebrew-get-list-of-formulas-in-a-tap
