# 🎲 Console Dice Game

A text-based dice rolling game implemented in Python where players compete against the computer. The game features ASCII art dice representations, score tracking, and result storage in CSV format.

## 🎮 Features

- Interactive console-based gameplay
- Beautiful ASCII art dice representations
- Multiple round support
- Score tracking based on dice value differences
- Game statistics tracking (max/min rolls)
- Result storage in CSV format
- Option to play multiple games
- Animated dice rolling with time delays for better user experience

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- A terminal/console with unicode support for dice ASCII art

### Installation

1. Clone the repository:
```bash
git clone [your-repository-url]
```

2. Navigate to the project directory:
```bash
cd dice-game
```

3. Ensure you have the required Python standard libraries (all libraries used are built-in):
- random
- os
- csv
- time

### Configuration

Update the `file_path` variable in the code to specify where you want to save the game results:

```python
file_path = r'path/to/your/Dice_results.csv'
```

## 🎲 How to Play

1. Run the game:
```bash
python dice_game.py
```

2. Enter the number of rounds you want to play
3. Watch as both you and the computer roll dice
4. Points are awarded based on the difference between rolls:
   - Higher roll wins the difference as points
   - Ties result in no points
5. After each game, choose to:
   - Press 'C' to play again
   - Press 'Q' to quit

## 📊 Scoring System

- Points are awarded based on the difference between the player's and computer's rolls
- The player with the higher roll wins the difference as points
- For example:
  - Player rolls 6, Computer rolls 3: Player wins 3 points
  - Player rolls 2, Computer rolls 5: Computer wins 3 points
  - Both roll 4: No points awarded

## 💾 Game Statistics

The game tracks and saves the following statistics to a CSV file:
- Number of rounds played
- Maximum dice value rolled by the player
- Minimum dice value rolled by the player
- Final player score
- Final computer score

## 🎨 Dice Representations

The game uses ASCII art to represent dice rolls. Example:

```
┌─────────┐
│  *   *  │
│    *    │
│  *   *  │
└─────────┘
```

## 🛠️ Future Enhancements

- [Commented out] Weighted dice rolling functionality
- Multiplayer support
- Different game modes
- High score tracking
- Statistical analysis of game results



## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
