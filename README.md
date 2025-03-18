# Swimclub Performance Tracker

This project is a Flask-based web application designed to track and analyze swimmer performance for a swim club. It allows users to navigate through swim session data, select swimmers and events, and view performance statistics with a bar chart. The application offers an easy-to-use interface to organize swim sessions and interpret swimmer data.

---

## Features

- **Session Management**: 
  - Easily browse and select swim sessions from previously recorded data.

- **Swimmer Selection**: 
  - Select swimmers based on age and name from swim sessions for tailored performance viewing.

- **Event Data Analysis**:
  - Choose specific events and view results, including detailed records of swimmer performance.

- **Chart Visualization**:
  - View a bar chart displaying swimmer performance times along with averages and comparisons to world records.

- **Data-Driven Approach**:
  - Efficiently fetches swim session, swimmer, and event data using utilities and integrates data from a database backend.

---

## Project Structure

The project is organized into several components for modularity and scalability:

### 1. **Main Flask Application**:
   The core application logic is handled in the `app.py` file, which defines the routes and the sequence of rendering templates for user interactions.

   - **Routes**:
     - `/`: Home page displaying a welcome message.
     - `/swims`: Displays all swim sessions available in the database.
     - `/swimmers`: Allows the selection of swimmers from a specific date.
     - `/showevents`: Displays events for a selected swimmer.
     - `/showbarchart`: Displays a bar chart comparing swimmer performance.

### 2. **Utility Modules**:
- **`data_utils.py`**:
  - Manages database interactions such as fetching swim session data, swimmer details, and performance metrics.
  
- **`convert_utils.py`**:
  - Handles data processing, including time conversions, scaling data for charts, and retrieving world records.

### 3. **Templates**:
The project uses HTML templates with Flask's `render_template` system for rendering views. Templates include:
   - `index.html`: The home/welcome page.
   - `select.html`: A generic form template for selecting swim sessions, swimmers, and events.
   - `chart.html`: Renders bar charts with swimmer times, averages, and world record data.

### 4. **Static Files**:
Contains resources like stylesheets, JavaScript, and images for enhancing the application interface and performance.

### 5. **Database Integration**:
   - Stores and accesses swim club data via a SQLite database, ensuring robust and efficient data management.

---

## Requirements

To run this project, ensure you have the following dependencies installed:

- Python 3.7 or higher
- Flask (`pip install flask`)
- SQLite3 (for database handling)


## Key Functionalities (Workflow)

### 1. **Home Page**:
   - A welcoming page where users can access swim-related data.

### 2. **Session Selection**:
   - List of available swim sessions fetched from the backend.

### 3. **Swimmer Selection**:
   - Based on the session date, users can filter swimmers by their name and age.

### 4. **Event Selection**:
   - View a swimmer's specific events (e.g., distances, strokes) from the chosen session.

### 5. **Performance Chart**:
   - Visual representation of swimmer performance through a bar chart, including average performance and world record comparisons.

---

## Future Enhancements

- **User Authentication**:
  - Add a login system to support personalized data management.

- **Extended Database Support**:
  - Expand database functionality to support additional swimming statistics, sessions, and reporting.

- **Mobile-Friendly Design**:
  - Optimize the UI for mobile devices with responsive templates.

- **Real-Time Data Updates**:
  - Allow users to upload new session data dynamically via CSV or editable forms.
