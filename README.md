# Faro Position Calculator | New and Improved!

A modern web application for calculating binary positions in faro shuffle sequences, built with Alpine.js. This tool helps magicians and card enthusiasts determine the binary path for moving cards to specific positions using faro shuffles.

[Try the Live Demo Here!](https://faro-shuffle-calc-2025.netlify.app/)

## Overview

The Faro Position Calculator transforms complex faro shuffle mathematics into an intuitive interface. Enter any starting position (1-52), and the calculator instantly generates the binary sequences needed to reach any other position in the deck using perfect faro shuffles.

## Features

- **Real-time Calculations**: Instant computation using Alpine.js
- **Complete Position Matrix**: Shows all possible target positions (1-52) and their binary paths
- **Responsive Design**: Built with Bulma CSS framework for seamless mobile experience
- **Modern UI/UX**: Clean animations and transitions for a polished feel
- **Efficient Performance**: Debounced inputs and optimized calculations

## Quick Start

```bash
# Clone the repository
git clone [your-repo-url]

# Open index.html in your browser
# No build step required!
```

## Technical Stack

- **Alpine.js**: Lightweight JavaScript framework for reactive interfaces
- **Bulma**: Modern CSS framework for responsive design
- **Vanilla JavaScript**: Core calculation logic
- **CSS Custom Properties**: For consistent theming and animations

## Understanding the Output

The calculator provides binary sequences where:
- Each digit represents one shuffle
- Read left to right: first shuffle to last shuffle
- `0` = Out shuffle
- `1` = Modified In shuffle

Example: `101` represents:
1. Modified In shuffle
2. Out shuffle
3. Modified In shuffle

## Shuffle Specifications

### Out Shuffle (0)
- Standard out faro cut for 52 cards
- For 51 cards: Cut 26 to left, 25 to right (when face up)

### Modified In Shuffle (1)
- Deck starts face up in left hand
- Cut 25 to left, 27 to right (52-card deck)
- Weave together, keeping one card from right packet on top
- Bottom two cards of right packet remain unweaved

## Technical Implementation

The calculator uses several key features:

```javascript
// Core calculation function
calculateBase2Position(startPos, targetPos) {
    const keyNumbers = [1, 3, 7, 15, 31, 63];
    // ... calculation logic
}

// Reactive data model
Alpine.data('faroCalculator', () => ({
    startingPosition: '',
    calculations: [],
    // ... methods
}))
```

## Technical Limitations

- Assumes perfect execution of all shuffles
- Maximum sequence length of 6 shuffles
- Calculations based on mathematical models
- Returns 'Invalid' for positions that require more than 6 shuffles
- Results are limited to binary sequences (Perfect Out / Modified In shuffles only)

## Support the Project

If this calculator has helped with your card magic or mathematics exploration, consider supporting the development:

![PayPal QR Code](paypal-qr.png)

Your support helps maintain and improve this tool for the magic community. Every contribution is greatly appreciated!

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

Please ensure your code follows the existing style and includes appropriate documentation.

## Credits

- Mathematical concepts from "Faro Concepts" by Murray Bonfeld
- UI/UX design inspired by modern web standards
- Built with Alpine.js and Bulma CSS

## License

MIT License - See LICENSE file for details
---

Made with ♥️ by Ken aka FaroShuffleWhileCoding for the magic community, mathematicians, and fellow developers
