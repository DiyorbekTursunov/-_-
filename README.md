# Manipulator Control Interface Project

## Project Overview

In this project, we are developing a **Manipulator Control Interface** for an underground laboratory. The manipulator is responsible for moving images across a table divided into cells. The user will control the manipulator with commands and see real-time results in the interface.

The interface will handle:
1. User authentication (admin/admin).
2. Command input with subsequent optimization before sending it to the manipulator.
3. Storing and displaying the history of executed commands.
4. Confirmation of successful operation with Material UI Snackbar.

## Technologies Used
- **React**: Frontend framework.
- **Material UI**: UI components library.
- **Redux Toolkit**: State management.
- **RTK Query**: API calls.
- **React Hook Form**: Form handling.

## Features

### 1. **Authorization**
- User authentication with username (`admin`) and password (`admin`).
- Use React Hook Form for the login form.
- On successful login, user is authenticated and granted access to the interface.

### 2. **Command Input & Optimization**
- The user inputs commands to control the manipulator (e.g., `ЛЛЛЛВПППОНННБ`).
- The command is optimized by removing redundant characters. For example:
  - `ЛЛЛЛВПППОНННБ` → `4L2V3PO3NB`
  - `ЛЛЛНННЛЛЛЛНННО` → `2(3L3N)O`

### 3. **Command History**
- Store and display a history of commands.
- Each entry in the history will show:
  - **Original Command**: What the user initially input.
  - **Optimized Command**: The optimized version of the command.
  - **Data**: Additional information such as image positions before the command.
  - **Time**: Timestamp of when the command was executed.
  - **Image Position**: Position of images before completion.

### 4. **Snackbar Confirmation**
- After each successful command execution, a **Snackbar** notification will be displayed to confirm that the operation was successful.

## How to Run the Project

### Prerequisites:
- Make sure you have `Node.js` installed.
- Use `Yarn` as the package manager.

### Installation Steps:
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd manipulator-control
