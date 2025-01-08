# Cookbook: JavaScript

- [Basics](https://androcado.github.io/cookbook-javascript)
- [Global Variables](https://androcado.github.io/cookbook-javascript/global-variables)
- [Functions](https://androcado.github.io/cookbook-javascript/functions)


## 1. General Properties

| **Property**   | **Description**                                                                |
|----------------|--------------------------------------------------------------------------------|
| `window`       | The global window object itself.                                               |
| `document`     | Represents the Document Object Model (DOM).                                    |
| `location`     | Provides access to the URL and navigation.                                     |
| `navigator`    | Information about the user's browser.                                          |
| `history`      | Access to the browser's history.                                               |
| `screen`       | Information about the user's screen resolution.                                |

## 2. Dimensions and Positions

| **Property**   | **Description**                                                                |
|----------------|--------------------------------------------------------------------------------|
| `innerWidth`   | Width of the viewport (excluding scrollbars).                                   |
| `innerHeight`  | Height of the viewport (excluding scrollbars).                                  |
| `outerWidth`   | Total width of the window (including browser decorations).                     |
| `outerHeight`  | Total height of the window (including browser decorations).                    |
| `screenX`      | X-coordinate of the window relative to the screen.                             |
| `screenY`      | Y-coordinate of the window relative to the screen.                             |
| `scrollX`      | Horizontal scroll position of the window.                                      |
| `scrollY`      | Vertical scroll position of the window.                                        |

## 3. Functions

| **Function**   | **Description**                                                                |
|----------------|--------------------------------------------------------------------------------|
| `alert()`      | Displays a popup window with a message.                                        |
| `confirm()`    | Displays a popup window with OK/Cancel options.                                |
| `prompt()`     | Displays a popup window with an input field.                                   |
| `setTimeout()` | Executes a function after a delay.                                             |
| `setInterval()`| Repeatedly executes a function at specified intervals.                         |
| `clearTimeout()` | Cancels a previously set timeout.                                            |
| `clearInterval()` | Stops a previously started interval.                                        |

## 4. Events

| **Event**      | **Description**                                                                |
|----------------|--------------------------------------------------------------------------------|
| `onload`       | Triggered when the page has fully loaded.                                      |
| `onresize`     | Triggered when the window is resized.                                          |
| `onscroll`     | Triggered when the user scrolls.                                               |
| `onerror`      | Triggered when a JavaScript error occurs.                                      |

## 5. Storage and APIs

| **API**        | **Description**                                                                |
|----------------|--------------------------------------------------------------------------------|
| `localStorage` | Local storage for persistent data.                                             |
| `sessionStorage` | Temporary storage for session data.                                          |
| `indexedDB`    | Access to IndexedDB for database-driven applications.                          |
| `fetch()`      | API for retrieving resources (e.g., HTTP requests).                            |
| `console`      | Access to the console (e.g., `console.log`).                                   |
| `performance`  | Measures the loading times and performance of a webpage.                      |

## 6. Other Properties

| **Property**   | **Description**                                                                |
|----------------|--------------------------------------------------------------------------------|
| `crypto`       | Access to cryptographic functions.                                             |
| `customElements` | Registration and access to web components.                                  |
| `matchMedia()` | Monitor media queries.                                                        |
| `closed`       | Indicates whether a window is closed.                                          |
| `frames`       | Access to embedded frames.                                                    |
| `name`         | Name of the window (if set).                                                  |
| `opener`       | Reference to the window that opened this one.                                  |
| `parent`       | Reference to the parent window (for frames).                                   |
| `top`          | Reference to the topmost window in the hierarchy.
