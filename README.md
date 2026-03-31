# README

Setup self hosted DocuSeal. Database backend is PostgreSQL. Databse can be connected via docker swarm overlay network.

## What is this repository for?

Easy setup and deployement of DocuSeal.

## How do I get set up

1. Clone repository to sutable folder 

	```
	cd /srv/
	git clone git@github.com:max-ra/CWA_docuseal.git
	cd cwa_docuseal
	```

1. Configure environment file. Take a look at **env.example**
1. Setup PostgreSQL databse. In this excample the db server is running insid a docker container. The db admin is called **dbadmin**. Pleas use youre one values for you're setup and set different password!

	```
	sudo docker exec -it -u postgres postgres /bin/bash
	psql -U dbadmin
	create database docuseal;
	create user docuseal with encrypted password 'HelloWorld';
	ALTER database docuseal owner to docuseal;
	```

## Contribution guidelines


## Who do I talk to?

* Repo owner or admin
* Other community or team contact
