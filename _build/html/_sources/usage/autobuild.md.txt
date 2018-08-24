# Autobuild Sphinx

## Setup Watchdog

```
pip install watchdog
```

## Run the Listener

```
watchmedo shell-command \
            --patterns="*.md;*.rst;*.txt;*.py" \
            --ignore-pattern='_build/*' \
            --recursive \
            --command='make html'
```
