## Content Sharing Platform (educational resources)

 * *Description*: a platform allowing (Moroccan) homeschooling parents to search, submit, upvote, download or share educational resources via an elegant UI.
 * *Type of content*: articles, documents, presentations, images, url's, announcements
 * *Use cases*: browse resources, search on keyword, refined search (subject, topic, age range, key competency), store your resources, share with others
 * *Key features*: great search experience, paginated results, submit / upvote / download / share resources, user profile, favorites (resources & search actions), user / moderator dashboard

### Design:

![design](https://github.com/JeroenAdam/Content-sharing-platform/assets/16437621/3e004c2a-00c0-4f08-bdbc-bc4102e8c615)

![editor2024](https://github.com/JeroenAdam/Content-sharing-platform/assets/16437621/022710d9-d01e-437b-bae6-64fb3477c36f)

### Status: early development phase

- [x] Design stage
- [x] Deploy CI/CD, Dockerize the (boilerplate) backend API and frontend app, Deploy prod server
- [x] Develop the backend API https://github.com/JeroenAdam/ta3lim
- [ ] **Develop the frontend app**
- [ ] Develop end-to-end testing
- [x] Automated Docker container deploy on prod server

### Status report:

The web app I am developing allows educators to browse, discover, store and share various educational resources such as articles, documents, presentations, etc. I'm using Java and React while practicing DevOps. The app will help educators facilitate children's learning.

So far, I completed the research and design phase. I started developing the backend API and included the entities you would expect such as EducationalResource, Subject, Topic, Skill, etc. I came up with a [basic prototype](https://login.adambahri.com:1112/realms/jhipster/protocol/openid-connect/auth?response_type=code&client_id=web_app&scope=openid%20profile%20email&redirect_uri=https://app.adambahri.com:1114/login&login_hint=user&password=cca86cd5b97b) and I dockerized the web app. 

I am currently working on the frontend (multipage React app), including a submit form using React Hook Forms and PrimeReact UI component library. As for the backend, I'm progressing with features such as notifications, voting, favorites, and sharing.

There is still much to be done. I'll continue working on the submit form, search box, search results, side panel (faceted search), navigation and user/moderator dashboard. I also plan to implement note taking and a better search experience by adding auto-completion and semantic search.

I aim to enter beta testing phase next year and I'll create an online community to gather feedback.

Future plans: improve search capabilities by integrating AI language models, implement a workspace for editors, implement end-to-end testing and scalability testing.

### Tech stack:
 * [JHipster](https://www.jhipster.tech)
 * [Java 17](https://openjdk.java.net)
 * [Spring Boot 2.7](https://spring.io/projects/spring-boot), [Spring Content](https://paulcwarren.github.io/spring-content)
 * [React](https://reactjs.org)
 * [MySQL](https://www.mysql.com)
 * [Liquibase](https://www.liquibase.org) (database version control)
 * [Keycloak](https://www.keycloak.org) (Identity and Access Management / SSO)
 * [Elasticsearch](https://github.com/elastic/elasticsearch)
 * [AWS S3 storage](https://aws.amazon.com/s3)
 * [Caffeine](https://github.com/ben-manes/caffeine) (in-memory cache)
 * [Jenkins](https://jenkins.io) (build server)
 * [Cypress](https://www.cypress.io) (end-to-end testing)
 * [Docker](https://www.docker.com) (test & production)

###  Source code:

Work in progress: https://github.com/JeroenAdam/ta3lim

### Want to contribute to this project?
If you have one of the below skills and want to contribute, take a look at this [Kanban](https://github.com/JeroenAdam/Content-sharing-platform/projects/1) and don't hesitate to [contact me](https://www.adambahri.com/contact)

 * Backend development (Java/Spring Boot/Elasticsearch)
 * Frontend development (React)
 * UI/UX design
