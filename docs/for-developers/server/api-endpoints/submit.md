# My Friend Morgan
# **/submit**

API endpoints for /submit

## **POST /submit/survey-response**
Writes survey to the DB

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

### Sample Response
```
[
    {
        "_id": "643d692a98d5e1de084917fd",
        "firstName": "Carol",
        "lastName": "Folt",
        "sessionId": "123",
        "building": "Fertitta Hall",
        "room": "JFF Room A",
        "surveyData": {
            1: {
            lifetime: boolean,
            recently: boolean
            }
            .
            .
            .
            17: {
                lifetime: boolean,
                recently: boolean
            }
        }
    },
]
```
## **POST /submit/individual-response**
Writes individual case scenario response to the DB

### Parameters
- first - Professor’s first name
- last - Professor’s last name
- sessionID - Session's ID
- building - Building name
- room - Room name
- recommendation - Do they recommend Morgan?
- reason - Reason for recommending Morgan
- gender - What gender they thought Morgan was
- genderReason - What factor most heavily impacted their choice

## **POST /submit/group-response**
Writes group case scenario response to the DB

### Parameters
- first - Professor’s first name
- last - Professor’s last name
- sessionID - Session's ID
- building - Building name
- room - Room name
- recommendation - Do they recommend Morgan?
- reason - Reason for recommending Morgan
- gender - What gender they thought Morgan was
- genderReason - What factor most heavily impacted their choice

## **GET /submit/events**
Listens for events emitted by other GET/POST requests (e.g., `POST /submit/survey-response` emits a `survey-response event`). Used to display information on the administrator's Activity Dashboard regarding the number of submitted surveys/ individual responses/ group responses.

### Server side events:
- `survey-response`
    - When the `survey-response` event is caught by the `GET /submit/events` request, the `startSurveyResponseListener()` function is triggered and updates the Activity Dashboard (occurs every time a student submits a survey).
- `individual-response`
    - When the `individual-response` event is caught by the `GET /submit/events` request, the `startIndividualResponseListener()` function is triggered and updates the Activity Dashboard (occurs every time a student submits an individual response).
- `group-response`
    - When the `group-response` event is caught by the `GET /submit/events` request, the `startGroupResponseListener()` function is triggered and updates the Activity Dashboard (occurs every time students in a shared ELC room submit a group response).