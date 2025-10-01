# Erlang Supervisor Node

**Note**: Nodes are implemented for [Erlang-Red](https://github.com/gorenje/erlang-red) and cannot - yet - be used with Node-RED but they can be installed in Node-RED.

What this package provides are key [OTP](https://www.erlang.org/doc/system/design_principles.html) behaviours from Erlang in a visual, Node-RED style to be used in flows to create more robust flows.

Erlang has the concept of workers and supervisors, together they build a process tree that is self-healing. Everything is process in Erlang, lightweight, independent processes is the key to Erlang.

A supervisor is designed to monitor a number of child processes (either workers or fellow supervisors) and when one or more fail, the supervisor is responsible for restarting those failed process. For more details, [Erlang Documentation](https://www.erlang.org/doc/apps/stdlib/supervisor.html).

A supervisor is a *behaviour* and a behaviour is a definition of a generic action/workflow/activity. These nodes also implement some of the more common behaviours in Erlang:

- Event handler for triggering functionality on specific events. Events are fire and forget, there is no synchronisation.

- Generic Server which is probably the most common behaviour. It is important as it allows processes to have atomic state in a concurrent/parallel system.

- Statemachine behaviour provides a generic approach to define clear state transitions based on actions occurring.

## Erlang Module

Behaviours require modules for callbacks, that is what the module node provides. It is similar to the function node only that it provides a library of functions. Module nodes are not executed, they define code that can be used by other nodes in Erlang-Red.

## Behaviour Documentation

- Event handler [gen_event](https://www.erlang.org/doc/apps/stdlib/gen_event.html).
- Statemachine [gen_statem](https://www.erlang.org/doc/apps/stdlib/gen_statem.html).
- Generic Server [gen_server](https://www.erlang.org/doc/apps/stdlib/gen_server.html).

## Resources

If you are interested in learning more about the project or Erlang then check out:

- [learn you some Erlang](https://learnyousomeerlang.com) for a solid description of the core Erlang concepts
- [Erlang official documentation](https://www.erlang.org/doc/readme.html) which is high level overview of Erlang
- [Erlang standard library](https://www.erlang.org/doc/apps/stdlib/api-reference.html) for the APIs.

To learn more about Erlang-Red:

- [Video of me talking about Erlang-Red](https://blog.tadsummit.com/2025/09/17/erlang-red/)
- [Erlang-Red presented in the Node-RED forum](https://discourse.nodered.org/t/erlang-red-erlang-backed-node-red/96458)
- [GitHub project page](https://github.com/gorenje/erlang-red)

## Artifacts for these nodes

- [NPMjs Package](https://www.npmjs.com/package/@gregoriusrippenstein/erlang-red-supervisor-node)
- [Node-RED node package](https://flows.nodered.org/node/@gregoriusrippenstein/erlang-red-supervisor-node)
- [GitHub Repo](https://github.com/gorenje/erlang-red-supervisor-node)
- Node-RED flow that maintains this [codebase](https://flowhub.org/f/d5b52b27a613e8c0).
