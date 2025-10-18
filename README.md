<h1>Giaxidis Evangelos - Final IDKI Project </h1>

<h2>Information about the game </h2>

<p>The game I desiced to deliver for the Final Project Assignment for the IDKI Course 2025, is about a Hack n' Slash survival platformer game. </p>

<h4>Game objective</h4>

<p>You control a cyllinder which moves along a platform loaded with medieval assets like furniture. The main objective is to survive by killing all the enemies that spawn randomly and chase you until they touch you. If an enemy eventually catches you, you die. The only way to avoid that is by killing them, throwing an axe towards them. There are also coins in the room you need to collect in order to win the game </p>

<h4>Controls</h4>

<p>You control the cyllinder by using WASD keys for movement, space bar for jumping and left click for attacking. You can also pause the game anytime by pressing esc.</p>

<h4>Game modes</h4>

<p>There are 3 available game modes: Easy, Medium and Hard. Each of them manifest some differences regarding difficulty of the game. Easy mode is simple, we have single spawns of enemies, while Medium mode increases enemy nummber that spawn every time to 2. Finally Hard mode makes 3 enemy spawns at a time. </p>

<h2> About game development </h2>

<h4>Game Development Process</h4>

<p>The development of the game began with the basic scene setup in Unity, which included the ground plane, the player (a red capsule), and an enemy (a gray cube). The environment was enriched with walls and 3D props such as furniture and decorative elements, creating the feeling of an indoor room.
The game is designed with a top-down perspective, where the camera is positioned high above the scene.</p>

<h4>Player Movement and Core Mechanics</h4>

<p>The player can move and jump within the environment and has the ability to throw an axe as a weapon. To achieve this, an axe prefab was created, equipped with a rigidbody and collider to ensure realistic physics interactions. When the player throws the axe and it hits an enemy, the enemy “dies” and respawns at a random position on the ground. To make the moment more impactful, a particle explosion effect appears at the location of the enemy’s death, adding a satisfying visual feedback to the combat.</p>

<h4>Enemy AI Behavior</h4>

<p>The enemy was programmed to constantly chase the player, calculating its direction and moving toward the player’s position. If it reaches and touches the player, the game triggers a Game Over event, and a message appears on screen. This behavior is handled through the EnemyChase script, which manages both the chasing logic and the respawn mechanism after the enemy is defeated.</p>

<h4>Collectibles and Scoring System</h4>

<p>A coin prefab was added to the scene, designed to spawn at random positions on the ground. Each time the player collects a coin, a new one appears elsewhere, keeping the gameplay continuous. On-screen UI counters display the number of coins collected and enemies killed.
Depending on the selected difficulty mode, the player can win the game by reaching a specific combination of collected coins and enemy kills.</p>

<h4>Difficulty Modes</h4>

<p>At the start of the game, a Mode Selection Panel appears, offering three options: Easy, Medium, and Hard.

- In Easy Mode, one enemy spawns, and the player wins after collecting 5 coins and achieving 5 kills.

- In Medium Mode, two enemies spawn every 5 seconds.

- In Hard Mode, three enemies spawn every 5 seconds.

Each mode increases the intensity and pace of the gameplay.
When the victory conditions are met, a “YOU WIN” message appears, along with a Restart button that brings the player back to the main menu.</p>

<h4>Background Music System</h4>

<p>The game includes a background music system that enhances the overall atmosphere and player immersion.A continuous music track plays throughout the game, creating a consistent mood during exploration and combat.The volume of the music can be adjusted through a UI slider, which is connected to an Audio Mixer parameter for real-time control.This setup allows players to personalize their audio experience by increasing or lowering the background volume without affecting the other in-game sounds or gameplay elements.
The music restarts automatically when it reaches the end, ensuring uninterrupted playback during the entire gaming session.</p>

<h4>Programming and Code Implementation</h4>

<p>The game was developed entirely using C# scripts in Unity, combining both object-oriented structure and event-driven behavior.Key Unity functions such as Start(), Update(), FixedUpdate(), and LateUpdate() were used to manage initialization, player input, physics updates, and camera behavior respectively.Physics-based actions like movement, jumping, and projectile launching were handled through Rigidbody components and commands such as AddForce() and velocity adjustments.Collisions and interactions between game objects were managed using OnTriggerEnter() and OnCollisionEnter(), allowing the player to collect coins or eliminate enemies with the axe.UI elements were updated dynamically through TextMeshPro fields, while coroutines (e.g., IEnumerator) were used to control timed events like enemy spawning.The camera used smooth transitions implemented with Vector3.SmoothDamp(), and random positioning of coins and enemies was achieved using Random.Range().Overall, the code structure focuses on clarity and modularity, allowing each script — such as PlayerController, EnemyChase, AxeProjectile, and GameManager — to handle specific gameplay mechanics efficiently and cohesively.</p>

