# My Friend Morgan
# **Page Breakdown**

## Admin Pages
- **AdminBackground.js** : Background template for admin pages. Can be called from other pages so the background are all constant.
- **AdminFlowNo5.js** : This page shows the link to the survey on the screen.
- **AdminGenerateCase.js** : This page only has the button "Generate Case Scenario" that the admin can click to show the case scenario on all the rooms. 
- **AdminGroupsResponded.js** : Has the activity dashboard that shows which rooms has submitted their response to the question "Do you recommend Morgan?" and has "Generate Results" button.
    - Admin can click on the "Generate Results" button once it shows that all the rooms have submitted their responses.
- **AdminIndividualsResponded.js** : Has the activity dashboard that shows the number of students that has submitted their response to the question "Do you recommend Morgan?" based on room and has "Start Group Response" button.
    - Admin can click on the "Start Group Response" button once it shows that all the students have submitted their responses.
- **AdminRoomSelectPage.js** : The admin can choose which building the class is in. Admin can also select which rooms are to be used for the session, if class is in JFF or JKP, and how many breakout rooms are opened, if class is in Zoom.
- **AdminSessionsPage.js** : This page shows the sessions the admin has in the database, as well as allows them to add or delete sessions.
    - If the admin’s name entered in the page before is found in the database, it will automatically populate the sessions with getSessionsAPI().
    - If the admin’s name entered in the page before is not found in the database, the admin can then create new sessions with createSessionAPI() and delete sessions with deleteSessionAPI().
- **AdminSignInPage.js** : The admin, usually the professor, can sign in. They can enter their first and last name.
- **AdminStartSurvey.js**: This page only has the button "Start Survey" that the admin can click to start the survey for all of the students.
- **AdminSurveysSubmitted.js** : Has the activity dashboard that shows the number of students that has submitted the survey based on room and has "Generate Case Scenario" button.
    - Admin can click on the "Generate Case Scenario" button once it shows that all the students have submitted their surveys.
- **GroupResults.js** : Shows a bar chart of the room responses to the question "Do you recommend Morgan?"
    - How many rooms responded "Yes" and how many responded "No."
- **GroupResultsBreakdown.js** : A full breakdown on the submitted results of the students based on each room.
    - Includes Morgan's Behavior, Individual Responses ("Recommended Morgan," "Morgan is...," and "__impacted my choice"), and Group Responses.
- **IndividualResults.js** : Shows a bar chart of the student responses to the question "Do you recommend Morgan?"
    - How many responded "Yes" and how many responded "No."

## Student Pages
- **StudentSignIn.js** : Starting page for students taking the survey/case inside the ELC where they sign-in with the building and room that they are in
    - Buildings and rooms are automatically populated with the getAvailableRoomsAPI() in useEffect()
- **Survey.js** : Survey Page that asks students to check their behaviors in the past year or in their lifetime. It can be accessed directly if the students are not taking in the ELC or accessed from the StudentSignIn page. 
    - Each question is sectioned into a SurveyRow component-to add or edit a question, pass in the question as props as a string. 
- **Case Scenario.js** : This page shows the generated case scenario for their room and ask corresponding questions for the students to answer. 

## Room Pages
- **RoomCaseScenario.js** : Shows only the whole case scenario on the page.
- **RoomCaseScenario2.js** : Shows both the case scenario and the case scenario questions on the page.
- **RoomSignIn.js** : Room sign-in page where room host can select which specific building and room they are in.
    - Buildings and rooms are automatically populated from the database with the getAvailableRoomsAPI() in useEffect().
- **SurveyTitle.js** : This page shows the link to the survey on the screen.
- **ThankYouTitle.js** : This page shows “Thank you - your response has been submitted!” after student responses are all submitted.
- **Title.js** : This is the title page with “My Friend Morgan” written in the center of the page.

## General Pages 
- **Home.js** : This is the starting page for all administrators and teachers. Individuals can get to the Room sign in and the Admin Sign in page from here. 
- **Wait.js** : This is a default waiting page that can be used to display different messages. 
    - Pass in a string for the message prop to set the string. 

