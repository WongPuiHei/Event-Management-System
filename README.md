# Event Management System

A C++ application for managing events, room bookings, and event registrations in an academic environment. The system supports different types of users (Students, Faculty, and Coordinators) and handles various room types including conference rooms.

## Features

### User Management
- Support for different user types:
  - Students (can register for events)
  - Faculty (can create events)
  - Coordinators (can approve room bookings)

### Event Management
- Create new events with detailed information:
  - Event name
  - Date and time
  - Location details
  - Capacity
- Event registration system for students
- Event approval workflow

### Room Management
- Different room types (including Conference Rooms)
- Room features tracking:
  - Projector availability
  - Video conferencing capability
  - Room capacity
- Room booking system with availability checking
- Room allocation based on requirements

### Validation & Security
- Input validation for:
  - Email addresses
  - Date formats
  - Time formats
  - User IDs
- Data integrity checks

## Project Structure

### Core Components
- `BookingManager`: Handles room booking operations
- `EventManager`: Manages event creation and registration
- `RoomFactory`: Creates different types of rooms
- `Utils`: Contains utility functions for validation and input handling

### User Classes
- `User`: Base class for all users
- `Student`: Handles student-specific functionality
- `Faculty`: Manages faculty-specific operations
- `Coordinator`: Implements coordinator-specific features

### Room Classes
- `IRoom`: Interface for room implementations
- `Room`: Base room implementation
- `ConferenceRoom`: Specialized room type with additional features

## Getting Started

### Prerequisites
- C++ compiler (GCC recommended, version 8.0 or higher)
- Code::Blocks IDE (version 20.03 or higher)
- C++17 or later
- Minimum 4GB RAM recommended
- 100MB free disk space

### Building the Project
1. Open the project in Code::Blocks
2. Build using the provided project file (`project.cbp`)
3. Run the compiled executable

### Configuration
1. Room Types Setup
   ```cpp
   // Example room configuration in RoomFactory
   Room* createRoom(const std::string& type, const std::string& id) {
       if (type == "conference") {
           return new ConferenceRoom(id, "Main Building", 50, true, true);
       }
       // Add more room types as needed
   }
   ```

2. User Permissions
   - Faculty IDs must start with 'F' (e.g., F101)
   - Student IDs must start with 'S' (e.g., S201)
   - Coordinator IDs must start with 'C' (e.g., C301)

### Usage
1. Launch the application
2. Choose from available options:
   - Create new events (Faculty)
   - Register for events (Students)
   - Approve room bookings (Coordinator)
   - View available events
   - Exit

## Development

### Build Configuration
The project includes two build configurations:
- Debug: Includes debugging information
- Release: Optimized for performance

### Project Files
- `project.cbp`: Code::Blocks project file
- `project.layout`: IDE layout configuration
- `project.depend`: Dependency information

### Application Interface

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License
[Add your chosen license here]

## Authors
[Add author information here] 