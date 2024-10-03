# Techniques of Knowledge Representation

## Issues in Knowledge Representation
1. **Ambiguity**:  
   Ambiguity arises when information can be interpreted in multiple ways, leading to misunderstandings.
   
2. **Incompleteness**:  
   It is difficult to represent all knowledge comprehensively, which may result in incomplete reasoning.

3. **Inconsistency**:  
   Conflicting information in the knowledge base can cause logical contradictions.

4. **Scalability**:  
   As knowledge grows, performance challenges arise due to the increased data complexity.

5. **Expressiveness vs. Computability**:  
   There is often a trade-off between how expressively a system can describe concepts and its efficiency in processing.

6. **Context Sensitivity**:  
   The meaning of information changes depending on its context, which is difficult for AI systems to handle.

7. **Temporal Representation**:  
   Representing time and temporal relationships, such as durations and sequences, is complex.

8. **Knowledge Acquisition Bottleneck**:  
   Acquiring and encoding knowledge is labor-intensive, a challenge known as the knowledge acquisition bottleneck.

9. **Difficulty Representing Common Sense Knowledge**:  
   Common sense, which humans use effortlessly, is hard to formalize in AI.

## Techniques of Knowledge Representation

### 1. Logical Representation
Logical representation uses propositions and rules with concrete syntax and semantics for communication. It includes:

- **Propositional Logic**  
- **Predicate Logic**

**Advantages**:
- Enables logical reasoning.
- Basis for programming languages.

**Disadvantages**:
- Restrictive and may not be efficient.

### 2. Semantic Network Representation
Semantic networks use graphs to represent knowledge, with nodes for objects and arcs for relationships.

**Types of Relations**:
- **IS-A relation**
- **Kind-of relation**

**Advantages**:
- Natural and simple representation.

**Disadvantages**:
- High computational time and complexity.

### 3. Frame Representation
Frames are structures containing attributes (slots) and their values to represent entities. Frames evolve into modern classes and objects.

**Advantages**:
- Easy to program and extend.
- Default data inclusion.

**Disadvantages**:
- Inference mechanisms are not efficient.

### 4. Production Rules
Production rules consist of condition-action pairs, where rules are fired if conditions are met.

**Advantages**:
- Expressed in natural language.
- Modular and easy to modify.

**Disadvantages**:
- Lacks learning capabilities.
- Inefficient with multiple active rules.

---

# Types of Knowledge

1. **Declarative Knowledge**  
   Knowledge about something, expressed in declarative sentences.

2. **Procedural Knowledge**  
   Knowledge of how to perform tasks, including rules, strategies, and procedures.

3. **Meta-Knowledge**  
   Knowledge about other types of knowledge.

4. **Heuristic Knowledge**  
   Expert knowledge in the form of rules of thumb.

5. **Structural Knowledge**  
   Describes relationships between concepts (e.g., kind of, part of).

---

# Probabilistic Reasoning in Artificial Intelligence

## Uncertainty
Uncertainty arises when we are unsure about information. Probabilistic reasoning is used to handle uncertainty in AI systems.

**Causes of Uncertainty**:
- Unreliable sources
- Experimental errors
- Equipment faults

## Probabilistic Reasoning
Probabilistic reasoning applies probability to indicate uncertainty. It uses:

- **Prior Probability**: Probability before observing new information.
- **Posterior Probability**: Probability after new evidence is considered.
- **Conditional Probability**: Probability of an event occurring given another event has already happened.

### Bayes' Theorem
Bayes' theorem calculates the probability of an event based on prior knowledge of related conditions.

**Applications**:
- Robot navigation
- Weather forecasting
- Solving the Monty Hall problem

### Example:
- Given a set of prior data, we can calculate posterior probabilities to predict outcomes.

---

# Predicate Logic (First-Order Logic) in AI

Predicate logic extends propositional logic to represent more complex knowledge, including relationships between objects.

**Basic Elements**:
- **Objects**: Entities like people, numbers, or colors.
- **Relations**: Unary or n-ary relations (e.g., is adjacent to, brother of).
- **Functions**: Mappings like "father of," or "best friend of."

**Syntax**:  
- **Atomic Sentences**: Basic sentences with a predicate and terms.
- **Complex Sentences**: Formed by combining atomic sentences with logical connectives.

### Quantifiers in First-Order Logic:
1. **Universal Quantifier (∀)**: Statements true for all instances.
2. **Existential Quantifier (∃)**: Statements true for at least one instance.

### Examples:
- "All birds fly" → ∀x bird(x) → fly(x)
- "Some boys play cricket" → ∃x boys(x) → play(x, cricket)

---

# Differences Between Forward and Backward Reasoning in AI
- **Forward Reasoning**: Starts with known facts and works towards a goal.
- **Backward Reasoning**: Starts with the goal and works backwards to determine the necessary conditions.