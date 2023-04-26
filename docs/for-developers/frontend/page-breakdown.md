# My Friend Morgan
# **Page Breakdown**

## Admin Pages

## Student Pages
- **StudentSignIn.js** : Starting page for students taking the survey/case inside the ELC where they sign-in with the building and room that they are in
    - Buidlings and rooms are automatically populated with the getAvailableRoomsAPI() in useEffect()
- **Survey.js** : Survey Page that asks students to check their behaviors in the past year or in their lifetime. It can be accessed directly if the students are not taking in the ELC or accessed from the StudentSignIn page. 
    - Each question is sectioned into a SurveyRow component-to add or edit a question, pass in the question as props as a string. 
- **Case Scenario.js** : This page shows the generated case scenario for their room and ask corresponding questions for the students to answer. 

## Room Pages

## General Pages 
- **Home.js** : This is the starting page for all administrators and teachers. Indisivuals can get to the Room sign in and the Admin Sign in page from here. 
- **Wait.js** : This is a default waiting page that can be used to display different messages. 
    - Pass in a string for the message prop to set the string. 

