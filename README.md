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
