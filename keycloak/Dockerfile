FROM jboss/keycloak
EXPOSE 8080

COPY ./realm-export.json /realm-export.json

ENV KEYCLOAK_USER admin
ENV KEYCLOAK_PASSWORD admin
ENV KEYCLOAK_IMPORT /realm-export.json
