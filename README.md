## Technical Overview

A thread-safe message queue implementation in SystemVerilog that enables safe communication between concurrent simulation threads. Uses semaphore-based synchronization to prevent race conditions during message passing.

**Key Features:**
- **Thread-Safe**: Binary semaphore ensures only one thread accesses the queue at a time
- **Dual Modes**: Both blocking (waits) and non-blocking (immediate) operations
- **Priority Support**: Optional priority-based message retrieval (HIGH, MEDIUM, LOW)
- **Configurable**: Supports both limited-size and unlimited mailboxes

**Use Case**: Perfect for SystemVerilog testbenches where multiple verification components need to exchange messages safely.

## Core Algorithm

The mailbox implements a **binary semaphore synchronization model**:
