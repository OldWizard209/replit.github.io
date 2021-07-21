# Getting repl metadata

In some cases, it's useful to automatically retrieve metadata about a repl from within that repl.

You can find **owner** and **project name** of the current repl in environment variables `REPL_OWNER` and `REPL_SLUG` respectively.

![owner and slug](/images/misc/ownerproject.png)

## Using Python:

```python
import os
print(os.getenv("REPL_OWNER"))
print(os.getenv("REPL_SLUG"))

# Output
# ritza
# repl-environment-variables
```

**Note:** The '@' is not included in the environment variable so, to build the full project URL, you need to manually include it. For example:

```python
import os
user = os.getenv("REPL_OWNER")
slug = os.getenv("REPL_SLUG")
print(f"This project can be found at https://replit.com/@{user}/{slug}")
```

## Using Node.js:
```js
console.log(process.env.REPL_OWNER) 
console.log(process.env.REPL_SLUG) 
```

