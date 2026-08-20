# CS-360

# Reflection

**Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?**  
Event Tracker is an offline Android app that lets users create an account, log in, and manage a personal list of events with full add, view, update, and delete support. It was designed for people who need a simple, private way to organize events without an internet connection.

**What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?**  
The Login, Event List, and permission screens cover the core tasks of signing in, managing events, and handling optional reminders. Clear labels, consistent colors, and obvious primary actions keep the interface simple and usable, which made the main workflows fast and easy to understand.

**How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?**  
I organized the code with a single SQLite helper, separate activities for each screen, and a custom adapter for the event list. This separation of data and UI is a pattern I can reuse on future Android projects of similar size.

**How did you test to ensure your code was functional? Why is this process important, and what did it reveal?**  
I tested repeatedly on the Android Emulator by creating accounts, adding and deleting events, and checking both permission outcomes. Testing early revealed dialog and emulator issues that were fixed before the final version.

**Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?**  
Early AppCompat and dialog crashes forced a switch to platform Activities and a simpler dialog layout, which kept the app stable without extra dependencies.

**In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?**  
The SQLite DatabaseHelper combined with the Event List screen best shows the work, because together they deliver reliable offline storage and full CRUD operations in a clean list interface.
