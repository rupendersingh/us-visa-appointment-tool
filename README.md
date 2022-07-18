## US Visa Appointment Tool

This tool automated the task of booking US visa appointments from Canada on this website: [https://ais.usvisa-info.com/en-ca/niv]().

### Running this tool

*Note: You need to have an account on the website and should have booked an appointment before running the tool.*

1. Install [Node.js](https://nodejs.org/en/).
2. Clone and cd into the repo.
3. Run `npm ci` in a terminal window.
4. Copy config.example.js to a new file called config.js and replace your username, password and lower limit date (the date after which you want to book the appointment).
5. Run `node ./index.js`.

The tool will run periodically and book the appointment for you. You will get an email from the official website when the new appointment is booked.

### Debugging

- Search for `headless: true` in index.js and change it to `headless: false` to see what's happening in the browser window. This can help you figure out what's going wrong if the tool isn't working.
- The official website occasionally rate-limits your account if you check for appointments too frequently. This can happen with the tool as well (since it is just a script acting on your behalf). If this happens, the tool will output "No appointments error". This is totally normal and usually lasts for 4-5 hours, after which the tool should start working as usual.

### Reporting an issue

Feel free to create an issue on the repo with a copy of the logs in the terminal window where you ran the tool. 
