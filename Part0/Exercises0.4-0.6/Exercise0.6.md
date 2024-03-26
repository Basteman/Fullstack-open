# Exercise 0.4
```mermaid
sequenceDiagram

Note left of Browser: User submits note "Basteman was here"
Note left of Browser: POST request includes both the content of the note and the timestamp
Browser ->>Server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
Server ->>Browser: Status code 201 created  
Note left of Browser: Browser stays on same page and sends no further HTTP requests
Note left of Browser: Executes event handler callback function that renders the notes