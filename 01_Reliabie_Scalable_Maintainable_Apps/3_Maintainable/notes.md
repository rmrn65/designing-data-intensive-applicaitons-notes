# Maintainability

## Introduction

Maintainability is the property of easily changing, fixing and understanding code and logic inside a service

## Characteristics

- Operability = easy for Ops teams to keep it running
- Simplicity = easy for new joiners to understand it
- Evolvability = easy to build upon it

### Operability

- Health monitoring and self-healing
- Keeping the service, libraries or dependencies up-to-date
- Anticipating future problems - pitfall: overengineering
- Observability
- Documentation

### Simplicity

- Respect SRP - single responsibility principle
- Avoid necessary complexities - turn complexities into abstraction and hide it behind a façade

### Evolvability

- Respect open closed principle

> Easy to understand services are easy to evolve