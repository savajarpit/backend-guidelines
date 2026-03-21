---
name: MASTER
description: >
  Read this first for ANY task in this project.
  Routes to the correct skill file based on what you're building.
  This project: NestJS SaaS starter, multi-tenant, PostgreSQL(Prisma) OR MongoDB(Mongoose).
---

# MASTER Skill Router

## ALWAYS READ FIRST
`general-guidelines.md` → applies to every task, every file, every technology.

## THEN READ based on the task

| Task involves | Read next |
|---|---|
| Module, controller, service, guard, interceptor, DTO, Swagger, versioning | `nestjs.md` |
| PostgreSQL, Prisma schema, migrations, prisma queries | `prisma.md` |
| MongoDB, Mongoose schema, hooks, populate | `mongoose.md` |
| Redis, caching, OTP, token blacklist, rate limit storage | `redis.md` |
| JWT, passwords, bcrypt, CORS, helmet, encryption, auth guards | `auth-security.md` |
| Stripe, webhooks, payments, subscriptions | `payment.md` |
| Docker, Dockerfile, docker-compose, containerization | `docker.md` |
| Git, branches, commits, PR workflow | `git.md` |
| S3, R2, file upload, presigned URLs, storage | `storage-s3.md` |
| Bull, queues, background jobs, processors | `queue.md` |
| Logger, Sentry, request tracing, monitoring | `logging-monitoring.md` |
| .env, ConfigService, Joi validation, secrets | `environment.md` |
| Jest, unit tests, e2e tests, mocking | `testing.md` |

## PROJECT QUICK REFERENCE

```
Repo:           nestjs-saas-starter
Framework:      NestJS (latest)
Language:       TypeScript strict
DB switch:      DB_DRIVER in src/database/database.config.ts
API prefix:     /api
Versioning:     /api/v1/, /api/v2/ (URI-based)
Auth:           JWT global — @Public() to opt out
Response:       { success, message, data, meta, timestamp }
Tenant:         tenantId on every scoped query — always
Port:           3000
Swagger:        http://localhost:3000/api/docs (dev only)
Health:         GET /api/v1/health
```

## SKILL FILES IN THIS REPO

```
skills/
├── MASTER.md                ← you are here
├── general-guidelines.md    ← architecture laws (read always)
├── nestjs.md                ← NestJS patterns
├── prisma.md                ← PostgreSQL / Prisma
├── mongoose.md              ← MongoDB / Mongoose
├── redis.md                 ← Redis / caching
├── auth-security.md         ← JWT / security
├── payment.md               ← Stripe / webhooks
├── docker.md                ← Docker / containerization
├── git.md                   ← Git workflow
├── storage-s3.md            ← S3 / R2 / file upload
├── queue.md                 ← Bull / background jobs
├── logging-monitoring.md    ← Logger / Sentry
├── environment.md           ← Config / env vars
└── testing.md               ← Jest / unit / e2e
```