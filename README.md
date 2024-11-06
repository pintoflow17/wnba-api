# UNOFFICIAL WNBA API DOCUMENTATION
 
The **WNBA API** provides basketball enthusiasts with up-to-date access to comprehensive data on WNBA games, players, and team statistics. This API offers endpoints covering a wide range of information, including scores, game schedules, player and team stats, standings, and the latest news—ideal for fans and developers creating sports applications, tracking performance, or staying informed on league activities.

With organized access to game stats, player profiles, team rankings, and more, the **WNBA API** allows for seamless data retrieval. The API’s structured JSON responses ensure straightforward integration, making it an excellent resource for real-time data applications and automated updates.

# Authentication
The URL you need to use is the following: `https://wnba-api.p.rapidapi.com/`
The API requires the headers listed below:

 - **`x-rapidapi-host`**: `wnba-api.p.rapidapi.com`
 - **`x-rapidapi-key`**: `YOUR_API_KEY`

Make sure to replace `YOUR_API_KEY` with your API key. You can register one [here](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/wnba-api/pricing).
Some frameworks automatically add extra headers, you have to make sure to remove them in order to get a response from the API.

# Endpoints
The API is configured to accept only **GET** requests. Below are the available endpoints with their descriptions and required parameters.


#### 1. **`GET /wnbaplay`**
-   **Description**: Fetches the play-by-play data for a specified WNBA game.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `gameId`  | string   | `-` | The unique identifier for the game.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbaplay?gameId=401244185', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "teams": [
    {
      "uid": "s:40~l:59~t:14",
      "homeAway": "home",
      "score": "92",
      "winner": true,
      "record": [
        {
          "summary": "18-4",
          "displayValue": "18-4",
          "type": "total"
        },
        {
          "summary": "10-1",
          "displayValue": "10-1",
          "type": "home"
        }
      ],
      "possession": false,
      "id": "14",
      "team": {
        "uid": "s:40~l:59~t:14",
        "alternateColor": "fee11a",
        "color": "2c5235",
        "displayName": "Seattle Storm",
        "name": "Storm",
        "location": "Seattle",
        "links": [
          {
            "rel": [
              "clubhouse",
              "desktop",
              "team"
            ],
            "href": "https://www.espn.com/wnba/team/_/name/sea/seattle-storm",
            "text": "Clubhouse"
          }
        ],
        "id": "14",
        "abbreviation": "SEA",
        "logos": [
          {
            "lastUpdated": "2023-05-10T21:43Z",
            "width": 500,
            "alt": "",
            "rel": [
              "full",
              "default"
            ],
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png",
            "height": 500
          },
          {
            "lastUpdated": "2023-05-10T21:45Z",
            "width": 500,
            "alt": "",
            "rel": [
              "full",
              "dark"
            ],
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/sea.png",
            "height": 500
          },
          {
            "lastUpdated": "2021-03-08T15:24Z",
            "width": 500,
            "alt": "",
            "rel": [
              "full",
              "scoreboard"
            ],
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500/scoreboard/sea.png",
            "height": 500
          },
          "..."
        ]
      },
      "linescores": [
        {
          "displayValue": "23"
        },
        {
          "displayValue": "20"
        },
        {
          "displayValue": "32"
        },
        "..."
      ],
      "order": 0
    },
    {
      "uid": "s:40~l:59~t:17",
      "homeAway": "away",
      "score": "59",
      "winner": false,
      "record": [
        {
          "summary": "18-4",
          "displayValue": "18-4",
          "type": "total"
        },
        {
          "summary": "9-2",
          "displayValue": "9-2",
          "type": "road"
        }
      ],
      "possession": false,
      "id": "17",
      "team": {
        "uid": "s:40~l:59~t:17",
        "alternateColor": "000000",
        "color": "a7a8aa",
        "displayName": "Las Vegas Aces",
        "name": "Aces",
        "location": "Las Vegas",
        "links": [
          {
            "rel": [
              "clubhouse",
              "desktop",
              "team"
            ],
            "href": "https://www.espn.com/wnba/team/_/name/lv/las-vegas-aces",
            "text": "Clubhouse"
          }
        ],
        "id": "17",
        "abbreviation": "LV",
        "logos": [
          {
            "lastUpdated": "2024-05-01T20:55Z",
            "width": 500,
            "alt": "",
            "rel": [
              "full",
              "default"
            ],
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500/lv.png",
            "height": 500
          },
          {
            "lastUpdated": "2024-05-01T20:55Z",
            "width": 500,
            "alt": "",
            "rel": [
              "full",
              "dark"
            ],
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/lv.png",
            "height": 500
          }
        ]
      },
      "linescores": [
        {
          "displayValue": "21"
        },
        {
          "displayValue": "13"
        },
        {
          "displayValue": "14"
        },
        "..."
      ],
      "order": 1
    }
  ],
  }
}
```



#### 2. **`GET /wnbabox`**
-   **Description**: Fetches the box score data for a specified WNBA game.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `gameId`  | string   | `-` | The unique identifier for the game.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbabox?gameId=401244185', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "teams": [
    {
      "homeAway": "away",
      "displayOrder": 1,
      "team": {
        "shortDisplayName": "Aces",
        "uid": "s:40~l:59~t:17",
        "alternateColor": "000000",
        "color": "a7a8aa",
        "displayName": "Las Vegas Aces",
        "name": "Aces",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/lv.png",
        "location": "Las Vegas",
        "id": "17",
        "abbreviation": "LV",
        "slug": "las-vegas-aces"
      },
      "statistics": [
        {
          "displayValue": "22-64",
          "name": "fieldGoalsMade-fieldGoalsAttempted",
          "label": "FG"
        },
        {
          "displayValue": "34.4",
          "name": "fieldGoalPct",
          "label": "Field Goal %",
          "abbreviation": "FG%"
        },
        {
          "displayValue": "2-5",
          "name": "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
          "label": "3PT"
        },
        "..."
      ]
    },
    {
      "homeAway": "home",
      "displayOrder": 2,
      "team": {
        "shortDisplayName": "Storm",
        "uid": "s:40~l:59~t:14",
        "alternateColor": "fee11a",
        "color": "2c5235",
        "displayName": "Seattle Storm",
        "name": "Storm",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png",
        "location": "Seattle",
        "id": "14",
        "abbreviation": "SEA",
        "slug": "seattle-storm"
      },
      "statistics": [
        {
          "displayValue": "38-80",
          "name": "fieldGoalsMade-fieldGoalsAttempted",
          "label": "FG"
        },
        {
          "displayValue": "47.5",
          "name": "fieldGoalPct",
          "label": "Field Goal %",
          "abbreviation": "FG%"
        },
        {
          "displayValue": "7-26",
          "name": "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
          "label": "3PT"
        },
        "..."
      ]
    }
  ],
  "players": [
    {
      "displayOrder": 1,
      "team": {
        "shortDisplayName": "Aces",
        "uid": "s:40~l:59~t:17",
        "alternateColor": "000000",
        "color": "a7a8aa",
        "displayName": "Las Vegas Aces",
        "name": "Aces",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/lv.png",
        "location": "Las Vegas",
        "id": "17",
        "abbreviation": "LV",
        "slug": "las-vegas-aces"
      },
      "statistics": [
        {
          "names": [
            "MIN",
            "FG",
            "3PT",
            "..."
          ],
          "keys": [
            "minutes",
            "fieldGoalsMade-fieldGoalsAttempted",
            "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
            "..."
          ],
          "athletes": [
            {
              "reason": "COACH'S DECISION",
              "starter": true,
              "athlete": {
                "uid": "s:40~l:59~a:872",
                "displayName": "Angel McCoughtry",
                "headshot": {
                  "alt": "Angel McCoughtry",
                  "href": "https://a.espncdn.com/i/headshots/wnba/players/full/872.png"
                },
                "guid": "6d80f287-6d06-b6c4-fda2-ed198b94434c",
                "links": [
                  {
                    "rel": [
                      "playercard",
                      "desktop",
                      "athlete"
                    ],
                    "href": "https://www.espn.com/wnba/player/_/id/872/angel-mccoughtry",
                    "text": "Player Card"
                  }
                ],
                "id": "872",
                "position": {
                  "displayName": "Forward",
                  "name": "Forward",
                  "abbreviation": "F"
                },
                "shortName": "A. McCoughtry"
              },
              "ejected": false,
              "stats": [
                "20",
                "2-7",
                "1-1",
                "..."
              ],
              "didNotPlay": false,
              "active": false
            },
            {
              "reason": "COACH'S DECISION",
              "starter": true,
              "athlete": {
                "uid": "s:40~l:59~a:982",
                "displayName": "Carolyn Swords",
                "guid": "13b22c0e-14ce-9ce4-67f3-49ba2e059c76",
                "links": [
                  {
                    "rel": [
                      "playercard",
                      "desktop",
                      "athlete"
                    ],
                    "href": "https://www.espn.com/wnba/player/_/id/982/carolyn-swords",
                    "text": "Player Card"
                  }
                ],
                "id": "982",
                "position": {
                  "displayName": "Center",
                  "name": "Center",
                  "abbreviation": "C"
                },
                "shortName": "C. Swords"
              },
              "ejected": false,
              "stats": [
                "25",
                "3-5",
                "0-0",
                "..."
              ],
              "didNotPlay": false,
              "active": false
            },
            {
              "reason": "COACH'S DECISION",
              "starter": true,
              "athlete": {
                "uid": "s:40~l:59~a:3149391",
                "displayName": "A'ja Wilson",
                "headshot": {
                  "alt": "A'ja Wilson",
                  "href": "https://a.espncdn.com/i/headshots/wnba/players/full/3149391.png"
                },
                "guid": "9d049a87-30bf-a718-0206-b47ef02f57df",
                "links": [
                  {
                    "rel": [
                      "playercard",
                      "desktop",
                      "athlete"
                    ],
                    "href": "https://www.espn.com/wnba/player/_/id/3149391/aja-wilson",
                    "text": "Player Card"
                  }
                ],
                "id": "3149391",
                "position": {
                  "displayName": "Center",
                  "name": "Center",
                  "abbreviation": "C"
                },
                "shortName": "A. Wilson"
              },
              "ejected": false,
              "stats": [
                "32",
                "7-15",
                "0-0",
                "..."
              ],
              "didNotPlay": false,
              "active": false
            },
            "..."
          ],
          "totals": [
            "",
            "22-64",
            "2-5",
            "..."
          ],
          "descriptions": [
            "Minutes",
            "Field Goals Made/Attempted",
            "3-Point Field Goals Made/Attempted",
            "..."
          ],
          "labels": [
            "MIN",
            "FG",
            "3PT",
            "..."
          ]
        }
      ]
    },
    {
      "displayOrder": 2,
      "team": {
        "shortDisplayName": "Storm",
        "uid": "s:40~l:59~t:14",
        "alternateColor": "fee11a",
        "color": "2c5235",
        "displayName": "Seattle Storm",
        "name": "Storm",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png",
        "location": "Seattle",
        "id": "14",
        "abbreviation": "SEA",
        "slug": "seattle-storm"
      },
      "statistics": [
        {
          "names": [
            "MIN",
            "FG",
            "3PT",
            "..."
          ],
          "keys": [
            "minutes",
            "fieldGoalsMade-fieldGoalsAttempted",
            "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
            "..."
          ],
          "athletes": [
            {
              "reason": "COACH'S DECISION",
              "starter": true,
              "athlete": {
                "uid": "s:40~l:59~a:924",
                "displayName": "Alysha Clark",
                "headshot": {
                  "alt": "Alysha Clark",
                  "href": "https://a.espncdn.com/i/headshots/wnba/players/full/924.png"
                },
                "guid": "09609790-79bb-81d4-522b-7a036e404c50",
                "links": [
                  {
                    "rel": [
                      "playercard",
                      "desktop",
                      "athlete"
                    ],
                    "href": "https://www.espn.com/wnba/player/_/id/924/alysha-clark",
                    "text": "Player Card"
                  }
                ],
                "id": "924",
                "position": {
                  "displayName": "Forward",
                  "name": "Forward",
                  "abbreviation": "F"
                },
                "shortName": "A. Clark"
              },
              "ejected": false,
              "stats": [
                "30",
                "3-8",
                "2-4",
                "..."
              ],
              "didNotPlay": false,
              "active": false
            },
            {
              "reason": "COACH'S DECISION",
              "starter": true,
              "athlete": {
                "uid": "s:40~l:59~a:2529130",
                "displayName": "Natasha Howard",
                "headshot": {
                  "alt": "Natasha Howard",
                  "href": "https://a.espncdn.com/i/headshots/wnba/players/full/2529130.png"
                },
                "guid": "2e32f80f-8560-a62e-8654-d21a12d1ed09",
                "links": [
                  {
                    "rel": [
                      "playercard",
                      "desktop",
                      "athlete"
                    ],
                    "href": "https://www.espn.com/wnba/player/_/id/2529130/natasha-howard",
                    "text": "Player Card"
                  }
                ],
                "id": "2529130",
                "position": {
                  "displayName": "Forward",
                  "name": "Forward",
                  "abbreviation": "F"
                },
                "shortName": "N. Howard"
              },
              "ejected": false,
              "stats": [
                "17",
                "2-4",
                "0-0",
                "..."
              ],
              "didNotPlay": false,
              "active": false
            },
            {
              "reason": "COACH'S DECISION",
              "starter": true,
              "athlete": {
                "uid": "s:40~l:59~a:2998928",
                "displayName": "Breanna Stewart",
                "headshot": {
                  "alt": "Breanna Stewart",
                  "href": "https://a.espncdn.com/i/headshots/wnba/players/full/2998928.png"
                },
                "guid": "4d83d500-2f40-c89e-4f85-62927c5abbeb",
                "links": [
                  {
                    "rel": [
                      "playercard",
                      "desktop",
                      "athlete"
                    ],
                    "href": "https://www.espn.com/wnba/player/_/id/2998928/breanna-stewart",
                    "text": "Player Card"
                  }
                ],
                "id": "2998928",
                "position": {
                  "displayName": "Forward",
                  "name": "Forward",
                  "abbreviation": "F"
                },
                "shortName": "B. Stewart"
              },
              "ejected": false,
              "stats": [
                "25",
                "10-14",
                "3-4",
                "..."
              ],
              "didNotPlay": false,
              "active": false
            },
            "..."
          ],
          "totals": [
            "",
            "38-80",
            "7-26",
            "..."
          ],
          "descriptions": [
            "Minutes",
            "Field Goals Made/Attempted",
            "3-Point Field Goals Made/Attempted",
            "..."
          ],
          "labels": [
            "MIN",
            "FG",
            "3PT",
            "..."
          ]
        }
      ]
    }
  ],
  "..."
}
```


#### 3. **`GET /wnbasummary`**
-   **Description**: Fetches the summary data for a specified WNBA game.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `gameId`  | string   | `-` | The unique identifier for the game.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbasummary?gameId=401244185', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "boxScore": {
    "teams": [
      {
        "team": {
          "id": "17",
          "uid": "s:40~l:59~t:17",
          "slug": "las-vegas-aces",
          "location": "Las Vegas",
          "name": "Aces",
          "abbreviation": "LV",
          "displayName": "Las Vegas Aces",
          "shortDisplayName": "Aces",
          "color": "a7a8aa",
          "alternateColor": "000000",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/lv.png"
        },
        "statistics": [
          {
            "name": "fieldGoalsMade-fieldGoalsAttempted",
            "displayValue": "22-64",
            "label": "FG"
          },
          {
            "name": "fieldGoalPct",
            "displayValue": "34.4",
            "abbreviation": "FG%",
            "label": "Field Goal %"
          },
          {
            "name": "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
            "displayValue": "2-5",
            "label": "3PT"
          },
          "..."
        ],
        "displayOrder": 1,
        "homeAway": "away"
      },
      {
        "team": {
          "id": "14",
          "uid": "s:40~l:59~t:14",
          "slug": "seattle-storm",
          "location": "Seattle",
          "name": "Storm",
          "abbreviation": "SEA",
          "displayName": "Seattle Storm",
          "shortDisplayName": "Storm",
          "color": "2c5235",
          "alternateColor": "fee11a",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png"
        },
        "statistics": [
          {
            "name": "fieldGoalsMade-fieldGoalsAttempted",
            "displayValue": "38-80",
            "label": "FG"
          },
          {
            "name": "fieldGoalPct",
            "displayValue": "47.5",
            "abbreviation": "FG%",
            "label": "Field Goal %"
          },
          {
            "name": "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
            "displayValue": "7-26",
            "label": "3PT"
          },
          "..."
        ],
        "displayOrder": 2,
        "homeAway": "home"
      }
    ],
    "players": [
      {
        "team": {
          "id": "17",
          "uid": "s:40~l:59~t:17",
          "slug": "las-vegas-aces",
          "location": "Las Vegas",
          "name": "Aces",
          "abbreviation": "LV",
          "displayName": "Las Vegas Aces",
          "shortDisplayName": "Aces",
          "color": "a7a8aa",
          "alternateColor": "000000",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/lv.png"
        },
        "statistics": [
          {
            "names": [
              "MIN",
              "FG",
              "3PT",
              "..."
            ],
            "keys": [
              "minutes",
              "fieldGoalsMade-fieldGoalsAttempted",
              "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
              "..."
            ],
            "labels": [
              "MIN",
              "FG",
              "3PT",
              "..."
            ],
            "descriptions": [
              "Minutes",
              "Field Goals Made/Attempted",
              "3-Point Field Goals Made/Attempted",
              "..."
            ],
            "athletes": [
              {
                "active": false,
                "athlete": {
                  "id": "872",
                  "uid": "s:40~l:59~a:872",
                  "guid": "6d80f287-6d06-b6c4-fda2-ed198b94434c",
                  "displayName": "Angel McCoughtry",
                  "shortName": "A. McCoughtry",
                  "links": [
                    {
                      "rel": [
                        "playercard",
                        "desktop",
                        "athlete"
                      ],
                      "href": "https://www.espn.com/wnba/player/_/id/872/angel-mccoughtry",
                      "text": "Player Card"
                    }
                  ],
                  "headshot": {
                    "href": "https://a.espncdn.com/i/headshots/wnba/players/full/872.png",
                    "alt": "Angel McCoughtry"
                  },
                  "position": {
                    "name": "Forward",
                    "displayName": "Forward",
                    "abbreviation": "F"
                  }
                },
                "starter": true,
                "didNotPlay": false,
                "reason": "COACH'S DECISION",
                "ejected": false,
                "stats": [
                  "20",
                  "2-7",
                  "1-1",
                  "..."
                ]
              },
              {
                "active": false,
                "athlete": {
                  "id": "982",
                  "uid": "s:40~l:59~a:982",
                  "guid": "13b22c0e-14ce-9ce4-67f3-49ba2e059c76",
                  "displayName": "Carolyn Swords",
                  "shortName": "C. Swords",
                  "links": [
                    {
                      "rel": [
                        "playercard",
                        "desktop",
                        "athlete"
                      ],
                      "href": "https://www.espn.com/wnba/player/_/id/982/carolyn-swords",
                      "text": "Player Card"
                    }
                  ],
                  "position": {
                    "name": "Center",
                    "displayName": "Center",
                    "abbreviation": "C"
                  }
                },
                "starter": true,
                "didNotPlay": false,
                "reason": "COACH'S DECISION",
                "ejected": false,
                "stats": [
                  "25",
                  "3-5",
                  "0-0",
                  "..."
                ]
              },
              {
                "active": false,
                "athlete": {
                  "id": "3149391",
                  "uid": "s:40~l:59~a:3149391",
                  "guid": "9d049a87-30bf-a718-0206-b47ef02f57df",
                  "displayName": "A'ja Wilson",
                  "shortName": "A. Wilson",
                  "links": [
                    {
                      "rel": [
                        "playercard",
                        "desktop",
                        "athlete"
                      ],
                      "href": "https://www.espn.com/wnba/player/_/id/3149391/aja-wilson",
                      "text": "Player Card"
                    }
                  ],
                  "headshot": {
                    "href": "https://a.espncdn.com/i/headshots/wnba/players/full/3149391.png",
                    "alt": "A'ja Wilson"
                  },
                  "position": {
                    "name": "Center",
                    "displayName": "Center",
                    "abbreviation": "C"
                  }
                },
                "starter": true,
                "didNotPlay": false,
                "reason": "COACH'S DECISION",
                "ejected": false,
                "stats": [
                  "32",
                  "7-15",
                  "0-0",
                  "..."
                ]
              },
              "..."
            ],
            "totals": [
              "",
              "22-64",
              "2-5",
              "..."
            ]
          }
        ],
        "displayOrder": 1
      },
      {
        "team": {
          "id": "14",
          "uid": "s:40~l:59~t:14",
          "slug": "seattle-storm",
          "location": "Seattle",
          "name": "Storm",
          "abbreviation": "SEA",
          "displayName": "Seattle Storm",
          "shortDisplayName": "Storm",
          "color": "2c5235",
          "alternateColor": "fee11a",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png"
        },
        "statistics": [
          {
            "names": [
              "MIN",
              "FG",
              "3PT",
              "..."
            ],
            "keys": [
              "minutes",
              "fieldGoalsMade-fieldGoalsAttempted",
              "threePointFieldGoalsMade-threePointFieldGoalsAttempted",
              "..."
            ],
            "labels": [
              "MIN",
              "FG",
              "3PT",
              "..."
            ],
            "descriptions": [
              "Minutes",
              "Field Goals Made/Attempted",
              "3-Point Field Goals Made/Attempted",
              "..."
            ],
            "athletes": [
              {
                "active": false,
                "athlete": {
                  "id": "924",
                  "uid": "s:40~l:59~a:924",
                  "guid": "09609790-79bb-81d4-522b-7a036e404c50",
                  "displayName": "Alysha Clark",
                  "shortName": "A. Clark",
                  "links": [
                    {
                      "rel": [
                        "playercard",
                        "desktop",
                        "athlete"
                      ],
                      "href": "https://www.espn.com/wnba/player/_/id/924/alysha-clark",
                      "text": "Player Card"
                    }
                  ],
                  "headshot": {
                    "href": "https://a.espncdn.com/i/headshots/wnba/players/full/924.png",
                    "alt": "Alysha Clark"
                  },
                  "position": {
                    "name": "Forward",
                    "displayName": "Forward",
                    "abbreviation": "F"
                  }
                },
                "starter": true,
                "didNotPlay": false,
                "reason": "COACH'S DECISION",
                "ejected": false,
                "stats": [
                  "30",
                  "3-8",
                  "2-4",
                  "..."
                ]
              },
              {
                "active": false,
                "athlete": {
                  "id": "2529130",
                  "uid": "s:40~l:59~a:2529130",
                  "guid": "2e32f80f-8560-a62e-8654-d21a12d1ed09",
                  "displayName": "Natasha Howard",
                  "shortName": "N. Howard",
                  "links": [
                    {
                      "rel": [
                        "playercard",
                        "desktop",
                        "athlete"
                      ],
                      "href": "https://www.espn.com/wnba/player/_/id/2529130/natasha-howard",
                      "text": "Player Card"
                    }
                  ],
                  "headshot": {
                    "href": "https://a.espncdn.com/i/headshots/wnba/players/full/2529130.png",
                    "alt": "Natasha Howard"
                  },
                  "position": {
                    "name": "Forward",
                    "displayName": "Forward",
                    "abbreviation": "F"
                  }
                },
                "starter": true,
                "didNotPlay": false,
                "reason": "COACH'S DECISION",
                "ejected": false,
                "stats": [
                  "17",
                  "2-4",
                  "0-0",
                  "..."
                ]
              },
              {
                "active": false,
                "athlete": {
                  "id": "2998928",
                  "uid": "s:40~l:59~a:2998928",
                  "guid": "4d83d500-2f40-c89e-4f85-62927c5abbeb",
                  "displayName": "Breanna Stewart",
                  "shortName": "B. Stewart",
                  "links": [
                    {
                      "rel": [
                        "playercard",
                        "desktop",
                        "athlete"
                      ],
                      "href": "https://www.espn.com/wnba/player/_/id/2998928/breanna-stewart",
                      "text": "Player Card"
                    }
                  ],
                  "headshot": {
                    "href": "https://a.espncdn.com/i/headshots/wnba/players/full/2998928.png",
                    "alt": "Breanna Stewart"
                  },
                  "position": {
                    "name": "Forward",
                    "displayName": "Forward",
                    "abbreviation": "F"
                  }
                },
                "starter": true,
                "didNotPlay": false,
                "reason": "COACH'S DECISION",
                "ejected": false,
                "stats": [
                  "25",
                  "10-14",
                  "3-4",
                  "..."
                ]
              },
              "..."
            ],
            "totals": [
              "",
              "38-80",
              "7-26",
              "..."
            ]
          }
        ],
        "displayOrder": 2
      }
    ]
  },
  "gameInfo": {
    "venue": {
      "id": "7097",
      "fullName": "IMG Academy",
      "address": {
        "city": "Bradenton",
        "state": "FL"
      },
      "grass": false,
      "images": []
    },
    "attendance": 0,
    "officials": [
      {
        "fullName": "Michael Price",
        "displayName": "Michael Price",
        "position": {
          "name": "Referee",
          "displayName": "Referee",
          "id": "40"
        },
        "order": 1
      },
      {
        "fullName": "Che Flores",
        "displayName": "Che Flores",
        "position": {
          "name": "Referee",
          "displayName": "Referee",
          "id": "40"
        },
        "order": 2
      },
      {
        "fullName": "Eric Brewton",
        "displayName": "Eric Brewton",
        "position": {
          "name": "Referee",
          "displayName": "Referee",
          "id": "40"
        },
        "order": 3
      },
      "..."
    ]
  },
  "..."
  }
}
```



#### 4. **`GET /wnbaschedule`**
-   **Description**: Fetches the schedule data for a specified date.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `year`  | string   | `-` | The year in `YYYY` format.   | Yes       |
| `month`  | string   | `-` | The month in `MM` format.   | No       |
| `day`  | string   | `-` | The day in `DD` format.   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbaschedule?year=2022&month=05&day=05', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "20220504": [],
  "20220505": [],
  "20220506": [
    {
      "id": "401391650",
      "competitors": [
        {
          "id": "16",
          "abbrev": "WSH",
          "displayName": "Washington Mystics",
          "shortDisplayName": "Mystics",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
          "teamColor": "e03a3e",
          "altColor": "002b5c",
          "uid": "s:40~l:59~t:16",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Washington",
          "links": "/wnba/team/_/name/wsh/washington-mystics",
          "name": "Washington Mystics",
          "shortName": "Mystics",
          "isHome": true,
          "score": 84,
          "winner": true,
          "leader": {
            "shortName": "E. Delle Donne",
            "name": "Elena Delle Donne",
            "href": "https://www.espn.com/wnba/player/_/id/2491877/elena-delle-donne",
            "uid": "",
            "displayValue": "21"
          }
        },
        "..."
      ],
      "date": "2022-05-06T23:00Z",
      "tbd": false,
      "completed": true,
      "broadcasts": [
        {
          "name": "Facebook",
          "type": "4",
          "market": "National"
        }
      ],
      "link": "/wnba/game/_/gameId/401391650/fever-mystics",
      "teams": [
        {
          "id": "16",
          "abbrev": "WSH",
          "displayName": "Washington Mystics",
          "shortDisplayName": "Mystics",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
          "teamColor": "e03a3e",
          "altColor": "002b5c",
          "uid": "s:40~l:59~t:16",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Washington",
          "links": "/wnba/team/_/name/wsh/washington-mystics",
          "name": "Washington Mystics",
          "shortName": "Mystics",
          "isHome": true,
          "score": 84,
          "winner": true,
          "leader": {
            "shortName": "E. Delle Donne",
            "name": "Elena Delle Donne",
            "href": "https://www.espn.com/wnba/player/_/id/2491877/elena-delle-donne",
            "uid": "",
            "displayValue": "21"
          }
        },
        "..."
      ],
      "isTie": false,
      "format": {
        "regulation": {
          "periods": 4
        }
      },
      "tickets": {},
      "headerPostfix": "",
      "venue": {
        "id": "5946",
        "fullName": "Entertainment & Sports Arena",
        "address": {
          "city": "Washington",
          "state": "DC"
        },
        "indoor": true
      },
      "status": {
        "id": "3",
        "state": "post",
        "detail": "Final"
      },
      "timeValid": true
    },
    "..."
  ],
  "20220507": [
    {
      "id": "401391654",
      "competitors": [
        {
          "id": "9",
          "abbrev": "NY",
          "displayName": "New York Liberty",
          "shortDisplayName": "Liberty",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/ny.png",
          "teamColor": "86cebc",
          "altColor": "000000",
          "uid": "s:40~l:59~t:9",
          "recordSummary": "",
          "standingSummary": "",
          "location": "New York",
          "links": "/wnba/team/_/name/ny/new-york-liberty",
          "name": "New York Liberty",
          "shortName": "Liberty",
          "isHome": true,
          "score": 81,
          "winner": true,
          "leader": {
            "shortName": "S. Ionescu",
            "name": "Sabrina Ionescu",
            "href": "https://www.espn.com/wnba/player/_/id/4066533/sabrina-ionescu",
            "uid": "",
            "displayValue": "25"
          }
        },
        {
          "id": "18",
          "abbrev": "CONN",
          "displayName": "Connecticut Sun",
          "shortDisplayName": "Sun",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/conn.png",
          "teamColor": "f05023",
          "altColor": "0a2240",
          "uid": "s:40~l:59~t:18",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Connecticut",
          "links": "/wnba/team/_/name/conn/connecticut-sun",
          "name": "Connecticut Sun",
          "shortName": "Sun",
          "isHome": false,
          "score": 79,
          "leader": {
            "shortName": "A. Thomas",
            "name": "Alyssa Thomas",
            "href": "https://www.espn.com/wnba/player/_/id/2529140/alyssa-thomas",
            "uid": "",
            "displayValue": "25"
          }
        }
      ],
      "date": "2022-05-07T22:00Z",
      "tbd": false,
      "completed": true,
      "broadcasts": [
        {
          "name": "ESPN",
          "type": "1",
          "market": "National",
          "link": "/watch/player/_/eventCalendarId/401391654",
          "logo": "https://a.espncdn.com/redesign/assets/img/logos/networks/espn-red@2x.png"
        }
      ],
      "link": "/wnba/game/_/gameId/401391654/sun-liberty",
      "teams": [
        {
          "id": "9",
          "abbrev": "NY",
          "displayName": "New York Liberty",
          "shortDisplayName": "Liberty",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/ny.png",
          "teamColor": "86cebc",
          "altColor": "000000",
          "uid": "s:40~l:59~t:9",
          "recordSummary": "",
          "standingSummary": "",
          "location": "New York",
          "links": "/wnba/team/_/name/ny/new-york-liberty",
          "name": "New York Liberty",
          "shortName": "Liberty",
          "isHome": true,
          "score": 81,
          "winner": true,
          "leader": {
            "shortName": "S. Ionescu",
            "name": "Sabrina Ionescu",
            "href": "https://www.espn.com/wnba/player/_/id/4066533/sabrina-ionescu",
            "uid": "",
            "displayValue": "25"
          }
        },
        {
          "id": "18",
          "abbrev": "CONN",
          "displayName": "Connecticut Sun",
          "shortDisplayName": "Sun",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/conn.png",
          "teamColor": "f05023",
          "altColor": "0a2240",
          "uid": "s:40~l:59~t:18",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Connecticut",
          "links": "/wnba/team/_/name/conn/connecticut-sun",
          "name": "Connecticut Sun",
          "shortName": "Sun",
          "isHome": false,
          "score": 79,
          "leader": {
            "shortName": "A. Thomas",
            "name": "Alyssa Thomas",
            "href": "https://www.espn.com/wnba/player/_/id/2529140/alyssa-thomas",
            "uid": "",
            "displayValue": "25"
          }
        }
      ],
      "isTie": false,
      "format": {
        "regulation": {
          "periods": 4
        }
      },
      "tickets": {},
      "headerPostfix": "",
      "venue": {
        "id": "3559",
        "fullName": "Barclays Center",
        "address": {
          "city": "Brooklyn",
          "state": "NY"
        },
        "indoor": true
      },
      "status": {
        "id": "3",
        "state": "post",
        "detail": "Final"
      },
      "timeValid": true
    },
    {
      "id": "401391655",
      "competitors": [
        {
          "id": "3",
          "abbrev": "DAL",
          "displayName": "Dallas Wings",
          "shortDisplayName": "Wings",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/dal.png",
          "teamColor": "002b5c",
          "altColor": "c4d600",
          "uid": "s:40~l:59~t:3",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Dallas",
          "links": "/wnba/team/_/name/dal/dallas-wings",
          "name": "Dallas Wings",
          "shortName": "Wings",
          "isHome": true,
          "score": 59,
          "leader": {
            "shortName": "M. Mabrey",
            "name": "Marina Mabrey",
            "href": "https://www.espn.com/wnba/player/_/id/3904576/marina-mabrey",
            "uid": "",
            "displayValue": "20"
          }
        },
        {
          "id": "20",
          "abbrev": "ATL",
          "displayName": "Atlanta Dream",
          "shortDisplayName": "Dream",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/atl.png",
          "teamColor": "e31837",
          "altColor": "5091cc",
          "uid": "s:40~l:59~t:20",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Atlanta",
          "links": "/wnba/team/_/name/atl/atlanta-dream",
          "name": "Atlanta Dream",
          "shortName": "Dream",
          "isHome": false,
          "score": 66,
          "winner": true,
          "leader": {
            "shortName": "R. Howard",
            "name": "Rhyne Howard",
            "href": "https://www.espn.com/wnba/player/_/id/4398674/rhyne-howard",
            "uid": "",
            "displayValue": "16"
          }
        }
      ],
      "date": "2022-05-08T00:00Z",
      "tbd": false,
      "completed": true,
      "broadcasts": [
        {
          "name": "CBSSN",
          "type": "1",
          "market": "National"
        }
      ],
      "link": "/wnba/game/_/gameId/401391655/dream-wings",
      "teams": [
        {
          "id": "3",
          "abbrev": "DAL",
          "displayName": "Dallas Wings",
          "shortDisplayName": "Wings",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/dal.png",
          "teamColor": "002b5c",
          "altColor": "c4d600",
          "uid": "s:40~l:59~t:3",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Dallas",
          "links": "/wnba/team/_/name/dal/dallas-wings",
          "name": "Dallas Wings",
          "shortName": "Wings",
          "isHome": true,
          "score": 59,
          "leader": {
            "shortName": "M. Mabrey",
            "name": "Marina Mabrey",
            "href": "https://www.espn.com/wnba/player/_/id/3904576/marina-mabrey",
            "uid": "",
            "displayValue": "20"
          }
        },
        {
          "id": "20",
          "abbrev": "ATL",
          "displayName": "Atlanta Dream",
          "shortDisplayName": "Dream",
          "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/atl.png",
          "teamColor": "e31837",
          "altColor": "5091cc",
          "uid": "s:40~l:59~t:20",
          "recordSummary": "",
          "standingSummary": "",
          "location": "Atlanta",
          "links": "/wnba/team/_/name/atl/atlanta-dream",
          "name": "Atlanta Dream",
          "shortName": "Dream",
          "isHome": false,
          "score": 66,
          "winner": true,
          "leader": {
            "shortName": "R. Howard",
            "name": "Rhyne Howard",
            "href": "https://www.espn.com/wnba/player/_/id/4398674/rhyne-howard",
            "uid": "",
            "displayValue": "16"
          }
        }
      ],
      "isTie": false,
      "format": {
        "regulation": {
          "periods": 4
        }
      },
      "tickets": {},
      "headerPostfix": "",
      "venue": {
        "id": "3416",
        "fullName": "College Park Center",
        "address": {
          "city": "Arlington",
          "state": "TX"
        },
        "indoor": true
      },
      "status": {
        "id": "3",
        "state": "post",
        "detail": "Final"
      },
      "timeValid": true
    }
  ],
  "..."
}
```



#### 5. **`GET /wnbascoreboard`**
-   **Description**: Fetches the scoreboard data for a specified date.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `year`  | string   | `-` | The year in `YYYY` format.   | Yes       |
| `month`  | string   | `-` | The month in `MM` format.   | Yes      |
| `day`  | string   | `-` | The day in `DD` format.   | Yes       |
| `limit`  | string   | `10` |  Maximum number of games to return (default is `100`).   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbascoreboard?year=2022&month=04&day=04&limit=02', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "leagues": [
    {
      "id": "59",
      "uid": "s:40~l:59",
      "name": "Women's National Basketball Association",
      "abbreviation": "WNBA",
      "slug": "wnba",
      "season": {
        "year": 2021,
        "startDate": "2021-05-01T07:00Z",
        "endDate": "2021-10-20T06:59Z",
        "displayName": "2021",
        "type": {
          "id": "2",
          "type": 2,
          "name": "Regular Season",
          "abbreviation": "reg"
        }
      },
      "logos": [
        {
          "href": "https://a.espncdn.com/i/teamlogos/leagues/500/wnba.png",
          "width": 500,
          "height": 500,
          "alt": "",
          "rel": [
            "full",
            "default"
          ],
          "lastUpdated": "2019-05-21T20:08Z"
        },
        {
          "href": "https://a.espncdn.com/i/teamlogos/leagues/500-dark/wnba.png",
          "width": 500,
          "height": 500,
          "alt": "",
          "rel": [
            "full",
            "dark"
          ],
          "lastUpdated": "2019-11-19T15:26Z"
        }
      ],
      "calendarType": "day",
      "calendarIsWhitelist": true,
      "calendarStartDate": "2021-05-01T07:00Z",
      "calendarEndDate": "2021-10-20T06:59Z",
      "calendar": [
        "2021-05-05T07:00Z",
        "2021-05-08T07:00Z",
        "2021-05-09T07:00Z",
        "..."
      ]
    }
  ],
  "events": []
}
```



#### 6. **`GET /wnbastandings`**
-   **Description**: Fetches the standings for WNBA teams.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `year`  | string   | `-` | The year in `YYYY` format.   | Yes       |
| `group`  | string   | `-` | The grouping type (options: `league`, `conference`, `division`).   | No      |


Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbastandings?year=2022', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "uid": "s:40~l:59~g:3",
  "id": "3",
  "name": "Women's National Basketball Assoc.",
  "abbreviation": "WNBA",
  "shortName": "WNBA",
  "standings": {
    "id": "0",
    "name": "overall",
    "displayName": "Overall Standings",
    "links": [
      {
        "language": "en-US",
        "rel": [
          "standings",
          "desktop"
        ],
        "href": "https://www.espn.com/wnba/standings/_/group/3",
        "text": "Table",
        "shortText": "Standings",
        "isExternal": false,
        "isPremium": false
      }
    ],
    "season": 2022,
    "seasonType": 2,
    "seasonDisplayName": "2022",
    "entries": [
      {
        "team": {
          "id": "17",
          "uid": "s:40~l:59~t:17",
          "location": "Las Vegas",
          "name": "Aces",
          "abbreviation": "LV",
          "displayName": "Las Vegas Aces",
          "shortDisplayName": "Aces",
          "isActive": true,
          "logos": [
            {
              "href": "https://a.espncdn.com/i/teamlogos/wnba/500/lv.png",
              "width": 500,
              "height": 500,
              "alt": "",
              "rel": [
                "full",
                "default"
              ],
              "lastUpdated": "2024-05-01T20:55Z"
            }
          ],
          "links": [
            {
              "language": "en-US",
              "rel": [
                "clubhouse",
                "desktop",
                "team"
              ],
              "href": "https://www.espn.com/wnba/team/_/name/lv/las-vegas-aces",
              "text": "Clubhouse",
              "shortText": "Clubhouse",
              "isExternal": false,
              "isPremium": false
            },
            {
              "language": "en-US",
              "rel": [
                "clubhouse",
                "mobile",
                "team"
              ],
              "href": "https://m.espn.com/wnba/clubhouse?teamId=17",
              "text": "Clubhouse",
              "shortText": "Clubhouse",
              "isExternal": false,
              "isPremium": false
            }
          ]
        },
        "stats": [
          {
            "name": "avgPointsAgainst",
            "displayName": "Opponent Points Per Game",
            "shortDisplayName": "OPP PPG",
            "description": "Opponent Points Per Game",
            "abbreviation": "OPP PPG",
            "type": "avgpointsagainst",
            "value": 84.083336,
            "displayValue": "84.1"
          },
          {
            "name": "avgPointsFor",
            "displayName": "Points Per Game",
            "shortDisplayName": "PPG",
            "description": "Points Per Game",
            "abbreviation": "PPG",
            "type": "avgpointsfor",
            "value": 90.44444,
            "displayValue": "90.4"
          },
          {
            "name": "clincher",
            "displayName": "Clincher",
            "shortDisplayName": "CLINCH",
            "description": "Clinched Best League Record and Won Commissioner's Cup",
            "abbreviation": "CLINCH",
            "type": "clincher",
            "value": 6,
            "displayValue": "c*"
          },
          "..."
        ]
      },
      {
        "team": {
          "id": "19",
          "uid": "s:40~l:59~t:19",
          "location": "Chicago",
          "name": "Sky",
          "abbreviation": "CHI",
          "displayName": "Chicago Sky",
          "shortDisplayName": "Sky",
          "isActive": true,
          "logos": [
            {
              "href": "https://a.espncdn.com/i/teamlogos/wnba/500/chi.png",
              "width": 500,
              "height": 500,
              "alt": "",
              "rel": [
                "full",
                "default"
              ],
              "lastUpdated": "2023-05-10T21:43Z"
            }
          ],
          "links": [
            {
              "language": "en-US",
              "rel": [
                "clubhouse",
                "desktop",
                "team"
              ],
              "href": "https://www.espn.com/wnba/team/_/name/chi/chicago-sky",
              "text": "Clubhouse",
              "shortText": "Clubhouse",
              "isExternal": false,
              "isPremium": false
            },
            {
              "language": "en-US",
              "rel": [
                "clubhouse",
                "mobile",
                "team"
              ],
              "href": "https://m.espn.com/wnba/clubhouse?teamId=19",
              "text": "Clubhouse",
              "shortText": "Clubhouse",
              "isExternal": false,
              "isPremium": false
            }
          ]
        },
        "stats": [
          {
            "name": "avgPointsAgainst",
            "displayName": "Opponent Points Per Game",
            "shortDisplayName": "OPP PPG",
            "description": "Opponent Points Per Game",
            "abbreviation": "OPP PPG",
            "type": "avgpointsagainst",
            "value": 81.25,
            "displayValue": "81.3"
          },
          {
            "name": "avgPointsFor",
            "displayName": "Points Per Game",
            "shortDisplayName": "PPG",
            "description": "Points Per Game",
            "abbreviation": "PPG",
            "type": "avgpointsfor",
            "value": 86.25,
            "displayValue": "86.3"
          },
          {
            "name": "clincher",
            "displayName": "Clincher",
            "shortDisplayName": "CLINCH",
            "description": "Clinched Playoff Berth",
            "abbreviation": "CLINCH",
            "type": "clincher",
            "value": 1,
            "displayValue": "x"
          },
          "..."
        ]
      },
      {
        "team": {
          "id": "18",
          "uid": "s:40~l:59~t:18",
          "location": "Connecticut",
          "name": "Sun",
          "abbreviation": "CONN",
          "displayName": "Connecticut Sun",
          "shortDisplayName": "Sun",
          "isActive": true,
          "logos": [
            {
              "href": "https://a.espncdn.com/i/teamlogos/wnba/500/conn.png",
              "width": 500,
              "height": 500,
              "alt": "",
              "rel": [
                "full",
                "default"
              ],
              "lastUpdated": "2023-05-10T21:43Z"
            }
          ],
          "links": [
            {
              "language": "en-US",
              "rel": [
                "clubhouse",
                "desktop",
                "team"
              ],
              "href": "https://www.espn.com/wnba/team/_/name/conn/connecticut-sun",
              "text": "Clubhouse",
              "shortText": "Clubhouse",
              "isExternal": false,
              "isPremium": false
            },
            {
              "language": "en-US",
              "rel": [
                "clubhouse",
                "mobile",
                "team"
              ],
              "href": "https://m.espn.com/wnba/clubhouse?teamId=18",
              "text": "Clubhouse",
              "shortText": "Clubhouse",
              "isExternal": false,
              "isPremium": false
            }
          ]
        },
        "stats": [
          {
            "name": "avgPointsAgainst",
            "displayName": "Opponent Points Per Game",
            "shortDisplayName": "OPP PPG",
            "description": "Opponent Points Per Game",
            "abbreviation": "OPP PPG",
            "type": "avgpointsagainst",
            "value": 77.75,
            "displayValue": "77.8"
          },
          {
            "name": "avgPointsFor",
            "displayName": "Points Per Game",
            "shortDisplayName": "PPG",
            "description": "Points Per Game",
            "abbreviation": "PPG",
            "type": "avgpointsfor",
            "value": 85.77778,
            "displayValue": "85.8"
          },
          {
            "name": "clincher",
            "displayName": "Clincher",
            "shortDisplayName": "CLINCH",
            "description": "Clinched Playoff Berth",
            "abbreviation": "CLINCH",
            "type": "clincher",
            "value": 1,
            "displayValue": "x"
          },
          "..."
        ]
      },
      "..."
    ]
  },
  "children": [],
  "links": [
    {
      "language": "en-US",
      "rel": [
        "standings",
        "desktop"
      ],
      "href": "https://www.espn.com/wnba/standings/_/group/3",
      "text": "Table",
      "shortText": "Standings",
      "isExternal": false,
      "isPremium": false
    }
  ],
  "seasons": [
    {
      "year": 2024,
      "startDate": "2024-04-15T07:00Z",
      "endDate": "2024-10-21T06:59Z",
      "displayName": "2024",
      "types": [
        {
          "id": "1",
          "name": "Preseason",
          "abbreviation": "pre",
          "startDate": "2024-04-15T07:00Z",
          "endDate": "2024-05-14T06:59Z",
          "hasStandings": true
        },
        {
          "id": "2",
          "name": "Regular Season",
          "abbreviation": "reg",
          "startDate": "2024-05-14T07:00Z",
          "endDate": "2024-09-21T06:59Z",
          "hasStandings": true
        },
        {
          "id": "3",
          "name": "Postseason",
          "abbreviation": "post",
          "startDate": "2024-09-21T07:00Z",
          "endDate": "2024-10-21T06:59Z",
          "hasStandings": false
        },
        "..."
      ]
    },
    "..."
  ]
}
```



#### 7. **`GET /wnbateamlist`**
-   **Description**: Fetches a list of all WNBA teams.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `limit`  | string   | `500` |  Maximum number of games to return.   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbateamlist?limit=2', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "sports": [
    {
      "id": "40",
      "uid": "s:40",
      "name": "Basketball",
      "slug": "basketball",
      "leagues": [
        {
          "id": "59",
          "uid": "s:40~l:59",
          "name": "Women's National Basketball Association",
          "abbreviation": "WNBA",
          "shortName": "WNBA",
          "slug": "wnba",
          "teams": [
            {
              "team": {
                "id": "3",
                "uid": "s:40~l:59~t:3",
                "slug": "dallas-wings",
                "abbreviation": "DAL",
                "displayName": "Dallas Wings",
                "shortDisplayName": "Wings",
                "name": "Wings",
                "nickname": "Dallas",
                "location": "Dallas",
                "color": "002b5c",
                "alternateColor": "c4d600",
                "isActive": true,
                "isAllStar": false,
                "logos": [
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500/dal.png",
                    "alt": "",
                    "rel": [
                      "full",
                      "default"
                    ],
                    "width": 500,
                    "height": 500
                  },
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/dal.png",
                    "alt": "",
                    "rel": [
                      "full",
                      "dark"
                    ],
                    "width": 500,
                    "height": 500
                  }
                ],
                "links": [
                  {
                    "language": "en-US",
                    "rel": [
                      "clubhouse",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/_/name/dal/dallas-wings",
                    "text": "Clubhouse",
                    "shortText": "Clubhouse",
                    "isExternal": false,
                    "isPremium": false,
                    "isHidden": false
                  },
                  {
                    "language": "en-US",
                    "rel": [
                      "roster",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/roster/_/name/dal/dallas-wings",
                    "text": "Roster",
                    "shortText": "Roster",
                    "isExternal": false,
                    "isPremium": false,
                    "isHidden": false
                  },
                  {
                    "language": "en-US",
                    "rel": [
                      "stats",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/stats/_/name/dal/dallas-wings",
                    "text": "Statistics",
                    "shortText": "Statistics",
                    "isExternal": false,
                    "isPremium": false,
                    "isHidden": false
                  },
                  "..."
                ]
              }
            },
            {
              "team": {
                "id": "5",
                "uid": "s:40~l:59~t:5",
                "slug": "indiana-fever",
                "abbreviation": "IND",
                "displayName": "Indiana Fever",
                "shortDisplayName": "Fever",
                "name": "Fever",
                "nickname": "Indiana",
                "location": "Indiana",
                "color": "002d62",
                "alternateColor": "e03a3e",
                "isActive": true,
                "isAllStar": false,
                "logos": [
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500/ind.png",
                    "alt": "",
                    "rel": [
                      "full",
                      "default"
                    ],
                    "width": 500,
                    "height": 500
                  },
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/ind.png",
                    "alt": "",
                    "rel": [
                      "full",
                      "dark"
                    ],
                    "width": 500,
                    "height": 500
                  }
                ],
                "links": [
                  {
                    "language": "en-US",
                    "rel": [
                      "clubhouse",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/_/name/ind/indiana-fever",
                    "text": "Clubhouse",
                    "shortText": "Clubhouse",
                    "isExternal": false,
                    "isPremium": false,
                    "isHidden": false
                  },
                  {
                    "language": "en-US",
                    "rel": [
                      "roster",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/roster/_/name/ind/indiana-fever",
                    "text": "Roster",
                    "shortText": "Roster",
                    "isExternal": false,
                    "isPremium": false,
                    "isHidden": false
                  },
                  {
                    "language": "en-US",
                    "rel": [
                      "stats",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/stats/_/name/ind/indiana-fever",
                    "text": "Statistics",
                    "shortText": "Statistics",
                    "isExternal": false,
                    "isPremium": false,
                    "isHidden": false
                  },
                  "..."
                ]
              }
            }
          ],
          "year": 2024,
          "season": {
            "year": 2024,
            "displayName": "2024"
          }
        }
      ]
    }
  ]
}
```



#### 8. **`GET /team/id`**
-   **Description**: Fetches team identification info.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `limit`  | string   | `-` | The maximum number of teams to return   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team/id?limit=2', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
[
  {
    "teamId": "3",
    "displayName": "Dallas Wings",
    "shortDisplayName": "Wings",
    "abbreviation": "DAL",
    "slug": "dallas-wings",
    "link": "https://www.espn.com/wnba/team/_/name/dal/dallas-wings"
  },
  {
    "teamId": "5",
    "displayName": "Indiana Fever",
    "shortDisplayName": "Fever",
    "abbreviation": "IND",
    "slug": "indiana-fever",
    "link": "https://www.espn.com/wnba/team/_/name/ind/indiana-fever"
  }
]
```



#### 9. **`GET /wnbateaminfo`**
-   **Description**: Fetches information for a specific WNBA team.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamid`  | string   | `-` | The unique identifier for the team.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbateaminfo?teamid=16', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "team": {
    "id": "16",
    "uid": "s:40~l:59~t:16",
    "slug": "washington-mystics",
    "location": "Washington",
    "name": "Mystics",
    "abbreviation": "WSH",
    "displayName": "Washington Mystics",
    "shortDisplayName": "Mystics",
    "color": "e03a3e",
    "alternateColor": "002b5c",
    "isActive": true,
    "logos": [
      {
        "href": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
        "width": 500,
        "height": 500,
        "alt": "",
        "rel": [
          "full",
          "default"
        ],
        "lastUpdated": "2023-05-10T21:43Z"
      },
      {
        "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/wsh.png",
        "width": 500,
        "height": 500,
        "alt": "",
        "rel": [
          "full",
          "dark"
        ],
        "lastUpdated": "2023-05-11T15:21Z"
      }
    ],
    "..."
    "standingSummary": "5th in Eastern Conference Division"
  }
}
```



#### 10. **`GET /wnbateamplayers`**
-   **Description**: Fetches the list of players for a specific WNBA team.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamid`  | string   | `-` | The unique identifier for the team.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnbateamplayers?teamid=16', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "team": {
    "id": "16",
    "uid": "s:40~l:59~t:16",
    "slug": "washington-mystics",
    "location": "Washington",
    "name": "Mystics",
    "abbreviation": "WSH",
    "displayName": "Washington Mystics",
    "shortDisplayName": "Mystics",
    "color": "e03a3e",
    "alternateColor": "002b5c",
    "isActive": true,
    "logos": [
      {
        "href": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
        "width": 500,
        "height": 500,
        "alt": "",
        "rel": [
          "full",
          "default"
        ],
        "lastUpdated": "2023-05-10T21:43Z"
      },
      {
        "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/wsh.png",
        "width": 500,
        "height": 500,
        "alt": "",
        "rel": [
          "full",
          "dark"
        ],
        "lastUpdated": "2023-05-11T15:21Z"
      }
    ],
    "..."
    "standingSummary": "5th in Eastern Conference Division"
  }
}
```



#### 11. **`GET /players/id`**
-   **Description**: Fetches player identification info.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamId`  | string   | `-` | The unique identifier for the team.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/players/id?teamId=14', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": [
    {
      "playerId": "887",
      "firstName": "Sami",
      "lastName": "Whitcomb",
      "fullName": "Sami Whitcomb",
      "displayName": "Sami Whitcomb",
      "shortName": "S. Whitcomb",
      "link": "https://www.espn.com/wnba/player/_/id/887/sami-whitcomb"
    },
    {
      "playerId": "1068",
      "firstName": "Nneka",
      "lastName": "Ogwumike",
      "fullName": "Nneka Ogwumike",
      "displayName": "Nneka Ogwumike",
      "shortName": "N. Ogwumike",
      "link": "https://www.espn.com/wnba/player/_/id/1068/nneka-ogwumike"
    },
    {
      "playerId": "2491205",
      "firstName": "Skylar",
      "lastName": "Diggins-Smith",
      "fullName": "Skylar Diggins-Smith",
      "displayName": "Skylar Diggins-Smith",
      "shortName": "S. Diggins-Smith",
      "link": "https://www.espn.com/wnba/player/_/id/2491205/skylar-diggins-smith"
    },
    "..."
  ]
}
```



#### 12. **`GET /wnba-news`**
-   **Description**: Fetches the latest news articles about the WNBA.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `limit`  | string   | `23` | The maximum number of news articles to return.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/wnba-news', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
[
  {
    "description": "Ahead of their debut appearance in the WNBL, Geelong United's Jaz Shelley speaks to ESPN's Megan Hustwaite about her journey to the team.",
    "headline": "Geelong United's Jaz Shelley speaks on WNBL launch",
    "images": [
      "https://a.espncdn.com/media/motion/2024/1028/dm_241028_NBL_Interview_Geelong_Uniteds_Jaz_Shelley_speaks_on_WNBL_launch_20241028/dm_241028_NBL_Interview_Geelong_Uniteds_Jaz_Shelley_speaks_on_WNBL_launch_20241028.jpg"
    ],
    "link": "https://www.espn.com/video/clip?id=42046166",
    "published": "2024-10-29T00:01:04Z",
    "premium": false,
    "lastModified": "2024-10-29T00:01:03Z",
    "categories": [
      {
        "id": 412353,
        "description": "Jaz Shelley",
        "type": "athlete",
        "sportId": 59,
        "leagueId": "",
        "createDate": "2024-10-28T06:11:45Z"
      },
      {
        "id": 9579,
        "description": "WNBA",
        "type": "league",
        "sportId": 59,
        "leagueId": 59,
        "createDate": "2024-10-28T06:11:45Z"
      },
      {
        "id": 9576,
        "description": "Men's College Basketball",
        "type": "league",
        "sportId": 41,
        "leagueId": 41,
        "createDate": "2024-10-28T06:11:45Z"
      },
      "..."
    ]
  },
  {
    "description": "A week after the season ended, the WNBA chose not to fine Minnesota Lynx coach Cheryl Reeve after her criticism of the officiating from the winner-take-all Game 5 of the WNBA Finals against the New York Liberty, a league source told ESPN.",
    "headline": "Source: WNBA doesn't fine Minnesota Lynx coach Cheryl Reeve",
    "images": [
      "https://a.espncdn.com/photo/2024/1028/r1407322_600x600_1-1.jpg",
      "https://a.espncdn.com/media/motion/2024/1021/dm_241021_Cheryl_Reeve_criticizes_officiating_after_late_Lynx_foul_sends_game_to_OT/dm_241021_Cheryl_Reeve_criticizes_officiating_after_late_Lynx_foul_sends_game_to_OT.jpg"
    ],
    "link": "https://www.espn.com/wnba/story/_/id/42060315/wnba-fine-minnesota-lynx-coach-cheryl-reeve",
    "published": "2024-10-29T00:54:59Z",
    "premium": false,
    "lastModified": "2024-10-29T00:54:54Z",
    "categories": [
      {
        "id": 409224,
        "description": "news",
        "type": "topic",
        "sportId": "",
        "leagueId": "",
        "createDate": "2024-10-28T23:30:00Z"
      },
      {
        "id": 9579,
        "description": "WNBA",
        "type": "league",
        "sportId": 59,
        "leagueId": 59,
        "createDate": "2024-10-28T23:30:00Z"
      },
      {
        "id": 5847,
        "description": "Minnesota Lynx",
        "type": "team",
        "sportId": 59,
        "leagueId": "",
        "createDate": "2024-10-28T23:30:00Z"
      },
      "..."
    ]
  },
  {
    "description": "Connecticut and Stephanie White parted ways Monday, leaving seven head-coaching positions open in the WNBA.",
    "headline": "WNBA coaching changes for 2025: Sun, White part ways",
    "images": [
      "https://a.espncdn.com/photo/2024/1017/r1401836_1296x729_16-9.jpg",
      "https://a.espncdn.com/photo/2024/1027/r1406474_1296x729_16-9.jpg",
      "https://a.espncdn.com/media/motion/2024/1028/dm_241028_Sun_Fever_coaches_out/dm_241028_Sun_Fever_coaches_out.jpg"
    ],
    "link": "https://www.espn.com/wnba/story/_/id/42033470/wnba-coaching-changes-tracker-carousel-hires-2025-season",
    "published": "2024-10-29T02:13:17Z",
    "premium": false,
    "lastModified": "2024-10-29T02:13:13Z",
    "categories": [
      {
        "id": 9579,
        "description": "WNBA",
        "type": "league",
        "sportId": 59,
        "leagueId": 59,
        "createDate": "2024-10-28T22:45:00Z"
      },
      {
        "id": 36562,
        "description": "Atlanta Dream",
        "type": "team",
        "sportId": 59,
        "leagueId": "",
        "createDate": "2024-10-28T22:45:00Z"
      },
      {
        "id": 20948,
        "description": "Chicago Sky",
        "type": "team",
        "sportId": 59,
        "leagueId": "",
        "createDate": "2024-10-28T22:45:00Z"
      },
      "..."
    ]
  },
  "..."
]
```



#### 13. **`GET /player-statistic`**
-   **Description**: Fetches statistics for a specific player.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `playerId`  | string   | `-` | The unique identifier for the player.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/player-statistic?playerId=2987869', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "id": "0",
  "name": "All Splits",
  "abbreviation": "Total",
  "type": "total",
  "categories": [
    {
      "name": "defensive",
      "displayName": "Defensive",
      "shortDisplayName": "Defensive",
      "abbreviation": "def",
      "summary": "",
      "stats": [
        {
          "name": "blocks",
          "displayName": "Blocks",
          "shortDisplayName": "BLK",
          "description": "Short for blocked shot, number of times when a defensive player legally deflects a field goal attempt from an offensive player.",
          "abbreviation": "BLK",
          "value": 80,
          "displayValue": "80"
        },
        {
          "name": "defensiveRebounds",
          "displayName": "Defensive Rebounds",
          "shortDisplayName": "DREB",
          "description": "The number of times when the defense obtains the possession of the ball after a missed shot by the offense.",
          "abbreviation": "DR",
          "value": 913,
          "displayValue": "913"
        },
        {
          "name": "steals",
          "displayName": "Steals",
          "shortDisplayName": "STL",
          "description": "The number of times a defensive player forced a turnover by intercepting or deflecting a pass or a dribble of an offensive player.",
          "abbreviation": "STL",
          "value": 389,
          "displayValue": "389"
        },
        "..."
      ]
    },
    {
      "name": "general",
      "displayName": "General",
      "shortDisplayName": "General",
      "abbreviation": "gen",
      "summary": "",
      "stats": [
        {
          "name": "disqualifications",
          "displayName": "Disqualifications",
          "shortDisplayName": "DQ",
          "description": "The number of times a player reached the foul limit.",
          "abbreviation": "DQ",
          "value": 1,
          "displayValue": "1"
        },
        {
          "name": "flagrantFouls",
          "displayName": "Flagrant Fouls",
          "shortDisplayName": "FLAG",
          "description": "The number of fouls that the officials thought were unnecessary or excessive.",
          "abbreviation": "FLAG",
          "value": 2,
          "displayValue": "2"
        },
        {
          "name": "fouls",
          "displayName": "Fouls",
          "shortDisplayName": "PF",
          "description": "The number of times a player had illegal contact with the opponent.",
          "abbreviation": "PF",
          "value": 559,
          "displayValue": "559"
        },
        "..."
      ]
    },
    {
      "name": "offensive",
      "displayName": "Offensive",
      "shortDisplayName": "Offensive",
      "abbreviation": "off",
      "summary": "",
      "stats": [
        {
          "name": "assists",
          "displayName": "Assists",
          "shortDisplayName": "AST",
          "description": "The number of times a player who passes the ball to a teammate in a way that leads to a score by field goal, meaning that he or she was \"assisting\" in the basket. There is some judgment involved in deciding whether a passer should be credited with an assist.",
          "abbreviation": "AST",
          "value": 1052,
          "displayValue": "1052"
        },
        {
          "name": "effectiveFGPct",
          "displayName": "Effective Field Goal Percentage",
          "shortDisplayName": "EFF FG%",
          "description": "Metric that gives 3pt field goals more worth than 2pt field goals: (FGM + (0.5 x 3PTM)) / FGA",
          "abbreviation": "EFF FG%",
          "value": 0,
          "displayValue": "0.0"
        },
        {
          "name": "fieldGoals",
          "displayName": "Field Goals",
          "shortDisplayName": "FG",
          "description": "Field Goal makes and attempts.",
          "abbreviation": "FG",
          "value": 0.402183,
          "displayValue": "1842/4580"
        },
        "..."
      ]
    }
  ]
}
```



#### 14. **`GET /team-statistic`**
-   **Description**: Fetches statistics for a specific team.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamId`  | string   | `-` | The unique identifier for the team.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team-statistic?teamId=16', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "stats": {
    "id": "0",
    "name": "All Splits",
    "abbreviation": "Total",
    "categories": [
      {
        "name": "general",
        "displayName": "General",
        "abbreviation": "gen",
        "stats": [
          {
            "name": "avgRebounds",
            "displayName": "Rebounds Per Game",
            "shortDisplayName": "RPG",
            "description": "The average rebounds per game.",
            "abbreviation": "REB",
            "value": 31.85,
            "displayValue": "31.9"
          },
          {
            "name": "assistTurnoverRatio",
            "displayName": "Assist To Turnover Ratio",
            "shortDisplayName": "AST/TO",
            "description": "The average number of assists a player or team records per turnover",
            "abbreviation": "AST/TO",
            "value": 1.428808,
            "displayValue": "1.4",
            "perGameValue": 1.399999976158142,
            "perGameDisplayValue": "1.4"
          },
          {
            "name": "avgFouls",
            "displayName": "Fouls Per Game",
            "shortDisplayName": "PFPG",
            "description": "The average fouls committed per game.",
            "abbreviation": "PF",
            "value": 18.425,
            "displayValue": "18.4"
          },
          "..."
        ]
      },
      {
        "name": "offensive",
        "displayName": "Offensive",
        "abbreviation": "off",
        "stats": [
          {
            "name": "freeThrowPct",
            "displayName": "Free Throw Percentage",
            "shortDisplayName": "FT%",
            "description": "The ratio of free throws made to free throws attempted: FTM / FTA",
            "abbreviation": "FT%",
            "value": 76.705,
            "displayValue": "76.7",
            "perGameValue": 0.7670000195503235,
            "perGameDisplayValue": "0.767"
          },
          {
            "name": "threePointPct",
            "displayName": "3-Point Field Goal Percentage",
            "shortDisplayName": "3P%",
            "description": "The ratio of 3pt field goals made to 3pt field goals attempted: 3PM / 3PA.",
            "abbreviation": "3P%",
            "value": 36.56,
            "displayValue": "36.6",
            "perGameValue": 0.3659999966621399,
            "perGameDisplayValue": "0.366"
          },
          {
            "name": "avgFieldGoalsMade",
            "displayName": "Average Field Goals Made",
            "shortDisplayName": "AFGM",
            "description": "The average field goals made per game.",
            "abbreviation": "FGM",
            "value": 29.025,
            "displayValue": "29.0"
          },
          "..."
        ]
      },
      {
        "name": "defensive",
        "displayName": "Defensive",
        "abbreviation": "def",
        "stats": [
          {
            "name": "avgDefensiveRebounds",
            "displayName": "Defensive Rebounds Per Game",
            "shortDisplayName": "DRPG",
            "description": "The average defensive rebounds per game.",
            "abbreviation": "DR",
            "value": 24.775,
            "displayValue": "24.8"
          },
          {
            "name": "avgBlocks",
            "displayName": "Blocks Per Game",
            "shortDisplayName": "BPG",
            "description": "The average blocks per game.",
            "abbreviation": "BLK",
            "value": 3.425,
            "displayValue": "3.4"
          },
          {
            "name": "avgSteals",
            "displayName": "Steals Per Game",
            "shortDisplayName": "SPG",
            "description": "The average steals per game.",
            "abbreviation": "STL",
            "value": 7.275,
            "displayValue": "7.3"
          },
          "..."
        ]
      }
    ]
  }
}
```



#### 15. **`GET /injuries`**
-   **Description**: Fetches injury information for the current season.

-   **Parameters**:
  This endpoint has no parameters.

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/injuries', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "timestamp": "2024-10-30T08:29:36Z",
  "status": "success",
  "season": {
    "year": 2024,
    "type": 4,
    "name": "Off Season",
    "displayName": "2024"
  },
  "injuries": [
    {
      "id": "20",
      "displayName": "Atlanta Dream",
      "injuries": [
        {
          "id": "21699",
          "longComment": "Powers hasn't played since the WNBA resumed following the Olympic break due to a calf injury, and she didn't have a return timetable, so this update isn't a surprise. Even if the Dream can secure the final playoff spot, Powers wouldn't be able to return. During her first season in Atlanta, Powers made 17 appearances (two starts) and averaged 8.6 points, 3.3 rebounds, 1.4 assists and 0.9 steals in 17.9 minutes per game.",
          "shortComment": "Powers (calf) has been ruled out for the remainder of the season, Malik Brown of Clutch Points reports.",
          "status": "Out",
          "date": "2024-09-17T20:19Z",
          "athlete": {
            "firstName": "Aerial",
            "lastName": "Powers",
            "displayName": "Aerial Powers",
            "shortName": "A. Powers",
            "links": [
              {
                "language": "en-US",
                "rel": [
                  "playercard",
                  "desktop",
                  "athlete"
                ],
                "href": "https://www.espn.com/wnba/player/_/id/2999035/aerial-powers",
                "text": "Player Card",
                "shortText": "Player Card",
                "isExternal": false,
                "isPremium": false
              },
              {
                "language": "en-US",
                "rel": [
                  "stats",
                  "desktop",
                  "athlete"
                ],
                "href": "https://www.espn.com/wnba/player/stats/_/id/2999035/aerial-powers",
                "text": "Stats",
                "shortText": "Stats",
                "isExternal": false,
                "isPremium": false
              },
              {
                "language": "en-US",
                "rel": [
                  "gamelog",
                  "desktop",
                  "athlete"
                ],
                "href": "https://www.espn.com/wnba/player/gamelog/_/id/2999035/aerial-powers",
                "text": "Game Log",
                "shortText": "Game Log",
                "isExternal": false,
                "isPremium": false
              },
              "..."
            ],
            "headshot": {
              "href": "https://a.espncdn.com/i/headshots/wnba/players/full/2999035.png",
              "alt": "Aerial Powers"
            },
            "position": {
              "id": "3",
              "name": "Guard",
              "displayName": "Guard",
              "abbreviation": "G",
              "leaf": false
            },
            "team": {
              "id": "20",
              "uid": "s:40~l:59~t:20",
              "slug": "atlanta-dream",
              "name": "Dream",
              "abbreviation": "ATL",
              "displayName": "Atlanta Dream",
              "logos": [
                {
                  "href": "https://a.espncdn.com/i/teamlogos/wnba/500/atl.png",
                  "width": 500,
                  "height": 500,
                  "alt": "",
                  "rel": [
                    "full",
                    "default"
                  ],
                  "lastUpdated": "2023-05-10T21:43Z"
                },
                {
                  "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/atl.png",
                  "width": 500,
                  "height": 500,
                  "alt": "",
                  "rel": [
                    "full",
                    "dark"
                  ],
                  "lastUpdated": "2023-05-10T21:45Z"
                }
              ],
              "links": [
                {
                  "language": "en-US",
                  "rel": [
                    "clubhouse",
                    "desktop",
                    "team"
                  ],
                  "href": "https://www.espn.com/wnba/team/_/name/atl/atlanta-dream",
                  "text": "Clubhouse",
                  "shortText": "Clubhouse",
                  "isExternal": false,
                  "isPremium": false
                },
                {
                  "language": "en-US",
                  "rel": [
                    "clubhouse",
                    "mobile",
                    "team"
                  ],
                  "href": "https://m.espn.com/wnba/clubhouse?teamId=20",
                  "text": "Clubhouse",
                  "shortText": "Clubhouse",
                  "isExternal": false,
                  "isPremium": false
                },
                {
                  "language": "en-US",
                  "rel": [
                    "roster",
                    "desktop",
                    "team"
                  ],
                  "href": "https://www.espn.com/wnba/team/roster/_/name/atl/atlanta-dream",
                  "text": "Roster",
                  "shortText": "Roster",
                  "isExternal": false,
                  "isPremium": false
                },
                "..."
              ]
            },
            "notes": {
              "items": []
            },
            "status": {
              "id": "1",
              "name": "Active",
              "type": "active",
              "abbreviation": "Active"
            }
          },
          "source": {
            "id": "1",
            "description": "basic/manual",
            "state": "basic"
          },
          "type": {
            "id": "4",
            "name": "INJURY_STATUS_OUT",
            "description": "out",
            "abbreviation": "O"
          },
          "details": {
            "fantasyStatus": {
              "description": "GTD",
              "abbreviation": "GTD"
            },
            "type": "Calf",
            "detail": "Not Specified",
            "side": "Left",
            "returnDate": "2025-05-01"
          }
        },
        {
          "id": "21364",
          "longComment": "Parker-Tyus had missed the last eight games due to an ankle injury, and she won't be able to return to the court until the 2025 campaign. Over 25 appearances (11 starts) for the Dream this year, she averaged 9.2 points and 4.8 rebounds in 19.7 minutes per game. Parker-Tyus is slated to become an unrestricted free agent during the offseason and should draw ample interest after averaging 11.6 points and 5.5 rebounds in 23.4 minutes per game over her four seasons in Atlanta.",
          "shortComment": "The Dream announced Friday that Parker-Tyus (ankle) has been ruled out for the remainder of the 2024 season, WNBA reporter Wilton C. Jackson II reports.",
          "status": "Out",
          "date": "2024-09-06T20:45Z",
          "athlete": {
            "firstName": "Cheyenne",
            "lastName": "Parker-Tyus",
            "displayName": "Cheyenne Parker-Tyus",
            "shortName": "C. Parker-Tyus",
            "links": [
              {
                "language": "en-US",
                "rel": [
                  "playercard",
                  "desktop",
                  "athlete"
                ],
                "href": "https://www.espn.com/wnba/player/_/id/2529458/cheyenne-parker-tyus",
                "text": "Player Card",
                "shortText": "Player Card",
                "isExternal": false,
                "isPremium": false
              },
              {
                "language": "en-US",
                "rel": [
                  "stats",
                  "desktop",
                  "athlete"
                ],
                "href": "https://www.espn.com/wnba/player/stats/_/id/2529458/cheyenne-parker-tyus",
                "text": "Stats",
                "shortText": "Stats",
                "isExternal": false,
                "isPremium": false
              },
              {
                "language": "en-US",
                "rel": [
                  "gamelog",
                  "desktop",
                  "athlete"
                ],
                "href": "https://www.espn.com/wnba/player/gamelog/_/id/2529458/cheyenne-parker-tyus",
                "text": "Game Log",
                "shortText": "Game Log",
                "isExternal": false,
                "isPremium": false
              },
              "..."
            ],
            "headshot": {
              "href": "https://a.espncdn.com/i/headshots/wnba/players/full/2529458.png",
              "alt": "Cheyenne Parker-Tyus"
            },
            "position": {
              "id": "7",
              "name": "Forward",
              "displayName": "Forward",
              "abbreviation": "F",
              "leaf": false
            },
            "team": {
              "id": "20",
              "uid": "s:40~l:59~t:20",
              "slug": "atlanta-dream",
              "name": "Dream",
              "abbreviation": "ATL",
              "displayName": "Atlanta Dream",
              "logos": [
                {
                  "href": "https://a.espncdn.com/i/teamlogos/wnba/500/atl.png",
                  "width": 500,
                  "height": 500,
                  "alt": "",
                  "rel": [
                    "full",
                    "default"
                  ],
                  "lastUpdated": "2023-05-10T21:43Z"
                },
                {
                  "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/atl.png",
                  "width": 500,
                  "height": 500,
                  "alt": "",
                  "rel": [
                    "full",
                    "dark"
                  ],
                  "lastUpdated": "2023-05-10T21:45Z"
                }
              ],
              "links": [
                {
                  "language": "en-US",
                  "rel": [
                    "clubhouse",
                    "desktop",
                    "team"
                  ],
                  "href": "https://www.espn.com/wnba/team/_/name/atl/atlanta-dream",
                  "text": "Clubhouse",
                  "shortText": "Clubhouse",
                  "isExternal": false,
                  "isPremium": false
                },
                {
                  "language": "en-US",
                  "rel": [
                    "clubhouse",
                    "mobile",
                    "team"
                  ],
                  "href": "https://m.espn.com/wnba/clubhouse?teamId=20",
                  "text": "Clubhouse",
                  "shortText": "Clubhouse",
                  "isExternal": false,
                  "isPremium": false
                },
                {
                  "language": "en-US",
                  "rel": [
                    "roster",
                    "desktop",
                    "team"
                  ],
                  "href": "https://www.espn.com/wnba/team/roster/_/name/atl/atlanta-dream",
                  "text": "Roster",
                  "shortText": "Roster",
                  "isExternal": false,
                  "isPremium": false
                },
                "..."
              ]
            },
            "notes": {
              "items": []
            },
            "status": {
              "id": "1",
              "name": "Active",
              "type": "active",
              "abbreviation": "Active"
            }
          },
          "source": {
            "id": "1",
            "description": "basic/manual",
            "state": "basic"
          },
          "type": {
            "id": "4",
            "name": "INJURY_STATUS_OUT",
            "description": "out",
            "abbreviation": "O"
          },
          "details": {
            "fantasyStatus": {
              "description": "GTD",
              "abbreviation": "GTD"
            },
            "type": "Ankle",
            "side": "Left",
            "returnDate": "2025-05-01"
          }
        }
      ]
    },
    "..."
  ]
}
```



#### 16. **`GET /team-roster`**
-   **Description**: Fetches the roster of a specific WNBA team.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamId`  | string   | `-` | The unique identifier for the team.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team-roster?teamId=16', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": [
    {
      "playerId": "3146151",
      "uid": "s:40~l:59~a:3146151",
      "firstName": "Ariel",
      "lastName": "Atkins",
      "fullName": "Ariel Atkins",
      "displayName": "Ariel Atkins",
      "shortName": "A. Atkins",
      "weight": 167,
      "displayWeight": "167 lbs",
      "height": 70,
      "displayHeight": "5' 10\"",
      "age": 28,
      "dateOfBirth": "1996-07-30T07:00Z",
      "links": [
        {
          "text": "Player Card",
          "href": "https://www.espn.com/wnba/player/_/id/3146151/ariel-atkins"
        },
        {
          "text": "Stats",
          "href": "https://www.espn.com/wnba/player/stats/_/id/3146151/ariel-atkins"
        },
        {
          "text": "Game Log",
          "href": "https://www.espn.com/wnba/player/gamelog/_/id/3146151/ariel-atkins"
        },
        "..."
      ],
      "birthPlace": {
        "city": "Dallas",
        "state": "TX",
        "country": "USA"
      },
      "college": {
        "collegeId": "251",
        "mascot": "Longhorns",
        "name": "Texas",
        "shortName": "Texas",
        "abbrev": "TEX",
        "logo": "https://a.espncdn.com/i/teamlogos/ncaa/500/251.png"
      },
      "slug": "ariel-atkins",
      "headshot": "https://a.espncdn.com/i/headshots/wnba/players/full/3146151.png",
      "jersey": "7",
      "position": {
        "id": "3",
        "name": "Guard",
        "displayName": "Guard",
        "abbreviation": "G",
        "leaf": false
      },
      "injuries": [],
      "contracts": [],
      "experience": {
        "years": 6
      },
      "contract": {},
      "status": "Active"
    },
    {
      "playerId": "4398911",
      "uid": "s:40~l:59~a:4398911",
      "firstName": "Shakira",
      "lastName": "Austin",
      "fullName": "Shakira Austin",
      "displayName": "Shakira Austin",
      "shortName": "S. Austin",
      "weight": 190,
      "displayWeight": "190 lbs",
      "height": 77,
      "displayHeight": "6' 5\"",
      "age": 24,
      "dateOfBirth": "2000-07-25T07:00Z",
      "links": [
        {
          "text": "Player Card",
          "href": "https://www.espn.com/wnba/player/_/id/4398911/shakira-austin"
        },
        {
          "text": "Stats",
          "href": "https://www.espn.com/wnba/player/stats/_/id/4398911/shakira-austin"
        },
        {
          "text": "Game Log",
          "href": "https://www.espn.com/wnba/player/gamelog/_/id/4398911/shakira-austin"
        },
        "..."
      ],
      "birthPlace": {
        "city": "Fredericksburg",
        "state": "VA",
        "country": "USA"
      },
      "college": {
        "collegeId": "145",
        "mascot": "Rebels",
        "name": "Ole Miss",
        "shortName": "Ole Miss",
        "abbrev": "MISS",
        "logo": "https://a.espncdn.com/i/teamlogos/ncaa/500/145.png"
      },
      "slug": "shakira-austin",
      "headshot": "https://a.espncdn.com/i/headshots/wnba/players/full/4398911.png",
      "jersey": "0",
      "position": {
        "id": "9",
        "name": "Center",
        "displayName": "Center",
        "abbreviation": "C",
        "leaf": false
      },
      "injuries": [
        {
          "status": "Out",
          "date": "2024-09-15T18:11Z"
        }
      ],
      "contracts": [],
      "experience": {
        "years": 2
      },
      "contract": {},
      "status": "Active"
    },
    {
      "playerId": "2529183",
      "uid": "s:40~l:59~a:2529183",
      "firstName": "Stefanie",
      "lastName": "Dolson",
      "fullName": "Stefanie Dolson",
      "displayName": "Stefanie Dolson",
      "shortName": "S. Dolson",
      "weight": 235,
      "displayWeight": "235 lbs",
      "height": 77,
      "displayHeight": "6' 5\"",
      "age": 32,
      "dateOfBirth": "1992-01-08T08:00Z",
      "links": [
        {
          "text": "Player Card",
          "href": "https://www.espn.com/wnba/player/_/id/2529183/stefanie-dolson"
        },
        {
          "text": "Stats",
          "href": "https://www.espn.com/wnba/player/stats/_/id/2529183/stefanie-dolson"
        },
        {
          "text": "Game Log",
          "href": "https://www.espn.com/wnba/player/gamelog/_/id/2529183/stefanie-dolson"
        },
        "..."
      ],
      "birthPlace": {
        "city": "Port Jervis",
        "state": "NY",
        "country": "USA"
      },
      "college": {
        "collegeId": "41",
        "mascot": "Huskies",
        "name": "UConn",
        "shortName": "UConn",
        "abbrev": "CONN",
        "logo": "https://a.espncdn.com/i/teamlogos/ncaa/500/41.png"
      },
      "slug": "stefanie-dolson",
      "headshot": "https://a.espncdn.com/i/headshots/wnba/players/full/2529183.png",
      "jersey": "31",
      "position": {
        "id": "9",
        "name": "Center",
        "displayName": "Center",
        "abbreviation": "C",
        "leaf": false
      },
      "injuries": [],
      "contracts": [],
      "experience": {
        "years": 10
      },
      "contract": {},
      "status": "Active"
    },
    "..."
  ]
}
```



#### 17. **`GET /schedule-team`**
-   **Description**: Fetches the schedule for a specific WNBA team.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `season`  | string   | `-` | The season year.   | Yes       |
| `teamId`  | string   | `-` | The unique identifier for the team.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/schedule-team?season=2019&teamId=16', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "requestedSeason": {
    "year": 2019,
    "type": 1,
    "name": "Preseason",
    "displayName": "2019"
  },
  "team": {
    "id": "16",
    "abbreviation": "WSH",
    "location": "Washington",
    "name": "Mystics",
    "displayName": "Washington Mystics",
    "clubhouse": "https://www.espn.com/wnba/team/_/name/wsh/washington-mystics",
    "color": "e03a3e",
    "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
    "recordSummary": "14-26",
    "seasonSummary": "2024",
    "standingSummary": "5th in Eastern Conference Division",
    "groups": {
      "id": "1",
      "parent": {
        "id": "3"
      },
      "isConference": true
    }
  },
  "events": [
    {
      "id": "401129934",
      "date": "2019-05-11T00:00Z",
      "name": "Washington Mystics at Minnesota Lynx",
      "shortName": "WSH @ MIN",
      "season": {
        "year": 2019,
        "displayName": "2019"
      },
      "seasonType": {
        "id": "1",
        "type": 1,
        "name": "Preseason",
        "abbreviation": "pre"
      },
      "timeValid": true,
      "competitions": [
        {
          "id": "401129934",
          "date": "2019-05-11T00:00Z",
          "attendance": 3201,
          "type": {
            "id": "1",
            "text": "Standard",
            "abbreviation": "STD",
            "slug": "standard",
            "type": "standard"
          },
          "timeValid": true,
          "neutralSite": false,
          "boxscoreAvailable": true,
          "ticketsAvailable": false,
          "venue": {
            "fullName": "Target Center",
            "address": {
              "city": "Minneapolis",
              "state": "MN"
            }
          },
          "competitors": [
            {
              "id": "8",
              "type": "team",
              "order": 0,
              "homeAway": "home",
              "winner": true,
              "team": {
                "id": "8",
                "location": "Minnesota",
                "abbreviation": "MIN",
                "displayName": "Minnesota Lynx",
                "shortDisplayName": "Lynx",
                "logos": [
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500/min.png",
                    "width": 500,
                    "height": 500,
                    "alt": "",
                    "rel": [
                      "full",
                      "default"
                    ],
                    "lastUpdated": "2023-05-10T21:43Z"
                  },
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/min.png",
                    "width": 500,
                    "height": 500,
                    "alt": "",
                    "rel": [
                      "full",
                      "dark"
                    ],
                    "lastUpdated": "2023-05-10T21:45Z"
                  }
                ],
                "links": [
                  {
                    "rel": [
                      "clubhouse",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/_/name/min/minnesota-lynx",
                    "text": "Clubhouse"
                  },
                  {
                    "rel": [
                      "clubhouse",
                      "mobile",
                      "team"
                    ],
                    "href": "https://m.espn.com/wnba/clubhouse?teamId=8",
                    "text": "Clubhouse"
                  }
                ]
              },
              "..."
            },
            {
              "id": "16",
              "type": "team",
              "order": 1,
              "homeAway": "away",
              "winner": false,
              "team": {
                "id": "16",
                "location": "Washington",
                "abbreviation": "WSH",
                "displayName": "Washington Mystics",
                "shortDisplayName": "Mystics",
                "logos": [
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
                    "width": 500,
                    "height": 500,
                    "alt": "",
                    "rel": [
                      "full",
                      "default"
                    ],
                    "lastUpdated": "2023-05-10T21:43Z"
                  },
                  {
                    "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/wsh.png",
                    "width": 500,
                    "height": 500,
                    "alt": "",
                    "rel": [
                      "full",
                      "dark"
                    ],
                    "lastUpdated": "2023-05-11T15:21Z"
                  }
                ],
                "links": [
                  {
                    "rel": [
                      "clubhouse",
                      "desktop",
                      "team"
                    ],
                    "href": "https://www.espn.com/wnba/team/_/name/wsh/washington-mystics",
                    "text": "Clubhouse"
                  },
                  {
                    "rel": [
                      "clubhouse",
                      "mobile",
                      "team"
                    ],
                    "href": "https://m.espn.com/wnba/clubhouse?teamId=16",
                    "text": "Clubhouse"
                  }
                ]
              },
              "score": {
                "value": 79,
                "displayValue": "79"
              },
              "leaders": [
                {
                  "name": "points",
                  "displayName": "Points",
                  "abbreviation": "Pts",
                  "leaders": [
                    {
                      "displayValue": "19",
                      "value": 19,
                      "athlete": {
                        "id": "3027368",
                        "lastName": "Meesseman",
                        "displayName": "Emma Meesseman",
                        "shortName": "E. Meesseman",
                        "links": [
                          {
                            "rel": [
                              "playercard",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/_/id/3027368/emma-meesseman"
                          },
                          {
                            "rel": [
                              "stats",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/stats/_/id/3027368/emma-meesseman"
                          },
                          {
                            "rel": [
                              "gamelog",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/gamelog/_/id/3027368/emma-meesseman"
                          },
                          "..."
                        ]
                      }
                    }
                  ]
                },
                {
                  "name": "assists",
                  "displayName": "Assists",
                  "abbreviation": "Ast",
                  "leaders": [
                    {
                      "displayValue": "3",
                      "value": 3,
                      "athlete": {
                        "id": "2529137",
                        "lastName": "Cloud",
                        "displayName": "Natasha Cloud",
                        "shortName": "N. Cloud",
                        "links": [
                          {
                            "rel": [
                              "playercard",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/_/id/2529137/natasha-cloud"
                          },
                          {
                            "rel": [
                              "stats",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/stats/_/id/2529137/natasha-cloud"
                          },
                          {
                            "rel": [
                              "gamelog",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/gamelog/_/id/2529137/natasha-cloud"
                          },
                          "..."
                        ]
                      }
                    }
                  ]
                },
                {
                  "name": "rebounds",
                  "displayName": "Rebounds",
                  "abbreviation": "Reb",
                  "leaders": [
                    {
                      "displayValue": "6",
                      "value": 6,
                      "athlete": {
                        "id": "3027368",
                        "lastName": "Meesseman",
                        "displayName": "Emma Meesseman",
                        "shortName": "E. Meesseman",
                        "links": [
                          {
                            "rel": [
                              "playercard",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/_/id/3027368/emma-meesseman"
                          },
                          {
                            "rel": [
                              "stats",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/stats/_/id/3027368/emma-meesseman"
                          },
                          {
                            "rel": [
                              "gamelog",
                              "desktop",
                              "athlete"
                            ],
                            "href": "https://www.espn.com/wnba/player/gamelog/_/id/3027368/emma-meesseman"
                          },
                          "..."
                        ]
                      }
                    }
                  ]
                }
              ],
              "record": [
                {
                  "id": "900",
                  "abbreviation": "Game",
                  "displayName": "Record Year To Date",
                  "shortDisplayName": "YTD",
                  "description": "Overall Record",
                  "type": "total",
                  "displayValue": "0-1"
                }
              ]
            }
          ],
          "notes": [],
          "broadcasts": [],
          "status": {
            "clock": 0,
            "displayClock": "0.0",
            "period": 4,
            "type": {
              "id": "3",
              "name": "STATUS_FINAL",
              "state": "post",
              "completed": true,
              "description": "Final",
              "detail": "Final",
              "shortDetail": "Final"
            }
          }
        }
      ],
      "links": [
        {
          "language": "en-US",
          "rel": [
            "summary",
            "desktop",
            "event"
          ],
          "href": "https://www.espn.com/wnba/game/_/gameId/401129934/mystics-lynx",
          "text": "Gamecast",
          "shortText": "Summary",
          "isExternal": false,
          "isPremium": false
        },
        {
          "language": "en-US",
          "rel": [
            "summary",
            "sportscenter",
            "app",
            "..."
          ],
          "href": "sportscenter://x-callback-url/showGame?sportName=basketball&leagueAbbrev=wnba&gameId=401129934",
          "text": "Gamecast",
          "shortText": "Summary",
          "isExternal": false,
          "isPremium": false
        },
        {
          "language": "en-US",
          "rel": [
            "now",
            "desktop",
            "event"
          ],
          "href": "https://www.espn.com/wnba/game/_/gameId/401129934",
          "text": "Now",
          "shortText": "Now",
          "isExternal": false,
          "isPremium": false
        },
        "..."
      ]
    },
    "..."
  ]
}
```



#### 18. **`GET /team/schedulev2`**
-   **Description**: Fetches the schedule for a specific WNBA team, including season type.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `season`  | string   | `-` | The season year.   | Yes       |
| `teamId`  | string   | `-` | The unique identifier for the team.   | Yes       |
| `seasonType`  | string   | `2` | The type of season (`1` for Regular Season, `2` for Preseason).   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team/schedulev2?season=2024&teamId=14&seasonType=2', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": {
    "requestedSeason": {
      "year": 2024,
      "type": 2,
      "name": "Regular Season",
      "displayName": "2024"
    },
    "team": {
      "teamId": "14",
      "abbreviation": "SEA",
      "location": "Seattle",
      "name": "Storm",
      "displayName": "Seattle Storm",
      "url": "https://www.espn.com/wnba/team/_/name/sea/seattle-storm",
      "color": "2c5235",
      "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png"
    },
    "events": [
      {
        "id": "401620221",
        "date": "2024-05-15T02:00Z",
        "name": "Minnesota Lynx at Seattle Storm",
        "shortName": "MIN @ SEA",
        "season": {
          "year": 2024,
          "displayName": "2024"
        },
        "seasonType": {
          "id": "2",
          "type": 2,
          "name": "Regular Season",
          "abbreviation": "reg"
        },
        "timeValid": true,
        "competitions": [
          {
            "id": "401620221",
            "date": "2024-05-15T02:00Z",
            "attendance": 8508,
            "type": {
              "id": "1",
              "text": "Standard",
              "abbreviation": "STD",
              "slug": "standard",
              "type": "standard"
            },
            "timeValid": true,
            "neutralSite": false,
            "boxscoreAvailable": true,
            "ticketsAvailable": false,
            "venue": {
              "fullName": "Climate Pledge Arena",
              "address": {
                "city": "Seattle",
                "state": "WA"
              }
            },
            "competitors": [
              {
                "id": "14",
                "type": "team",
                "order": 0,
                "homeAway": "home",
                "winner": false,
                "team": {
                  "id": "14",
                  "location": "Seattle",
                  "abbreviation": "SEA",
                  "displayName": "Seattle Storm",
                  "shortDisplayName": "Storm",
                  "logos": [
                    {
                      "href": "https://a.espncdn.com/i/teamlogos/wnba/500/sea.png",
                      "width": 500,
                      "height": 500,
                      "alt": "",
                      "rel": [
                        "full",
                        "default"
                      ],
                      "lastUpdated": "2023-05-10T21:43Z"
                    },
                    {
                      "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/sea.png",
                      "width": 500,
                      "height": 500,
                      "alt": "",
                      "rel": [
                        "full",
                        "dark"
                      ],
                      "lastUpdated": "2023-05-10T21:45Z"
                    },
                    {
                      "href": "https://a.espncdn.com/i/teamlogos/wnba/500/scoreboard/sea.png",
                      "width": 500,
                      "height": 500,
                      "alt": "",
                      "rel": [
                        "full",
                        "scoreboard"
                      ],
                      "lastUpdated": "2021-03-08T15:24Z"
                    },
                    "..."
                  ],
                  "links": [
                    {
                      "rel": [
                        "clubhouse",
                        "desktop",
                        "team"
                      ],
                      "href": "https://www.espn.com/wnba/team/_/name/sea/seattle-storm",
                      "text": "Clubhouse"
                    },
                    {
                      "rel": [
                        "clubhouse",
                        "mobile",
                        "team"
                      ],
                      "href": "https://m.espn.com/wnba/clubhouse?teamId=14",
                      "text": "Clubhouse"
                    }
                  ]
                },
                "score": {
                  "value": 70,
                  "displayValue": "70"
                },
                "leaders": [
                  {
                    "name": "points",
                    "displayName": "Points",
                    "abbreviation": "Pts",
                    "leaders": [
                      {
                        "displayValue": "20",
                        "value": 20,
                        "athlete": {
                          "id": "1068",
                          "lastName": "Ogwumike",
                          "displayName": "Nneka Ogwumike",
                          "shortName": "N. Ogwumike",
                          "links": [
                            {
                              "rel": [
                                "playercard",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/_/id/1068/nneka-ogwumike"
                            },
                            {
                              "rel": [
                                "stats",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/stats/_/id/1068/nneka-ogwumike"
                            },
                            {
                              "rel": [
                                "gamelog",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/gamelog/_/id/1068/nneka-ogwumike"
                            },
                            "..."
                          ]
                        }
                      }
                    ]
                  },
                  {
                    "name": "assists",
                    "displayName": "Assists",
                    "abbreviation": "Ast",
                    "leaders": [
                      {
                        "displayValue": "6",
                        "value": 6,
                        "athlete": {
                          "id": "2491205",
                          "lastName": "Diggins-Smith",
                          "displayName": "Skylar Diggins-Smith",
                          "shortName": "S. Diggins-Smith",
                          "links": [
                            {
                              "rel": [
                                "playercard",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/_/id/2491205/skylar-diggins-smith"
                            },
                            {
                              "rel": [
                                "stats",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/stats/_/id/2491205/skylar-diggins-smith"
                            },
                            {
                              "rel": [
                                "gamelog",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/gamelog/_/id/2491205/skylar-diggins-smith"
                            },
                            "..."
                          ]
                        }
                      }
                    ]
                  },
                  {
                    "name": "rebounds",
                    "displayName": "Rebounds",
                    "abbreviation": "Reb",
                    "leaders": [
                      {
                        "displayValue": "10",
                        "value": 10,
                        "athlete": {
                          "id": "2987869",
                          "lastName": "Loyd",
                          "displayName": "Jewell Loyd",
                          "shortName": "J. Loyd",
                          "links": [
                            {
                              "rel": [
                                "playercard",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/_/id/2987869/jewell-loyd"
                            },
                            {
                              "rel": [
                                "stats",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/stats/_/id/2987869/jewell-loyd"
                            },
                            {
                              "rel": [
                                "gamelog",
                                "desktop",
                                "athlete"
                              ],
                              "href": "https://www.espn.com/wnba/player/gamelog/_/id/2987869/jewell-loyd"
                            },
                            "..."
                          ]
                        }
                      }
                    ]
                  }
                ],
                "record": [
                  {
                    "id": "900",
                    "abbreviation": "Game",
                    "displayName": "Record Year To Date",
                    "shortDisplayName": "YTD",
                    "description": "Overall Record",
                    "type": "total",
                    "displayValue": "0-1"
                  }
                ]
              },
              {
                "id": "8",
                "type": "team",
                "order": 1,
                "homeAway": "away",
                "winner": true,
                "team": {
                  "id": "8",
                  "location": "Minnesota",
                  "abbreviation": "MIN",
                  "displayName": "Minnesota Lynx",
                  "shortDisplayName": "Lynx",
                  "logos": [
                    {
                      "href": "https://a.espncdn.com/i/teamlogos/wnba/500/min.png",
                      "width": 500,
                      "height": 500,
                      "alt": "",
                      "rel": [
                        "full",
                        "default"
                      ],
                      "lastUpdated": "2023-05-10T21:43Z"
                    },
                    {
                      "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/min.png",
                      "width": 500,
                      "height": 500,
                      "alt": "",
                      "rel": [
                        "full",
                        "dark"
                      ],
                      "lastUpdated": "2023-05-10T21:45Z"
                    }
                  ],
                  "links": [
                    {
                      "rel": [
                        "clubhouse",
                        "desktop",
                        "team"
                      ],
                      "href": "https://www.espn.com/wnba/team/_/name/min/minnesota-lynx",
                      "text": "Clubhouse"
                    },
                    {
                      "rel": [
                        "clubhouse",
                        "mobile",
                        "team"
                      ],
                      "href": "https://m.espn.com/wnba/clubhouse?teamId=8",
                      "text": "Clubhouse"
                    }
                  ]
                },
                "score": {
                  "value": 83,
                  "displayValue": "83"
                },
                "record": [
                  {
                    "id": "900",
                    "abbreviation": "Game",
                    "displayName": "Record Year To Date",
                    "shortDisplayName": "YTD",
                    "description": "Overall Record",
                    "type": "total",
                    "displayValue": "1-0"
                  }
                ]
              }
            ],
            "notes": [],
            "broadcasts": [
              {
                "type": {
                  "id": "4",
                  "shortName": "Streaming"
                },
                "market": {
                  "id": "1",
                  "type": "National"
                },
                "media": {
                  "shortName": "ESPN3"
                },
                "lang": "en",
                "region": "us"
              }
            ],
            "status": {
              "clock": 0,
              "displayClock": "0.0",
              "period": 4,
              "type": {
                "id": "3",
                "name": "STATUS_FINAL",
                "state": "post",
                "completed": true,
                "description": "Final",
                "detail": "Final",
                "shortDetail": "Final"
              }
            }
          }
        ],
        "links": [
          {
            "language": "en-US",
            "rel": [
              "summary",
              "desktop",
              "event"
            ],
            "href": "https://www.espn.com/wnba/game/_/gameId/401620221/lynx-storm",
            "text": "Gamecast",
            "shortText": "Summary",
            "isExternal": false,
            "isPremium": false
          },
          {
            "language": "en-US",
            "rel": [
              "summary",
              "sportscenter",
              "app",
              "..."
            ],
            "href": "sportscenter://x-callback-url/showGame?sportName=basketball&leagueAbbrev=wnba&gameId=401620221",
            "text": "Gamecast",
            "shortText": "Summary",
            "isExternal": false,
            "isPremium": false
          },
          {
            "language": "en-US",
            "rel": [
              "now",
              "desktop",
              "event"
            ],
            "href": "https://www.espn.com/wnba/game/_/gameId/401620221",
            "text": "Now",
            "shortText": "Now",
            "isExternal": false,
            "isPremium": false
          },
          "..."
        ]
      },
      "..."
    ]
  }
}
```



#### 19. **`GET /player-overview`**
-   **Description**: Fetches an overview of a specific player's career.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `playerId`  | string   | `-` | The unique identifier for the player.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/player-overview?playerId=4433403', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "player_overview": {
    "statistics": {
      "displayName": "Stats",
      "labels": [
        "GP",
        "MIN",
        "PTS",
        "..."
      ],
      "names": [
        "gamesPlayed",
        "avgMinutes",
        "avgPoints",
        "..."
      ],
      "displayNames": [
        "Games Played",
        "Minutes Per Game",
        "Points Per Game",
        "..."
      ],
      "splits": [
        {
          "displayName": "Regular Season",
          "stats": [
            "40",
            "35.4",
            "19.2",
            "..."
          ]
        },
        {
          "displayName": "Postseason",
          "stats": [
            "2",
            "38.0",
            "18.0",
            "..."
          ]
        },
        {
          "displayName": "Career",
          "stats": [
            "40",
            "35.4",
            "19.2",
            "..."
          ]
        }
      ]
    },
    "news": [
      {
        "headline": "Indiana fires coach Christie Sides; what's next for Fever?",
        "lastModified": "2024-10-27T18:49:42.000+00:00",
        "root": "wnba",
        "premium": false,
        "links": {
          "web": {
            "href": "https://www.espn.com/wnba/story/_/id/42034591/wnba-indiana-fever-fires-christie-sides-coaching-changes"
          }
        },
        "type": "Story",
        "section": "WNBA",
        "id": 42034591,
        "linkText": "Coach Christie Sides is out in Indiana; what's next for the Fever?",
        "metrics": [
          {
            "count": 0,
            "type": "views"
          },
          {
            "count": 0,
            "type": "fShares"
          },
          {
            "count": 0,
            "type": "tweets"
          },
          "..."
        ],
        "description": "Christie Sides, who led Indiana to its first WNBA playoffs since 2016, was fired Sunday. What are the Fever looking for in her successor?",
        "nowId": "1-42034591",
        "allowComments": true,
        "images": [
          {
            "width": 1296,
            "height": 729,
            "url": "https://a.espncdn.com/photo/2024/1027/r1406555_1296x729_16-9.jpg",
            "name": "Caitlin Clark and Christie Sides [1296x729]",
            "peers": [
              {
                "width": 1296,
                "height": 1296,
                "url": "https://a.espncdn.com/photo/2024/1027/r1406555_1296x1296_1-1.jpg",
                "name": "Caitlin Clark and Christie Sides [1296x1296]"
              },
              {
                "width": 1296,
                "height": 729,
                "url": "https://a.espncdn.com/photo/2024/1027/r1406555_1296x729_16-9.jpg",
                "name": "Caitlin Clark and Christie Sides [1296x729]"
              },
              {
                "width": 864,
                "height": 1296,
                "url": "https://a.espncdn.com/photo/2024/1027/r1406555_864x1296_2-3.jpg",
                "name": "Caitlin Clark and Christie Sides [864x1296]"
              },
              "..."
            ]
          },
          {
            "width": 576,
            "height": 324,
            "url": "https://a.espncdn.com/media/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.jpg",
            "name": "How Caitlin Clark paved her way as WNBA's Rookie of the Year",
            "caption": "Chiney Ogwumike looks back at Caitlin Clark's record-breaking season that led her to becoming the WNBA Rookie of the Year."
          }
        ],
        "published": "2024-10-27T18:49:46.000+00:00",
        "video": [
          {
            "source": "espn",
            "id": 41792946,
            "headline": "How Caitlin Clark paved her way as WNBA's Rookie of the Year",
            "title": "How Caitlin Clark paved her way as WNBA's Rookie of the Year",
            "caption": "Chiney Ogwumike looks back at Caitlin Clark's record-breaking season that led her to becoming the WNBA Rookie of the Year.",
            "description": "Chiney Ogwumike looks back at Caitlin Clark's record-breaking season that led her to becoming the WNBA Rookie of the Year.",
            "premium": false,
            "ad": {
              "sport": "wnba",
              "bundle": "wnba_top_plays_highlights"
            },
            "tracking": {
              "sportName": "wnba",
              "leagueName": "No League",
              "coverageType": "Highlight",
              "trackingName": "COM_WNBA Feature (How Caitlin Clark paved her way as WNBA's Rookie of the Year) 2024/10/14 ESHEET ENHL",
              "trackingId": "dm_241014_Caitlin_Clark_Rookie_of_the_Year"
            },
            "cerebroId": "670d50d0e929ad56b814594f",
            "lastModified": "2024-10-14T17:24:59.000+00:00",
            "originalPublishDate": "2024-10-14T17:07:05.000+00:00",
            "timeRestrictions": {
              "embargoDate": "2024-10-14T17:07:05.000+00:00",
              "expirationDate": "2024-11-30T18:07:05.000+00:00"
            },
            "deviceRestrictions": {
              "type": "whitelist",
              "devices": [
                "desktop",
                "ipad",
                "settop",
                "..."
              ]
            },
            "geoRestrictions": {
              "type": "whitelist",
              "countries": [
                "BJ",
                "PY",
                "RE",
                "..."
              ]
            },
            "syndicatable": true,
            "duration": 115,
            "categories": [
              {
                "id": 9579,
                "uid": "s:40~l:59",
                "description": "WNBA",
                "type": "league",
                "sportId": 59,
                "leagueId": 59,
                "league": {
                  "id": 59,
                  "links": {
                    "web": {},
                    "mobile": {},
                    "api": {}
                  }
                }
              },
              {
                "id": 145735,
                "description": "espnw - sports",
                "type": "topic",
                "sportId": 0
              },
              {
                "id": 557855,
                "uid": "s:40~l:59~a:4433403",
                "description": "Clark, Caitlin",
                "type": "athlete",
                "sportId": 59,
                "athleteId": 4433403,
                "athlete": {
                  "id": 4433403,
                  "links": {
                    "web": {
                      "athletes": {
                        "href": "https://www.espn.com/wnba/player/_/id/4433403/caitlin-clark"
                      }
                    },
                    "mobile": {
                      "athletes": {
                        "href": "http://m.espn.com/wnba/playercard?playerId=4433403"
                      }
                    },
                    "api": {
                      "athletes": {
                        "href": "http://now.core.api.espn.com/v1/sports/basketball/wnba/athletes/4433403"
                      }
                    }
                  }
                }
              },
              "..."
            ],
            "posterImages": {
              "square": {
                "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_1x1.jpg"
              },
              "default": {
                "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_default.jpg",
                "width": 576,
                "height": 324
              },
              "wide": {
                "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_5x2.jpg"
              },
              "full": {
                "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.jpg"
              }
            },
            "images": [
              {
                "width": 576,
                "height": 324,
                "url": "https://media.video-cdn.espn.com/images/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.jpg",
                "name": "Poster Image"
              }
            ],
            "thumbnail": "https://a.espncdn.com/media/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.jpg",
            "links": {
              "web": {
                "href": "http://espn.com/video/clip?id=41792946",
                "self": {
                  "href": "http://espn.com/video/clip?id=41792946"
                }
              },
              "mobile": {
                "href": "https://watch.auth.api.espn.com/video/auth/brightcove/009c8d35-935b-4cba-99a1-81f164751d2b/asset?UMADPARAMreferer=https://www.espn.com/video/clip?id=41792946",
                "alert": {
                  "href": "http://m.espn.com/general/video/videoAlert?vid=41792946"
                },
                "progressiveDownload": {
                  "href": "https://watch.auth.api.espn.com/video/auth/brightcove/009c8d35-935b-4cba-99a1-81f164751d2b/asset?UMADPARAMreferer=https://www.espn.com/video/clip?id=41792946"
                },
                "source": {
                  "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.mp4"
                },
                "streaming": {
                  "href": "https://watch.auth.api.espn.com/video/auth/brightcove/009c8d35-935b-4cba-99a1-81f164751d2b/asset?UMADPARAMreferer=https://www.espn.com/video/clip?id=41792946"
                }
              },
              "api": {
                "artwork": {
                  "href": "https://artwork.api.espn.com/artwork/collections/media/009c8d35-935b-4cba-99a1-81f164751d2b"
                },
                "self": {
                  "href": "http://api-app.espn.com/v1/video/clips/41792946"
                }
              },
              "source": {
                "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_360p30_1464k.mp4",
                "flash": {
                  "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.smil"
                },
                "full": {
                  "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_360p30_1464k.mp4"
                },
                "hds": {
                  "href": "https://hds.video-cdn.espn.com/z/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_rel.smil/manifest.f4m"
                },
                "mezzanine": {
                  "href": "http://media.video-origin.espn.com/espnvideo/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year.mp4"
                },
                "HD": {
                  "href": "https://media.video-cdn.espn.com/motion/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year_720p30_2896k.mp4"
                },
                "HLS": {
                  "href": "https://service-pkgespn.akamaized.net/opp/hls/espn/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year/playlist.m3u8",
                  "HD": {
                    "href": "https://service-pkgespn.akamaized.net/opp/hls/espn/2024/1014/dm_241014_Caitlin_Clark_Rookie_of_the_Year/dm_241014_Caitlin_Clark_Rookie_of_the_Year/playlist.m3u8"
                  }
                }
              }
            }
          }
        ],
        "byline": "Michael Voepel, Kevin Pelton, Alexa Philippou",
        "source": "ESPN",
        "dataSourceIdentifier": "6301d69684274"
      },
      "..."
    ],
    "..."
  }
}
```



#### 20. **`GET /player-advanced-stats`**
-   **Description**: Fetches advanced statistics for a specific player.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `playerId`  | string   | `-` | The unique identifier for the player.   | Yes       |
| `type`  | string   | `-` | The type of statistics (`wnba` or `ncaa`).   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/player-advanced-stats?playerId=4433403', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "player_stats": {
    "teams": {
      "indiana-fever": {
        "id": "5",
        "uid": "s:40~l:59~t:5",
        "guid": "bfef1bdd-c2d1-310d-dd9f-645b90575da9",
        "slug": "indiana-fever",
        "location": "Indiana",
        "name": "Fever",
        "abbreviation": "IND",
        "displayName": "Indiana Fever",
        "shortDisplayName": "Fever",
        "color": "002d62",
        "alternateColor": "e03a3e",
        "isActive": true,
        "isAllStar": false,
        "logos": [
          {
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500/ind.png",
            "width": 500,
            "height": 500,
            "rel": [
              "full",
              "default"
            ]
          },
          {
            "href": "https://a.espncdn.com/i/teamlogos/wnba/500-dark/ind.png",
            "width": 500,
            "height": 500,
            "rel": [
              "full",
              "dark"
            ]
          }
        ],
        "links": [
          {
            "language": "en-US",
            "rel": [
              "clubhouse",
              "desktop",
              "team"
            ],
            "href": "https://www.espn.com/wnba/team/_/name/ind/indiana-fever",
            "text": "Clubhouse",
            "shortText": "Clubhouse",
            "isExternal": false,
            "isPremium": false
          },
          {
            "language": "en-US",
            "rel": [
              "clubhouse",
              "mobile",
              "team"
            ],
            "href": "https://m.espn.com/wnba/clubhouse?teamId=5",
            "text": "Clubhouse",
            "shortText": "Clubhouse",
            "isExternal": false,
            "isPremium": false
          },
          {
            "language": "en-US",
            "rel": [
              "roster",
              "desktop",
              "team"
            ],
            "href": "https://www.espn.com/wnba/team/roster/_/name/ind/indiana-fever",
            "text": "Roster",
            "shortText": "Roster",
            "isExternal": false,
            "isPremium": false
          },
          "..."
        ],
        "groups": {},
        "venue": {
          "id": "2183",
          "fullName": "Gainbridge Fieldhouse",
          "address": {
            "city": "Indianapolis",
            "state": "IN"
          },
          "grass": false,
          "indoor": true,
          "images": [
            {
              "href": "https://a.espncdn.com/i/venues/wnba/day/2183.jpg",
              "width": 2000,
              "height": 1125,
              "rel": [
                "full",
                "day"
              ]
            }
          ]
        },
        "record": {},
        "athletes": {},
        "ranks": {},
        "franchise": {}
      }
    },
    "glossary": [
      {
        "abbreviation": "3P%",
        "displayName": "3-Point Field Goal Percentage"
      },
      {
        "abbreviation": "3PT",
        "displayName": "3-Point Field Goals Made-Attempted Per Game"
      },
      {
        "abbreviation": "AST",
        "displayName": "Assists Per Game"
      },
      "..."
    ],
    "categories": [
      {
        "name": "averages",
        "displayName": "Regular Season Averages",
        "labels": [
          "GP",
          "GS",
          "MIN",
          "..."
        ],
        "names": [
          "gamesPlayed",
          "gamesStarted",
          "avgMinutes",
          "..."
        ],
        "displayNames": [
          "Games Played",
          "Games Started",
          "Minutes Per Game",
          "..."
        ],
        "descriptions": [
          "Games Played",
          "The number of games started by an athlete.",
          "The average number of minutes per game.",
          "..."
        ],
        "statistics": [
          {
            "teamId": "5",
            "teamSlug": "indiana-fever",
            "season": {
              "year": 2024,
              "displayName": "2024"
            },
            "stats": [
              "40",
              "40",
              "35.4",
              "..."
            ],
            "position": "G"
          }
        ],
        "totals": [
          "40",
          "40",
          "35.4",
          "..."
        ],
        "sortKey": "averages"
      },
      {
        "name": "totals",
        "displayName": "Regular Season Totals",
        "labels": [
          "PTS",
          "OR",
          "DR",
          "..."
        ],
        "names": [
          "points",
          "offensiveRebounds",
          "defensiveRebounds",
          "..."
        ],
        "displayNames": [
          "Points",
          "Offensive Rebounds",
          "Defensive Rebounds",
          "..."
        ],
        "descriptions": [
          "The number of points scored.",
          "The number of times when the offense obtains the possession of the ball after a missed shot.",
          "The number of times when the defense obtains the possession of the ball after a missed shot by the offense.",
          "..."
        ],
        "statistics": [
          {
            "teamId": "5",
            "teamSlug": "indiana-fever",
            "season": {
              "year": 2024,
              "displayName": "2024"
            },
            "stats": [
              "769",
              "14",
              "213",
              "..."
            ],
            "position": "G"
          }
        ],
        "totals": [
          "769",
          "14",
          "213",
          "..."
        ],
        "sortKey": "totals"
      },
      {
        "name": "miscellaneous",
        "displayName": "Regular Season Misc Totals",
        "labels": [
          "DD2",
          "TD3",
          "AST/TO",
          "..."
        ],
        "names": [
          "doubleDouble",
          "tripleDouble",
          "assistTurnoverRatio",
          "..."
        ],
        "displayNames": [
          "Double Double",
          "Triple Double",
          "Assist To Turnover Ratio",
          "..."
        ],
        "descriptions": [
          "The number of times double digit values were accumulated in 2 of the following categories: points, rebounds, assists, steals, and blocked shots",
          "The number of times double digit values were accumulated in 3 of the following categories: points, rebounds, assists, steals, and blocked shots",
          "The average number of assists a player or team records per turnover",
          "..."
        ],
        "statistics": [
          {
            "teamId": "5",
            "teamSlug": "indiana-fever",
            "season": {
              "year": 2024,
              "displayName": "2024"
            },
            "stats": [
              "14",
              "2",
              "1.5",
              "..."
            ],
            "position": "G"
          }
        ],
        "totals": [
          "14",
          "2",
          "1.5",
          "..."
        ],
        "sortKey": "miscellaneous"
      }
    ]
  }
}
```



#### 21. **`GET /player-gamelog`**
-   **Description**: Retrieves the game log for a specific WNBA or NCAA player for a given year.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `playerId`  | string   | `-` | The unique identifier for the player.   | Yes       |
| `type`  | string   | `-` | The type of statistics (`wnba` or `ncaa`).   | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/player-gamelog?playerId=4433403', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "player_gamelog": {
    "labels": [
      "MIN",
      "PTS",
      "REB",
      "..."
    ],
    "names": [
      "minutes",
      "points",
      "totalRebounds",
      "..."
    ],
    "displayNames": [
      "Minutes",
      "Points",
      "Rebounds",
      "..."
    ],
    ".."
  }
}
```



#### 22. **`GET /player/bio`**
-   **Description**: Retrieves the biography and detailed information for a specific WNBA player.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `playerId`  | string   | `-` | The unique identifier for the player.   | Yes       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/player/bio?playerId=2988756', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": {
    "awards": [
      {
        "id": "245",
        "league": "wnba",
        "name": "All-Defensive 1st Team",
        "displayCount": "2x",
        "seasons": [
          "2023",
          "2021"
        ]
      },
      {
        "id": "246",
        "league": "wnba",
        "name": "All-Defensive 2nd Team",
        "displayCount": "2x",
        "seasons": [
          "2022",
          "2020"
        ]
      },
      {
        "id": "248",
        "league": "wnba",
        "name": "All-Rookie Team",
        "displayCount": "1x",
        "seasons": [
          "2017"
        ]
      }
    ],
    "teamHistory": [
      {
        "id": "16",
        "uid": "s:40~l:59~t:16",
        "slug": "washington-mystics",
        "displayName": "Washington Mystics",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/wsh.png",
        "seasons": "2023-CURRENT",
        "links": [
          "https://www.espn.com/wnba/team/_/name/wsh/washington-mystics",
          "https://m.espn.com/wnba/clubhouse?teamId=16",
          "https://www.espn.com/wnba/team/roster/_/name/wsh/washington-mystics",
          "..."
        ],
        "seasonCount": "2",
        "isActive": true
      },
      {
        "id": "6",
        "uid": "s:40~l:59~t:6",
        "slug": "los-angeles-sparks",
        "displayName": "Los Angeles Sparks",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/la.png",
        "seasons": "2020-2022",
        "links": [
          "https://www.espn.com/wnba/team/_/name/la/los-angeles-sparks",
          "https://m.espn.com/wnba/clubhouse?teamId=6",
          "https://www.espn.com/wnba/team/roster/_/name/la/los-angeles-sparks",
          "..."
        ],
        "seasonCount": "3",
        "isActive": true
      },
      {
        "id": "20",
        "uid": "s:40~l:59~t:20",
        "slug": "atlanta-dream",
        "displayName": "Atlanta Dream",
        "logo": "https://a.espncdn.com/i/teamlogos/wnba/500/atl.png",
        "seasons": "2017-2019",
        "links": [
          "https://www.espn.com/wnba/team/_/name/atl/atlanta-dream",
          "https://m.espn.com/wnba/clubhouse?teamId=20",
          "https://www.espn.com/wnba/team/roster/_/name/atl/atlanta-dream",
          "..."
        ],
        "seasonCount": "3",
        "isActive": true
      }
    ]
  }
}
```



#### 23. **`GET /player/splits`**
-   **Description**: Retrieves the statistical splits for a specific WNBA player, categorized by the specified type.

-   **Parameters**:

| Parameter   | Type   | Default              | Description                              | Required |
|-------------|--------|----------------------|------------------------------------------|----------|
| `playerId`  | string | `-`                  | The unique identifier for the player.   | Yes      |
| `year`      | string | `2024`               | The year for the statistics.             | No       |
| `category`   | string | `perGame`            | The category of stats, with accepted values: `perGame`, `total`, `per48`. | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/player/splits?playerId=2988756&year=2024&category=perGame', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": {
    "filters": [
      {
        "displayName": "League",
        "name": "league",
        "value": "wnba",
        "options": [
          {
            "value": "wnba",
            "displayValue": "Women's National Basketball Association",
            "shortDisplayName": "WNBA"
          },
          {
            "value": "womens-college-basketball",
            "displayValue": "NCAA Women's Basketball",
            "shortDisplayName": "NCAAW"
          }
        ]
      },
      {
        "displayName": "Season",
        "name": "season",
        "value": "2024",
        "options": [
          {
            "value": "2024",
            "displayValue": "2024"
          },
          {
            "value": "2023",
            "displayValue": "2023"
          },
          {
            "value": "2022",
            "displayValue": "2022"
          },
          "..."
        ]
      },
      {
        "displayName": "Category",
        "name": "category",
        "value": "perGame",
        "options": [
          {
            "value": "perGame",
            "displayValue": "Per Game"
          },
          {
            "value": "total",
            "displayValue": "Total"
          },
          {
            "value": "per48",
            "displayValue": "Per 48 Minutes"
          }
        ]
      }
    ],
    "displayName": "2024 Splits",
    "labels": [
      "GP",
      "MIN",
      "FG",
      "..."
    ],
    "names": [
      "gamesPlayed",
      "avgMinutes",
      "avgFieldGoalsMade-avgFieldGoalsAttempted",
      "..."
    ],
    "displayNames": [
      "Games Played",
      "Minutes Per Game",
      "Field Goals Made-Attempted Per Game",
      "..."
    ],
    "descriptions": [
      "Games Played",
      "The average number of minutes per game.",
      "avgFieldGoalsMade-avgFieldGoalsAttempted",
      "..."
    ],
    "splitCategories": [
      {
        "name": "split",
        "displayName": "split",
        "splits": [
          {
            "displayName": "All Splits",
            "stats": [
              "18",
              "23.3",
              "4.5-11.1",
              "..."
            ],
            "abbreviation": "Total"
          }
        ]
      },
      {
        "name": "byMonth",
        "displayName": "Month"
      },
      {
        "name": "byResult",
        "displayName": "Result"
      },
      "..."
    ]
  }
}
```



#### 24. **`GET /team/transactions`**
-   **Description**: Retrieves the list of transactions (e.g., trades, signings) for a specific WNBA team in a given year.

-   **Parameters**:

| Parameter  | Type   | Default              | Description                              | Required |
|------------|--------|----------------------|------------------------------------------|----------|
| `teamId`   | string | `-`                  | The unique identifier for the team.     | Yes      |
| `year`     | string | `2024`               | The year of the transactions.            | No       |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team/transactions?teamId=14', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": {
    "transactions": {
      "2024-08": [
        {
          "date": "2024-08-15T07:00Z",
          "description": "Released G Kiana Williams."
        },
        {
          "date": "2024-08-13T07:00Z",
          "description": "Released G Kiana Williams."
        }
      ],
      "2024-07": [
        {
          "date": "2024-07-09T07:00Z",
          "description": "Signed G Kiana Williams to a seven-day contract."
        },
        {
          "date": "2024-07-07T07:00Z",
          "description": "Released G Kiana Williams."
        }
      ],
      "2024-06": [
        {
          "date": "2024-06-30T07:00Z",
          "description": "Signed G Kiana Williams to a seven-day hardship contract."
        },
        {
          "date": "2024-06-27T07:00Z",
          "description": "Waived G Kiana Williams."
        }
      ],
      "2024-05": [
        {
          "date": "2024-05-30T07:00Z",
          "description": "Signed F/C Ezi Magbegor to a contract extension."
        },
        {
          "date": "2024-05-26T07:00Z",
          "description": "Waived F Dulcy Fankam Mendjiadeu."
        },
        {
          "date": "2024-05-08T07:00Z",
          "description": "Waived F Joyner Holmes."
        },
        "..."
      ],
      "2024-04": [
        {
          "date": "2024-04-17T07:00Z",
          "description": "Signed G Nika Mühl to a rookie scale contract. Signed F Quay Miller to a training camp contract."
        }
      ],
      "2024-01": [
        {
          "date": "2024-01-27T08:00Z",
          "description": "Signed G Skylar Diggins-Smith to a contract."
        }
      ]
    }
  }
}
```



#### 25. **`GET /team/injuries`**
-   **Description**: Retrieves the list of injuries for players on a specific WNBA team.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamId`   | string | `-`                  | The unique identifier for the team.     | Yes      |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team/injuries?teamId=16', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": {
    "injuries": [
      {
        "date": "Sep 18",
        "items": [
          {
            "type": {
              "id": "4",
              "name": "INJURY_STATUS_OUT",
              "description": "out",
              "abbreviation": "O"
            },
            "athlete": {
              "shortName": "A. Edwards",
              "name": "Aaliyah Edwards",
              "url": "https://www.espn.com/wnba/player/_/id/4433408/aaliyah-edwards",
              "uid": "",
              "logo": "https://a.espncdn.com/i/headshots/wnba/players/full/4433408.png",
              "position": "F"
            },
            "status": "injury-4",
            "description": ""
          }
        ]
      },
      {
        "date": "Sep 15",
        "items": [
          {
            "type": {
              "id": "4",
              "name": "INJURY_STATUS_OUT",
              "description": "out",
              "abbreviation": "O"
            },
            "athlete": {
              "shortName": "S. Austin",
              "name": "Shakira Austin",
              "url": "https://www.espn.com/wnba/player/_/id/4398911/shakira-austin",
              "uid": "",
              "logo": "https://a.espncdn.com/i/headshots/wnba/players/full/4398911.png",
              "position": "C"
            },
            "status": "injury-4",
            "description": "Coach Eric Thibault said Sunday that Austin will be shut down for the remainder of the season due to an ankle injury, Tyler Byrum of Monumental Sports Network reports."
          }
        ]
      }
    ],
    "injuriesNews": [
      {
        "headline": "Geelong United's Jaz Shelley speaks on WNBL launch",
        "writer": "",
        "description": "Ahead of their debut appearance in the WNBL, Geelong United's Jaz Shelley speaks to ESPN's Megan Hustwaite about her journey to the team.",
        "image": "https://a.espncdn.com/combiner/i?img=/media/motion/2024/1028/dm_241028_NBL_Interview_Geelong_Uniteds_Jaz_Shelley_speaks_on_WNBL_launch_20241028/dm_241028_NBL_Interview_Geelong_Uniteds_Jaz_Shelley_speaks_on_WNBL_launch_20241028.jpg&h=120",
        "premium": false,
        "published": "2024-10-29T00:01:04Z",
        "logoSrc": "https://a.espncdn.com/redesign/assets/img/logos/espnplus/espnplus-2x.png",
        "images": [
          "https://a.espncdn.com/combiner/i?img=/media/motion/2024/1028/dm_241028_NBL_Interview_Geelong_Uniteds_Jaz_Shelley_speaks_on_WNBL_launch_20241028/dm_241028_NBL_Interview_Geelong_Uniteds_Jaz_Shelley_speaks_on_WNBL_launch_20241028.jpg&h=120"
        ],
        "link": "https://www.espn.com/video/clip/_/id/42046166"
      },
      {
        "headline": "Source: WNBA doesn't fine Minnesota Lynx coach Cheryl Reeve",
        "writer": "Alexa Philippou",
        "description": "A week after the season ended, the WNBA chose not to fine Minnesota Lynx coach Cheryl Reeve after her criticism of the officiating from the winner-take-all Game 5 of the WNBA Finals against the New York Liberty, a league source told ESPN.",
        "image": "https://a.espncdn.com/combiner/i?img=/photo/2024/1028/r1407322_600x600_1-1.jpg&h=120",
        "premium": false,
        "published": "2024-10-29T00:54:59Z",
        "logoSrc": "https://a.espncdn.com/redesign/assets/img/logos/espnplus/espnplus-2x.png",
        "images": [
          "https://a.espncdn.com/combiner/i?img=/photo/2024/1028/r1407322_600x600_1-1.jpg&h=120"
        ],
        "link": "https://www.espn.com/wnba/story/_/id/42060315/wnba-fine-minnesota-lynx-coach-cheryl-reeve"
      },
      {
        "headline": "WNBA coaching changes for 2025: Sun, White part ways",
        "writer": "ESPN",
        "description": "Connecticut and Stephanie White parted ways Monday, leaving seven head-coaching positions open in the WNBA.",
        "image": "https://a.espncdn.com/combiner/i?img=/photo/2024/1017/r1401836_1296x729_16-9.jpg&h=120",
        "premium": false,
        "published": "2024-10-29T02:13:17Z",
        "logoSrc": "https://a.espncdn.com/redesign/assets/img/logos/espnplus/espnplus-2x.png",
        "images": [
          "https://a.espncdn.com/combiner/i?img=/photo/2024/1017/r1401836_1296x729_16-9.jpg&h=120"
        ],
        "link": "https://www.espn.com/wnba/story/_/id/42033470/wnba-coaching-changes-tracker-carousel-hires-2025-season"
      }
    ]
  }
}
```

#### 26. **`GET /team/depth`**
-   **Description**: Retrieves the depth chart for a specific WNBA team, detailing the hierarchy of players by position.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `teamId`   | string | `-`                  | The unique identifier for the team.     | Yes      |

Example request:
```javascript
fetch('https://wnba-api.p.rapidapi.com/team/depth?teamId=14', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'wnba-api.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "data": {
    "dethTeamGroups": {},
    "glossary": {
      "glossaryData": false,
      "glossaryInjurie": [],
      "glossaryFooter": "Powered by RotoWire"
    },
    "deptTable": {}
  }
}
```

## Error Handling
The  API returns standard HTTP status codes to indicate the success or failure of API requests. Below are common errors and suggestions for handling them.

|Status Code|Message|Description|Suggested Handling|
|--|--|--|--|
| **400** | Bad Request | The request was malformed or missing required parameters (e.g., `domain` parameter not provided). | Verify that all required parameters are included and correctly formatted. |
| **401** | Unauthorized | Invalid or missing API key in the request headers. | Check that a valid API key is included in `x-rapidapi-key`. |
| **403** | Forbidden | Access to the requested resource is denied, possibly due to rate limits or restricted access. | Review rate limits and ensure API permissions. Retry after a delay if rate limit exceeded. |
| **404** | Not Found | The requested domain information could not be found (e.g., domain does not exist). | Check the spelling or availability of the domain. |
| **429** | Too Many Requests | The API rate limit has been exceeded. | Implement rate-limiting logic and retry after the specified rate limit reset time. |
| **500** | Internal Server Error | A server error occurred while processing the request. | Retry the request after a few seconds. If the error persists, contact API support. |
| **503** | Service Unavailable | The API service is temporarily unavailable (e.g., due to maintenance). | Retry the request later or check the API status page for maintenance alerts. |
