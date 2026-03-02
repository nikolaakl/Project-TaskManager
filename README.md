# TaskManager 
Object-oriented task management system supporting personal workflows and collaborative projects through a command-line interface.

- Designed and implemented custom heterogeneous containers without using STL

- Managed dynamic memory manually

- Developed task lifecycle management system (ON_HOLD, IN_PROCESS, DONE, OVERDUE)

- Implemented binary file persistence for users and tasks

- Built collaboration module with shared tasks and role-based access control

- Implemented automatic deadline validation and dashboard synchronization

# User Commands

- register \<username> \<password> – registers a new user with a username and password. User data is stored in a binary file

- login \<username> \<password> – logs in a registered user

- logout – logs out the current user

- exit – exits the program

 # Task Management Commands

- add-task \<name> \<due_date> \<description> – adds a new task with a default status of ON_HOLD. If a task with the same name and due date exists, an error is shown

- update-task-name \<id> \<name> – updates the name of a task with the given ID

- update-task-description \<id> \<description> – updates the description of a task with the given ID

- start-task \<id> – marks the task as IN_PROCESS

- finish-task \<id> – marks the task as DONE

- delete-task \<id> – deletes the task permanently

- get-task \<id> – shows task information for a task with the specified ID in a human-readable format

- get-task \<name> – shows task information for the task with the specified name and lowest ID

- list-tasks – lists all tasks for the logged-in user

- list-tasks \<date> – lists all tasks for the logged-in user with a specific due date

- list-completed-tasks – lists all tasks marked as DONE

#  Dashboard Commands

- add-task-to-dashboard \<id> – adds a task to the dashboard if its status is not OVERDUE

- remove-task-from-dashboard \<id> – removes a task from the dashboard

- list-dashboard – shows all tasks currently in the dashboard for today

# Collaboration Commands

- add-collaboration \<name> – creates a new collaboration (shared project).

- delete-collaboration \<name> – deletes a collaboration. Only the creator can delete it. All tasks within the collaboration are also removed

- list-collaborations – lists all collaborations for the current user (created or joined)

- add-user \<collaboration name> \<username> – adds a user to a collaboration

- assign-task \<collaboration name> \<username> \<name> \<due_date> \<description> – assigns a task to a user within a collaboration

- list-tasks \<collaboration name> – lists all tasks for a given collaboration, including assignees and statuses

## Technologies & Concepts:
C++, Object-Oriented Programming, Polymorphism, Dynamic Memory Management, Custom Data Structures, Binary File I/O, Date Handling (<ctime>)
