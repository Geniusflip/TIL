# Formatting JS Dates with Intl

Discovered [here.](https://github.com/jbranchaud/til)

The default output of JS Dates is not too friendly.
```
> const now = new Date();
> now 
Sat Apr 25 2020 12:57:38 GMT+1000 (Australian Eastern Standard Time)
```

To get around doing hacky `Date.getDay()` concatination hell, usually you would use a date library like *Moment*.

However, the *Intl* standard library actually provides a simple alternative:

```
> Intl.DateTimeFormat('en-US', { dateStyle: "full" }).format(now)
"Saturday, April 25, 2020"
> Intl.DateTimeFormat('en-US', { dateStyle: "long" }).format(now)
"April 25, 2020"
> Intl.DateTimeFormat('en-US', { dateStyle: "medium" }).format(now)
"Apr 25, 2020"
> Intl.DateTimeFormat('en-US', { dateStyle: "short" }).format(now)
"04/25/20"
```

Also works with time values: 
```
> Intl.DateTimeFormat('en-US').format(1587783648787)
"Saturday, April 25, 2020"
```

The Intl library is incredibly powerful, and deserves many more TIL's. 

e.g. Intl for number formatting & standardisation.
