# CS-360

## Reflection

### Requirements and Goals

Event Tracker was designed for users who need a simple way to keep track of personal events without relying on an internet connection or a complex calendar app. The main goals were secure local login, a persistent list of events that can be created, read, updated, and deleted, and support for optional reminders once notification permission is granted. The app addresses the need for a lightweight, private, offline organizer that keeps all data on the device.

### Screens and User-Centered UI

Three main screens support these needs: Login, Event List, and the permission screen. The Login screen uses clear labels, password masking, and separate buttons for logging in versus creating an account so new and returning users are both handled cleanly. The Event List shows events in a readable row layout with title, date/time, and a delete action; long-press enables editing. The permission screen explains why the permission is useful and lets the user grant or deny it without breaking the rest of the app. The UI keeps users in mind through consistent teal and orange colors, simple language, and layouts that prioritize the most common actions. These choices were successful because they make the core tasks (log in, see events, add or remove an event) fast and obvious.

### Coding Approach

The code is organized around a single SQLite helper class for both users and events, separate Activity classes for each screen, and a custom BaseAdapter for the event list. Dialogs are used for adding and editing so no extra activities were required. Runtime permission checks keep the app stable whether the user grants or denies notification access. Naming is consistent, and inline comments explain the purpose of each major block. The same pattern—dedicated helper, focused activities, and clear separation of UI from data—can be reused on future Android projects of similar size.

### Testing

Functionality was tested repeatedly on the Android Emulator. Login and account creation were checked with both valid and invalid credentials. Events were added, edited via long-press, and deleted to confirm the database and list stayed in sync. Permission denial was verified so the rest of the app continued to work. This process is important because it surfaces crashes and logic errors early; it revealed issues with dialog construction and emulator startup that were fixed before the final version.

### Innovation and Challenges

One challenge was keeping the project free of AppCompat dependencies after early theme and import problems. Switching fully to the platform Activity class and adjusting the permission request style resolved the crashes. Another challenge was the Add Event dialog initially crashing; rebuilding it with a simple LinearLayout of EditTexts produced a stable solution. The emulator occasionally failed to come online, which required cold boots and data wipes. These fixes kept the app running on the target platform without expanding the dependency footprint.

### Strongest Component

The combination of the SQLite DatabaseHelper and the Event List screen best demonstrates the skills developed in this project. The helper cleanly separates user authentication from event storage, supports all four CRUD operations, and keeps data persistent across app restarts. The list screen then surfaces that data with a custom adapter, immediate delete confirmation, and an add/edit dialog, giving the user a complete and reliable offline experience.
