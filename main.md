# main.py – Entry Point

This script is the entry point for the Domain Checker project. It does the following:

1. Loads configuration from a YAML file.
2. Calls the main checker function (`run_checker`) using async.
3. Prints the result to the console.

## Flow Summary

```python
load_config(...) → run_checker(config) → print result
