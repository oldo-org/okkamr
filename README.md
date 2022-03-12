# okkanr

- O - Oldo's
- K - Kontakt
- K - Kalender
- A - Aufgaben
- N - Nachricht
- R - "Rasierer" / raiser / racer / runboxer / rrr

Focus on client side

- All server-side storage is done into email folders (initially using
  IMAP), simply by using a folder name convention:
  - Contacts (addressbook)
  - Events (calendar)
  - Tasks (action)
  - etc (later)

- Each entity is represented by a plain-text email 
- Structure conventions for subject and body
- On startup, load contents into in-memory database
- Persist = Sync the content back to mail server

- Relational schema of contacts, events, messages, tasks
- Java process with in-memory database holds items (eg. h2 or hsqldb)
- cruddyb is used for CRUD web interface
- cruddyb interacts with the in-mem database

=> No server setup other than initial IMAP server setup (sec/auth)
=> UI for modern and fast navigation of messages, people, etc

Open questions : 
- How to layer user-friendly in-page interactions onto a server-centric CRUD UI ?
