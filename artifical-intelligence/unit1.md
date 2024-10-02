# ARTIFICIAL INTELLIGENCE AND EXPERT SYSTEMS (CSE209)


## Introduction
- What is intelligence?
- What is artificial intelligence?
- Foundations of Artificial Intelligence (AI)
- History of AI
- Basics of AI: AI Problems, AI Techniques, Applications of AI, Branches of AI

### Problem Spaces and Search
- Defining the problem as a state space search
- Production systems, Problem characteristics, Production system characteristics
- Issues in designing search problems
- Breadth-First Search (BFS), Depth-First Search (DFS), Bidirectional Search, Iterative Deepening

## Intelligence
- "Ability to learn, understand, and think" (Oxford Dictionary) and apply knowledge and skills.
- It involves problem-solving, reasoning, adapting to new situations, and understanding complex ideas.
- Intelligence can manifest in analytical, creative, practical, and emotional forms.

## Theories of Intelligence
1. **General Intelligence (g factor)**: Proposed by Charles Spearman, intelligence is a single ability that influences various cognitive tasks.
2. **Multiple Intelligences**: Howard Gardner’s theory of different types of intelligence like linguistic, logical-mathematical, musical, etc.
3. **Triarchic Theory**: Robert Sternberg’s model divides intelligence into analytical, creative, and practical components.
4. **Emotional Intelligence (EI)**: Popularized by Daniel Goleman, focuses on recognizing and managing one's emotions and others.

## Artificial Intelligence (AI)
- AI refers to developing systems capable of performing tasks that require human intelligence.
- Tasks include reasoning, learning, problem-solving, perception, language understanding, and decision-making.

### Categories of AI
1. **Narrow AI (Weak AI)**: Designed for specific tasks (e.g., Siri, Alexa).
2. **General AI (Strong AI)**: A theoretical system with general intelligence like humans.
3. **Superintelligent AI**: Surpassing human intelligence, still theoretical.

## AI Technologies
- **Machine Learning (ML)**: Systems that learn from data.
- **Deep Learning**: Neural networks with many layers, used for image recognition, NLP, etc.
- **Natural Language Processing (NLP)**: Machines understanding and generating human language.
- **Computer Vision**: Machines interpreting visual information.
- **Robotics**: AI combined with robotics to perform physical tasks.

## Applications of AI

### 1. Healthcare
- Medical diagnosis, personalized treatment, drug discovery.
  
### 2. Finance
- Fraud detection, algorithmic trading, risk management, customer service.

### 3. Retail and E-commerce
- Recommendation systems, inventory management, price optimization.

### 4. Transportation and Logistics
- Autonomous vehicles, traffic management, route optimization, predictive maintenance.

### 5. Manufacturing
- Quality control, robotics, predictive maintenance, supply chain optimization.

### 6. Entertainment
- Content creation, personalized recommendations, deepfakes.

### 7. Education
- Personalized learning, tutoring systems, grading, and administrative tasks.

### 8. Customer Service
- AI chatbots, sentiment analysis, voice assistants.

### 9. Human Resources
- Recruitment, employee engagement, performance evaluation.

### 10. Agriculture
- Precision farming, crop monitoring, yield prediction.

### 11. Security and Surveillance
- Facial recognition, anomaly detection, cybersecurity.

### 12. Environmental Monitoring
- Climate modeling, wildlife conservation, pollution control.

## Branches of AI Problem Spaces and Search
Problem spaces and search are fundamental to how AI systems solve problems.

### 1. Problem Spaces in AI:
A problem space consists of all possible states that can be reached while solving a problem:
- **State Space**: All possible states (e.g., each configuration in a chess game).
- **Initial State**: The starting point of the problem.
- **Goal State(s)**: The final state(s) to reach.
- **Actions (Operators)**: Moves to transition between states.
- **Path Cost**: The cost function for each path.

### 2. Search in AI
Search is the process of navigating the problem space to find a solution. Two main types:
- **Uninformed Search (Blind Search)**: BFS, DFS, Uniform-Cost Search, Iterative Deepening Search, Bidirectional Search.
- **Informed Search (Heuristic Search)**: Greedy Best-First Search, A* Search, IDA*, Memory-Bounded A*, Hill Climbing.

### Problem-Space Representation Techniques:
- **Graph Search Representation**: Treats problem space as a graph.
- **Tree Search Representation**: Visualizes each decision as a branch of a tree.

### Production System
A model of computation using rules (productions) to transform an initial state into a goal state.

#### Components:
- **Working Memory**: Stores the current state.
- **Rule Base**: Condition-action pairs.
- **Control System**: Rule interpreter deciding the order of applying rules.
- **Goal**: The final state.

### Types of Production Systems:
- **Monotonic**: Adds facts but doesn't remove.
- **Non-Monotonic**: Can revise earlier decisions.
- **Deterministic**: No ambiguity in rule selection.

### Applications of Production Systems:
- Expert systems, AI planning, NLP, Cognitive modeling.

### Key Characteristics:
- Rule-based structure, Modularity, Separation of knowledge and control, Forward/Backward chaining, Goal-oriented behavior.

### Example: Jug Problem
Objective: Obtain 4 liters exactly in a 5-liter jug. A solution could be steps 1,8,4,6,1,8 or 3,5,3,7,2,5,3,5.

## Heuristic Functions and Algorithms

### Heuristic Function:
A method to estimate the best path or solution in problems where exact solutions are costly.

### Algorithm and Shortest Path:
- **A* (A-star) algorithm**: Finds the shortest path between two nodes, used in GPS, robotics, etc.

### Constraint Satisfaction Problems (CSPs):
Used for solving problems with a set of constraints (e.g., scheduling, resource allocation).

#### Example: Map Coloring Problem
Objective: Color regions so no two adjacent regions have the same color.

Final Solution:
- A = Red
- B = Green
- C = Blue
- D = Red