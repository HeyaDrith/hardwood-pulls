# 🏀 Hardwood Pulls

**Hardwood Pulls** is a basketball-themed virtual card pack opening game built with **Python and Pygame**.

Open packs, reveal randomly generated basketball cards, and chase higher-rarity pulls. The project is currently a **work in progress**, with additional gameplay features and polish planned.

## 🎮 Features

* 🃏 **Virtual Pack Opening** — Open basketball card packs and reveal a random card.
* 🎲 **Rarity System** — Cards are categorized into four rarity tiers:

  * Common — 30%
  * Rare — 25%
  * Epic — 25%
  * Legendary — 20%
* ✨ **Card Reveal Effects** — Visual effects accompany each card reveal based on its rarity.
* 📦 **Pack Animation** — Packs shake before the card is revealed.
* 🔊 **Sound & Music** — Background music and opening sound effects enhance the experience.
* 🖼️ **Custom Assets** — Card images and other visual assets are loaded dynamically from the `assets` directory.
* 🌐 **Web Deployment** — The project includes configuration for running the game through a web deployment.

## 🛠️ Tech Stack

* **Python**
* **Pygame**
* **Pygbag** — WebAssembly/web deployment for Pygame
* **Vercel** — Deployment
* **HTML/CSS/JavaScript** — Web wrapper/interface

## 📁 Project Structure

```text
hardwood-pulls/
├── assets/             # Game images, cards, sounds, and other assets
├── web/                # Web/deployment files
├── main.py             # Main Pygame application
├── package.json        # Web project configuration
├── requirements.txt    # Python dependencies
├── pygbag.ini          # Pygbag configuration
├── vercel.json         # Vercel deployment configuration
└── .gitignore
```

## 🚀 Getting Started

### Prerequisites

Make sure you have **Python 3** installed.

Clone the repository:

```bash
git clone https://github.com/HeyaDrith/hardwood-pulls.git
cd hardwood-pulls
```

### Install Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### Run Locally

Start the game with:

```bash
python main.py
```

The game will open in a Pygame window.

## 🃏 How It Works

The game uses a weighted random selection system to determine the rarity of each pull.

Each rarity has an associated weight:

```python
RARITY = {
    "common": 30,
    "rare": 25,
    "epic": 25,
    "legendary": 20,
}
```

When a pack is opened, the game selects a rarity using weighted randomness. It then searches the corresponding rarity folder for an available card and displays the selected card.

Cards can be organized inside the assets directory like this:

```text
assets/
├── common/
│   ├── card1.png
│   └── card2.png
├── rare/
│   ├── card3.png
│   └── card4.png
├── epic/
│   └── card5.png
└── legendary/
    └── card6.png
```

This allows new cards to be added without changing the core game logic.

## 🎨 Game Flow

The current game follows a simple pack-opening loop:

```text
Title Screen
     ↓
   Play
     ↓
 Pack Appears
     ↓
 Pack Shakes
     ↓
 Rarity Selected
     ↓
 Card Revealed
     ↓
   Continue
```

The game is built around a state-based system that manages the title screen, idle state, pack animation, and card reveal.

## 🔮 Planned Features

Hardwood Pulls is still under development. Planned improvements include:

* [ ] Expanded card collection
* [ ] Player/card statistics
* [ ] Card collection system
* [ ] Duplicate tracking
* [ ] Pack-opening history
* [ ] Multiple pack types
* [ ] Improved animations
* [ ] More advanced card reveal effects
* [ ] Player collection/progression
* [ ] Improved web experience
* [ ] Additional game modes

## 📸 Project Status

> 🚧 **Work in Progress**

The core pack-opening system is functional, but the project is still being actively developed. Features, visuals, card pools, and gameplay systems may change as development continues.

## 👤 Author

**HeyaDrith**

Built as a personal project exploring **Python game development, randomization systems, animation, asset management, and web deployment**.

## 📄 License

This project is currently a personal work-in-progress. Licensing information will be added as the project develops.
