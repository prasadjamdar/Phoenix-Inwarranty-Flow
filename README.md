# Postman API Automation Integration with GitHub Actions #

This Repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in Postman and they are executed in VM with the help of newman and newman-reporter-htmlextra. 
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch.The projects runs on scheduled time with the help of cron job.

The HTML Report is archived and kept in the artifacts section for the team to download. Along with that they can view the report directly from the github page : https://prasadjamdar.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using Gmail SMTP.

## About Me ##
Hi My name is Prasad Jamdar. I have 4.5 years of experience in API Testing. My Skillset include POSTMAN, SOA-PARASOFT, MLQC, JIRA, GITHUB.
My Linked In : https://www.linkedin.com/in/prasadjamdar/

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge case testing
3. Token testing
4. Data driven testing with CSV
5. Schema Validation
6. Secrets Management with GitHub Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. newman
4. newman-reporter-htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV For Data Driven Testing
9. AWS-EC2 instance for self hosted github runner.

## GitHub Pages ##
You can directly view the latest test report of the postman test at the Github Page Link : https://prasadjamdar.github.io/Phoenix-Inwarranty-Flow/.

## HTML Report ##
The Report will be created in the newman folder.
![Postman Report](https://github.com/prasadjamdar/Phoenix-Inwarranty-Flow/blob/static-content/HTML_Report.jpg)

## Project Structure ##

```
Phonix Inwarranty Flow
├─ Inwarranty-flow Collection Copy.postman_collection.json # Collection File
├─ QA.postman_environment.json #Environment File
└─ testdata.csv #TestData File

```

## How to run the project? ##
You can run the project on your local system for that:
1. Clone the project on Local System : https://github.com/prasadjamdar/Phoenix-Inwarranty-Flow.git
2. Install NodeJS and NPM from https://nodejs.org/en
3. Install newman using
```
npm install -g newman
```
6. Install newman-reporter-htmlextra using
```
 npm install -g newman-reporter-htmlextra
 ```
8. Run the newman command:
```
              newman run 'Inwarranty-flow Collection Copy.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
```
