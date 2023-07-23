#Computer 
In [[Comput]] [[programming]], an S-expression (or [[symbol]]ic expression, abbreviated as sexpr or sexp) is an expression in a like-named notation for [[nested list]] ([[tree-structure]]d) [[data]]. S-expressions were invented for and popularized by the programming language [[Lisp]], which uses them for [[source code]] as well as data.

In the usual parenthesized [[Synta]] of Lisp, an S-expression is classically defined[1] as

an atom of the form x, or
an expression of the form (x . y) where x and y are S-expressions.

This definition reflects LISP's representation of a list as a series of "cells", each one an ordered pair. In plain lists, y points to the next cell (if any), thus forming a list. The recursive clause of the definition means that both this representation and the S-expression notation can represent any [[binary tree]]. However, the representation can in principle allow [[circ]]ular references, in which cases the structure is not a tree at all, but a [[cyclic]] [[graph]], and cannot be represented in classical S-expression notation unless a convention for cross-reference is provided (analogous to [[SQL]] foreign keys, [[SGML]]/[[XML]] [[IDREF]]s, etc.). Modern Lisp dialects such as Common Lisp[2] and Scheme[3] provide such syntax via datum labels, with which objects can be marked, which can then recur elsewhere, indicating shared rather than duplicated structure, enabling the reader or printer to detect and thus trigger evaluation or display of cycles without infinitely recursing


