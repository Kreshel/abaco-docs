.. _state:

===========
Actor State
===========

In this section we describe the state that persists (or not) through Abaco actor container executions.

State
-------

When an actor is registered, the :stateless: property is automatically set to 'false'. In order to maintain state across executions, an actor must be registed with :stateless=false:

actor writes state to state endpoint(over HTTP with some latency) and worker injects it back in when actor is called again