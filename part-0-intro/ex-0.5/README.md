```mermaid
sequenceDiagram
    participant u as user/browser
    participant s as server

    u->>s: GET https://studies.cs.helsinki.fi/exampleapp/spa
    s->>u: HTML document

    u->>s: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    s->>u: CSS file

    u->>s: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    s->>u: JS file

    note right of u: Executes JavaScript code that fetches JSON data from the server

    u->>s: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    s->>u: Data file containing JSON data

    note right of u: Executes the callback function that renders all the notes on the webpage
```