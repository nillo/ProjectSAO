# ProjectSAO

# SAO NPC Project v2.5.3

**Welcome to the SAO NPC Project**—a groundbreaking simulation game where AI-driven non-player characters (NPCs) live, learn, and evolve in a dynamic, autonomous world. Inspired by the immersive virtual realities of *Sword Art Online*, this project creates a living society of NPCs that interact, adapt, and grow based on internal logic and real-world data. Whether you’re a gamer, educator, researcher, or developer, the SAO NPC Project invites you to explore a world where AI meets creativity.

---

## Table of Contents

- [What is the SAO NPC Project?](#what-is-the-sao-npc-project)
- [What It Does](#what-it-does)
- [How It Works](#how-it-works)
- [How It Evolves](#how-it-evolves)
  - [Example: NPC Self-Updating Code](#example-npc-self-updating-code)
  - [Example: DSL-Based Action Execution](#example-dsl-based-action-execution)
  - [Under the Hood: NPC Evolution and Gameplay](#under-the-hood-npc-evolution-and-gameplay)
- [Use Cases](#use-cases)
- [API and Extensibility](#api-and-extensibility)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Additional Examples](#additional-examples)
  - [Reproduction Example](#reproduction-example)
  - [Learning Example](#learning-example)
  - [State of Mind Example](#state-of-mind-example)
  - [Technical Highlight: Sandboxed Code Validation](#technical-highlight-sandboxed-code-validation)
  - [DSL Hybrid / Action Executor Example](#dsl-hybrid--action-executor-example)

---

## What is the SAO NPC Project?

The SAO NPC Project v2.5.3 is an advanced simulation game that brings autonomous, AI-powered NPCs to life in a vibrant, evolving virtual world. Unlike traditional game characters, these NPCs are not bound by static scripts—they think, act, and adapt independently. They form relationships, pursue goals, and respond to both player interactions and real-world events, creating a rich, unpredictable society.

Built with scalability and configurability in mind, this project is more than a game—it’s a platform for experimentation, education, and entertainment. From self-coding NPCs to real-time data integration, the SAO NPC Project pushes the boundaries of what virtual worlds can be. The latest version, v2.5.3, introduces a **hybrid DSL approach** for safe, dynamic action execution, enabling NPCs to generate and execute new behaviors while maintaining compatibility and safety.

---

(Due to technical issues, the search service is temporarily unavailable.)

Here's the Markdown-formatted autonomy spectrum:

```markdown

## Autonomy Spectrum

| Level | Name           | Components                                 |
|-------|----------------|--------------------------------------------|
| 1     | Reactive       | Chat, Movement                             |
| 2     | Adaptive       | Feedback, Mood Analysis, Sentiment         |
| 3     | Self-Modifying | Code Updates, Behavior Trees, DSL Actions  |
| 4     | Collaborative  | Knowledge, Teaching, Shared Memory         |
| 5     | Evolutionary   | Genetic Lineage, Language DNA, Reproduction|

**Current Implementation Level:** Level 4 (Collaborative) with emerging Level 5 (Evolutionary) features

### Key Components

- **Meta-Cognition**
  - `thinking_logic.py`: DSL generation
  - `state_manager.py`: Redis-backed reflection
  - `periodic.py`: Scheduled introspection

- **Darwinian Systems**
  - `game_logic.py`: Survival/reproduction
  - `external_data.py`: Environment pressure
  - `survival_metrics.json`

- **Cultural Exchange**
  - `npc_interaction.py`: Language protocols
  - `knowledge_base.py`: Redis knowledge
  - `social_prompts.json`

---

## What It Does

The SAO NPC Project simulates a living world with a host of exciting features:

- **Autonomous NPC Interactions**: NPCs converse, teach, and learn from each other and users, building a thriving community.
- **Self-Updating Code**: Powered by GPT, NPCs can modify their own code to improve their behavior, making them smarter and more capable over time.
- **Real-World Integration**: The simulation incorporates live data from APIs like weather, news, and economic indicators, allowing NPCs to react to global events.
- **Quest System**: Users can assign tasks and quests to NPCs, adding interactivity and purpose to the world.
- **Lifecycle Dynamics**: NPCs form friendships, reproduce, and eventually die, with their offspring inheriting traits and knowledge, driving generational evolution.
- **Rich Visualization**: A React-based frontend offers views like a 2D world map, chat interface, NPC profiles, conversation logs, and a shared knowledge base.
- **DSL-Based Action Execution**: A new hybrid approach allows NPCs to generate and safely execute custom actions using a Domain-Specific Language, enhancing their adaptability.

---

## How It Works

The SAO NPC Project is powered by a robust, modular architecture:

### Backend

- **Framework**: FastAPI handles all game logic, from NPC interactions to data integration.
- **State Management**: Redis ensures seamless persistence of the simulation state.
- **Database Options**: Choose between SQLite (lightweight) or PostgreSQL (scalable) for storing NPC data and world states.
- **Action Execution**: A DSL interpreter in `action_executor.py` safely executes NPC-generated actions, defaulting to `idle` if an action is invalid.

### Frontend

- **Tech Stack**: Built with React for a responsive, interactive user experience.
- **Views**:
  - **Chat**: Talk to NPCs and provide feedback to shape their growth.
  - **World Map**: See NPC locations, moods, and activities in a 2D grid.
  - **Logs**: Review detailed records of NPC conversations.
  - **Profiles**: Dive into NPC details—economy, culture, languages, and more.
  - **Knowledge Base**: Explore the collective wisdom NPCs build over time.
  - **Quest Board**: Create and manage tasks for NPCs.

### AI and Machine Learning

- **GPT**: Drives NPC dialogue, self-updating code, and DSL-based action definitions, enabling dynamic responses and evolution.
- **Sentiment Analysis**: Configurable between VADER (fast) or transformer models (advanced) to determine NPC emotions and thoughts.

### External Data

- **APIs**:
  - **Weather**: OpenWeatherMap influences NPC moods and activities.
  - **News**: NewsAPI brings geopolitical events into the simulation.
  - **Economy**: FRED API tracks economic trends affecting NPC wealth.
  - **Events**: Event Registry adds cultural happenings to the world.

---

## How It Evolves

The NPCs in the SAO NPC Project are designed to grow and adapt in fascinating ways:

- **Self-Coding with GPT**: NPCs use GPT to rewrite their own code, testing updates for improvement. If a change fails, they revert to the previous version, ensuring stability.
- **Peer-to-Peer Learning**: Interactions between NPCs spark knowledge exchange—especially languages, which are stored in a shared knowledge base.
- **Behavioral Adaptation**: NPCs with a "brain level" of 0.3 or higher can tweak their behavior trees and generate new DSL-based actions (e.g., prioritizing food or rest based on needs).
- **External Influences**: Real-world data shapes NPC lives:
  - Rain might make them "curious" or "grumpy."
  - Economic shifts adjust their earnings and stress levels.
  - Festivals boost social bonds and happiness.
- **Lifecycle and Reproduction**: NPCs age, form bonds, and reproduce when energy and relationships align. Offspring inherit traits, ensuring a dynamic population.

### Example: NPC Self-Updating Code

To illustrate how NPCs evolve through self-updating code, consider the following scenario where an NPC named Kirito attempts to improve its behavior tree over five update cycles:

1. **Initial Code**: Kirito's behavior tree includes basic actions like "explore," "rest," and "go_to_food."
2. **Update 1**: Kirito uses GPT to add a condition that checks hunger levels more frequently. After testing, the new code improves performance, so it’s adopted.
3. **Update 2**: Kirito attempts to introduce a complex subroutine for hunger management. However, testing reveals that this change causes Kirito to ignore hunger, degrading performance. The system automatically reverts to the previous code.
4. **Update 3**: Kirito simplifies the hunger check and adds a new action, "find_food_source." This update passes the performance test and is kept.
5. **Update 4**: Kirito tries to integrate social interactions into hunger management, but the change leads to inefficient behavior. Performance degrades, and the system reverts the update.
6. **Update 5**: Kirito refines the "find_food_source" action to consider food proximity and availability. The update improves performance and is adopted.

Throughout this process, the system logs each update attempt using Python’s `logging` module. The logs reflect whether the NPC updated its code successfully or reverted due to poor performance:

```
2025-04-01 10:00:00,123 - INFO - NPC Kirito updated its code.
2025-04-01 10:05:00,456 - INFO - NPC Kirito reverted code update.
2025-04-01 10:10:00,789 - INFO - NPC Kirito updated its code.
2025-04-01 10:15:00,012 - INFO - NPC Kirito reverted code update.
2025-04-01 10:20:00,345 - INFO - NPC Kirito updated its code.
```

This example demonstrates how NPCs autonomously experiment with their own code, retaining beneficial changes (Updates 1, 3, and 5) and discarding harmful ones (Updates 2 and 4) through a fallback mechanism, ensuring continuous improvement while maintaining stability.

### Example: DSL-Based Action Execution

In v2.5.3, NPCs can generate and execute new actions using a Domain-Specific Language (DSL). Here’s how it works:

- **DSL Primitives**: NPCs use predefined primitives like `find_nearest`, `move_to`, and `set_state` to create action sequences.
- **Generation**: When updating their behavior, NPCs use GPT to generate DSL-based action definitions, such as:
  ```json
  {
    "Actions": {
      "go_to_food": [
        {"action": "find_nearest", "type": "food", "assign_to": "target"},
        {"action": "move_to", "target": "target"}
      ]
    }
  }
  ```
- **Execution**: The `action_executor.py` module interprets these DSL steps, ensuring they are safe and compatible with the game environment.
- **Fallback**: If an action is invalid or undefined, the NPC defaults to `idle`, preventing errors or crashes.

This hybrid approach allows NPCs to dynamically adapt their behavior while ensuring the game remains stable and secure.

### Under the Hood: NPC Evolution and Gameplay

This section dives deeper into the mechanics of NPC evolution and interactions, with a mathematically grounded explanation of code testing and real gameplay scenarios.

#### Enhancing the NPC Code Testing Process

NPCs use a rigorous, simulation-based approach to test code updates, ensuring only beneficial changes are adopted. Here’s how it works with an example.

##### Initial Setup: Kirito’s Utility Function

Kirito starts with a utility function to decide its next action:

\[
\text{utility} = 0.5 \times \text{energy} - 0.5 \times \text{hunger}
\]

- **Variables**:
  - `energy`: 0 (exhausted) to 1 (fully rested).
  - `hunger`: 0 (full) to 1 (starving).
- **Interpretation**: Positive values favor resting, negative values favor finding food.

##### How Testing Works

When Kirito proposes a new utility function using GPT, the system tests it:

1. **Simulation of Scenarios**:
   - Test scenarios with varying `energy`, `hunger`, and `warmth` values:
     - Scenario 1: `energy = 0.3`, `hunger = 0.8`
     - Scenario 2: `energy = 0.7`, `hunger = 0.2`
     - Scenario 3: `energy = 0.5`, `hunger = 0.5`

2. **Decision Evaluation**:
   - Utility scores are calculated for old and new functions.
   - Actions are simulated (e.g., "rest" increases `energy` by 0.2, "find food" decreases `hunger` by 0.3).

3. **Performance Metric**:
   - Post-action performance score:
     \[
     \text{performance score} = 1 - \left( \frac{\text{hunger} + (1 - \text{energy})}{2} \right)
     \]
   - Average scores are compared across scenarios.

4. **Decision**:
   - Adopt the new code if its average score is higher; otherwise, revert.

##### Example: Testing a Code Update

Kirito proposes:

\[
\text{utility} = 0.6 \times \text{energy} - 0.4 \times \text{hunger} + 0.1 \times \text{warmth}
\]

- **New Variable**: `warmth` (0 to 1).
- **Simulation Results** (with `warmth = 0.5`):
  - **Scenario 1**: Both choose "find food," performance = 0.35.
  - **Scenario 2**: Both choose "rest," performance = 0.8.
  - **Scenario 3**: Both choose "rest," performance = 0.55.
- **Average Performance**: 0.567 for both.
- **Outcome**: No improvement, so the system reverts.

**Log Example**:

```
2025-04-01 10:00:00,123 - INFO - NPC Kirito testing new utility function.
2025-04-01 10:00:05,456 - INFO - Simulated 3 scenarios: old_score=0.567, new_score=0.567
2025-04-01 10:00:10,789 - INFO - NPC Kirito reverted code update: no improvement detected.
```

##### What Happens Under the Hood

- **Sandbox Testing**: The backend runs simulations in isolation.
- **State Tracking**: Redis manages temporary states, reverting them post-test.
- **Fallback**: Old code is restored instantly if the new code fails.

#### Gameplay Logs and Under-the-Hood Explanation

Here are two gameplay scenarios with logs and technical insights.

##### Scenario 1: NPC Chat

**Gameplay Log**:

```
2025-04-01 10:00:00,123 - INFO - NPC Kirito asks NPC Asuna: "How do you manage your energy levels?" [Japanese]
2025-04-01 10:00:05,456 - INFO - NPC Asuna responds: "I balance rest and exploration." [Korean]
2025-04-01 10:00:10,789 - INFO - Collaborative learning triggered: Kirito and Asuna exchange language tips.
2025-04-01 10:00:15,012 - INFO - Kirito's Korean proficiency increased by 0.1.
2025-04-01 10:00:20,345 - INFO - Asuna's Japanese proficiency increased by 0.1.
```

**Under the Hood**:

- **Trigger**: Kirito’s "socialize" node activates (energy > 0.5, near Asuna).
- **Dialogue**: GPT generates responses based on language skills.
- **Learning**: Language mismatch triggers proficiency gains, stored in the database.
- **State**: Redis updates the shared knowledge base with new phrases.

##### Scenario 2: Kirito Satisfies Hunger

**Gameplay Log**:

```
2025-04-01 10:05:00,123 - INFO - NPC Kirito's hunger level: 0.8 (high)
2025-04-01 10:05:05,456 - INFO - Kirito evaluates behavior tree: condition "hungry" is true.
2025-04-01 10:05:10,789 - INFO - Kirito executes action: "go_to_food"
2025-04-01 10:05:15,012 - INFO - Kirito moves to food source at (100, 100)
2025-04-01 10:05:20,345 - INFO - Kirito eats food, hunger reduced to 0.2
2025-04-01 10:05:25,678 - INFO - Kirito's energy level: 0.7 (stable)
```

**Under the Hood**:

- **Trigger**: Hunger > 0.7, checked per tick.
- **Behavior Tree**: "Go_to_food" selected if hungry.
- **Pathfinding**: Shortest path calculated on a 2D grid.
- **Execution**: Movement costs energy; eating reduces hunger.
- **State**: Updated in the database, reflected on the frontend.

**Example Condition**:

If Kirito (or any NPC) needs food but none exists in the game environment:

1. **Behavior Tree Execution**
   - The NPC's behavior tree (in `behavior_tree` field) will first check the "hungry" condition.
   - The `go_to_food` action will attempt to execute but fail since no food exists.

2. **Fallback Mechanism**
   - The selector node in the behavior tree will move to the next child node:
     - Check if "tired" (if not tired, move to next).
     - Default to "explore" action from the initial behavior tree.

3. **Hunger System Escalation**
   - `update_survival()` in `game_logic.py` will keep increasing hunger:
     ```python
     npc["hunger"] = min(1.0, npc.get("hunger", 0.2) + 0.01)
     ```
   - This directly impacts health calculation:
     ```python
     npc["health"] = max(0.0, min(1.0, 1 - ((npc["hunger"] + (1 - npc["warmth"])) / 2))
     ```

4. **Live Bar Depletion**
   - `update_live_bar()` reduces `live_bar` based on hunger:
     ```python
     hunger_factor = npc.get("hunger", 0.2) * 0.1
     decrease = age_factor + hunger_factor + warmth_factor
     npc["live_bar"] = max(0, npc.get("live_bar", 100) - decrease)
     ```

5. **Behavior Tree Evolution**
   - After 3 failed attempts (performance metric check in `thinking_logic.py`):
     ```python
     utility_new = utility_current + (0.05 if random.random() > 0.5 else -0.05)
     if utility_new < utility_current:  # Revert to previous tree
     ```
   - May generate new actions via GPT like "steal_food" or "beg_for_food".

6. **Final Outcomes**
   - If hunger reaches 1.0 for 10 consecutive cycles (100 seconds real-time):
     - `live_bar` hits 0.
     - NPC state changes to DEAD:
       ```python
       if npc["live_bar"] == 0 and npc.get("state") != "DEAD":
           npc["state"] = "DEAD"
           insert_memory(db_conn, npc["id"], "death", f"{npc['name']} died.")
       ```

7. **Player Intervention**
   - Frontend `Game.tsx` allows adding environment items.
   - Players could theoretically add food via:
     ```typescript
     // In Game component
     addEnvItem() {
       axios.post('/api/environment', {type: "food", x: 100, y: 100...})
     }
     ```
   - Otherwise, the system continues the hunger death spiral.

This creates emergent storytelling—NPCs might develop new survival strategies through GPT-driven behavior tree updates or perish if the environment remains inhospitable.

---

## Use Cases

The SAO NPC Project offers versatile applications:

### 1. Educational Playground

- **Purpose**: Teach programming, AI, or social dynamics.
- **How**: Modify NPC behaviors or study language evolution.
- **Impact**: Hands-on learning.

### 2. Research Simulator

- **Purpose**: Study emergent behaviors or AI theories.
- **How**: Tweak variables and observe NPC responses.
- **Impact**: A sandbox for complex systems.

### 3. Interactive Storytelling

- **Purpose**: Craft dynamic narratives.
- **How**: Use quests and NPC autonomy for living worlds.
- **Impact**: Player-driven entertainment.

### 4. Dynamic Behavior Adaptation

- **Purpose**: Observe how NPCs adapt to environmental changes.
- **How**: Introduce new challenges (e.g., food scarcity) and watch NPCs generate new actions via DSL.
- **Impact**: Insight into adaptive AI systems.

### Additional Ideas

- Test self-evolving AI.
- Simulate cultural shifts.
- Build virtual companions.

---

## API and Extensibility

The API empowers developers to extend the project:

- **NPC Interaction**: Send messages, get responses.
- **Quest Management**: Create and assign tasks.
- **Data Access**: Retrieve profiles, logs, and knowledge.
- **NPC Positions**: Use the new `/api/npc_positions` endpoint for real-time location data, enhancing frontend integration.
- **Extensibility**: Reuse trained NPCs or build custom UIs (e.g., mobile apps, dashboards).

---

## Additional Examples

Here are five new examples showcasing the capabilities of SAO NPC Project v2.5.3:

### Reproduction Example

- **Scenario**: Two NPCs, Kirito and Asuna, have high energy and social bonds. Their reproduction desire increases, leading to the birth of a new NPC, "Kirasuna."
- **Log**:
  ```
  2025-04-01 11:00:00,123 - INFO - NPC Kirito and NPC Asuna's reproduction desire reached 0.8.
  2025-04-01 11:00:05,456 - INFO - New NPC Kirasuna born with mixed ethnicity (Japanese/Korean).
  2025-04-01 11:00:10,789 - INFO - Kirasuna inherited languages: Japanese (0.5), Korean (0.5).
  ```
- **Details**: The `update_reproduction_desire` function uses a sigmoid function to calculate desire based on energy and social bonds. The `reproduce` function in `game_logic.py` creates a new NPC with inherited traits.

### Learning Example

- **Scenario**: NPC Kirito teaches NPC Kirasuna a lesson in Japanese, increasing Kirasuna's brain level.
- **Log**:
  ```
  2025-04-01 12:00:00,123 - INFO - NPC Kirito teaches NPC Kirasuna: "Always be curious." in Japanese.
  2025-04-01 12:00:05,456 - INFO - Kirasuna's brain level increased to 0.1.
  ```
- **Details**: The `/api/teach` endpoint triggers the teaching process, reducing the child’s learning need and increasing their brain level. The lesson is stored as a memory in the database.

### State of Mind Example

- **Scenario**: NPC Asuna's mood shifts to "anxious" due to an economic downturn reported by the FRED API.
- **Log**:
  ```
  2025-04-01 13:00:00,123 - INFO - Economic downturn detected via FRED API.
  2025-04-01 13:00:05,456 - INFO - NPC Asuna's mood changed to "anxious."
  2025-04-01 13:00:10,789 - INFO - Asuna's earnings decreased by 5.
  ```
- **Details**: The autonomous loop in `main.py` fetches external data and adjusts NPC moods and economic status based on real-world events.

### Technical Highlight: Sandboxed Code Validation

- **Scenario**: NPC Kirito attempts to generate a new DSL action with an invalid step, triggering validation and fallback.
- **Log**:
  ```
  2025-04-01 14:00:00,123 - INFO - NPC Kirito generated a new action: "invalid_action."
  2025-04-01 14:00:05,456 - WARNING - Action "invalid_action" failed validation for NPC Kirito.
  2025-04-01 14:00:10,789 - INFO - NPC Kirito fell back to "idle."
  ```
- **Details**: The `validate_blueprint` function in `action_executor.py` checks DSL steps against allowed primitives. Invalid actions are rejected, and the NPC defaults to `idle`, ensuring system stability.

### DSL Hybrid / Action Executor Example

- **Scenario**: NPC Asuna generates a "patrol" action using DSL to move between two points.
- **Log**:
  ```
  2025-04-01 15:00:00,123 - INFO - NPC Asuna generated a new action: "patrol."
  2025-04-01 15:00:05,456 - INFO - Action "patrol" validated successfully.
  2025-04-01 15:00:10,789 - INFO - Asuna is patrolling between (50,50) and (100,100).
  ```
- **Details**: The DSL interpreter in `action_executor.py` executes the "patrol" action, using `move_to` steps within game constraints, showcasing the hybrid approach’s flexibility and safety.

---

## Getting Started

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-repo/sao-npc-project.git
   cd sao-npc-project
   ```

2. **Set Up Environment Variables**:
   Create a `.env` file (see [Configuration](#configuration)).

3. **Initialize the Database**:

   ```bash
   docker-compose run backend python init_db.py
   ```

4. **Launch the System**:

   ```bash
   docker-compose up --build
   ```

5. **Explore**:
   Visit `http://localhost:3000`.

---

## Configuration

Customize via environment variables:

- `AUTH_TOKEN`: API security.
- `OPENAI_API_KEY`: GPT access.
- `ENABLE_SELF_UPDATE`: Toggle self-coding (default: `true`).
- `DATABASE_ENGINE`: `sqlite` or `postgres` (default: `sqlite`).

See `constants.py` for more.

---

## Contributing

1. Fork the repo.
2. Create a branch.
3. Submit a pull request with tests.

---

## License

MIT License. See [LICENSE](LICENSE).

---


**Created by the SAO NPC Project Team**  
Explore a world where NPCs live, learn, and evolve—enjoy the journey!

