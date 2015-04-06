# Pass Arguments to Script Run From URL

Sometimes it's useful to run a script directly from it's URL rather than saving it locally*. If you need to pass arguments to such a script, just precede the arguments with `/dev/stdin` after your call to `bash`:

	curl -s script_url | bash /dev/stdin arg1 arg2

*: Note, this can also be quite dangerous; don't just run around executing random scripts directly from the internet without reason.
