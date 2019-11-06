# sicp-notes
SICP notes


I want to create some notes that I take when I'm reading the SICP book.

I'm not intending to solve the entirity of the book, instead, I want to read thorugh the book and make notes that will allow me to skim the chapters easily.


# Chapter 1.1

## Every powerful language has three mechanisms for accomplishing this:

* primitive expressions, which represent the simplest entities the language is concerned with,
* means of combination, by which compound elements are built from simpler ones, and
* means of abstraction, by which compound elements can be named and manipulated as units.

* In programming, we deal with two kinds of elements: procedures and data

* A critical aspect of a programming language is the means it provides for using names to refer to computational objects. We say that the name identifies a variable whose value is the object.

# Evaluation orders:

* Applicative order versus normal order

## Applicative order

The interpreter first evaluates the operator and operands and then applies the resulting procedure to the resulting arguments

## Normal order

Not evaluate the operands until their values were needed. Instead it would first substitute operand expressions for parameters until it obtained an expression involving only primitive operators, and would then perform the evaluation.

# Procedures as Black-Box Abstractions


## Local names

### Bound variables
A formal parameter of a procedure has a very special role in the procedure definition, in that it doesn’t matter what name the formal parameter has

### Free variables

If a variable is not bound, we say that it is free. The set of expressions for which a binding defines a name is called the scope of that name.


# Chapter 1.2 Procedures and the Processes They Generate

A procedure is a pattern for the local evolution of a computational process. It specifies how each stage of the process is built upon the previous stage. We would like to be able to make statements about the overall, or global, behavior of a process whose local evolution has been specified by a procedure. This is very difficult to do in general, but we can at least try to describe some typical patterns of process evolution.

## Linear Recursion and Iteration

The expansion occurs as the process builds up a chain of deferred operations (in this case, a chain of multiplications). The contraction occurs as the operations are actually performed. This type of process, characterized by a chain of deferred operations, is called a recursive process. Carrying out this process requires that the interpreter keep track of the operations to be performed later on.

In general, an iterative process is one whose state can be summarized by a fixed number of state variables, together with a fixed rule that describes how the state variables should be updated as the process moves from state to state and an (optional) end test that specifies conditions under which the process should terminate.
