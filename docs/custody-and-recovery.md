# Custody and recovery constraints

The initial integration requires one shared synchronous independently administered custodian for minimal WC1, plus a separately enforceable old-instance fence. Logical topology is shown in [custody topology](../diagrams/artefacts/custody-topology.svg). A second process with shared administration is a replica, not independent custody. A prototype may share a provider only with separate accounts/projects and no shared API token; independent provider and requalification are required before production.

| Consumer | Separate scope and use |
| --- | --- |
| Keymaker | Bootstrap/enrollment, original caller authority, exact predecessor/control/receipt, fresh-head and durable use transitions |
| Broker time settlement | RollbackWitness/time confidence history, separate enrollment, credentials, genesis approval and use transition |
| Broker store rollback | Independent store rollback history, enrollment, credentials and genesis; time history cannot substitute for it |
| User-manager | Ordinary initial create/retire/launch/stop is not a consuming adapter. Later PC2 or explicitly selected additional recovery/time scope uses the same custodian with separate history/enrollment |

Every actual consumer must bind service/chain/stream/sequence/record/receipt/control predecessor and authenticate a fresh head synchronously before authority release. Periodic replication, a local floor, heartbeat, file lock, receipt-valid flag or manual recovery does not replace this requirement. Namespaces, use transitions, recovery authority and original budgets remain separate; no wire encoding is invented here.

Independently enforce exclusion of old, restored, cloned and paused instances for all write, sign and authority-use release paths throughout the relevant lifetime. A replacement or successful append alone is not proof. Test paused/partitioned old writers and signers resuming after replacement. Unknown exclusion keeps authority closed.

Recovery binds the original intent/outcome, exact surviving independent history/floor, retained completion/use evidence and continuously excluded old instance. Missing receipts, unknown original outcomes or restored local state cannot create a new genesis, regenerate an acknowledgement, lower a mode or reset a floor. Stop/containment proceeds while original debts remain. Binary rollback, state restoration and emergency containment are distinct operations.

Joint rollback is detectable only against surviving independent evidence. Simultaneous custodian and ALL independent-evidence loss/rollback lies outside that guarantee; it must not be represented as a detected-refusal case. Archive/audit custody, retention/retrieval and independent completion/use evidence require separate acceptance. A record custodian does not discharge those obligations.

All proof pages, reconnects, transport, locks, durable commit and final use fit each original caller budget. Local CAS behavior proves no equivalent network transaction. Trusted time, post-read reserve, actual adapter frontier, native administration/placement/keys and recovery remain qualification gates.
