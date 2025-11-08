# Calculate Age Function

Use this Javascript function to calculate an age for the current date based on an input date field's value. Returns the current age in whole years.

## Code

Insert this code in Properties->Custom Code:

```
<script>
  function calcAge(sourceDate) {
    if (sourceDate!='') {
      age=Math.floor((new Date() - new Date(sourceDate)) / (365.25 * 24 * 60 * 60 * 1000));
    } else {
      age='';
    }
    return age;
  }
</script>
```

## Usage

In a calculted field, call the Javascript function using this syntax: ` calcAge(<FieldName>) `.

## Special Notes

The function accounts for the value of the date field starting blank. Considerations should be made for validation that the source date you specify is not in the future–otherwise the function will return a negative value.