While in vim, you can open multiple files as tabs with the following command:
	
	:args file1 file2 | argdo tabe | tabdo syntax on

Even better, you can use wildcards to open more files more easily. E.g.,

	:args *.xml | argdo tabe | tabdo syntax on

(Note: using argdo turns off syntax highlighting, which is why `tabdo syntax on` is added).

[Source]

[Source]: http://stackoverflow.com/questions/11430361/open-several-files-in-new-tabs-with-vim
