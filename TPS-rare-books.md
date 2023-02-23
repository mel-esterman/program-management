# Rare Books Prompt
### Product Requirements
- 

### Technical Requirements
- 

### Questions
- How many locations?
- Do we care about how many times a person has taken a book?
- Do we have a damage scale?


```mermaid
sequenceDiagram
participant Image Scanner
participant Library App
participant Non-rare Book
participant Rare Book
participant Image Storage
participant Raw Photo Storage
participant Photo Instance


Image Scanner->>Library App: Scanner pushes book data to Library App
Library App->>Rare Book: Checks if the book is rare or not
Rare Book->>Image Storage: Uploads images
Library App->>Non-rare Book: Checks if the book is rare or not
```
