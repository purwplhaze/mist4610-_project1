# mist4610_project1

# Team Name:

# Team Members
1. Hayes Herzog
2. Jack Mathison
3. Carson Whitt
4. Marco Young
5. John Hulsey

# Problem Description
The task at hand is to model and build a relational database for the general workings of a football team. The central entity in the model is the 'team' entity. The team operates in conjunction with player, staff, coach, etc... in order to track equipment, events, facilities, and donatons. We are interested in modeling these relationships, generating samlple data, and populating the entities and their attributes with sample data. We are also interested in performing functioning queries on the data so that we can generate reports and build insight about operations within the footaball team.

# Data Model
Our model is based on the structure of a hypothetical football team. At the heart of the data model lies the 'Player' entity, representing the individuals who participate in the sports club's activities. Each player is uniquely identified by a 'playerid' and holds attributes such as their name, date of birth, and contact information. Players are often associated with specific teams, establishing a one-to-many relationship between the 'Player' and 'Team' entities.

The 'Team' entity represents the groups of players who compete together in various sports. Each team has a unique 'teamid', a name, an age range, a mascot, and a team captain. Teams are managed by 'Coach' entities, establishing a one-to-many relationship between 'Team' and 'Coach'. Coaches are identified by a unique 'coachid' and possess attributes such as their name, experience, and contact information.

The sports club's facilities play a crucial role in enabling sports activities. The 'Facility' entity represents the physical spaces where sports are practiced and competitions take place. Each facility has a unique 'facilityid', a name, and a type (e.g., gym, field, pool). Facilities can be rented for various events, establishing a one-to-many relationship between 'Facility' and 'Rental of Facility'.

Events, represented by the 'Event' entity, are the organized competitions or training sessions that take place at the sports club. Each event has a unique 'eventid', a name, a type (e.g., game, tournament, practice), a location, a date, and a time. Players can register for events, establishing a one-to-many relationship between 'Player' and 'Event Registration'. Teams can also participate in events, establishing a many-to-many relationship between 'Team' and 'Event'.

Equipment, represented by the 'Equipment' entity, comprises the various items used during sports activities. Each piece of equipment has a unique 'equipmentid', a type (e.g., ball, jersey, bat), a description, a quantity, and a condition. Equipment can be checked out by players for use during events or practices, establishing a one-to-many relationship between 'Player' and 'Equipment Checkout'.

Financial contributions to the sports club are captured through the 'Donation' entity. Each donation has a unique 'donationid', a donor's name, an amount, and a date. Sponsorships, represented by the 'Sponsorship' entity, provide financial support to the sports club from external organizations. Each sponsorship has a unique 'sponsorid', a sponsor's name, and contact information.

The sports club's staff, represented by the 'Staff' entity, comprises the individuals who manage and support the club's operations. Each staff member has a unique 'staffid', a name, a position, and contact information. Staff members can be assigned to specific facilities, establishing a one-to-many relationship between 'Staff' and 'Facility'.

Injuries sustained by players are recorded through the 'Specific Injury' entity. Each injury has a unique 'injuryid', a type, a severity, the affected body part, and a date of occurrence. Injuries are associated with the players who sustained them, establishing a one-to-one relationship between 'Player' and 'Specific Injury'.

These entities, with their interconnected relationships, form a comprehensive data model that represents the sports club's organizational structure, activities, and resource management. The data model provides a foundation for tracking player participation, managing teams and events, maintaining equipment inventories, recording financial transactions, monitoring player health, and ensuring the smooth operation of the sports club.

![Group Project Data Model 1670](https://github.com/purwplhaze/mist4610_project1/assets/148249080/5a2cb81b-0b6e-4d3b-ae0b-8df1e16e613c)
