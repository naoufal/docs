# Network Users Index

Shows active developers within the network.

## Path

`GET /networks/{ID}/users.{FORMAT}`

## Auth

- authentication
- authorization

## Arguments

- `{ID}`: The ID of the network. This resource is authorized by the API key and will be provided when an API
key is requested

## Options

*None*

## Example

Request:

```
curl https://app.crew.co/api/networks/40/users.json \
   -u 12345:
```

Response:

```
[
  {
    "first_name": "Finn",
    "last_name": "Human",
    "email": "finn@ooo.com",
    "company": null,
    "avatar_url": "http://i.cdn.turner.com/toon/tools/img/social/social30/characters/finn.png",
    "bio": "Finn is a teenage human. He currently lives in a tree in the land of Ooo with his dog, Jake, and robot, BMO.",
    "description": "Finn is a defender of good and righteous things. He also designs things.",
    "hourly_rate": 100,
    "rank": "A",
    "location": "Tree, Ooo",
    "works": [
      {
        "name": "Logo: Pig",
        "description": "After flooping his first pig Finn rebranded The Pig as a master character of Card Wars.",
        "url": "http://example.com",
        "tags": ["design", "logo", "CW"]
      }
    ]
  },
  {
    "first_name": "BMO",
    "last_name": null,
    "email": "bmo@ooo.com",
    "company": "Mo Corp.",
    "avatar_url": "http://i.cdn.turner.com/v5cache/CARTOON/site/Images/i47/at_174x252_beemo.png",
    "bio": "BMO is a video game console, portable electrical outlet, music player, roommate, camera... etc.",
    "description": "BMO is really good at programming video games.",
    "hourly_rate": 180,
    "rank": "B",
    "location": "Tree, Ooo",
    "works": [
      {
        "name": "Adventure Master",
        "description": "A video game for the adventure enthusiast!",
        "url": "http://example.com",
        "tags": ["game", "atari", "adventure"]
      },
      {
        "name": "Pro Football 1861",
        "description": "Kick that ball, tackle those foes! A football game for the whole family.",
        "url": "http://example.com",
        "tags": ["game", "atari", "sports"]
      }
    ]
  }
]
```
