FROM jboss/keycloak

COPY ./realm.json /realm.json

ENV KEYCLOAK_USER admin
ENV KEYCLOAK_PASSWORD admin
ENV KEYCLOAK_IMPORT /realm.json
