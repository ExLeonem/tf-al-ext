

# How to create a custom tf-al package?


1. Clone this directory with 

```shell
git clone https://github.com/ExLeonem/tf-al-ext
```

2. Replace the `ext` in the folder names as well as in the pyproject.toml with a personal extension.
3. Setup [poetry](https://python-poetry.org/docs/#installation) and [install dependencies](https://python-poetry.org/docs/basic-usage/#installing-dependencies)
4. Start developing and extending the package
5. Share via github/pypi


## Directory structure

To keep an easy and generic API across different extension, please keep following structure. 


| Directory name | Description
| --- | ---
| `\wrapper` | Custom model wrappers.
| `\score`| Custom scores to evaluate active learning experiments
| `\utils` | For utility functions


No fitting folder? Just create a custom one.



## Versioning

Follow the [semantic versioning](https://semver.org/lang/de/) rule set. (v. Major.Minor.Patch)



# Scripts

## Unittests

To execute unit tests, type in following command:

```
poetry run pytest
```

## Depenency managament

To add another package dependency, execute following command

```
poetry add <package-name>
```

Likewise if you want to delete a dependency:

```
poetry remove <package-name>
```

## Publish to pypi

Run following commands one after another.

```
poetry build
```

```
poetry publish
```


For other commands that are executeable check the documentation of [poetry](https://python-poetry.org/docs/cli/).