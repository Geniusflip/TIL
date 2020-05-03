# Loops in Bash

We can easily loop over output using the ```for do``` keywords

e.g.

``` 
for i in *.png
do
    convert $i : $i.jpg
done
```