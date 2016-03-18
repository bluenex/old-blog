---
layout: page
title: Random App
permalink: /random/
---

Coming soon..

<form>
  First name:<br>
  <input id="getname" type="text" name="firstname"><br>
  Last name:<br>
  <input type="text" name="lastname">
  <button type="button" id="dumbbutton"> temp </button>
</form>

<script>
  for(i = 0; i < 5; i++) {
    console.log(Math.floor((Math.random() * 10) + 1));
  }

  document.getElementById('dumbbutton').onclick = function() {
    var a = document.getElementById("getname").value;
    console.log(a)
  };
</script>
