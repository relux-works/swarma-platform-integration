# Integration plan

## Initial limited integration

The target is one non-federated trusted Linux worker, with bounded immutable input and text/evidence output. It uses an already prepared active station generation and a qualified, explicitly activated broker v0 worker-UID allowlist. No binding, caller grant, account creation on dispatch, recursive delegation or general session service is included.

Ordinary station creation allocates a fresh random 128-bit generation token and durably reaches active. An authorized active operator then registers the active, unbound signing station with Keymaker. Provision/confirm is a generation-bump path, not first-create enrollment; no fake predecessor, pre-active enrollment or temporary activation is allowed. A lease-only worker does not need a signing key, but a selected signing caller must actually be qualified.

Protected setup binds caller and worker UID/generation independently, including an explicitly selected same-account mapping. Broker v0 sees only the actual worker kernel UID. Recreating a station requires fresh association, policy and allowlist installation even if the numerical UID is reused. Dispatch starts the existing generation and creates nothing.

After closed-admission worker setup and its controls, preserve the original sequence: reserve the closed bootstrap occurrence; stage metadata; install the inert public-key association; establish joint currentness; install dispatcher policy only; revalidate both identities and setup, commit durable outcomes/audit/custody, then open admitted scope. No lease is produced as a setup probe. No cross-service atomic transaction is assumed. See [budgets](clocks-and-budgets.md).

Purpose 6 authenticates only typed dispatch and owned-run cancel. Dispatcher policy supplies launch authority; the dispatcher owns intent, reservation, claims, effects, reconciliation and independent deadline stop. The worker runner owns broker request, renew and normal release under its own kernel UID. Dispatcher receives no lease observer, foreign-release authority or reason to widen the allowlist.

Selected start semantics use receiver commit C ordered against durable invalidation and expiry, after the root receipt and verified privilege drop. C strictly before invalidation is already-started work with a stop obligation. C is not physical execution release S. Every resumer and the bounded C-to-exec-or-abort residual, including quiet stop, must fit the same earliest original deadline. Equality or invalidation-first refuses; a late committed start refuses success while retaining effects and stop debt. The joint interlock is a required design, not an implemented capability claimed here. Strict physical-release semantics remain a later acceptance requirement.

The actual shared custody prerequisite is minimal WC1 with one synchronous independently administered custodian and separate lifetime old-instance exclusion. Keymaker and broker import it through distinct scopes. Ordinary manager create/retire/launch/stop has no custodian RPC dependency; later full PC2 does. [Custody requirements](custody-and-recovery.md) preserve that distinction.

Convergence requires reviewed authority, actual custody/time/exclusion adapters, qualified station/caller, signer/dispatcher/runner/launcher, executor/result joins, independent exact-tuple native acceptance and explicit owner installation/activation. Preparation alone admits no run.

## Full acceptance

Later acceptance retains narrowed caller delegation and broker binding/grant, signed `swarm-envelope/2` result over Matrix, independent verification, registry/witness snapshot and `freshness/1`, external-root currency, full PC2/custody and security revocation. The online registry-owner signer stays separate from the personal owner root. The limited run cannot waive any later predicate.

General workspace checkout, archive import, arbitrary home copy, worker retirement, federation, pool and memory are outside the selected limited input/output path. Required bounded output export and protected evidence retention are included. If the actual runtime needs an additional service, its real seam must be published and qualified before use.
