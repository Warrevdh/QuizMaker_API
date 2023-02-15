## Vereisten

Ik verwacht dat volgende software reeds geïnstalleerd is:

- [NodeJS](https://nodejs.org)
- [Yarn](https://yarnpkg.com)
- [MySQL Community Server](https://dev.mysql.com/downloads/mysql/)

Ik verwacht dat volgende packages reeds geïnstalleerd zijn:

- [Prisma ORM](https://yarnpkg.com/package/prisma)
- [uuid](https://yarnpkg.com/package/uuid)

## Opstarten

Voor het opstarten van de applicatie is er een .env bestand nodig. Dit bestand moet de volgende variabelen bevatten:

- NODE_ENV=development
- JWT_SECRET="verysecret"
- DATABASE_URL="mysql://janedoe:mypassword@localhost:3306/mydb" [(Database url opstellen)](https://www.prisma.io/docs/reference/database-reference/connection-urls)
- AUTH_JWKS_URI="https://{TENANT}/.well-known/jwks.json"
- AUTH_AUDIENCE="{API-IDENTIFIER}"
- AUTH_ISSUER="https://{TENANT}"
- AUTH_USER_INFO="https://{TENANT}/userinfo"

Om de API te starten moet je de volgende commando's uitvoeren:

- yarn install
- yarn start

## Testen

Voor het testen van de applicatie is er een .env.test bestand nodig. Dit bestand moet de volgende variabelen bevatten:

- NODE_ENV=test
- JWT_SECRET="verysecret"
- DATABASE_URL="mysql://janedoe:mypassword@localhost:3306/mydb" [(Database url opstellen)](https://www.prisma.io/docs/reference/database-reference/connection-urls)
- AUTH_JWKS_URI="https://{TENANT}/.well-known/jwks.json"
- AUTH_AUDIENCE="{API-IDENTIFIER}"
- AUTH_ISSUER="https://{TENANT}"
- AUTH_USER_INFO="https://{TENANT}/userinfo"
- AUTH_TOKEN_URL="https://{TENANT}/oauth/token"
- AUTH_CLIENT_ID="{YOUR-CLIENT-ID}}"
- AUTH_CLIENT_SECRET="{YOUR-CLIENT-SECRET}"
- AUTH_TEST_USER_ID="{YOUR-TEST-USERS-AUTH0ID}"
- AUTH_TEST_USER_USERNAME="{YOUR-TEST-USER-USERNAME}"
- AUTH_TEST_USER_PASSWORD="{YOUR-TEST-USER-PASSWORD}"

Om de testen uit te voeren moet je de volgende commando's uitvoeren:

- yarn install
- yarn test
- yarn test:coverage
