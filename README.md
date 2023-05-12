# TimeZones-Clock

A simple clock written in HTML, CSS and JavaScript.

This code is an HTML document that presents a world clock and allows users to change the displayed time zone. Let's break it down:

The code follows the typical structure of an HTML document, including the declaration (<!DOCTYPE html>) and the opening and closing <html> tags.

Inside the <head> section, there's a <title> tag that sets the web page's title as "World Clock".

The <style> section contains CSS code defining the appearance of various elements on the web page. It specifies properties like background color, font size, text alignment, padding, borders, border-radius, box shadow, and more.

Within the <body> section, there are three main elements:

The <div> element with the id="clock" attribute is where the current time will be displayed.

The <form> element with the id="timezone-form" attribute contains a dropdown <select> element (id="timezone-select") with a default option to choose a time zone. It also includes a <button> element (id="timezone-button") for modifying the time zone.

The <script> section contains JavaScript code that interacts with the HTML elements to populate the time zone dropdown, display the current time based on the selected time zone, and handle time zone change events.

The JavaScript code starts by selecting the clock element and the time zone select element using their respective id attributes.

The populateTimezones() function utilizes the Moment.js library (loaded from external sources) to retrieve a list of time zone names. It iterates through the list, dynamically creating <option> elements for each time zone. Each option is assigned the corresponding time zone name as its value and text content. These options are appended to the time zone select element.

The displayTime() function retrieves the selected time zone from the time zone select element. If a time zone is chosen, it uses Moment.js to fetch the current time in that time zone (formatted as "HH:mm:ss") and updates the clock element's text content accordingly.

The changeTimezone() function is triggered when the time zone button is clicked. It simply calls the displayTime() function to update the displayed time based on the newly selected time zone.

The setInterval(displayTime, 1000) statement repeatedly invokes the displayTime() function every second (1000 milliseconds) to continuously update the displayed time.

Finally, an event listener is added to the time zone button, so that when it's clicked, the changeTimezone() function is executed.

At the end of the code, the populateTimezones() function is called to populate the time zone options when the page loads.

In essence, this code generates a web page featuring a world clock that automatically refreshes the displayed time every second, based on the selected time zone. Users can choose a time zone from a dropdown menu, and the clock will adjust accordingly.
