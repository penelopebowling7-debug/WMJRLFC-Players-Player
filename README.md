## Project Executive Summary

**Project Name:** Wallsend Maryland Junior Rugby League Football Club – Player’s Player Voting App

### Overview

This project is a lightweight web-based application designed to allow junior rugby league teams to conduct weekly **Player’s Player voting** in a simple, fair, and transparent way.

The system enables players to vote for the teammate who demonstrated the best team spirit, effort, and sportsmanship after each game.

The application was initially developed for a single team and has since been expanded to support **multiple teams across a club**, with independent voting, administration, and audit tracking.

The solution is intentionally designed to be:

* Simple to deploy
* Low maintenance
* Secure enough for junior sport use
* Accessible on any mobile device
* Easy for non-technical volunteers to operate

---

### Purpose

The primary purpose of the system is to:

* Encourage sportsmanship and team culture
* Provide a fair and transparent voting mechanism
* Reduce manual tallying and errors
* Enable consistent weekly recognition of players
* Provide visibility for coaches and administrators

Secondary goals include:

* Supporting multiple teams within a single club
* Allowing independent team setup
* Providing basic governance and accountability
* Serving as a foundation for future club-wide digital tools

---

### Target Users

* Junior rugby league players
* Coaches
* Team managers
* Club administrators
* Parents

---

### Key Features

#### Team Setup

* Coaches can create their own team
* Coaches define:

  * Team name
  * Coach name
  * Coach PIN
  * Player list
* Supports multiple teams within the same age group
  Example:

  * U12's Black
  * U12's Orange

---

#### Voting System

* Each player votes once per round
* Voting can be opened or locked by the coach
* Voting is confirmed before submission
* Duplicate voting is prevented
* Voting is isolated per team

---

#### Round Management

Coaches can:

* Open voting
* Lock voting
* Move to the next round
* View round tallies
* View season tallies
* Track which players have voted

---

#### Player Management

Coaches can:

* Add players
* Edit player names
* Remove players
* Restore removed players

All historical votes are preserved.

---

#### Club Administration

A club administrator role has been implemented with additional permissions.

Admin capabilities include:

* Reset coach PIN
* Reset current round
* Reset entire season
* Add teams
* Remove teams
* View audit trail

---

#### Audit Trail

All administrative actions are logged, including:

* Coach PIN resets
* Round resets
* Season resets
* Team creation
* Team removal

Each log entry records:

* Action
* Team
* Details
* Timestamp

---

### Technology Stack

Frontend:

* HTML
* CSS
* JavaScript (Vanilla)

Backend:

* Firebase Firestore (NoSQL database)

Hosting:

* GitHub Pages

Authentication Model:

* PIN-based access control
* No user accounts
* No personal identity storage

---

### Data Model (Simplified)

collections:

teams
teams/{teamId}
teams/{teamId}/players
teams/{teamId}/seasonVotes
teams/{teamId}/roundVotes
teams/{teamId}/roundAudit
adminAudit

---

### Security Model

The application intentionally avoids collecting sensitive personal information.

Stored data includes:

* Player names
* Votes
* Team configuration

The system does not store:

* Email addresses
* Phone numbers
* Personal data
* Location data
* Authentication credentials

Security controls include:

* Team-level isolation
* Coach PIN protection
* Admin PIN protection
* Audit logging for administrative actions

---

### Deployment Model

The application is deployed using:

GitHub Pages

This provides:

* Free hosting
* Version control
* Simple rollback capability
* Public accessibility

No server infrastructure is required.

---

### Design Principles

The project prioritises:

* Simplicity
* Reliability
* Transparency
* Low technical overhead
* Ease of use for volunteers
* Maintainability

---

### Current Status

Version: Production-ready for club use

The system currently supports:

* Multiple teams
* Independent voting
* Admin controls
* Audit tracking
* Mobile-friendly interface
* Browser-based installation (Add to Home Screen)

---

### Future Enhancements (Planned)

Potential future improvements include:

* Club-wide dashboard
* Season reporting
* Export to CSV / Excel
* Role-based permissions
* Team statistics
* Award tracking
* Integration with club communication systems
* Multi-club support

---

### Project Author

Developed by a club volunteer to support junior sport operations and reduce administrative workload while encouraging positive team culture.
