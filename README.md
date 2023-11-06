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
Our model is based on the structure of a hypothetical football team. At the heart of the data model lies the 'player' entity, representing the individuals who participate in the football team activities. Each player is identified by a unique 'playerid' and holds attributes such as their name, date of birth, and contact information. Players are often associated with specific teams, establishing a one-to-many relationship between the 'player' and 'team' entities.

The 'team' entity represents the groups of players who compete together. Each team has a unique 'teamid', a name, an age range, and a mascot. Teams are managed by 'coach' entities, establishing a one-to-one relationship between 'team' and 'coach'. Coaches are identified by a unique 'coachid' and possess attributes such as their name, experience, and contact information.

The team's facilities play a crucial role in enabling sports activities. The 'facility' entity represents the physical spaces where the football team practices and competitions take place. Each facility has a unique 'facilityid', a name, and a type (e.g., gym, field, etc). Facilities can be rented for various events, establishing a one-to-many relationship between 'facility' and 'rental of facility'.

Events, represented by the 'event' entity, are the organized competitions or training sessions that take place with the football team. Each event has a unique 'eventid', a name, a type (e.g., game, tournament, practice), a location, a date, and a time. Teams can register for events, establishing a one-to-many relationship between 'team' and 'event registration'.

Equipment, represented by the 'equipment' entity, comprises the various items used during activities. Each piece of equipment has a unique 'equipmentid', a type (e.g., ball, jersey, helmet), a description, a quantity, and a condition. Equipment can be checked out by players for use during events or practices, establishing a one-to-many relationship between 'player' and 'equipment checkout'.

Financial contributions to the football team are captured through the 'donation' entity. Each donation has a unique 'donationid', a donor's name, an amount, and a date. Sponserrs, represented by the 'sponser' entity, provide financial support to the football team from external organizations. Each sponser has a unique 'sponserid', a sponser's name, and contact information. The 'sponser' and 'donation' entities share a one-to-many relationship where a sponser can make many donations.

The team's staff, represented by the 'staff' entity, comprises the individuals who manage and support the team's operations. Each staff member has a unique 'staffid', a name, a position, and contact information. Staff members can be assigned to many different teams establishing a one-to-many relationship between them.

Injuries sustained by players are recorded through the 'injury' entity. Each injury has a unique 'injuryid', a type, a severity, the affected body part, and a date of occurrence. Many players can sustain the same injury which is represented by the one-to-many relationship between 'injury' and 'player'.

![Group Project Data Model Rough Draft 12](https://github.com/purwplhaze/mist4610_project1/assets/148249080/b719ba50-1d17-4e61-b73d-4cd5b47884e2)
