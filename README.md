# envoy-keycloak-oauth2

An example of configuring Envoy proxy to authenticate users against Keycloak before allowing access to upstream.

Envoy is levereging built-in [oauth2 filter](https://www.envoyproxy.io/docs/envoy/latest/configuration/http/http_filters/oauth2_filter)

Keycloak uses static import to create realm called "demorealm" and a client "democlient" with specified client secret. Same client/secret are specified in Envoy configuration of the oauth2 filter.

### how to run

1. Start containers via `docker-compose up`
2. Navigate to http://keycloak:8080, login as admin user (admin:admin) and create a test user
3. Go to http://localhost:10000 where Envoy listens. You should see immediate redirect to keycloak for user auth. After successful auth you should see redirect to upstream (Nginx with default web page).

