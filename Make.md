# A collection of Makefile things to remember

## Bash branching
Make sure to include back slashes at the end of each line. Also don't forget 
the semi-colons for each line
```bash
random-target:
    if which rustc; then \
        echo "rust is installed"; \
    else \
        echo "rust is not installed"; \
    fi;
```

## De referencing bash variables
Since the $ symbol is used to dereference variables in make, the $ symbol must
be dereferenced in order to be used with bash variables.
```bash
random-target:
    @echo $$PATH
```
