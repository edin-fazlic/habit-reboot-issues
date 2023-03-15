# HabitReboot
### 1. Introduction
HabitReboot is an app designed to help users maintain their habits. The app allows for quick and easy habit creation without needing to log in or create an account. Once created it can be shared with others for preview and mutual contribution to creating milestones that keep the habit going. In the event that habit gets broken, such occurrence is automatically logged, which enables analyzing/identifying areas for improvement.

### 2. Features
HabitReboot includes the following features:
- Create a habit
- Break a habit with and without explanation
- Logs of breaking habit
- Add, update, delete milestones

### 3. User Interface
HabitReboot includes the following pages:
- Home page / Create a habit page
- Habit preview page
- Logs of breaking habit
- Milestones list page
- Milestone add/edit page

![alt text](https://github.com/edin-fazlic/habit-reboot-issues/blob/master/habitRebootSiteMap.drawio.png "SiteMap")

### 4. Functionality
#### 4.1. Home page https://github.com/edin-fazlic/habit-reboot-issues/issues/1
Home page shows web app general information, like help and about, but more importantly allows creation of a habit.

Components which support creation of a habit:
- input field, to enter habit title
- button, to confirm creation of a habit

When habit is created, user is navigated to the habit preview page.

#### 4.2. Habit preview page https://github.com/edin-fazlic/habit-reboot-issues/issues/2
Habit preview page of every habit is accessed via URL containing hard to guess id. As no authorization is required to create and access habits, this complex URL offers some protection from unwanted access, relying on the user to safeguard the URL link by not disclosing it.

Habit preview page shows counter in large font at the center of the screen. Counter ticks every second, and initially it is counter since habit was created. When habit is broken, counter is reset.

At the bottom of the screen, habit can be broken/reset using components:
- input field, to enter a reason for breaking habit
- button, to break habit (reset the counter), which shows a yes/no popup ("Interrupt a habit with no explanation?") in case input field is left empty

Once habit is broken, counter is reset, and breaking of habit is logged.

Habit preview page includes the following navigations:
- simple navigation to Home page
- link to page containing list of breaking habit logs
- link to Milestones list page.

#### 4.3. Logs of breaking habit https://github.com/edin-fazlic/habit-reboot-issues/issues/3
The page for breaking habit logs displays list of all logs. Each log is displayed with time of interruption and reasoning (if reasoning is left out display in italic font "no explanation"). The page includes obvious navigation back to the habit and a simple navigation to Home page.

#### 4.4. Milestones list page https://github.com/edin-fazlic/habit-reboot-issues/issues/4
The Milestones list page displays list of all milestones. Each milestone includes a color, title, time required to achieve it, info if milestone has been reached, action which navigates to editing of a milestone.

The page includes the following navigations:
- obvious navigation back to the habit
- link to create a new milestone
- simple navigation to Home page

#### 4.5. Milestone add/edit page https://github.com/edin-fazlic/habit-reboot-issues/issues/5
Milestones add/edit page shows the same content for both actions, adding and editing of the milestone. Form to input the data consists of the following components:
- field to select the color (color picker or a dropdown list of predefined colors)
- input field, to enter the milestone title
- numeric input field, to enter the amount of time required to reach the milestone (with dropdown to choose the unit: sec, min, hrs, days, etc.)
- button, to save (create or update) the milestone

When accessing the page to edit the milestone, fields are automatically prefilled.

The page includes the following navigations:
- obvious navigation back to the milestones list page discarding any changes made
- simple navigation to Home page

### 5. Technical Requirements
The HabitReboot is built using the following technologies:
- Backend: Java, Spring, PostgreSQL https://github.com/edin-fazlic/habit-reboot-issues/issues/11 https://github.com/edin-fazlic/habit-reboot-issues/issues/13
- Frontend: Angular https://github.com/edin-fazlic/habit-reboot-issues/issues/12

The app Frontend/Backend is hosted on a Netlify/Heroku cloud server respectively.

### 6. Out of scope
- Captcha https://github.com/edin-fazlic/habit-reboot-issues/issues/6  
When creating habits, since non authorized user can do that, request user to confirm that they are not a robot.
- Improved milestones https://github.com/edin-fazlic/habit-reboot-issues/issues/7  
Assign an icon to every milestone. When habit is opened for the first time in a session, animate obtained milestones. Offer calculation when determining that milestone has been reached (if time since last interruption was longer than the previous, last three interruptions were at least a week/month apart, etc.)
- Non responsive UI design https://github.com/edin-fazlic/habit-reboot-issues/issues/8  
Design is not responsive. It might not offer the best user-friendly experience on smaller resolutions.
- Multiple habits https://github.com/edin-fazlic/habit-reboot-issues/issues/9  
Create multiple habits on a single page (single URL link). It would include several counters for every habit, and a functionality to interrupt only one of those habits.
- Time zones https://github.com/edin-fazlic/habit-reboot-issues/issues/10  
When habit is created in one time zone, counter might not be correct in another time zone.
