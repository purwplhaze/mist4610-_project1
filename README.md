# # MIST4610 Project 1 #

# Team Name
MIST 4610 9:35-10:50 Group 9 

# Team Members
1. John Hulsey | @J-Hulsey
   
   REPO: https://github.com/purwplhaze/mist4610_project1
   
3. Jack Mathison | @JackMathison
   
   REPO: https://github.com/JackMathison/tissue
   
5. Carson Whitt | @whittcarson

   REPO: https://github.com/whittcarson/MIST4610GroupProject1
   
7. Justin Sullivan | @Justin7ime
   
   REPO: https://github.com/Justn7ime/effective-parakeet
   
9. Hayes Herzog | @purwplhaze
    
   REPO: https://github.com/purwplhaze/mist4610_project1
   

# Problem Description
The task at hand is to model and build a relational database for the general workings of a football team. The central entity in the model is the 'team' entity. The team operates in conjunction with players, staff, coaches in order to track equipment, injuries, events, donations, and rental of facilities. We are interested in modeling these relationships and populating the entities and their attributes with sample data. We are also interested in performing functioning queries on the data so that we can generate reports and build insight about operations within the footaball team.

# Data Model
In this football team database, the entities represent the various aspects and participants involved in managing a football organization. Each entity is equipped with attributes that provide details essential to the organization's operation, such as personal information, roles, and activities within the team structure.

The team entity holds central information about each football team, including its unique identifier, name, average age of players, mascot, and the captain's name. It is directly related to several other entities that provide a comprehensive view of the team's functioning. For instance, each team is associated with multiple staff members; this one-to-many relationship indicates that a team has various staff members fulfilling different roles, identified by their names, contact information, and specific position within the team.

Coaches are crucial to a team's performance and are tracked in the database by their full name, experience, specialty, and contact info. Each coach is linked to one football team, following the one-to-many relationship paradigm, suggesting that while a coach is dedicated to a single team, the team could have multiple coaches, one or many for different aspects of the game such as offense, defense, and special teams.

The player entity captures detailed information on every individual player, including their first and last name, date of birth, contact info, and position on the team. Each player is associated with one team, hinting at an exclusive contract situation. While a player can only play for one team, by nature, a team has multiple players.

Sponsor entities are external supporters of the football team. They are detailed by their name and contact information. Sponsors are linked to donations, where each sponsor can make multiple donations, but each donation is specifically tied to one sponsor and one team, emphasizing the targeted support sponsors provide to the teams.

Donations are financial contributions made by sponsors, recorded with details such as the amount, date, and the related sponsor and team. The entity reflects the financial support structure behind sports teams, with many donations potentially supporting a single team.

Football teams require equipment, and the equipment entity tracks each item by name, quantity, and condition. Players use the equipment, which leads to the equipment_checkout entity, indicating a many-to-one relationship where multiple pieces of equipment are checked out by players over time. The checkout process is logged with dates for accountability and management.

Players may, unfortunately, suffer injuries, which are recorded in the specific_injury entity. This entity captures the association between a player and their injury, the type of which is detailed in the injury entity. Injuries are characterized by the affected body part and the severity, acknowledging that one injury type can be associated with multiple instances of player injuries.

The facility entity manages the locations where football activities occur, including their name, type (e.g., stadium, training ground), and availability. Facilities are rented for events, as tracked by the rental_of_facility entity, which also logs the renting party's name and contact information. Since multiple facilities might be rented for a single event, such as a tournament, this creates a one-to-many relationship with the event entity.

Lastly, events are any significant occurrences, like games or tournaments, associated with the team. The event entity captures details like the event's name, date, type (e.g., game, practice, meeting), and result.

Overall, this football team database is designed to comprehensively represent and manage the complex interactions, activities, and components that make up a professional football team's ecosystem. From the individuals who play, coach, and manage, to the logistical elements of equipment and facilities, the database's entities and their interrelationships provide a structured insight into the team's operations.

![project1_model](https://github.com/purwplhaze/mist4610_project1/assets/148249080/689f3f19-eb51-4e6c-9147-0c7bc3c6946d)

# Data Dictionary
![Screenshot 2023-11-07 at 12 56 34 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/1eb363f5-3d52-4f7c-9ee3-f41c403d2428)

![Screenshot 2023-11-07 at 12 57 21 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/a1e044e3-de85-4c12-8b80-e358c739294f)

![Screenshot 2023-11-07 at 12 57 33 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/60528420-6ece-4f74-92fd-df8e78855b93)

![Screenshot 2023-11-07 at 12 58 54 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/0362cbcb-48e0-4134-9fef-0411f4154b36)

![Screenshot 2023-11-07 at 12 59 14 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/c5596454-aadc-485e-b67f-33de52033296)

![Screenshot 2023-11-07 at 12 59 06 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/18fcadc3-d25a-487d-b849-84b38ecaef84)

![Screenshot 2023-11-07 at 12 59 40 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/3505ecaa-a985-4089-8d85-249b3601473d)

![Screenshot 2023-11-07 at 12 59 27 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/46848010-25ab-4b27-af28-bb04963fdeba)

![Screenshot 2023-11-07 at 12 57 43 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/c12eb111-9d7b-45ff-9a66-16acb3f4c9c5)

![Screenshot 2023-11-07 at 12 57 54 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/27d93c9d-e4d5-4825-8ff1-4b0307e3dc9b)

<img width="624" alt="Screenshot 2023-11-07 at 2 26 18 PM" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/a4c5ec41-639e-4300-a2a3-5783067db3c8">

![Screenshot 2023-11-07 at 12 56 15 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/6587a198-e53e-420b-9d81-e57d4b9e70ff)

![Screenshot 2023-11-07 at 12 56 25 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/4b776c94-09cd-4acf-83ec-82a34adbb244)

# Queries

**QUERY 1**

Query 1 lists the team name and ID for any team having players out from injuries, specifically those who will be recovering for a time greater than 2 months. The results are also grouped by teams having at least 2 players with long-term injuries.

<img width="702" alt="A1" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/233cdba3-0bdf-4b17-bc1f-99ae4ea929b4">


This query allows managers to quickly determine how what teams have players benched due to entended injury. During the season, it is crucial to know what key players you might be lacking on your team, and also what other teams are suffering the loss of players. Then coaches can make strategic changes to a game plan. Grouping by teams who have at least 2 players out for an extended time also shows what teams may be more vulnerable with more players injured.

RESULTS

<img width="287" alt="Q1" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/ac2aea6e-30ef-47da-a6e9-c2c8b02e8c26">

**QUERY 2**

Query 2 reports the information regarding renter information when booking an event and that event was a winning game. Results are ordered by descending book date to better organize the information in chronological order.

<img width="523" alt="A2" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/7ad050f7-76a1-4d24-9fc5-69abd3ade6f6">


Query 2 is helpful in allowing a manager access to information regarding the renter of a facility. It also allows the manager to pinpoint groups of information by detailing the event type and event result. Having previous renters' information can reduce the trouble of reaching out to a renter should problems arise during the event.

RESULTS

<img width="661" alt="Q2" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/bf2fe28a-275d-47a4-8081-5023848c6c0c">

**QUERY 3**

Query 3 retrieves information about about what players have checked out certain equipment items and have since returned the item.

<img width="631" alt="A3" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/8b8feb81-769e-41b8-88a3-118b96adc47a">


Keeping track of equipment inventory is a big job for a team. Query 3 provides easy access to listings of players who have returned their items, subsequently allowing someone to know what items are still checked out. The query will also reveal trends to teams about which players keep items the longest and what items are most commonly checked out.

RESULTS

<img width="819" alt="Q3" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/2b4ebe3c-8991-4194-a1f5-90b66b43898d">

**QUERY 4**

This query reports donations, by team, that have a value greater than the average donation value for their team.

<img width="877" alt="A4" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/30de6306-c7c8-4d0b-937d-89e0d65f90cb">


It is important for teams and sponsors to keep track of the flow of donations and where those donations are coming from. By understanding which donors on each team are generally gifting more money, financial linguistics officials will have more concrete reasoning to pursue certain people versus others when looking to fundraise.

RESULTS

<img width="970" alt="Q4" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/743c3679-9837-4fcf-82ac-76b58518ac58">

**QUERY 5**

This query selects teams who have rented a facility for the purpose of practicing or watching film from a previous game, but who also have an offensive coordinator with less than 8 years of experience. The results are ordered by the correlating event date.

<img width="774" alt="A5" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/220821cc-d582-4d46-82f0-e9874c5e8704">


Query 5 allows a person to see when teams are training and how they split that time between practice and film review. The results also show teams where they stand with total experience among coaches. A team may use this information and gain more confidence in its possibilities or cause it to think about hiring new coaching staff to balance the skill set.

RESULTS

<img width="804" alt="Q5" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/c3b65011-8e46-4ff0-9a5e-83c35ace73c5">

**QUERY 6**

Query 6 identifies how many injured players a team had before a specified date, and lists the injured players’ ID, date of birth, position, and the severity of the injury. Results are ordered by ascending teamID.    

<img width="806" alt="A6" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/4df20172-34ea-4669-b575-010fcdd8f9c7">


Query 6 becomes valuable to a team and coaches by creating a way of determining what players were hurt before a specific date alongside information about the severity of the injury in order to make an estimate on how much longer a specific player might be hurt.

RESULTS

<img width="1105" alt="Q6" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/087e70ca-39b4-413a-a24f-5611bfc9f4a5">

**QUERY 7**

This query lists the staffID and name of staff members working for certain teams by relating the team’s name or mascot.

<img width="440" alt="A7" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/798518df-78e9-427d-a37b-fa000e57d12e">


Team managers will use query 7 to track which staff members are working under which teams. The staff work with many teams and managers may use this information to increase organization and the ease of identifying staff members under a range of teams.


RESULTS

<img width="320" alt="Q7" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/9a66e624-895b-4492-bf05-f07dfebd18e5">

**QUERY 8**

The query identifies football teams that have an above-average frequency of equipment checkouts. It counts how many times equipment has been checked out for each team, presenting this number alongside the team’s ID, name, and mascot. The teams included in the results are those where the count of equipment checkouts per team is greater than the average number of checkouts across all teams.

<img width="961" alt="A8" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/7ac4b21a-ff59-4a59-b165-45e200b12df5">


For a football team manager, this information is crucial for inventory management. Teams with high equipment checkout rates may have higher wear and tear on gear, indicating a potential need for more frequent replacements or the purchase of additional equipment to meet demand.



RESULTS

<img width="715" alt="Q8" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/86428e07-a18e-4d52-b885-6dfb2c2c61fc">

**QUERY 9**

The query tallies the number of donations made to football teams from sponsors identified as tech companies—specifically Verizon, Microsoft, Cisco Systems, and Uber Eats. It shows each team's ID, name, and mascot, along with the total number of donations received, only including teams that have received more than one donation. The results are sorted in descending order of the number of donations.

<img width="763" alt="A9" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/2bad3075-fad9-411c-be69-93dafbae3685">

From a team manager's standpoint, this query is useful for recognizing and prioritizing relationships with key sponsors. By understanding which tech companies are most supportive, the manager can focus on nurturing these partnerships, allocating appropriate recognition and engagement efforts to maintain and possibly increase their support.


RESULTS

<img width="626" alt="Q9" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/17e45704-8199-45ef-99c6-9b91ed55103b">

**QUERY 10**

The query retrieves details of players who have borrowed helmets from their football team and have not returned them. It connects player and equipment records, focusing on unreturned helmets by checking for a null return date and lists them along with player and team details, sorting by the date the helmets were borrowed.

<img width="930" alt="A10" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/d3ca6649-f413-4874-8abb-8eca499fd43b">

For a football team manager, this query helps manage equipment efficiently, ensuring helmets are returned on time for use by other players and maintaining safety standards by keeping track of gear usage.



RESULTS
<img width="1025" alt="Q10" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/a4dec95a-38aa-4a73-9333-73482341a26d">

# Query Features

<img width="694" alt="DatabaseInfo" src="https://github.com/whittcarson/MIST4610GroupProject1/assets/131502055/e4976440-2dc9-44be-8382-6e666b71be71">


# Database Information
Name of the database: cs_g9p1

Additional Information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
