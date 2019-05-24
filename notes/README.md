# Notes Service
This directory contain the code for the Notes Service, which deals with the storage of the notes.  
This is the service that maintains a stream with the Client App, to stream changes to the notes back and forth.  
This service also creates events published to the central event broker on data changes for other services to catch if interested.  
# Schema of the database
Top level collection:
- User document (1 document for each user)
    - UserID (Basically user email)
    - Note Collection (Each note will be a Note Document)
        - Note Document
            - NoteID
            - Note type
            - Note title
            - Note text
            - Last cursor position? (So that user can continue from where they last left off)