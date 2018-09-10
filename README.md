# TN Plan Backend 

## Getting Started
 1. `npm install`
 2. `npm run dev`.

## Goals 

Create 

    /api/goals/

    Example of http request to create a goal
    ```
    this.http.post('/api/goals/', JSON.stringify(goal), {
      headers: new HttpHeaders({
        'Content-Type': 'application/json'
      })
    });
    ```

    **goal** is expected to be an object with the following properties:  

    ```
    {
        "user_id": "a693a1d3-53da-4ac7-9ac3-c4f91a4a7089", 
        "longtermgoal": "Album of the year", 
        "vote": 0,
        "shorttermgoals": [
            {"goal": "short-term 1", "completed": 0},
            {"goal": "short-term 2", "completed": 0},
            {"goal": "short-term 3", "completed": 0}
        ]
    }
    ```
