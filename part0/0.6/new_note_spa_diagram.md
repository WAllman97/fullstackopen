# 0.6: New note in Single Page App diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a new note and clicks Save

    Note right of browser: Browser prevents the default form submit

    Note right of browser: Browser creates a new note object with content and date

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: Browser adds the new note to the notes list

    Note right of browser: Browser re-renders the notes on the page without reloading
```
