# Reclaim start page, home button and address search engine
1. Navigate to `edge://settings/startHomeNTP`
2. Under **On startup**, select **Open custom sites**
3. Click **Add site** and enter your desired URL
4. Enable **Show the home button on the toolbar**
5. Select **Set custom Site** and set your preferred home page URL

<img width="1245" height="862" alt="image" src="https://github.com/user-attachments/assets/f7189cea-c815-4472-8c95-c2e27f6c5666" />
   
7. Navigate to `edge://settings/privacy/services/search`
8. Set **Search engine used in the address bar** to your desired engine

<img width="1222" height="461" alt="image" src="https://github.com/user-attachments/assets/ac56e607-f44c-43bf-adc9-507b08ac8ae9" />


# Reclaim new tab extension
1. Create a folder (example: NewTabRedirect)
2. Within NewTabRedirect folder create manifest.json
```
{
  "manifest_version": 3,
  "name": "New Tab Redirect",
  "version": "1.0.0",
  "description": "Overrides the new tab page and redirects to Google.",
  "chrome_url_overrides": {
    "newtab": "newtab.html"
  }
}
```
3. Within NewTabRedirect folder create newtab.html (update the url to suit)

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="refresh" content="0; url=https://www.google.com.au/" />
    <title>New Tab</title>
  </head>
  <body>
    Redirecting...
  </body>
</html>
```

Load the extension
1. Open edge://extensions
2. Enable Developer mode
3. Click Load unpacked
4. Select the extension folder
5. Open a new tab — it should redirect.
