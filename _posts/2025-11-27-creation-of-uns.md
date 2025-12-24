---
layout: post
title: "Introducing UNS: A New Foundation for Computation and Meaning"
date: 2025-11-27
categories: uns
tags: [UNS, mathematics, runtime, systems]
layout: single
author_profile: true
read_time: true
toc: false
toc_label: "Contents"
toc_icon: "list"

---

There are certain problems in computing that keep resurfacing no matter how many abstractions we build.  
You see them in symbolic systems, probabilistic modeling, distributed reasoning, and even in the finer details of everyday application logic when uncertainty, partiality, or undefined behavior creeps in.

Across all these domains, we tend to contort the tools we already have—scalars, arrays, objects, neural nets—into shapes they were never designed to hold. And when they inevitably break, we patch them with exceptions, special cases, or layers of indirection.

Over the last few years, I found myself running into these same structural cracks over and over again. Eventually, a simple realization emerged:

**The problem wasn’t the models.  
The problem was the numbers.**

We were asking atomic numbers to carry multi-dimensional, state-dependent, sometimes contradictory information, and then punishing them for not being able to do it gracefully.

So I went back to the beginning to determine what numbers really are, and then worked forward through what emerged. Following is one possible result.

This is the first public introduction to **UNS**, the *Universal Number Set*—a foundation for numerical reasoning that treats numbers not as isolated atoms but as structured, distributed objects with a meaningful internal universe.

---

## The core idea is simple:  
**A number is not a point.  
A number is a distribution of value across a universe of microstates.**

Classical arithmetic treats `7` as a single indivisible object. In UNS, that same `7` is represented as a constant function over a space of microstates. That may sound like unnecessary overhead, but it opens the door to an important generalization:

- Classical numbers become a *subset* of a larger, richer world.  
- Distributed values—functions over microstates—become numbers in their own right.  
- Undefined operations don’t halt execution; they produce *new values* that carry full provenance.  
- Dimension becomes a representational detail, not part of the meaning.  
- Readout gives you a classical number only when you need one.

The goal isn’t to replace classical math. In fact, UNS preserves classical arithmetic exactly when the values you give it are classical. But when your model goes beyond the classical world—and modern computation increasingly does—UNS gives you a consistent, principled way to operate without resorting to exceptions or ad-hoc structures.

---

## Why build UNS at all?

Because after two decades of building systems—large, small, neural, symbolic, engineered, emergent—you eventually see the same pattern:  
every field invents its own workaround for where classical numbers fall short.

Machine learning uses tensors and softmax.  
Physics uses fields and Hilbert spaces.  
Programming languages use try/catch and option types.  
Databases use NULL.  
Functional languages wrap everything in monads.  
Your average engineer writes a comment apologizing to the next person.

UNS expresses all these patterns through one consistent notion:  
a number as a structured, microstate-indexed object.

The result is not a high-level language or framework, but a **mathematical substrate**—a simple, compact, extensible model beneath everything else you might build. Something closer to integers and floating-point formats than to a library or toolkit.

---

## What UNS provides

Here is the short list of what UNS gives you out of the box:

### **1. A universal representation for numbers**  
Every UNS number is a function over microstates.  
Classical numbers embed as constant functions.

### **2. A principled way to interpret values**  
A *state*—also a function—tells you how to read a UNS value as a classical scalar.

### **3. A unified algebra of operations**  
All classical functions lift cleanly into UNS without domain restrictions.  
If classical math doesn’t define a result (like dividing by zero), UNS does:
it generates a **novel value** with full provenance.

### **4. Dimensional invariance**  
UNS does not tie meaning to dimensional representation.  
A state can be 1-dimensional or 500-dimensional—readout returns the same numeric result.

### **5. A portable runtime**  
The baseline implementation uses nothing more than Q16.16 fixed-point numbers and 32-bit integer arithmetic.  
This makes UNS implementable anywhere, from GPUs to microcontrollers.

### **6. A complete specification**  
Modules define:
- foundations and universe  
- axioms and core rules  
- syntax and grammar  
- types and lifted functions  
- dimensional equivalence  
- concrete runtime models  
- aggregates, collections, and integration  

It is small, but it is complete.

---

## What makes UNS different?

UNS is designed to **extend classical mathematics without breaking it.**  
You can work entirely in familiar territory if you like. Everything behaves normally:

- addition is addition  
- multiplication is multiplication  
- square roots work over complex numbers  
- readout returns classical scalars exactly as expected  

But when you hit something classical math considers illegal, UNS doesn’t collapse:

- divide by zero  
- log of a negative number without domain extension  
- operations over mixed domains  
- partial functions in corner cases  

Instead of halting, UNS creates *new*, well-typed values that live inside the same unified system.  
These values carry structured provenance, so nothing ever “disappears into an exception.”

This creates a numerical environment where nothing is undefined, yet everything remains traceable.

---

## What can you do with it?

UNS began as a simple thought experiment. From it emerged a general-purpose foundation for:

- symbolic reasoning and hybrid systems  
- probabilistic and statistical models  
- distributed state machines  
- interpretable neural-symbolic bridges  
- numerical simulations involving partial operations  
- speculative mathematical exploration  

The runtime is small enough to embed anywhere.  
The semantics are clean enough to formally analyze.  
The expressive space is large enough to build entire domains on top of it.

---

## What comes next?

The UNS repository includes:

- the full specification  
- the guided discovery document  
- modules covering semantics, operations, types, examples, and runtime  
- reference implementations  
- addendums for aggregates and integrations  

More is coming:  
domain translators, higher-level tooling, benchmark suites, and several experimental applications built entirely on UNS.

I’ve spent much of my career designing systems that needed something like UNS but didn’t have it yet. Now that it's real, I’m excited to see what other people may build on it.

If UNS interests you, or if you find yourself struggling with the limits of classical numbers in your own systems, feel free to explore the repository or reach out. This is only the beginning of what UNS can do.

[https://github.com/ReedKimble/UNS](https://github.com/ReedKimble/UNS)

---

*UNS is small, simple, and surprisingly powerful. Sometimes changing the foundation changes everything.*
