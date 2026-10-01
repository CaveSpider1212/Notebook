---
tags: CMSC_330
created: 2026-9-29
description: 9/29 notes
---

**Abstract machine**: Idea for how a machine would work, containing its rules (theoretical, no one builds them)

**Automata Theory**: Idea that machines do computation 

- Logic machines
- Finite state machines (FSM or FA, finite automata)
- Pushdown Automata (PDA)
- Turing Machine

Anything one machine above can do, another machine can do as well.

### Finite State Machines

- States: $Q$
	- Like nodes on a graph
- Start: $q \in Q$
- Actions: $\Sigma$
- Transitions: $\delta [(\text{N}, \text{right}, \text{E}), ...]$
	- Like edges on a graph between the nodes
- Final states: $F \subseteq Q$
	- State that marks the successful completion of an input sequence

### DFAs and NFAs

Types of FSMs: DFA (deterministic) and NFA (non-deterministic)

- Deterministic: Given an input, should know what the output is
	- When in a state, know exactly what will happen (only one place it could end up at)
	- Given a state, FSM and input, should be able to tell where it will end up (called **move**)
- Non-deterministic: Don't exactly know what output is given the current state
	- Multiple outputs (more than one place it could end up)

> [!tip]
> Any NFA can be reduced to a DFA.
> Any regular expression can be easily changed to an NFA.
> Any DFA can be converted to a regular expression.

> [!info] Do Nothing ($\epsilon$)
> In NFAs, there is a concept of do nothing, called $\epsilon$ (epsilon).
> 
> $\epsilon$ is a transition from a state to another state. It is reached automatically if a state has the epsilon transition, so if the machine reaches a state with an epsilon, it branches into the next state simultaneously.

**$\epsilon$-closure**: Set of all states reachable from a given state by following only the $\epsilon$-transitions, including the state.

### Regular Expression --> NFA

Base case (single-symbol): Have a starting state, a transition (with the symbol) that we are looking for, and a final state

> [!tip]
> Every FSM has 1 start and 1 final state.