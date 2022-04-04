# Print multiple log file in single step

You can use this action to print multiple log files in a single step. Each log
file is printed in its own output group `File: $path` so it can be collapsed and
expanded in the workflow web-ui. A file that does not exist is ignored.

## Inputs

### `working-directory`

Working directory. Defaults to current working directory.

### `files`

List of files to print.

## Example usage

```yaml
- name: Print logs
  uses: next-actions/print-logs@master
  with:
    working-directory: logs
    files: |
      *.log
      added.err
      fixed.err
```
