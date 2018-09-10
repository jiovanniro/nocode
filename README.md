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

Get

    /api/goals/

    Example of http request to get goals
    ```
    this.http.get('/api/goals/');
    ```

    /api/goals/id

    Example of http request to get a goal
    ```
    this.http.get('/api/goal/id');
    ```

    The returned data will be an array of objects. Each object representing a long-term goal, vote total, and associated short-term goals.

Update 

    /api/goals/id

    Example of http request to update a goal
    ```
    this.http.patch('/api/goals/id', JSON.stringify(goal), {
      headers: new HttpHeaders({
        'Content-Type': 'application/json'
      })
    });
    ```

    **goal** is expected to be an object with the following properties:  

    ```
    {
        "longtermgoal": {"id": "id", "goal": "a new goal"}, 
        "shorttermgoals": [
            {"id": "id", "goal": "short-term 1"},
            {"id": "id", "goal": "short-term 2"},
            {"id": "id", "goal": "short-term 3"},
        ]
    }
    ```

Delete 

    /api/goals/id

    ```
    this.http.delete('/api/goals/id');
    ```
