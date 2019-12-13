# Content sharing platform (educational resources)

Type of content: articles, documents, presentations, images, url's

User base: Moroccan homeschooling parents

# Status: early development phase

# Tech stack:
 * [JHipster](https://www.jhipster.tech)
 * [Java 11](https://openjdk.java.net)
 * [Spring Boot 2.1](https://spring.io/projects/spring-boot), [Spring Content](https://paulcwarren.github.io/spring-content)
 * [Angular 8](https://angular.io)
 * [MySQL 8](https://www.mysql.com)
 * [Liquibase](https://www.liquibase.org) (database version control)
 * [HikariCP](https://github.com/brettwooldridge/HikariCP) (connection pooling)
 * [Elasticsearch](https://github.com/elastic/elasticsearch)
 * [Caffeine](https://github.com/ben-manes/caffeine) (in-memory cache)
 * [Jenkins](https://jenkins.io) (automation server)
 * [Protractor](https://www.protractortest.org) (end-to-end testing)
  * [Docker](https://www.docker.com) (test & production)

# Dev env:
 * compte Github Free (répo privé, max. 3 comptes)
 * installation en local (Git, OpenJDK 11, Node.js, Eclipse) https://www.jhipster.tech/installation
 * communication interne avec [RocketChat](https://rocket.chat) (hébergé nous-mêmes sur VPS 2GB) et sur Github (issues)

# Devops flow:
 * (laptop dev) commit
 * (VPS 2 GB) [Jenkins pipeline](https://www.jhipster.tech/setting-up-ci-jenkins2) déclenche dans une VM sur laptop testeur (avec SSH tunnel ouvert), à cause de la [Angular AoT compilation](https://www.codingame.com/playgrounds/504/unleash-the-power-of-angular-aot-compilation) besoin >4GB mem., c'est lourd
 * envoi statut build vers Github + [https://labs.ovh.com/private-registry](OVH Private Registry) push (gratuit)
 * (VM sur laptop testeur) [Watchtower](https://github.com/containrrr/watchtower) > update container en cours
 * (optionnel, VM sur laptop testeur) app temporairement public via VPS (avec SSH tunnel ouvert)
