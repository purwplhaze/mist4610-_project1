# mist4610_project1

# Team Name:

# Team Members
1. Hayes Herzog
2. Jack Mathison
3. Carson Whitt
4. Marco Young
5. John Hulsey

# Problem Description
The task at hand is to model and build a relational database for the general workings of a football team. The central entity in the model is the 'team' entity. The team operates in conjunction with players, staff, coaches in order to track equipment, injuries, events, and donatons. We are interested in modeling these relationships and populating the entities and their attributes with sample data. We are also interested in performing functioning queries on the data so that we can generate reports and build insight about operations within the footaball team.

# Data Model
In this football team database, the entities represent the various aspects and participants involved in managing a football organization. Each entity is equipped with attributes that provide details essential to the organization's operation, such as personal information, roles, and activities within the team structure.

The team entity holds central information about each football team, including its unique identifier, name, average age of players, mascot, and the captain's name. It is directly related to several other entities that provide a comprehensive view of the team's functioning. For instance, each team is associated with multiple staff members; this one-to-many relationship indicates that a team has various staff members fulfilling different roles, identified by their names, contact information, and specific position within the team.

Coaches are crucial to a team's performance and are tracked in the database by their full name, experience, specialty, and contact info. Each coach is linked to one football team, following the one-to-many relationship paradigm, suggesting that while a coach is dedicated to a single team, the team could have multiple coaches, possibly for different aspects of the game such as offense, defense, and special teams.

The player entity captures detailed information on every individual player, including their first and last name, date of birth, contact info, and position on the team. Each player is associated with one team, hinting at an exclusive contract situation typical in sports organizations.

Sponsor entities are external supporters of the football team. They are detailed by their name and contact information. Sponsors are linked to donations, where each sponsor can make multiple donations, but each donation is specifically tied to one sponsor and one team, emphasizing the targeted support sponsors provide to the teams.

Donations are financial contributions made by sponsors, recorded with details such as the amount, date, and the related sponsor and team. The entity reflects the financial support structure behind sports teams, with many donations potentially supporting a single team.

Football teams require equipment, and the equipment entity tracks each item by name, quantity, and condition. Players use the equipment, which leads to the equipment_checkout entity, indicating a many-to-one relationship where multiple pieces of equipment are checked out by players over time. The checkout process is logged with dates for accountability and management.

Players may, unfortunately, suffer injuries, which are recorded in the specific_injury entity. This entity captures the association between a player and their injury, the type of which is detailed in the injury entity. Injuries are characterized by the affected body part and the severity, acknowledging that one injury type can be associated with multiple instances of player injuries.

The facility entity manages the locations where football activities occur, including their name, type (e.g., stadium, training ground), and availability. Facilities are rented for events, as tracked by the rental_of_facility entity, which also logs the renting party's name and contact information. Since multiple facilities might be rented for a single event, such as a tournament, this creates a many-to-one relationship with the event entity.

Lastly, events are any significant occurrences, like games or tournaments, associated with the team. The event entity captures details like the event's name, date, type (e.g., game, practice, meeting), and result.

Overall, this football team database is designed to comprehensively represent and manage the complex interactions, activities, and components that make up a professional football team's ecosystem. From the individuals who play, coach, and manage, to the logistical elements of equipment and facilities, the database's entities and their interrelationships provide a structured insight into the team's operational dynamics.

![project1_model](https://github.com/purwplhaze/mist4610_project1/assets/148249080/689f3f19-eb51-4e6c-9147-0c7bc3c6946d)

# Data Dictionary
![Screenshot 2023-11-07 at 12 56 15 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/99fcf4e2-57f4-4ddf-9aa1-81a0bd84667f)
