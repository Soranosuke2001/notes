# `bisect` Command

**Finding a bug from multiple commits**
```bash
git bisect start

git bisect bad

git bisect good <commitish>

git bisect run <command or script>

git bisect reset
```

Note: when using a script, `exit 0` is good and `exit 1` is bad
