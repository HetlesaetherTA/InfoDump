## InfoDump version: Planned future project

InfoDump is a simple solution to a simple problem. 

I often have to move files from one computer to another, there are many solutions for this,
but none are as fast as I want it to be. 

The goal is to minimize the amount of keystrokes needed to send and collect data from a centralized bucket.
Support planed for CLI and Android initially. 

### Implementation plan 

The server and client will be written in Go using request/receive pattern. 
Client will not use and CGO libraries. Should compile cleanly using `GOOS=android GOARCH=arm64`

The android app will be written in Flutter, OS and persistence should be handled by dart. 
It simply a wrapper for the CLI client which is included as a module. 

### MVP

- Server can receive, send, store and delete text data
- Client can interact with server to do the operations above
- App should be dead simple supporting the features above + copy to clipboard

### Expansion ideas 

- Filtering, sorting and grouping of data
- User access (for different users on the same network)
- Embeddable web version
- Minimal Linux GUI (vim based keybinds)
