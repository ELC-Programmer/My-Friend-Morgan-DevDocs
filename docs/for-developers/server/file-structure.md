# My Friend Morgan
# **File Structure (Server)**

## casescenario/
Files related to case scenario generation
- skeleton.txt
  - The skeleton of the case scenario
  - ```*l*``` marks where the lifetime ethical behaviors will go.
  - ```*p*``` marks where the past year ethical behaviors will go.
- inserts.tsv
  - The first column is the survey question that corresponds to the insert
  - The second column is the lifetime insert
  - The third column is the past year insert
  - Since it's a tsv file, it can be imported, editted, and exported through google sheets
- behaviors.tsv
  - The behaviors that will be used in the group breakdown page

## routes/
API routes

## server.js
Server set up code