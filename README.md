# agenda-app
A Google script based app which automatically creates agendas for meeting from template

### How It Works

The script is quite simple. The main trigger for the code is in the `onCalendarChange` function. This function is triggered whenever a new Google Calendar event happens. It then "looks ahead" and picks up any Calendar event with the keyword "#agenda". When it finds those, it replaces the keyword with a link to the agenda doc, which it creates by first using the `checkFolder` function (to see if a folder and a template already exist). If a template exists, it uses that for the new document. If not, it has a default agenda **hard coded** into the script which it uses to create a template.

As mentioned, the script is very simple so it's all in `main.js` in this repository. Currently runs on my Google account using Google's Script Dashboard.

### To-Dos

* Finalize the default template used in the script.
* Make the script run on button click and not on calendar change event.
* Far-future: remove the template from the script and use a global template stored in Drive.
