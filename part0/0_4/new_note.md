```mermaid
    sequenceDiagram
      participant browser
      participant server

      browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note (form data)
      activate server
      serve-->>browser: 302 - URL redirect (refresh page)
      browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
      deactivate server
```
