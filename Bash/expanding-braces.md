# Expanding braces

Almost magically we can do a cartesian product on text using magical braces.

Like so

```
$ convert file.{jpg, png}
```

expands to

```
$ convert file.jpg file.png
```