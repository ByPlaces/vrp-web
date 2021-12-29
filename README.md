# vrp-web

Experimental [vrp](https://github.com/reinterpretcat/vrp) web server

## Example problem

```json
{
  "plan": {
    "jobs": [
      {
        "id": "job1",
        "deliveries": [
          {
            "places": [
              {
                "location": {
                  "lat": 52.52599,
                  "lng": 13.45413
                },
                "duration": 300.0,
                "times": [
                  [
                    "2019-07-04T09:00:00Z",
                    "2019-07-04T18:00:00Z"
                  ],
                  [
                    "2019-07-05T09:00:00Z",
                    "2019-07-05T18:00:00Z"
                  ]
                ]
              }
            ],
            "demand": [
              1
            ]
          }
        ]
      },
      {
        "id": "job2",
        "pickups": [
          {
            "places": [
              {
                "location": {
                  "lat": 52.5225,
                  "lng": 13.4095
                },
                "duration": 240.0,
                "times": [
                  [
                    "2019-07-04T10:00:00Z",
                    "2019-07-04T16:00:00Z"
                  ]
                ]
              }
            ],
            "demand": [
              1
            ]
          }
        ]
      },
      {
        "id": "job3",
        "pickups": [
          {
            "places": [
              {
                "location": {
                  "lat": 52.5225,
                  "lng": 13.4095
                },
                "duration": 300.0,
                "tag": "p1"
              }
            ],
            "demand": [
              1
            ]
          }
        ],
        "deliveries": [
          {
            "places": [
              {
                "location": {
                  "lat": 52.5165,
                  "lng": 13.3808
                },
                "duration": 300.0,
                "tag": "d1"
              }
            ],
            "demand": [
              1
            ]
          }
        ]
      }
    ]
  },
  "fleet": {
    "vehicles": [
      {
        "typeId": "vehicle",
        "vehicleIds": [
          "vehicle_1"
        ],
        "profile": {
          "matrix": "normal_car"
        },
        "costs": {
          "fixed": 22.0,
          "distance": 0.0002,
          "time": 0.004806
        },
        "shifts": [
          {
            "start": {
              "earliest": "2019-07-04T09:00:00Z",
              "location": {
                "lat": 52.5316,
                "lng": 13.3884
              }
            },
            "end": {
              "latest": "2019-07-04T18:00:00Z",
              "location": {
                "lat": 52.5316,
                "lng": 13.3884
              }
            }
          }
        ],
        "capacity": [
          10
        ]
      }
    ],
    "profiles": [
      {
        "name": "normal_car"
      }
    ]
  }
}
```
