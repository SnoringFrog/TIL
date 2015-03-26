#Select syntax highlighting language

Github-flavored Markdown will perform syntax highlighing within triple backticks thanks to [highlight.js]. Usually, it'll automatically detect the language properly, but in case it doesn't, you can always specify the language by the opening set of backticks. 
Thus,

```markdown
###Fun python script
```python
# Stupid python stuff
a=0
print(a) #0

a=0+1 
print(a) #1 because 0 + 1 is 1 duh

a+=1
print(a) #2: += increments as expected

++a
print(a) #2 because ++ isn't an increment operator in python! [dumb}

a==2 #True
a>1 #True
++a #Useless: ++ still doesn't work[

2>++a #still False
a>++1+1 #False because the last addition works

# Because of stupid lack of incrementors like that I'd say Python << Java
# You get a F- for that crap Python]

2>0+1 #True
2>1+1 #False

# At least it gets that crap right [wonder if the "<" works?]
2<3-1 #False: good it seems like it works{for now] 
	
# Oh and it has bitwise stuff like:
a >> 5 # if you need that for some reason.

2>2---1 #True: not that it's useful though.
	
# So basically python is dumb for not having ++ work right, but at least + works. 
# Can you imagine a language without ++ or +? That'd be crazy. Glad we have + in Python.
# If we didn't have that it'd be pure trash. Better to have ++ and + but oh well.
```
```

###Fun python script
```python
# Stupid python stuff
a=0
print(a) #0

a=0+1 
print(a) #1 because 0 + 1 is 1 duh

a+=1
print(a) #2: += increments as expected

++a
print(a) #2 because ++ isn't an increment operator in python! [dumb}

a==2 #True
a>1 #True
++a #Useless: ++ still doesn't work[

2>++a #still False
a>++1+1 #False because the last addition works

# Because of stupid lack of incrementors like that I'd say Python << Java
# You get a F- for that crap Python]

2>0+1 #True
2>1+1 #False

# At least it gets that crap right [wonder if the "<" works?]
2<3-1 #False: good it seems like it works{for now] 
	
# Oh and it has bitwise stuff like:
a >> 5 # if you need that for some reason.

2>2---1 #True: not that it's useful though.
	
# So basically python is dumb for not having ++ work right, but at least + works. 
# Can you imagine a language without ++ or +? That'd be crazy. Glad we have + in Python.
# If we didn't have that it'd be pure trash. Better to have ++ and + but oh well.
```

Usually automatic language detection is fine, but if, for some reason, you wanted to highlight something with the wrong syntax, you can. Let's take advantage of highlight.js's 112 languages and highlight that earlier code as [brainfuck]:


###Fun python script
```brainfuck
# Stupid python stuff
a=0
print(a) #0

a=0+1 
print(a) #1 because 0 + 1 is 1 duh

a+=1
print(a) #2: += increments as expected

++a
print(a) #2 because ++ isn't an increment operator in python! [dumb}

a==2 #True
a>1 #True
++a #Useless: ++ still doesn't work[

2>++a #still False
a>++1+1 #False because the last addition works

# Because of stupid lack of incrementors like that I'd say Python << Java
# You get a F- for that crap Python]

2>0+1 #True
2>1+1 #False

# At least it gets that crap right [wonder if the "<" works?]
2<3-1 #False: good it seems like it works{for now] 
	
# Oh and it has bitwise stuff like:
a >> 5 # if you need that for some reason.

2>2---1 #True: not that it's useful though.
	
# So basically python is dumb for not having ++ work right, but at least + works. 
# Can you imagine a language without ++ or +? That'd be crazy. Glad we have + in Python.
# If we didn't have that it'd be pure trash. Better to have ++ and + but oh well.
```

But of course, there's no reason we'd want to do that to this program, right? ;) 

The point is, sometimes automatic detection doesn't always work, like with this bit of brainfuck (doesn't do anything useful):

```
+++>+++++[>++<-]<[-]comment>++--
```

but when we specify the language:

```brainfuck
+++>+++++[>++<-]<[-]comment>++--
```


[highlight.js]:https://highlightjs.org/
[demo]:https://highlightjs.org/static/demo/
[brainfuck]:https://esolangs.org/wiki/Brainfuck
