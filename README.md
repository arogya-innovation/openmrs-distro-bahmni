openmrs-distro-bahmni
==================

`./mvnw clean deploy` command to create artifacts.

This command will attempt to upload & publish artifacts to https://bahmnirepo.thoughtworks.com (maven repository). You will need authorization to upload (your public key needs to be on the server). 

This distribution also includes [FHIR CDSS module](https://github.com/Bahmni/openmrs-module-cdss) and [FHIR Terminology Service Module](https://github.com/Bahmni/openmrs-module-snomed) along with other modules bundled with standard Bahmni.
More details can be found [here](https://bahmni.atlassian.net/wiki/spaces/BAH/pages/3132686337/SNOMED+FHIR+Terminology+Server+Integration+with+Bahmni)


docker build -f package/docker/openmrs/Dockerfile -t bahmni-openmrs-custom .


mvn -U clean install -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true
