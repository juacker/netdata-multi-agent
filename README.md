# Multi-Agent configuration for Netdata

Multi agent netdata configuration, this creates a 3 level grandparent/parent/children setup:

```mermaid
stateDiagram-v2
    GrandParent --> Parent1
    GrandParent --> Parent2
    Parent1 --> Child1_latest
    Parent1 --> Child1_stable
    Parent1 --> Child1_old_stable
    Parent2 --> Child2_latest
    Parent2 --> Child2_stable
    Parent2 --> Child2_old_stable
```

## Setup

- Create a `.env` file with the required claim tokens (if you want to claim agents to different spaces, set new env vars for them):

```txt
CLAIM_TOKEN_ENV=<TOKEN_VALUE>
CLAIM_URL_ENV=<NETDATA_URL> // for public production env use: https://app.netdata.cloud
```

- start all agents using docker compose:

```shell
> docker compose up
```

You can also run individual agents, as needed:

```shell
> docker compose up child1 child2
```

Refer to the docker compose [docs](https://docs.docker.com/compose/reference/) for more useful commands.
