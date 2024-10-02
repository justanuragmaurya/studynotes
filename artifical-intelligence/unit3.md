
# Unit 3: Knowledge Representation Techniques

### Weak Slot and Filler Structures: Semantic Nets, Frames
Weak slot and filler structures are frameworks used in AI to model the organization of knowledge. These structures offer flexibility compared to more formal systems like logic-based approaches.

#### 1. Semantic Nets:
Semantic networks (semantic nets) represent knowledge using a graph structure. Concepts or objects are represented by nodes, while edges capture relationships.

##### Example:
- "A dog is a mammal."
- "A dog has a tail."
- "John owns a dog."

This could be represented as:
- A node for "Dog," "Mammal," "Tail," and "John."
- Connections between "Dog" and "Mammal" using an "is a" edge.
- Connections between "Dog" and "Tail" using a "has" edge.

##### Characteristics of Semantic Nets:
- **Hierarchical structure:** General concepts like "animal" can have more specific ones like "dog."
- **Inheritance:** Properties from higher categories, e.g., "dog" inherits "can breathe" from "animal."
- **Associative network:** Focuses on associations between concepts.

#### 2. Frames:
Frames are designed to capture typical situations or concepts. Each frame contains slots (attributes or properties) and fillers (values for those attributes).

##### Example:
A frame for a "dog" might have:
- Slots for "Color" with a default of "Brown" but overridden with "Black" for a specific dog named Rex.
- Inheritance of attributes such as "has a tail" from a general "Animal" frame.

##### Characteristics of Frames:
- **Slots and Fillers:** Used to represent properties.
- **Inheritance:** Frames can inherit from more general frames.
- **Procedural Attachments:** Procedures triggered when values are required.

### Strong Slot and Filler Structures: Conceptual Dependency, Scripts
These structures are more formal than weak structures and facilitate machine reasoning in constrained contexts.

#### 1. Conceptual Dependency (CD):
CD captures the underlying meaning of actions using primitive actions (e.g., **PTRANS** for physical transfer).

##### Example:
For the sentence "John gave a book to Mary":
- Action: ATRANS (abstract transfer)
- Agent: John
- Object: Book
- Recipient: Mary

#### 2. Scripts:
Scripts model stereotypical sequences of events, such as going to a restaurant. They describe typical actions and roles.

##### Example:
**Restaurant Script**:
- Entry: Customer enters.
- Order: Customer orders food.
- Payment: Customer pays for the meal.
- Exit: Customer leaves.

Scripts also capture causal and temporal relations between events.

---

### Game Playing: Evaluation Function
In AI game-playing, an evaluation function assigns a numerical score to game states, guiding the AI in making optimal moves.

#### Key Characteristics:
- **Heuristic-based:** Uses approximations for complex game states.
- **Player-centric:** Favors one player when evaluating.

#### Example Components in Chess:
- Material balance
- Positional control
- Mobility
- King safety

---

### Minimax Algorithm:
Minimax is used to determine optimal moves in two-player, zero-sum games by recursively evaluating possible outcomes.

#### Key Principles:
- **Maximizer vs. Minimizer:** One player tries to maximize, while the other minimizes the score.
- **Zero-Sum Game:** One player's gain is the other's loss.
- **Complete Knowledge:** Both players have full knowledge of the game state.

---

### Alpha-Beta Pruning:
An optimization for Minimax, alpha-beta pruning reduces the number of nodes evaluated in the search tree by cutting off branches that cannot affect the final outcome.

#### Benefits:
- Reduces time complexity.
- Allows deeper searches without compromising optimal decisions.

---

### Simple Two-Player Game Example:
For a game where Player A (Max) and Player B (Min) take turns picking numbers, Alpha-Beta pruning helps evaluate which branches to cut, focusing on the most promising paths.

---

