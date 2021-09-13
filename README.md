# envoy-keycloak-oauth2

An example of using Keycloak with Envoy proxy for user auth utilizing Envoy's [oauth2 filter](https://www.envoyproxy.io/docs/envoy/latest/configuration/http/http_filters/oauth2_filter)

Keycloak image has pre-configured realm "demorealm" with client_id/secret and a test user. Same client_id/secret are specified in Envoy configuration of the oauth2 filter.

### how to run

1. Start containers via `docker-compose up`
1. Go to http://localhost:10000 where Envoy listens. You should see immediate redirect to keycloak for user auth at http://localhost:8080
1. Log in as user "aa" password "aa". You should see redirect to upstream (Nginx with default web page)
