# Counter App

## Description

- This project is a counter application where users can modify a numerical value using plus (+) and minus (-) buttons.If you press (+) or (-), the counter value info will be increased or decreased accordingly. The application is structured into three different levels: Basic, Intermediate, and Expert.

## Tech Stack

- Next.js (App Router)
- Tailwind CSS with shadcn/UI
- Theming with next-themes
- Lucide React for icons

## Features

- **Three Counter Levels:** Basic, Intermediate, and Expert pages, each with different rules.
- **Easy Navigation:** A navigation bar allows seamless switching between the counter levels.
- **Clean UI & UX:** A consistent and clean user interface using Card components.
- **Dark & Light Mode:** Theme support for user preference.
- **Conditional Logic:** Buttons on the Expert level are disabled based on the counter's value.

## Project Details

The Counter app has 3 pages: `Basic`, `Intermediate`, and `Expert`. Each page acts as a counter level and has its own set of rules. The UI for each page is built using a reusable Card component, and navigation is handled by a central NavBar.

The core logic for each counter is encapsulated within 3 separate components.

### State Management & Event Handling

In all 3 logic components, a single state variable `count` is defined using the `useState` hook. The `setCount` function is used to track and update the counter's value.

When a button is pressed, an `onClick` event triggers an attached function. These functions command the `setCount` setter to change (increase or decrease) the `count` value accordingly, and the UI updates in real-time.

### Page Breakdown

#### Basic Page (Homepage)

- **Functionality:** This page has two buttons, `(+)` and `(-)`, to increment or decrement the counter value by 1.
- **Constraints:** There are no limits on the counter's value.

#### Intermediate Page

- **Functionality:** This page features four buttons: `(+)`, `(-)`, `(+10)`, and `(-10)`.
- **Constraints:** Like the Basic page, there are no limits on the counter's value.

#### Expert Page

- **Functionality:** This level also has four buttons with the same increment/decrement logic as the Intermediate page.
- **Constraints:** This page introduces specific rules and button disabling logic.
    - The counter's value cannot go below **0** or above **100**.
    - The decrement buttons (`-` & `-10`) are disabled when the counter value is 0.
    - The increment buttons (`+` & `+10`) are disabled when the counter value is 100.
