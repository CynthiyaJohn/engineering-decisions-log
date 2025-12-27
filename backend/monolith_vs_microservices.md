# Monolith vs Microservices

## Context
As applications grow, teams must decide how to structure backend services to balance
development speed, scalability, and operational complexity.

## Options Considered

### Monolithic Architecture
A single deployable unit where all features and services are tightly integrated.

### Microservices Architecture
A collection of independently deployable services, each responsible for a specific domain.

## Decision
Monoliths are typically preferred for early-stage products and small teams, while
microservices are adopted when independent scaling, team autonomy, and system complexity
increase.

## Trade-offs

### Monolith – Pros
- Simpler development and deployment
- Easier debugging and testing
- Lower operational overhead

### Monolith – Cons
- Difficult to scale specific components
- Tight coupling between features
- Slower deployments as the codebase grows

### Microservices – Pros
- Independent scaling and deployment
- Clear domain boundaries
- Better fault isolation

### Microservices – Cons
- Increased operational complexity
- Network latency and failure handling
- Requires mature DevOps practices

## When This Decision Fails
- Using microservices without proper monitoring, CI/CD, or team maturity
- Scaling a large monolith beyond manageable limits without modular boundaries

