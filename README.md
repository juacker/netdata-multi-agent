# Multi-Agent configuration for Netdata

Multi agent netdata configuration. This setup places children in one space and parent in another space.
As children are streaming to parent, the three of them will be available at the parent's space.

## Setup

- Create a `.env` file with the required claim tokens:

```txt
CLAIM_TOKEN_PARENT_SPACE=<TOKEN_VALUE>
CLAIM_TOKEN_CHILD_SPACE=<TOKEN_VALUE>
```

- start docker compose

```shell
> docker-compose up
```
