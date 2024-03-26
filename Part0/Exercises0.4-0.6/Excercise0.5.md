# Exercise 0.5

```mermaid

sequenceDiagram

 Note left of Browser: User visits: https://studies.cs.helsinki.fi/exampleapp/spa
  Browser ->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa

 
  Server ->> Browser: HTML code
  Note left of Browser: Browser sends HTTP GET request for CSS and JS data
  Browser ->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
  Server ->> Browser: main.css
  Browser ->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa.js
  Server ->> Browser: spa.js
  Note left of Browser: Browser executes JS code which sends HTTP GET request for JSON
  Browser ->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server ->> Browser: data.json including: [{ content: "Basteman was here", date 2024-03-26]}...]
  Note left of Browser: Executes event handler callback function that renders the notes


