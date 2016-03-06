# settings.py: configuration for the site

At the root of the site there is a configuration file called `settings.py` that
is interpreted via Python similarly to what happens in
[Django](https://docs.djangoproject.com/en/1.9/topics/settings/).

Only uppercase settings are used.

Default settings are defined in the module `staticsite/global_settings.py` and
overridden by `settings.py`.

## Common settings

```py
# Name of the website
SITE_NAME = "Example web site"

# Author of the website
SITE_AUTHOR = "Example author"

# Absolute URL to the root of the website
SITE_URL = "https://www.example.org"

# Time zone used for site posts
TIMEZONE = "Europe/Rome"

# Root directory of the site in the URLs we generate.
# If you are publishing the site at /prefix instead of root of the domain,
# override this with /prefix
SITE_ROOT = "/"

# Directory with the source content of the site
# Default: the project directory itself
CONTENT = "content"

# Theme used to render the stie
# Default: the one installed in the system
THEME = "theme"
```


## Other settings

```py
# Editor used to edit new pages (defaults to $EDITOR)
EDITOR = os.environ.get("EDITOR", "sensible-editor")

# Command used to run the editor, as passed to subprocess.check_command.
# Each list element is expanded with string.format. All settings are available
# for expansion, and {name} is the absolute path of the file to edit.
EDIT_COMMAND = ["{EDITOR}", "{name}"]
```

[Back to README](../README.md)
