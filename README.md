# Infrastructure Thinking

How highly scalable, highly available infrastructure *should* look — written from production experience, not certifications. Each guide ends with a rule of thumb you can defend in a design review.

GitHub renders all diagrams below natively (Mermaid). Start anywhere; suggested order:

1. [Load Balancers](docs/01-load-balancers.md) — L4 vs L7, ALB/NLB, health checks that actually work
2. [Deployment Strategies](docs/02-deployment-strategies.md) — rolling, blue-green, canary, and when each one hurts
3. [Auto Scaling](docs/03-auto-scaling.md) — the feedback loop, policies, and why cooldowns exist
4. [Availability Zones](docs/04-availability-zones.md) — blast radius thinking and what multi-AZ really costs
5. [Disaster Recovery](docs/05-disaster-recovery.md) — active-active vs active-passive, RTO/RPO as design inputs
6. [DNS Failover with Route 53](docs/06-dns-failover-route53.md) — health checks, routing policies, TTL tradeoffs
7. [Database Backup Strategy](docs/07-database-backups.md) — why backups, GFS rotation, restore drills at scale
8. [Event-Driven Architecture](docs/08-event-driven-architecture.md) — brokers, sagas, idempotence, outbox at scale
9. [Replica Set Architecture](docs/09-replica-set-architecture.md) — elections, concerns, multi-region sets at scale
10. [Full Application Architecture](docs/10-full-application-architecture.md) — capstone: all nine guides in one millions-scale system

## How these are written

- **Tradeoffs first.** Every pattern lists what it costs (money, complexity, or both).
- **Failure modes included.** If a doc doesn't say how the thing breaks, it's marketing.
- **AWS-flavored, cloud-portable.** Examples use AWS names (ALB, Route 53, Aurora) but the ideas transfer to any cloud.

## Contribute an idea

Open a PR adding a new file under `docs/` numbered next (`07-...md`), with at least one Mermaid diagram and one rule of thumb. Keep it opinionated.

## License

MIT.
