# Hoppscotch GraphQL API

The Hoppscotch backend exposes a GraphQL API used by the web, desktop, and CLI clients for team collaboration, personal workspaces, and infrastructure management in self-hosted deployments. The API covers user authentication sessions, team management, shared request collections, environments, request history, shortcodes (shared request links), mock servers, and published API documentation. Admin/infra operations are available to administrators for managing users, SSO providers, SMTP configuration, and infrastructure tokens.

Authentication uses JWT bearer tokens issued after login via supported OAuth providers (Google, GitHub, Microsoft) or email magic-link. Pass the token as an `Authorization: Bearer <token>` header.

**Endpoint:** https://{your-hoppscotch-backend}/graphql

**Documentation:** https://docs.hoppscotch.io

**References:**

- Documentation: https://docs.hoppscotch.io
- GettingStarted: https://docs.hoppscotch.io/documentation/getting-started/introduction
- SelfHost: https://docs.hoppscotch.io/documentation/self-host/getting-started
- GitHub: https://github.com/hoppscotch/hoppscotch
