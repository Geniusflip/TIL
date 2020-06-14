# Input type for numbers

When writing accessible HTML forms, you should tend to prefer (1):
```html
<input type="text" inputmode="numeric" pattern="[0-9]*">
``` 
over (2):
```html
<input type="number">
```

for significant accessiblity reasons.

```Input(2)``` doesn't render well with common screenreaders, and with natural language inputs.

```Input(2)``` is also incrementable, meaning that it shouldn't be used with numbers that aren't incrementable, i.e Credit card numbers; Telephone numbers; Postcodes. 

```Input(2)``` also attempts to round larger numbers and convert to scientific format. This is particularly worse in Safari 6 where it rounds on unfocus.

```Input(2)``` in Safari 5.6 attempts to make things more readable by inserting commas

```Input(2)``` accepts all numeric input, meaning it also accepts 'e'. Some browsers implement this by accepting all input and silently discarding what is irrelevant. Meaning that users don't get feedback on what is valid. And assistive technologies don't alert the user that their input has been discarded.

```Input(2)``` also increments on scroll when focused!

