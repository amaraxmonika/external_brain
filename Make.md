# A collection of Makefile things to remember

## Phony target
A phony target is a make target that is not the name of a file, but the name
of a recipe.
```bash
random-target:
    do_things
    ...
    
.PHONY: random-target
```

## Shell control flow
Make sure to include back slashes at the end of each line. Also don't forget 
the semi-colons for each line.
```bash
random-target:
    if which rustc; then \
        echo "rust is installed"; \
    else \
        echo "rust is not installed"; \
    fi;
```

## Dereferencing shell variables
Since the $ symbol is used to dereference variables in make, the $ symbol must
be dereferenced in order to be used with shell variables.
```bash
# Example where result of shell function is assigned to a make variable.
GIT_HASH := $$(git rev-parse --verify HEAD | cut -b1-4)
# Example of dereferencing the PATH shell variable in a make target
random-target:
    @echo $$PATH
```
