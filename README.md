# Content sharing platform (educational resources)

Type of content: articles, documents, presentations, images, url's

User base: Moroccan homeschooling parents

# Status: early development phase

# Tech stack:
 * [JHipster](https://www.jhipster.tech)
 * [Java 14](https://openjdk.java.net)
 * [Spring Boot 2.3](https://spring.io/projects/spring-boot), [Spring Content](https://paulcwarren.github.io/spring-content)
 * [React](https://reactjs.org)
 * [MySQL 8](https://www.mysql.com)
 * [Liquibase](https://www.liquibase.org) (database version control)
 * [Keycloak](https://www.keycloak.org) (Identity and Access Management / SSO)
 * [Elasticsearch](https://github.com/elastic/elasticsearch)
 * [AWS S3 object storage](https://aws.amazon.com/s3)
 * [Caffeine](https://github.com/ben-manes/caffeine) (in-memory cache)
 * [Jenkins](https://jenkins.io) (build server)
 * [Cypress](https://www.cypress.io) (end-to-end testing)
 * [Docker](https://www.docker.com) (test & production)

# Dev env:
 * compte Github Free (répo privé, peut-être public dans le futur)
 * installation en local (Git, OpenJDK 14, Node.js, Eclipse) https://www.jhipster.tech/installation
 * communication interne avec [RocketChat](https://rocket.chat) (hébergé nous-mêmes) et sur Github (issues)

# Devops flow:
 * (laptop dev) commit
 * (build server) [Jenkins pipeline](https://www.jhipster.tech/setting-up-ci-jenkins2) déclenche dans une VM sur laptop testeur (via reverse SSH tunnel)
 * (build server) [Harbor](https://goharbor.io) > push vers le Docker registry / publication statut build sur Github
 * (VPS) [Watchtower](https://github.com/containrrr/watchtower) > update container en cours
