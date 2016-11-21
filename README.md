# cdn
An auth-protected, dedicated CDN implemented with Angel. 
All resources are protected via JWT, and user management is CLI-based. 
To see all CLI options, run:

```bash
$ bin/manager --help
```

# Usage

## Server-side
To upload resources, you need a JWT for a user with write access.

## Client
To download a resource, you only need to be signed in as a user with
read access. It is recommended to create a public user with read-only
access, and use this user on the client-side.

You can pass the token as an HTTP header, send it with a cookie, or even
include it in the request query. For example:

```html
<img src="//cdn.example.com/resource/id?token=myJwt" />
```
