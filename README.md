# slack-dracula-theme

It's not perfect but for me close enough!

1. Close slack
2. Open this file
```/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js```
3. Append this to the end of it
```
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/Rand-o/slack-dracula-theme/master/dracula.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
```

4. Open slack and enjoy.