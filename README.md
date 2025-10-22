<!DOCTYPE html>
<html>
  <head>
        <script>
        // This script is a fallback and runs if meta refresh is ignored or delayed.
        // It waits 5 seconds, matching the meta tag.
        window.onload = function() {
            setTimeout(function() {
                window.location.href = "https://www.example.com/new-location";
            }, 5000); // 5000 milliseconds = 5 seconds
        };
    </script>
  </head>
  <body>
    <h1> YOU ARE BEING REDIRECTED THE AI PAGE IS AT A DIFFRENT URL </h1>
  </body>
</html>
