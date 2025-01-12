# Quantum Dino — Amplitude Amplification Action Based Selection for Playing 2D Platformers
Playing the "No Internet Google Chrome Dinosaur Game" with a quantum computer!

Keywords: Quantum Reinforcement Learning, Quantum Error Correction, Amplitude Amplification


In video games, we constantly pick moves we need to perform from a given moveset. Maybe, it's something like ["move up", "move down", "move left" , "move right", "punch", "kick"]. When we play video games, we choose what inputs we want to send through the controller based on certain key parameters in a video game at a given frame. Maybe if an enemy is too close, we want to select the "kick" move, or if the objective is to the far right of the screen, perhaps the "move right" move is the most beneficial. In classical computing, we can determine which move to select from the moveset using an else-if chain, which will find the optimal move in linear time. Finding an item from a list is nothing but a search algorithm! It turns out that we can upgrade the search speed quadratically for selecting an item in a list using Grover's Algorithm!

Therefore, in this project, I develop a way to play Google's "No Internet Dino Game", using a modified parameterized Grover's Algorithm. I use Amplitude Amplification Action Based Selection to select the optimal move from a moveset at a given frame of the video game.

For a simple move set of length two: ["Jump", "Wait"], the control schematic of the game looks like

![image](https://github.com/user-attachments/assets/8fa1f754-c0c6-45bd-aef5-a0018f0626fa)

With a quantum circuit architecture:

![image](https://github.com/user-attachments/assets/bc8ce485-85c2-4051-9483-9c8ffa390b9a)

which is just an error-corrected $R_{y}$ gate. Error correction is necesary here because not only are quantum computers noisy, but if the dino makes a 'jump' move by accident when it really should have done a "wait" move, that mistake could end the entire game. Therefore, when a move is selected, the error corrected code essentially triple checks if that was really the optimal move in the move set for a given frame.


Download and run the *dino_game_simple_QNN.ipynb* to watch the quantum circuit play the Dino Game in the PyGame interface!
