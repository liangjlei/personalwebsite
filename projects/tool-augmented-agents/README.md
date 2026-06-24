# Tool-Augmented General-Purpose Agents: Planning and Sandboxed Execution

**Jinglei Liang** · Technical Note, 2026

## Abstract
A study and extension of a ReAct-style general-purpose agent that *plans*,
*selects tools*, and *executes* them in a sandbox with a pluggable LLM backend.
I use it as a testbed for connecting general agents to the perception and
robotics services in my other projects.

## What I did
- Analyzed the **plan → select-tool → execute → observe** loop and its failure
  modes.
- Added and evaluated **custom tools** (retrieval, file/code, service calls).
- Wired the agent to external robotics/perception services as callable tools.

## Notes
This builds on a well-known open-source agent framework; credit for the base
framework belongs to its original authors. This write-up covers my experiments
and extensions only.
