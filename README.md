# BoardGameOlympics
This application is for both admins and players at the Board Game Olympics. 

# Admin
## Create Event

###### Add Category
Add a category and a list of games

###### Signup Participant
Add a participant to the current event

###### Register Participant
lookup an existing participant and register them at the doot

```mermaid
erDiagram
Event }|..|{ Event-Participants : has
Event-Participants }|..|{ Participants : links
Event ||--o{ Categories : has
Categories ||--o{ Category-Games : links
Category-Games ||--|{ Games : links
Event ||--|{ Rounds : has
Rounds ||--|{ Categories : "has a"
Category-Games ||--|{ Event-Participants : links
Category-Game-Players ||--|{ Category-Games : "players for round"
Category-Game-Players ||--|{ Event-Participants : links

```
