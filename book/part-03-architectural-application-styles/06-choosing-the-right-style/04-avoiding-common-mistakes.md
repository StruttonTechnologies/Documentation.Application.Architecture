# Avoiding Common Mistakes

Application styles are often selected for reasons unrelated to the actual needs of the system.

One common mistake is designing for anticipated scale before the system has demonstrated where scale will occur. This creates boundaries, services, and operational responsibilities based on prediction rather than evidence.

Another mistake is using distribution to compensate for poor architecture.

Splitting a system does not clarify unclear responsibilities or repair uncontrolled dependencies. Those problems must be resolved before distribution, or they will become harder to change across service boundaries.

Teams also underestimate permanent operational cost.

Independent services require deployment, observation, security, support, recovery, and contract coordination for as long as they exist. The cost is not limited to the initial implementation.

A further mistake is choosing style by prestige.

A distributed system may appear more advanced, but unnecessary complexity is not architectural maturity. Mature architecture accepts only the complexity required to satisfy real constraints.

The correct application style is the one that preserves architectural integrity while imposing the lowest justified long-term cost.

Begin simply.

Strengthen boundaries when evidence requires it.

Distribute only when independent deployment provides value worth the complexity it creates.

---

[← When Distribution Becomes Necessary](03-when-distribution-becomes-necessary.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Part 3 Summary →](../99-part-03-summary/README.md)
