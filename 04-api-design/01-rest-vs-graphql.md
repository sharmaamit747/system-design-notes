# REST vs GraphQL

## REST API (Most Common)

### What is REST?
REST is a resource-based API design.

Example:
```http
GET /api/users/1
```
Each endpoint returns a fixed response.

### Pros
- Simple
- Easy to cache
- Widely used

### Cons
- Over-fetching
- Under-fetching


## GraphQL

Client requests exactly the data it needs.
Example:

```graphql
{
  user(id: 1) {
    name
    email
  }
}
```

## Pros

-Flexible responses
- One endpoint

## Cons

- Complex
- Harder caching
- Learning curve

## Laravel Perspective

REST → Default choice

GraphQL → Large frontend teams, mobile apps