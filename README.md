# GuitarLA

A guitar e-commerce storefront built with React and Vite. Browse a catalog of 12 guitar models and manage a shopping cart with full quantity controls and localStorage persistence.

## Features

- **Product catalog** — 12 guitar models displayed in a responsive grid.
- **Shopping cart** — Add, remove, increment and decrement items, or clear the entire cart.
- **Quantity limits** — Each product allows a minimum of 1 and a maximum of 5 units.
- **Persistent cart** — Cart state is saved to `localStorage` and restored on page reload.

## Tech Stack

| Tool      | Version |
| --------- | ------- |
| React     | 19      |
| Vite      | 8       |
| Bootstrap | 5 (CDN) |
| ESLint    | 9       |

## Project Structure

```
src/
├── App.jsx              # Root component — state management and cart logic
├── components/
│   ├── Guitar.jsx       # Product card component
│   └── Header.jsx       # Navigation bar with cart dropdown
└── data/
    └── db.js            # Static guitar catalog (12 items)
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm 9+

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

The app will be available at `http://localhost:5173`.

### Production Build

```bash
npm run build
```

Output is placed in the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

## Cart Logic

| Action      | Behaviour                                                       |
| ----------- | --------------------------------------------------------------- |
| Add to cart | Adds the item with `quantity: 1`; increments if already present |
| Increment   | Increases quantity up to the `MAX_ITEMS` (5) limit              |
| Decrement   | Decreases quantity down to the `MIN_ITEMS` (1) limit            |
| Remove      | Removes the item from the cart entirely                         |
| Clear cart  | Empties the cart                                                |
