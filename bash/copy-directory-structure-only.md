#Copy Directory Structure Without Files

If you need to copy some piece of directory structure elsewhere without any of the internal files, these two commands get it done:

```bash
find . -type d >dirs.txt
xargs mkdir -p <dirs.txt
```

[Source]

[Source]:http://stackoverflow.com/questions/4073969/copy-folder-structure-sans-files-from-one-location-to-another
