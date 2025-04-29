# csed342---assignment-8-from-language-to-logic-solved
**TO GET THIS SOLUTION VISIT:** [CSED342 – Assignment 8. From Language to Logic Solved](https://www.ankitcodinghub.com/product/csed342-assignment-8-from-language-to-logic-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115702&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSED342 - Assignment 8. From Language to Logic Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Hwanjo Yu

CSED342 – Artificial Intelligence

General Instructions

This (and every) assignment has a written part and a programming part.

Ò This icon means a written answer is expected in writeup.pdf.

¥ This icon means you should write code in submission.py.

You should modify the code in submission.py between

# BEGIN_YOUR_CODE and

# END_YOUR_CODE

but you can add other helper functions outside this block if you want. Do not make changes to files other than submission.py.

Your code will be evaluated on two types of test cases, basic and hidden, which you can see in grader.py. Basic tests, which are fully provided to you, do not stress your code with large inputs or tricky corner cases. Hidden tests are more complex and do stress your code. The inputs of hidden tests are provided in grader.py, but the correct outputs are not. To run all the tests, type

python grader.py

This will tell you only whether you passed the basic tests. On the hidden tests, the script will alert you if your code takes too long or crashes, but does not say whether you got the correct output. You can also run a single test (e.g., 1a-0-basic) by typing

python grader.py 1a-0-basic

We strongly encourage you to read and understand the test cases, create your own test cases, and not just blindly run grader.py.

In this assignment, you will get some hands-on experience with logic. You’ll see how logic can be used to represent the meaning of natural language sentences. Most of this assignment will be translating English into logical formulas, but in Problem 2, we will delve into the mechanics of logical inference.

To get started, launch a Python shell and try typing the following commands to add logical expressions into the knowledge base.

from logic import *

Rain = Atom(“Rain”) # Shortcut

Wet = Atom(“Wet”) # Shortcut

kb = createResolutionKB() # Create the knowledge base

kb.ask(Wet) # Prints “I don’t know.”

kb.ask(Not(Wet)) # Prints “I don’t know.”

kb.tell(Implies(Rain, Wet)) # Prints “I learned something.”

kb.ask(Wet) # Prints “I don’t know.”

kb.tell(Rain) # Prints “I learned something.”

kb.tell(Wet) # Prints “I already knew that.”

kb.ask(Wet) # Prints “Yes.”

kb.ask(Not(Wet)) # Prints “No.”

kb.tell(Not(Wet)) # Prints “I don’t buy that.”

To print out the contents of the knowledge base, you can call kb.dump(). For the example above, you get:

==== Knowledge base [3 derivations] ===

* Or(Not(Rain),Wet)

* Rain

– Wet

In the output, ‘*’ means the fact was explicitly added by the user, and ‘-’ means that it was inferred. Here is a table that describes how logical formulas are represented in code. Use it as a reference guide:

Name Mathematical notation Code

Atomic formula

(atom) Rain Atom(“Rain”) (predicate must be uppercase)

Negation ¬Rule Not(Atom(“Rain”))

Conjunction Rain ∧ Snow And(Atom(“Rain”), Atom(“Snow”))

Disjunction Rain ∨ Snow Or(Atom(“Rain”), Atom(“Snow”))

Implication Rain → Wet Implies(Atom(“Rain”), Atom(“Wet”))

Equivalence Rain ↔ Wet (syntactic sugar for Equiv(Atom(“Rain”), Atom(“Wet”))

Rain → Wet ∧ Wet → Rain)

The operations And and Or only take two arguments. If we want to take a conjunction or disjunction of more than two, use AndList and OrList. For example: AndList([Atom(“A”), Atom(“B”), Atom(“C”)]) is equivalent to And(And(Atom(“A”), Atom(“B”)), Atom(“C”)).

Problem 1. Propositional logic

Write a propositional logic formula for each of the following English sentences in the given function in submission.py. For example, if the sentence is “If it is raining, it is wet,” then you would write Implies(Atom(“Rain”), Atom(“Wet”)), which would be Rain → Wet in symbols (see examples.py). Note: Don’t forget to return the constructed formula!

Problem 1a [2 points] ¥

“If it’s summer and we’re in California, then it doesn’t rain.”

Problem 1b [2 points] ¥

“It’s wet if and only if it is raining or the sprinklers are on.”

Problem 1c [2 points] ¥

“Either it’s day or night (but not both).”

You can run the following command to test each formula: python grader.py 1a

If your formula is wrong, then the grader will provide a counterexample, which is a model that your formula and the correct formula don’t agree on. For example, if you accidentally wrote And(Atom(“Rain”), Atom(“Wet”)) for “If it is raining, it is wet,”, then the grader would output the following:

Your formula (And(Rain,Wet)) says the following model is FALSE, but it should be TRUE:

* Rain = False

* Wet = True

* (other atoms if any) = False

In this model, it’s not raining and it is wet, which satisfies the correct formula Rain → Wet (TRUE), but does not satisfy the incorrect formula Rain ∧ Wet (FALSE).

Problem 2. Logical Inference

Having obtained some intuition on how to construct formulas, we will now perform logical inference to derive new formulas from old ones. Recall that:

• Modus ponens asserts that if we have two formulas, A → B and A in our knowledge base, then we can derive B.

• If A ∧ B is in the knowledge base, then we can derive both A and B.

Also, we will use conjunctive normal form (CNF). A CNF formula is a conjunction of clauses. Example: (A∨B∨¬C)∧(¬B∨D). Every formula f in propositional logic can be converted into an equivalent CNF formula f0: M(f) = M(f0). Some conversion rules are below.

• Eliminate

• Eliminate

• Move ¬ inwards:

• Move ¬ inwards:

• Eliminate double negation:

• Distribute ∨ over

Problem 2a [5 points] Ò

Some inferences that might look like they’re outside the scope of Modus ponens are actually within reach. Suppose the knowledge base contains the following formulas:

KB = {(A ∨ B) → C,A}.

Your task: First, convert the knowledge base into conjunctive normal form (CNF). Then apply Modus ponens to derive C. Please show how your knowledge base changes as you apply derivation rules.

Remember, this isn’t about you as a human being able to arrive at the conclusion, but rather about the rote application of a small set of transformations (which a computer could execute).
