# Phase 2 Code Challenge: Plantsy

## Demo

Use this gif as an example of how the app should work.

![Demo GIF](./demo.gif)

## Overview

Plantsy is a plant shop admin application. The frontend is connected to a JSON backend, allowing users to view, add, search, and manage plants in real time.

## Setup

1. Run `npm install` in your terminal.
2. Run `npm run server`. This will run your backend on port `6001`.
3. In a new terminal, run `npm run dev`.
4. Run `npm run test` to run the test suite.

Make sure to open [http://localhost:6001/plants](http://localhost:6001/plants)
in the browser to verify that your backend is working before you proceed!

## Features

- **View all plants** — plants are fetched from the backend and displayed on page load
- **Add a new plant** — fill out the form and click Add Plant to POST to the backend and render it on the page
- **Mark as out of stock** — click the In Stock button on any plant card to toggle it to Out of Stock (non-persisting)
- **Search plants** — type in the search bar to filter plants by name in real time

## Component Structure

- `App` — renders Header and PlantPage
- `PlantPage` — manages plants and search state, handles fetch and form submission
- `NewPlantForm` — controlled form for adding a new plant
- `Search` — controlled input for filtering plants
- `PlantList` — renders a list of PlantCard components
- `PlantCard` — displays individual plant info and in/out of stock toggle

## Endpoints

The base URL for your backend is: `http://localhost:6001`

## Deliverables

As a user:

1. When the app starts, I can see all plants.
2. I can add a new plant to the page by submitting the form.
3. I can mark a plant as "sold out".
4. I can search for plants by their name and see a filtered list of plants.

### Endpoints for Core Deliverables

#### GET /plants

Example Response:

```json
[
  {
    "id": 1,
    "name": "Aloe",
    "image": "./images/aloe.jpg",
    "price": 15.99
  },
  {
    "id": 2,
    "name": "ZZ Plant",
    "image": "./images/zz-plant.jpg",
    "price": 25.98
  }
]
```

#### POST `/plants`

Required Headers:

```js
{
  "Content-Type": "application/json"
}
```

Request Object:

```json
{
  "name": "string",
  "image": "string",
  "price": number
}
```

Example Response:

```json
{
  "id": 1,
  "name": "Aloe",
  "image": "./images/aloe.jpg",
  "price": 15.99
}
```

## Technologies

- React
- Vite
- JSON Server