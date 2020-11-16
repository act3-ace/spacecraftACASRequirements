# spacecraftACASRequirements
This is a set of requirements written in the Specification and Analysis of Requirements (SpeAR) tool for formal analysis.

Approved for public release; distribution is unlimited. Case Number: 88ABW-2020-0449.

The code in this repository corresponds to work in: 

[1] Hobbs, K. L., “Elicitation and Formal Specification of Run Time Assurance Requirements for Aerospace Collision Avoidance Systems,” Doctoral Dissertation, Aerospace Engineering, Georgia Institute of Technology, May 2020.

[2] Kerianne L. Hobbs and Eric M Feron, “Formal Specification and Analysis of Spacecraft Collision Avoidance Run Time Assurance Requirements.” IEEE Aerospace, Big Sky, MT, 6-13 Mar 2021.

[3] Kerianne L. Hobbs, Alexander R. Collins, and Eric Feron, “Risk-Based Formal Requirement Elicitation for Automatic Spacecraft Maneuvering,” AIAA SciTech, 11-15 Jan 2021, Nashville, TN.

[4] Hobbs, K. L., Perez, I., Fifarek, A. W., Feron, E. M., “Formal Specification and Verification of System States for Spacecraft Automatic Maneuvering” 2019 AIAA Information Systems-AIAA Infotech @ Aerospace, San Diego, California 7-11 January, 2019.


This repository contains the design specifications and requirements in formal logic (past time linear temporal logic), which can be analyzed manually for common patterns and automatically with formal methods for realizability, logical entailment, logical consistency, and traceability using the SpeAR tool, available here: https://github.com/lgwagner/SpeAR.

Logical entailment analysis shows that a metamodel defined by design specifications meets the atomic safety requirements. This is completed by evaluating that a conjunction of the design specifications and assumptions satisfy requirements (A1 ∧ A2 ∧ ... ∧ An ∧ D1 ∧ D2 ∧ ... ∧ Dm =⇒ Ri). Logical entailment is usually shown by proof. In some cases proof can be generated automatically using tools like model checking. When the expression is too complex interactive proof tools like theorem provers are typically employed. Model checking  is an automatic verification technique that shows a model of a concurrent system satisfies properties in temporal logic. Several techniques may be applied to do this including binary decision trees, k-induction, and property directed graphs. The logical entailment in this work is accomplished with k-induction model checking.

Logical Consistency checks that the design specification items and assumptions are free of conflicts for N time steps.

Realizability checks that the design specification can coexist for all possible input conditions that satisfy the requirements (A1 ∧ A2 ∧ ... ∧ An ∧ D1 ∧ D2 ∧ ... ∧ Dm). 

Traceability analysis shows which design specifications fulfill each of the requirements. In complex state machines, traceability analysis may be used to analyze the system logic to determine if there is a reduced set of logic may be used to describe the system transitions. The benefit of reducing the logic with logic equivalence is that it may be easier to implement and verify in a complete system. The disadvantage is that the intuition is lost as to why the logic is written a certain way. During early system analysis, an intuitive
set of logic may be constructed and proved equivalent to a simpler set of logic which is implemented. One way to reduce to a smaller, logically equivalent set is to evaluate whether the design specifications which define the state machine are unnecessary to meet the desired requirements.
