## Content Sharing Platform (educational resources)

 * *Description*: a platform allowing (Moroccan) homeschooling parents to search, submit, upvote, download or share educational resources via an elegant UI.
 * *Type of content*: articles, documents, presentations, images, url's, announcements
 * *Use cases*: search resources on keyword or explore (by subject / age range / resource type / key competency), store your own resources
 * *Key features*: paginated search results, submit / upvote / download / share resources, user profile, favorites (resources & search actions), user / moderator dashboard

### Status: early development phase

- [x] Design stage
- [x] Deploy CI/CD, Dockerize the (boilerplate) backend API and frontend app, Deploy prod server
- [ ] **Develop the backend API** https://github.com/JeroenAdam/ta3lim
- [ ] Develop the frontend app
- [ ] Develop end-to-end testing
- [x] Automated Docker container deploy on prod server

### Design:

![design](http://images.ctfassets.net/miz0cgjcqgye/4npYG5TiwIaNqk4ASIADAZ/4790d9a3fd092c41a2b5d334338c9955/ta3limnew.png)

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

### Dev workflow:
 * Compte Github Free (répo privé, peut-être public dans le futur)
 * [Installation](https://www.jhipster.tech/installation) en local (Git, OpenJDK 15, Node.js, Eclipse)
 * Communication interne avec [RocketChat](https://rocket.chat) (hébergé nous-mêmes) et [Kanban](https://github.com/JeroenAdam/Content-sharing-platform/projects/1) (Github)

### Devops workflow:
 * (laptop dev) git commit
 * (build server) [Jenkins pipeline](https://github.com/JeroenAdam/ta3alama/blob/master/Jenkinsfile) déclenche dans une VM sur laptop dev/testeur (via reverse SSH tunnel)
 * (build server) [Harbor](https://goharbor.io) > push vers le Docker registry / publication statut build sur Github
 * (prod) [Watchtower](https://github.com/containrrr/watchtower) > update container en cours
