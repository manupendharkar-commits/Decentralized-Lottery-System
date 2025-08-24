# 🏆 Fortune Coins 🎰

A premium React-based gaming platform featuring lottery draws and mini-games with real-time prize pools and interactive gameplay.

![Fortune Coins Banner](https://via.placeholder.com/800x200/4A5568/FFFFFF?text=Fortune+Coins+-+Premium+Gaming+Destination)

## ✨ Features

### 🎯 Lottery System
- **Interactive Lottery Draws** - Automated 15-minute draw cycles
- **Dynamic Prize Pools** - Based on ticket sales (₹150 per ticket)
- **Luck Point System** - Increases winning chances for non-winners
- **Multiple Winner Modes** - Support for 2 or 3 winners per draw
- **Real-time Statistics** - Live tracking of participants and prize pools

### 🎮 Mini Games
- **🪙 Coin Flip** - Classic heads/tails with ₹300 prizes
- **🎲 Two Dice** - Roll dice for exciting rewards
- **🃏 Card Guess** - Test your card prediction skills
- **🎰 Slot Machine** - Spin to win jackpots
- **🎯 Roulette** - European-style roulette gameplay
- **✂️ Rock Paper Scissors** - Challenge the house

### 🎨 User Experience
- **Modern Design** - Glassmorphism and gradient aesthetics
- **Responsive Layout** - Works on desktop and mobile devices
- **Real-time Updates** - Live prize pools and countdown timers
- **Accessibility** - Full ARIA support and keyboard navigation
- **Smooth Animations** - Engaging hover effects and transitions

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/fortune-coins.git
   cd fortune-coins
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000` to see the application

### Build for Production

```bash
npm run build
```

This creates an optimized production build in the `build` folder.

## 🎯 How to Play

### Lottery System

1. **Buy a Ticket** - Click "Buy Lottery Ticket" and enter your name
2. **Wait for Draw** - Automatic draws every 15 minutes
3. **Check Results** - Winners are announced with prize breakdown
4. **Earn Luck Points** - Non-winners may receive luck boosts for better future odds

### Prize Distribution
- **2 Winners**: 50% / 50% split
- **3 Winners**: 50% / 30% / 20% split

### Luck Point System
- Each luck point increases your winning chances
- Up to 2 non-winners receive luck boosts per draw
- Higher luck = better odds in future draws

## 🛠️ Technical Details

### Built With
- **React 18** - Modern hooks and functional components
- **JavaScript ES6+** - Clean, maintainable code
- **CSS-in-JS** - Styled components with dynamic theming
- **Local State Management** - React hooks for state management

### Key Components

```javascript
├── App.js                 # Main application component
├── Header()              # Navigation and stats display
├── TabButtons()          # Game selection interface
├── ParticipantsTable()   # Lottery participant display
├── RecentDraws()         # Draw history component
└── ResultsAnnouncement() # Winner announcement
```

### State Management

The app uses React's built-in state management:
- `useState` for component state
- `useEffect` for timer and lifecycle management
- No external state management needed

### Styling Approach
- **Inline Styles** - Component-scoped styling
- **Dynamic Theming** - Conditional styling based on state
- **Modern CSS** - Flexbox, gradients, and shadows
- **Responsive Design** - Mobile-first approach

## 🎮 Game Logic

### Lottery Algorithm
```javascript
// Weighted random selection based on luck points
const pool = [];
tickets.forEach((ticket, index) => {
  for (let i = 0; i < 1 + ticket.luck; i++) {
    pool.push(index);
  }
});
```

### Timer System
- 15-minute automatic draw cycles
- Real-time countdown display
- Automatic winner selection and prize distribution

### Prize Calculation
```javascript
const prizeSplits = numWinners === 2 ? [0.5, 0.5] : [0.5, 0.3, 0.2];
const prizes = prizeSplits.map(split => Math.floor(prizePool * split));
```

## 📊 Statistics & Analytics

### Tracked Metrics
- Active ticket count
- Total prize pool value
- Winner distribution
- Luck point allocation
- Game balance tracking

### Recent Draws History
- Last 5 draws displayed
- Winner names and prizes
- Draw timestamps
- Luck point awards

## 🎨 Customization

### Styling
Modify the color scheme by updating the CSS variables:

```javascript
// Primary colors
const primaryGray = '#4A5568';
const secondaryGray = '#718096';
const accentOrange = '#ED8936';

// Update in component styles
background: `linear-gradient(135deg, ${primaryGray}, #2D3748)`
```

### Game Configuration
```javascript
// Lottery settings
const ticketPrice = 150;        // Price per ticket (₹)
const timerDuration = 15 * 60;  // Draw interval (seconds)
const maxRecentDraws = 5;       // History display limit

// Prize distribution
const twoWinnerSplit = [0.5, 0.5];
const threeWinnerSplit = [0.5, 0.3, 0.2];
```

## 🔒 Security Considerations

- Client-side randomization (for demo purposes)
- No real money transactions
- Local state management only
- No external API dependencies

> **Note**: This is a demonstration app. For production use with real money, implement server-side randomization, user authentication, payment processing, and proper security measures.

## 📱 Browser Support

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow React best practices
- Maintain consistent code formatting
- Add comments for complex logic
- Test on multiple browsers
- Ensure accessibility compliance

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🎯 Roadmap

### Upcoming Features
- [ ] User authentication system
- [ ] Persistent game history
- [ ] Multiplayer competitions
- [ ] Advanced statistics dashboard
- [ ] Mobile app version
- [ ] Sound effects and animations
- [ ] Tournament modes
- [ ] Social sharing features

### Mini-Games Expansion
- [ ] Blackjack
- [ ] Poker variants
- [ ] Wheel of Fortune
- [ ] Scratch cards
- [ ] Number guessing games

## 📞 Support

For support, questions, or feature requests:
- 📧 Email: support@fortunecoins.com
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/fortune-coins/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/yourusername/fortune-coins/discussions)

## 🙏 Acknowledgments

- React team for the amazing framework
- Community contributors and testers
- UI/UX inspiration from modern gaming platforms
- Open source libraries and tools used

---

<div align="center">

**⭐ Star this repo if you found it helpful! ⭐**

Made with ❤️ by [Your Name](https://github.com/yourusername)

[Demo](https://your-demo-link.com) • [Documentation](https://your-docs-link.com) • [Report Bug](https://github.com/yourusername/fortune-coins/issues)

</div>
