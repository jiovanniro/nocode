# TN Plan Backend 

###Getting Started 
 1. `npm install`
 2. `npm run dev`.

###Goals 

    ####Create 

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

    ####Get

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

    ####Update 

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

    ####Delete 

    /api/goals/id

    ```
    this.http.delete('/api/goals/id');
    ```


###Assets

    ####Create 

    /api/goals/

    Example of http request to create an asset
    ```
    this.http.post('/api/assets/', JSON.stringify(asset), {
      headers: new HttpHeaders({
        'Content-Type': 'application/json'
      })
    });
    ```

    **asset** is expected to be an object with the following properties:  

    ```
    {
        "user_id": "a693a1d3-53da-4ac7-9ac3-c4f91a4a7089", 
        "category_id": "6eb32914-8ad4-4f14-a243-b15af54cd682", 
        "assets": [
            "Cumberland Gap",
            "National Historic Site",
            "Powell River"
        ]
    }
    ```

    ####Get

    /api/assets/

    Example of http request to get assets
    ```
    this.http.get('/api/assets/');
    ```

    /api/assets/id

    Example of http request to get a goal
    ```
    this.http.get('/api/goal/id');
    ```

    The returned data will be an array of object(s). Each object representing a asset, and associated asset category.

    ####Update 

    /api/assets/id

    Example of http request to update a asset
    ```
    this.http.patch('/api/asset/id', JSON.stringify(goal), {
      headers: new HttpHeaders({
        'Content-Type': 'application/json'
      })
    });
    ```

    **asset** is expected to be an object with the following properties:  

    ```
    {
        "category_id": "e8c13a02-ce79-487d-8ccc-1f68fb5ec96c", 
        "asset": "Norris Lake"
    }
    ```

    ####Delete 

    /api/assets/id

    ```
    this.http.delete('/api/assets/id');
    ```


###Votes

    ####Update 

    /api/votes/id

    Example of http request to update a vote
    ```
    this.http.patch('/api/asset/id', JSON.stringify(vote), {
      headers: new HttpHeaders({
        'Content-Type': 'application/json'
      })
    });
    ```

    **vote** is expected to be an object with the following properties:  

    ```
    {
        "user_id": "eccf8dad-2020-4194-9acd-e9e9420ddb4f", 
        "vote": 1
    }
    ```
