## What I Did (Task 2 Summary)

1. Ran Jenkins in Docker using GitHub Codespaces (`jenkins-setup/`).
2. Wrote a `Jenkinsfile` with these stages: Checkout, Install Dependencies, Test, Build Docker Image, Deploy.
3. Created a Jenkins Pipeline job (`cicd-demo`) that reads the `Jenkinsfile` from this GitHub repo.
4. Enabled SCM polling so Jenkins starts a new build automatically after each commit.
5. Pushed a code change (greeting updated to "Version 2") and confirmed Jenkins built and deployed it without me clicking Build Now.

## Screenshots

### Jenkins builds (#1 manual, #2 triggered by a commit)

<img width="1711" height="852" alt="#1 built" src="https://github.com/user-attachments/assets/b116dfa7-a81d-452d-b204-e782cf8cb322" />

### Pipeline stages
<img width="1857" height="536" alt="#2 stages" src="https://github.com/user-attachments/assets/f22c4f33-fb2d-4e5e-977d-11683c34e8e2" />


### Console output (SUCCESS)
<img width="1895" height="875" alt="#3 console output" src="https://github.com/user-attachments/assets/820cb333-6ce1-4e2d-af06-e05d91c233f5" />


### Deployed app
<img width="1918" height="552" alt="#4 app running" src="https://github.com/user-attachments/assets/32b7a2a3-6859-4de9-a5f1-54ef7c14d3f0" />


### Health check
<img width="1918" height="611" alt="#5 health check" src="https://github.com/user-attachments/assets/87d5b6a9-c7bc-4b3c-834b-645f12772b62" />
