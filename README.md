# Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for POC for integrating Postman tester with GitHub Actions. The tests are written in Postman, and they are executed on VM with the help newman and newman-reporter-htmlextra.
GitHub Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of cron job. 

The HTML report is archived and kept in the artifact section for the team to download it. Along with that, they can view the report directly from github page : https://pradipkumb13.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.

## Testing Coverage ##
1. Happy Flow testing
2. Negative testing and Edge case testing
3. Token testing
4. Data-driven testing with CSV
5. Schema validation
6. Secrets Management with GitHub secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV for data-driven testing
9. AWS  EC2 instance for self-hosted runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link:-https://pradipkumb13.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the Newman folder
![Postman Report] (https://github.com/pradipkumb13/Phoenix-Inwarranty-Flow/blob/Static-content/newman-report.png)

![Postman Report] (https://raw.githubusercontent.com/pradipkumb13/Phoenix-Inwarranty-Flow/Static-content/newman-report.png)

## Project Strcture ##

```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json # Collection file
├─ QA.postman_environment.json #Environment file
└─ testData.csv #Data file

```

## How to run Project ##
You can run the project on your local system for that:-
1. Clone the project on the local system: https://github.com/pradipkumb13/Phoenix-Inwarranty-Flow.git
2. Install Node.js and NPM from https://nodejs.org/en
3. Install Newman using npm install ``` -g newman ```
4. Install Newman-reporter-htmlextra ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman command :
   ```
          newman run "Inwarranty-flow Collection.postman_collection.json" \
          -e QA.postman_environment.json \
          -d testData.csv \
          -r cli,htmlextra \
          --reporter-htmlextra-export newman/index.html
   ```



  

