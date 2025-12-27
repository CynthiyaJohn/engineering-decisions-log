# JWT vs Session-Based Authentication

## Context
Applications require a way to identify and authenticate users across multiple requests.

## Options Considered
- JSON Web Tokens (JWT)
- Server-side Sessions

## Decision
JWTs are often chosen for stateless APIs and distributed systems, while sessions are preferred for server-rendered or tightly controlled environments.

## Trade-offs
**JWT Pros**
- Stateless
- Scales well horizontally
- No server-side storage

**JWT Cons**
- Hard to revoke
- Token leakage is dangerous
- Larger payload size

**Session Pros**
- Easy revocation
- Smaller client footprint
- Better control

**Session Cons**
- Requires server-side storage
- Scaling needs shared session store

## When This Decision Fails
- JWTs in highly sensitive systems without rotation
- Sessions in large distributed microservices without centralized storage

