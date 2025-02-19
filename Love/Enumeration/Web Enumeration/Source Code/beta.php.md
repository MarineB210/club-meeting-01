***
> [!TIP]
> Always a good idea to give the source code of each page a quick check.

```
 <form name="fileform" method=post action="[/beta.php](view-source:http://staging.love.htb/beta.php)" onsubmit="return validateForm()">
```

```js
    <script>
  function validateForm() {
    var x = document.forms["fileform"]["file"].value;
    if (x == "") {
    alert("Please enter a file url to scan");
    return false;
  }
  
}
    </script>
```

