# Flow
Overview

This project implements a trustless escrow contract using the Clarity language on the Stacks blockchain.
It provides a secure and transparent way to manage digital agreements between a payer and a payee, optionally involving an arbiter in case of disputes.

The escrow is self-executing and tamper-proof, ensuring that funds are only released once the pre-agreed conditions are met.

🚀 Features

Token-Agnostic → Works with any SIP-010 fungible token.

Secure Escrow Lifecycle → Supports creation, locking, partial release, refunds, and finalization.

Arbiter Support → Neutral third-party intervention in disputes.

Event Logging → Every critical action (create, lock, release, refund, finalize) is logged for off-chain transparency.

Gas-Efficient → Minimal storage footprint and optimized execution.

🔑 How It Works

Create → Payer initializes the escrow with details (payee, token, amount, deadline, arbiter).

Pre-Fund → Payer deposits the specified tokens into the contract.

Lock → Escrow becomes active once funding is confirmed.

Release → Payer or arbiter can release tokens to the payee (fully or partially).

Refund → If deadlines are not met, remaining funds can be refunded to the payer.

Finalize → Once complete, escrow data is removed from storage.

🛠️ Public Functions

create → Initializes a new escrow agreement.

lock → Confirms escrow after deposit.

release → Transfers tokens to payee.

refund → Returns unused funds to payer.

finalize → Deletes escrow record once closed.

📊 Events Emitted

escrow_created

escrow_locked

escrow_released

escrow_refunded

escrow_finalized

Each event ensures traceability and audit-readiness, making it simple for external apps (like Google Clarity dashboards) to integrate real-time escrow updates.
