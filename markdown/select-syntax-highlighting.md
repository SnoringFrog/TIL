#Select syntax highlighting language

Github-flavored Markdown will perform syntax highlighing within triple backticks thanks to [highlight.js]. Usually, it'll automatically detect the language properly, but in case it doesn't, you can always specify the language by the opening set of backticks. 
Thus,

```markdown
	```bash
	$ ls ~
	$ echo $USER
	```
```
becomes

```bash
$ ls ~
$ echo $USER
```

There are a ton of languages supported (112 at time of writing), you can find them all at highlight.js's [demo]. So even this works:

```markdown
#test
```brainfuck
+++++ +++++ [->++ +++++ +++<] >++++ .+.-- .+.++ ++.-- -.--. +.<++ +[->+
++<]> +++.< +++++ +++[- >---- ----< ]>--- ---.< +++++ ++[-> +++++ ++<]>
+++++ +++++ +.+++ +++++ +.<++ +++++ ++[-> ----- ----< ]>--. <++++ ++++[
->+++ +++++ <
random comment
]>++ +++++ ++.<+ ++[-> +++<] >+.<+ +++++ +++[- >---- -----
<]>-- .<+++ +++++ [->++ +++++ +<]>+ +++++ +.<++ +[->+ ++<]> ++.<+ ++[->
---<] >---- .---- .<+++ +[->+ +++<] >+++. <
```
```

```brainfuck
+++++ +++++ [->++ +++++ +++<] >++++ .+.-- .+.++ ++.-- -.--. +.<++ +[->+
++<]> +++.< +++++ +++[- >---- ----< ]>--- ---.< +++++ ++[-> +++++ ++<]>
+++++ +++++ +.+++ +++++ +.<++ +++++ ++[-> ----- ----< ]>--. <++++ ++++[
->+++ +++++ <
random comment
]>++ +++++ ++.<+ ++[-> +++<] >+.<+ +++++ +++[- >---- -----
<]>-- .<+++ +++++ [->++ +++++ +<]>+ +++++ +.<++ +[->+ ++<]> ++.<+ ++[->
---<] >---- .---- .<+++ +[->+ +++<] >+++. <
```

And here it is without specifying the language:

```
+++++ +++++ [->++ +++++ +++<] >++++ .+.-- .+.++ ++.-- -.--. +.<++ +[->+
++<]> +++.< +++++ +++[- >---- ----< ]>--- ---.< +++++ ++[-> +++++ ++<]>
+++++ +++++ +.+++ +++++ +.<++ +++++ ++[-> ----- ----< ]>--. <++++ ++++[
->+++ +++++ <
random comment
]>++ +++++ ++.<+ ++[-> +++<] >+.<+ +++++ +++[- >---- -----
<]>-- .<+++ +++++ [->++ +++++ +<]>+ +++++ +.<++ +[->+ ++<]> ++.<+ ++[->
---<] >---- .---- .<+++ +[->+ +++<] >+++. <
```

[highlight.js]:https://highlightjs.org/
[demo]:https://highlightjs.org/static/demo/
