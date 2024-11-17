# Post Timer Application

This Flutter application demonstrates a post list with individual timers for each post. The timers pause when a post is clicked and resume when the user navigates back. The application uses `GetX` for state management and routing to provide a seamless and reactive experience.

---

## Architectural Choices

### State Management
- **`GetX`**:
  - Handles reactive state management, dependency injection, and routing.
  - Reduces boilerplate while improving code maintainability.

### Modular Design
- Divided into controllers and views for better separation of concerns:
  - **`PostListView`**: Displays the list of posts and manages their timers.
  - **`PostDetailView`**: Shows detailed information about a selected post.
  - **`TimerController`**: Manages individual post timers, ensuring that timers work independently.

### Timer Management
- The timer system ensures:
  - Each post has its own timer.
  - Only the timer for the clicked post pauses, while others continue running.
  - Timers resume when the user navigates back to the list.

---

## Third-Party Libraries

1. **`http`**  
   - Handles API requests for fetching post data.

2. **`get`**  
   - Provides state management, dependency injection, and navigation.
   - Simplifies app development by offering a single, unified approach.

3. **`visibility_detector`**  
   - Monitors the visibility of list items (posts) to start or pause timers dynamically based on visibility.

---

## How to Run the Application

### Prerequisites
- Flutter SDK (latest stable version)
- Android Studio, VS Code, or any preferred IDE
- An emulator or a physical device for testing

### Setup
1. Clone the repository:
   ```
   git clone <repository-url>
   cd <repository-folder>
2. Install dependencies:
   ```
   flutter pub get
3. Run the application:
   ```
   flutter run
