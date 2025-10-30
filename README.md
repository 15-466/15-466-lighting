# Lighting Demo

A demonstration comparing multi-pass, forward, and deferred rendering methods.

See [DemoLightingMultipassMode.cpp](DemoLightingMultipassMode.cpp), [DemoLightingForwardMode.cpp](DemoLightingForwardMode.cpp), and [DemoLightingDeferredMode.cpp](DemoLightingDeferredMode.cpp) for the implementations.


Multi-pass lighting draws the scene once per light, using a shader that only deals with one light at a time, and adds up the contributions.

Forward lighting draws the scene once, using a shader that loops over all lights.

Deferred lighting draws information about the scene to off-screen buffers, then draws each *light*, using a shader that reads information about the scene from these buffers.

This game was built with [NEST](NEST.md).
