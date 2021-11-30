# A collection of shell things to remember

## Check if binary exists and is in the path
```bash
if which rustc > /dev/null; then
    echo "rust compiler installed!"
else
    echo "rust compiler missing!"
fi
```

## Do something if a pattern match exists
```bash
if pyenv virtualenvs | grep --quiet "test-env"; then
    echo "test-env virtualenv exist :)"
else
    echo "test-env does not exist :("
fi
```
