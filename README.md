# Nginx Router

## Description

Solution documentation of NGINX router implementation serving subscriber traffic migration to a new system. 

Subscriber-id is populated to a Redis key-value server. This information used by NGINX as subscriber traffic routing decision.

## Topology

```
                      Redis
                        |     +---- new backend
                        |     |
Subs ---[subs-id] --- NGINX --+
                              |
                              +---- old backend

```