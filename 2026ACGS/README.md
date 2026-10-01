# 2026ACGS

## ChatGPT (July 2026)

### Summary

Modern C++ MPI wrappers must reconcile language-level types, ownership, and deterministic lifetimes with MPI's opaque handles, global state, and underspecified mutation rules. Rather than proposing another concrete binding, this paper develops design guidance for a future high-level interface. It examines RAII representations of MPI objects, the consequences of `const` for communicators, compile-time mapping from C++ types to MPI datatypes, and contiguous, sized, typed buffer concepts. Moving buffers into request objects can prevent invalid access during nonblocking communication, while compile-time checks, layered assertions, exceptions, and `std::expected` separate usage errors from recoverable failures. The discussion also covers serialization, datatype pools, and sensible defaults. It identifies specification gaps, especially datatype lifetimes under sessions and callback state, that obstruct safe automated resource management. The result is a conceptual blueprint, not a standardized API or performance evaluation.

### Contributions

1. Organized modern MPI C++ interface design around object models, types, lifetimes, ownership, and communication buffers.
2. Proposed C++ concepts for contiguous, sized, typed buffers with compile-time datatype checking.
3. Showed how move semantics can enforce exclusive buffer ownership during nonblocking operations.
4. Developed an idiomatic error-handling hierarchy spanning static checks, optional runtime assertions, exceptions, and `std::expected`.
5. Identified MPI specification ambiguities that must be resolved before robust language-level resource management is possible.
