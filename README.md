## Content Sharing Platform (educational resources)

 * *Description*: a platform allowing educators to search, submit, download or share educational resources
 * *Type of content*: articles, documents, presentations, images, URLs, announcements
 * *Use cases*: browse educational resources, search & discover, store your resources, share w/ others
 * *Key features*: great search experience, relevant results, submit / upvote / download / share resources, user profile, favorites (resources & search actions), user / moderator dashboard

### Design:

![design](https://github.com/user-attachments/assets/3996165c-32fe-402a-b4be-ddbc8ca6e5a3)

![editor](https://github.com/user-attachments/assets/800706da-49df-41bf-8405-bce7490aca20)

### Status: live on Talim.app
try the demo on [talim.app](https://talim.app)

- [x] Design stage
- [x] Deploy CI/CD, Dockerize the (boilerplate) backend API and frontend app, Deploy prod server
- [x] Develop the backend API
- [x] Develop the frontend
- [ ] **Develop more features: upvoting, favorites, moderation, notifications and user/moderator dashboards**.
- [ ] Develop end-to-end testing
- [x] Automated Docker container deploy on prod server

### Status report:

So far, I've completed the research and design phase and I developed a [basic prototype](https://login.adambahri.com:1112/realms/jhipster/protocol/openid-connect/auth?response_type=code&client_id=web_app&scope=openid%20profile%20email&redirect_uri=https://app.adambahri.com:1114/login&login_hint=user&password=cca86cd5b97b) and I dockerized the web app. .

I am currently working on the UI (React). As for the backend, I'm progressing with features such voting and favorites.

There are quite some other features still to be done. I'll continue working on the filters, navigation, moderation, notifications and user/moderator dashboards. I'm planning for even a better search experience by adding semantic search and a better editor with inbuilt note-taking.

I'm not in a hurry so there is no timeline, eventually I'll publish educational resources that are relevant to me but for now I'm focusing on the technical aspects. Maybe one day I'll create an online community to gather feedback.

Future plans: integrate a Large Language Model for better discoverability of educational resources.

### Tech stack:
 * [JHipster](https://www.jhipster.tech)
 * [Java 17](https://openjdk.java.net)
 * [Spring Boot](https://spring.io/projects/spring-boot)
 * [React](https://reactjs.org)
 * [PostgreSQL](https://www.postgresql.org)
 * [Liquibase](https://www.liquibase.org) (database version control)
 * [Keycloak](https://www.keycloak.org) (Identity and Access Management / SSO)
 * [Elasticsearch](https://github.com/elastic/elasticsearch)
 * [AWS S3 storage](https://aws.amazon.com/s3)
 * [Jenkins](https://jenkins.io) (build server)
 * [Playwright](https://playwright.dev) (end-to-end testing)
 * [Docker](https://www.docker.com) (test & production)

###  Source code:
Currently not open source

### Contributing:
Open to collaboration, don't hesitate to [contact me](https://www.adambahri.com/contact)
