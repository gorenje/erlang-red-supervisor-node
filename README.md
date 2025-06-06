# Erlang Supervisor Node

**Note**: Nodes are exclusively for [Erlang-Red](https://github.com/gorenje/erlang-red), not to be used with Node-RED.

Erlang has the concept of workers and Supervisors, together they build a process tree that is self-healing.

A supervisor is designed to monitor a number of child processes (either workers or fellow supervisors) and when one or more fail, the supervisor is responsible for restarting the process.

This node allows for the definition of dynamic supervisors to monitor a set of nodes (which in ErlangRED are all processes) and restart as necessary.

For more details, [Erlang Documentation](https://www.erlang.org/doc/apps/stdlib/supervisor.html).

Example [flow](https://flows.red-erik.org/f/83c5e1824f32abec).

## Erlang Module

Node for defining the code for an erlang module.

## Erlang statemachine

Node for defining a [state machine](https://www.erlang.org/doc/apps/stdlib/gen_statem) as a node. This uses an erlmodule node as handler, so that the state machine can be completely defined inside of Erlang-Red. Example [flow](https://flows.red-erik.org/f/5672fa442b2b881d).

## Erlang event handler

Event handler [gen_event](https://www.erlang.org/doc/apps/stdlib/gen_event.html).

