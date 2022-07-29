# webauthn.io

Duo's introduction to the wonderful world of WebAuthn. Powered by [py_webauthn](https://github.com/duo-labs/py_webauthn).

## Prerequisites

- Docker
- Pipenv
  - Make sure Python3 is available
  - Enables `pipenv install` to set up libraries locally for the editor to crawl. The Django container also uses Pipenv to install dependencies to encourage use of this new Python package management tool.

## Environmental Variable

- `DJANGO_SECRET_KEY`: A sufficiently random string
- `POSTGRES_USER`: Database username
- `POSTGRES_PASSWORD`: Database password
- `PROD_HOST_NAME`: The domain name the site will be hosted at
- `RP_ID`: The Relying Party ID, typically the same as `PROD_HOST_NAME`
- `RP_NAME`: A representation of the site's name to be shown to users
- `RP_EXPECTED_ORIGIN`: The domain name plus protocol at which WebAuthn will be invoked (e.g. `https://webauthn.io`)

## Development

Run the following command to get started:

```sh
$> ./start-dev.sh
```

The site will be available at http://localhost:8000

## Production

Run the following command to start up the website with production-ready settings:

```sh
$> ./start-prod.sh
```

The site will be available for viewing at http://{PROD_HOST_NAME}. SSL should be handled in a way that's appropriate for your server.
