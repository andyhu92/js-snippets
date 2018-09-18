# js-snippets
Some JS snippets I wrote and might be useful?

```
/*
  There was a task I need to import a whole bunch of select options value into database tables.
  It's really a pain to manually type those options...so if you have options value like a,b,c,d,e,
  this code will give you ('a'),('b'),('c'),('d'),('e')
  so you can do your insert like 
  -------------------------------------------
  insert into YourMasterTable (description)
  values ('a'),('b'),('c'),('d'),('e')
  -------------------------------------------
*/

function getSelectOptionsValue(id){
    var options = $("#" + id)[0].options, res = [];
    for(let i = 0; i < options.length; i++){
        res.push(options[i].textContent)
    }
    return "('" + res.join("'),('") + "')"
}
```
