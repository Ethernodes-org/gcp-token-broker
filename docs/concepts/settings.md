This page lists the settings available for the broker application, in alphabetical order.

## Available settings

### `ACCESS_TOKEN_LOCAL_CACHE_TIME`

Default: `30` (in seconds)

[Local cache](caching.md#local-cache) lifetime for access tokens.

### `ACCESS_TOKEN_REMOTE_CACHE_TIME`

Default: `60` (in seconds)

[Remote cache](caching.md#remote-cache) lifetime for access tokens.

### `AUTHENTICATION_BACKEND`

Default: `com.google.cloud.broker.authentication.backends.SpnegoAuthenticator`

[Authentication](authentication.md) backend class.

### `BROKER_SERVICE_HOSTNAME`

Broker principal's hostname.

### `BROKER_SERVICE_NAME`

Default: `broker`

Broker principal's service name.

### `CLIENT_SECRET_PATH`

Default: `/secrets/client_secret.json`

Path to the OAuth client ID used by the [Authorizer](authorizer.md) app and the [refresh token provider](providers.md#refresh-token-provider).

### `DATABASE_BACKEND`

Default: `com.google.cloud.broker.database.backends.CloudDatastoreBackend`

[Database](database.md) backend class.

### `DOMAIN_NAME`

Domain name for your GSuite users.

### `ENCRYPTION_BACKEND`

Default: `com.google.cloud.broker.encryption.backends.KMSEnvelopeEncryptionBackend`

[Encryption](encryption.md) backend class.

### `ENCRYPTION_CRYPTO_KEY`

Name of the Cloud KMS key used to [encrypt](encryption.md) data.

### `ENCRYPTION_DEK_URI`

URI of the Cloud KMS [encryption](encryption.md) key ring in format `projects/_/locations/_/keyRings/_/cryptoKeys/_`.

### `DATABASE_JDBC_URL`

JDBC url for the relational database. Only necessary if you choose to use the [JDBC database backend](database.md#jdbc-backend).

### `JWT_LIFE`

Default: `30` (in seconds)

Life duration for JWT tokens for the [service account provider](providers.md#service-account-provider) and
the [domain-wide delegation authority provider](providers.md#domain-wide-delegation-authority-provider)
(the shorter the time the better).

### `KEYTABS_PATH`

Default: `/keytabs`

Path on the filesystem for the directory that contains the broker principals' keytabs.

### `LOGGING_LEVEL`

Default: `INFO`

Base level for application logs.

### `PROVIDER`

Default: `com.google.cloud.broker.accesstokens.providers.RefreshTokenProvider`

Access token [provider](providers.md) backend class.

### `PROXY_USER_WHITELIST`

Default: `""` (Empty string)

Comma-separated whitelist of [proxy users](authentication.md#proxy-user-impersonation).

### `REDIS_CACHE_DB`

Default: `0`

Redis database number used for caching. Only necessary if you use the [Redis cache backend](caching.md#redis-backend).

### `REDIS_CACHE_HOST`

Default: `localhost`

Host of the Redis cache server. Only necessary if you use the [Redis cache backend](caching.md#redis-backend).

### `REDIS_CACHE_PORT`

Default: `6379`

Port of the Redis cache server. Only necessary if you use the [Redis cache backend](caching.md#redis-backend).

### `REMOTE_CACHE`

Default: `com.google.cloud.broker.caching.remote.RedisCache`

[Remote cache](caching.md#remote-cache) backend class.

### `SCOPE_WHITELIST`

Default: `https://www.googleapis.com/auth/devstorage.read_write`

Comma-separated whitelist of API scopes for access tokens.

### `SERVER_HOST`

Default: `0.0.0.0`

Hostname where the broker application is served.

### `SERVER_PORT`

Default: `5000`

Port number where the broker application is served. A valid port value is between `0` and `65535`.
A port number of `0` will let the system pick up an ephemeral port in a bind operation.

### `SESSION_LOCAL_CACHE_TIME`

Default: `30` (in seconds)

[Local cache](caching.md#local-cache) lifetime for [session](sessions.md) details.

### `SESSION_MAXIMUM_LIFETIME`

Default: `604800000` (7 days, in milliseconds)

[Session](sessions.md) maximum lifetime.

### `SESSION_RENEW_PERIOD`

Default: `86400000` (24 hours, in milliseconds)

[Session](sessions.md) lifetime increment.

### `SHADOW_PROJECT`

GCP project where the [shadow service accounts](providers.md#service-account-provider) are hosted.

### `SHADOW_USERNAME_PATTERN`

Default: `%s-shadow`

Pattern for the [shadow service account](providers.md#service-account-provider) username.

### `TLS_ENABLED`

Default: `true`

Flag to enable/disable [TLS](tls.md).

### `TLS_CRT_PATH`

Default: `/secrets/tls.crt`

Path on the filesystem for the [TLS](tls.md) certificate.

### `TLS_KEY_PATH`

Default: `/secrets/tls.pem`

Path on the filesystem for the [TLS](tls.md) private key.