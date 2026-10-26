# Original clocks and finite budgets

Every operation retains its original occurrence, first-entry times, cumulative work and earlier component limits. Equality at an exclusive cutoff refuses. Pauses, human confirmation, provider lookup, locks, retries, reconciliation, reconnect, reboot and late acknowledgements count; none refills time, bytes, calls or use slots. Complete durable endpoints and residual work must be measured at maximum admitted load.

Security stop requires original detection and boot-inclusive elapsed continuity. Confirm qualified narrowing or account-wide descendant/resumer absence plus quiet period within a published bound of at most 300s, intersected with every shorter original limit. A tighter initial profile includes separate detection and stop obligations: for original start 0s, detection 20s, 300s original envelope and 270s post-detection allowance, the effective deadline is at most 290s. Detection within 30s is independently required in that profile. These are requirements, not measured latencies, and cannot convert planned expiry into a security event.

Published enrollment profile ceilings of 60s for initial enrollment and 10s for completion are distinct original operations, with preparation, load and final durable endpoint included. Load-only work cannot consume the whole completion allowance. No automatic ceiling increase follows from overload; unknown headroom keeps the operation unqualified.

The finite installation profile remains an INITIAL PROPOSAL, not an accepted or qualified budget:

| Bootstrap phase | Proposed allowance | Exclusive cumulative cutoff from original reservation |
| --- | ---: | ---: |
| Reserve closed intent | 10s | +10s |
| Stage metadata | 10s | +20s |
| Install inert association | 20s | +40s |
| Joint currentness | 20s | +60s |
| Dispatcher policy only | 40s | +100s |
| Final durable activation | 20s | +120s |

Intersect the proposed 120s whole bound, each phase FIRST entry plus its allowance, cumulative cutoff and all shorter original bounds. Inert association entered at +15s cuts off at +35s; entry at +25s still cuts off at +40s. No unused allowance transfers. Proposed local work is 8 MiB and 16 dependency calls per phase, 48 MiB and 96 calls total, charging repeated work again. These are installer work caps, not remote promises or wire limits; the single 256 MiB state budget is unchanged.

Protected worker setup before reservation has no assigned accepted budget. Dispatcher closure/install/lookup/retry/currentness/activation time, bytes, calls and nested work also lack jointly accepted bounds. Missing is unqualified, not zero or unlimited. Never borrow enrollment ceilings, native subcall bounds, approval TTL or an invented reload allowance. Final activation cannot succeed on an expired occurrence; reconcile its original outcome and contain effects without reopening it.

WC1 consumers retain separate whole-operation budgets. Registry decision budget is 5s including custody; Keymaker path budgets of 250/1000/2000ms and registrar startup/client budgets concern different operations and cannot be exchanged. An unseen whole attempt is not bounded by a server timeout.

For `freshness/1`, require qualified UTC and durable watermark W, protected 0 < A <= 60s, age using max(now,W) and future bound using min(now,W). Receipt expiry is fixed as E = min(tip.issued_at + A, issuing witness-read-at + A). Use requires max(now,W) < E - delta, including a qualified post-read-to-durable-act/send reserve. Later reads never extend E. A process-local receipt cannot be serialized, copied or reconstructed as authority. Evidence, snapshot, head and anchor are immutable bindings and current checks repeat at the serialized effect. Existing external-root own-age checks remain until an agreed currency-format change is accepted.

Native elapsed/UTC backends, suspend/preemption/storage margins, cross-boot continuity and independent completion/use custody remain qualification inputs. Unknown continuity keeps holds; a recorded timestamp never proves a met deadline.
