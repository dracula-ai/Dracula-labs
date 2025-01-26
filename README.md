# DRACULA Framework

**Distributed Rules for Agent Consensus in Unified Logic Applications**

![Dracula Logo](logo.png)

---

## Overview

The **DRACULA Framework** is a TypeScript-based platform designed to enable the creation of distributed AI agents that operate on verifiable state machines and achieve consensus through cryptographic proofs. With a focus on adaptability and collaboration, DRACULA provides tools to build, evolve, and manage autonomous agents within a unified logic system inspired by the elegance and mystery of Dracula.

### Key Features

- **Distributed Consensus**: Cryptographically verified state transitions ensure trust and integrity in agent interactions.
- **Rule-Based Logic**: Agents operate using dynamic rule sets, adaptable to changing conditions.
- **Phase Evolution**: Agents evolve behavior in sync with the lunar calendar, adapting phases based on the moon's cycles.
- **Dynamic Persona Development**: Agents evolve their personalities and traits based on historical interactions and defined goals.
- **Collaborative Swarms**: Manage and deploy coordinated multi-agent systems for complex tasks.
- **Integrated Knowledge Gathering**: Seamless integration with external data sources, enabling agents to adapt based on real-world knowledge.
- **Visual State Tracking**: Gothic-themed ASCII art logs for detailed tracking of state changes and agent evolution.

---

## Getting Started

### Prerequisites

```bash
# Node.js v18+ required
node -v

# Install dependencies
npm install
```

### Environment Setup

Create a `.env` file with the following configuration:

```env
POSTGRES_URL=your_postgres_connection_string
CLAUDE_API_KEY=your_anthropic_api_key
```

### Basic Usage

```typescript
// Create a DRACULA agent
const agent = new DraculaAgent(
    "agent_id",
    "session_id",
    privateKeyHex
);

// Initialize with a default persona
await agent.start(defaultPersona);

// Monitor state transitions
agent.getCurrentState();
agent.getEvolutionHistory();
```

---

## State Machine Verification

Agents use cryptographic proofs for state transitions, ensuring a secure and verifiable operational history:

```typescript
interface Proof {
    stateHash: string;     // Hash of the current state
    prevHash: string;      // Hash of the previous state
    merkleRoot: string;    // Root of the Merkle tree
    merkleProof: string[]; // Proof path
    signature: string;     // Digital signature
    timestamp: number;     // Proof generation time
}
```

---

## Persona Evolution

Personas in the DRACULA framework evolve dynamically, driven by a hierarchical structure of traits and behaviors:

```typescript
interface PersonaStateData {
    personalityTraits: string[];
    goals: string[];
    interests: string[];
    background: string[];
    skills: string[];
    lore: string[];
    memories: string[];
    learnings: string[];
    patterns: string[];
    values: string[];
    prompt: string;
}
```

Agents synchronize their evolution phases with the lunar calendar, enabling unique periodic behavioral changes that reflect the moon's influence.

---

## Database Schema

DRACULA relies on PostgreSQL to maintain state histories and agent logs:

- **`agent_personas`**: Stores persona states and their evolution history.
- **`execution_logs`**: Tracks cryptographic proofs and state transition logs for transparency and debugging.

---

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push to the branch.
5. Open a Pull Request.

---

## Testing

Run tests to ensure the framework is functioning correctly:

```bash
npm test
```

---

## License

MIT License - see the LICENSE file for details.