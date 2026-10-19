---
tags: CMSC_330
created: 2026-9-29
description: 9/29, 10/1, 10/15 notes
---

**Abstract machine**: Idea for how a machine would work, containing its rules (theoretical, no one builds them)

**Automata Theory**: Idea that machines do computation 

- Logic machines
- Finite state machines (FSM or FA, finite automata)
- Pushdown Automata (PDA)
- Turing Machine

Anything one machine above can do, another machine can do as well.

### Finite State Machines

![[10.4.26 FSM.png]]

- States: $Q$
	- Like nodes on a graph
- Start: $q \in Q$
- Actions: $\Sigma$
- Transitions: $\delta [(\text{N}, \text{right}, \text{E}), ...]$
	- Like edges on a graph between the nodes
- Final states: $F \subseteq Q$
	- State that marks the successful completion of an input sequence

> [!info] Final States
> Final states are usually shown as a double circle, and that should be the *last state* the machine is in for the entire input combination for the combination to be accepted.

### DFAs and NFAs

Types of FSMs: DFA (deterministic) and NFA (non-deterministic)

- Deterministic: Given an input, should know what the output is
	- When in a state, know exactly what will happen (only one place it could end up at)
- Non-deterministic: Don't exactly know what output is given the current state
	- Multiple outputs (more than one place it could end up)

> [!tip]
> Any NFA can be reduced to a DFA.
> Any regular expression can be easily changed to an NFA.
> Any DFA can be converted to a regular expression.

> [!info] Move
> **Move**: Given a state, FSM, and input, should be able to tell where state machine would end up

> [!info] Do Nothing ($\epsilon$)
> In NFAs, there is a concept of do nothing, called $\epsilon$ (epsilon).
> 
> $\epsilon$ is a transition from a state to another state. It is reached automatically if a state has the epsilon transition, so if the machine reaches a state with an epsilon, it branches into the next state simultaneously.

**$\epsilon$-closure**: Set of all states reachable from a given state by following only the $\epsilon$-transitions, including the state. (Note: The current state is also included in the set of states reachable by epsilon)

### Regular Expression --> NFA

Base case (single-symbol): Have a starting state, a transition (with the symbol) that we are looking for, and a final state

> [!tip]
> Every FSM has 1 start and 1 final state.

##### Base cases ($\oslash, \epsilon, \sigma$)

- $\oslash$ (accept nothing): Have a single state
- $\epsilon$ (empty string): Have a single final state
- $\sigma$ (single character): Have a state with a transition of $\sigma$ to a final state

##### Concatenation ($R_1 R_2$)

To concatenate two regular expressions ($R_1 R_2$), say both expressions already have NFAs (from their base cases) with starting and final states (doesn't matter what's in between).

The NFA for $R_1 R_2$ is the two NFAs (for $R_1$ and $R_2$) with an epsilon transition between them (so between the final state of $R_1$'s NFA and the starting state of $R_2$'s NFA).

![[10.15.26 RegEx Concat to NFA.png]]

##### Union/Branching ($R_1 | R_2$)

Let's say both expressions $R_1$ and $R_2$ already have NFAs with starting and final states (doesn't matter what's in between).

The NFA for $R_1 | R_2$ has a new single starting state, with epsilon transitions to both $R_1$'s NFA's and $R_2$'s NFA's starting states. It also has a new single final state with epsilon transition between both expressions' final states to that new final state.

![[10.15.26 RegEx Union to NFA.png]]

##### Kleene Closure ($R_1 ^*$)

Let's say the regular expression already has an NFA with a starting and final state. The NFA for $R_1^*$ has a new starting and final state, and epsilon transitions between the new starting and expression NFA's starting, expression's final and new final, and between the new start and final states.

![[10.15.26 RegEx Star to NFA.png]]

### NFA --> DFA

Let the starting state of the DFA $r_0$ be equal to an e-closure of the starting state of the NFA $q_0$, and add $r_0$ to the list of states $R$ in the DFA.

For each state $r$ in the list of states $R$, call `move` on the state for each symbol $\sigma$ in $\Sigma$ (result would be $E$), then call e-closure on that result (result would be $e$). Add $e$ to the list of states $R$ (as long as it isn't a duplicate or an empty list).

Also, the transition of $\sigma$ between states $r$ and $e$ is a transition in the DFA.

Keep repeating the process of processing states and adding new states to the list $R$ until there are no more states to process. The final states $F_d$ of the DFA are all the states which contain a final state of the NFA.

> [!example] NFA to DFA Example
> ![[10.18.26 NFA to DFA Example.png|300]]
> 
> Note: Arrows indicate result after e-closure
> 
> |Final?|State|a|b
> |-|-|-|-
> |N|`[0, 1]`|`[0, 2] --> [0, 1, 2]`|`[2]`
> |Y|`[0, 1, 2]`|`[0, 2] --> [0, 1, 2]`|`[2]`
> |Y|`[2]`|`[]`|`[2]`
> 
> Result:
> ![[10.18.26 NFA to DFA Result.png]]