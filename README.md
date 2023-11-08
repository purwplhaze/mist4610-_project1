# MIST4610_project1

# Team Members
1. John Hulsey
2. Jack Mathison
3. Carson Whitt
4. Justin Sullivan
5. Hayes Herzog

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

![Screenshot 2023-11-07 at 12 58 40 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/b4964f17-dad2-48a4-a9b7-e6046d6494f6)

![Screenshot 2023-11-07 at 12 56 15 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/6587a198-e53e-420b-9d81-e57d4b9e70ff)

![Screenshot 2023-11-07 at 12 56 25 AM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/4b776c94-09cd-4acf-83ec-82a34adbb244)

# Queries
![Screenshot 2023-11-07 at 10 55 00 PM](https://github.com/purwplhaze/mist4610_project1/assets/148249080/2759845c-2f01-48c7-addb-20b39c08d76a)

Q1.
Query 1 lists the team name and ID for any team having players out from injuries, specifically those who will be recovering for a time greater than 2 months. The results are also grouped by teams having at least 2 players with long-term injuries.

> Select team_name, teamid 
From injury Join specific_injury On injuryid = injury_injuryid Join player On 
    player_playerid = playerid Join team On team_teamid = teamid
Where injury_severity RegExp "4-6 Months|6-8 Months|6-12 Months"
Group By team_name, teamid
Having Count(playerid) >= 2

+ -------------- + ----------- +
| team_name      | teamid      |
+ -------------- + ----------- +
| Carolina       | 2           |
| Tampa Bay      | 4           |
| Los Angeles    | 7           |
+ -------------- + ----------- +
3 rows

This query allows managers to quickly determine how what teams have players benched due to entended injury. During the season, it is crucial to know what key players you might be lacking on your team, and also what other teams are suffering the loss of players. Then coaches can make strategic changes to a game plan. Grouping by teams who have at least 2 players out for an extended time also shows what teams may be more vulnerable with more players injuered.

Q2.
Query 2 reports the information regarding renter information when booking an event and that event was a winning game. Results are ordered by descending book date to better organize the information in chronological order.

> Select event_id, renter_name, renter_contact_info, book_date 
From rental_of_facility Join event On event_id = event_event_id
Where event_type RegExp 'Game'
And event_result RegExp 'Win'
Order By book_date Desc

+ ------------- + ---------------- + ------------------------ + -------------- +
| event_id      | renter_name      | renter_contact_info      | book_date      |
+ ------------- + ---------------- + ------------------------ + -------------- +
| 8             | Ulysses Grant    | management@atlfalcons.com | 2023-10-26     |
| 2             | John Adams       | management@nolasaints.com | 2023-10-15     |
+ ------------- + ---------------- + ------------------------ + -------------- +
2 rows

Query 2 is helpful in allowing a manager access to information regarding the renter of a facility. It also allows the manager to pinpoint groups of information by detailing the event type and event result. Having previous renters' information can reduce the trouble of reaching out to a renter should problems arise during the event.

Q3.
Query 3 retrieves information about about what players have checked out certain equipment items and have since returned the item.

> Select equipment_name, player_l_name, player_f_name, player_position 
From equipment Join equipment_checkout On equipmentid = equipment_equipmentid 
Join player On player_playerid = playerid
Where equipment_equipmentid In (3,4,5) And Exists
(Select return_date From equipment_checkout)
Group By player_position, equipment_name, player_l_name, player_f_name

+ ------------------- + ------------------ + ------------------ + -------------------- +
| equipment_name      | player_l_name      | player_f_name      | player_position      |
+ ------------------- + ------------------ + ------------------ + -------------------- +
| Jersey              | Davis              | Tae                | Linebacker           |
| Jersey              | Montana            | Joe                | Quarter Back         |
| Cleats              | Jefferson          | Van                | Wide Receiver        |
+ ------------------- + ------------------ + ------------------ + -------------------- +
3 rows

Keeping track of equipment inventory is a big job for a team. Query 3 provides easy access to listings of players who have returned their items, subsequently allowing someone to know what items are still checked out. The query will also reveal trends to teams about which players keep items the longest and what items are most commonly checked out.

Q4.
This query reports donations, by team, that have a value greater than the average donation value for their team.

> Select team_name, team_mascot, donation_amount, donor_f_name, donor_l_name, sponsor_name
from team, donation, sponser
where team.teamid = donation.team_teamid
and donation.sponser_sponserid = sponser.sponserid
and donation_amount >= (select avg(donation_amount) from donation where donation.team_teamid = team.teamid)
Order by team_name, donation_amount

+ -------------- + ---------------- + -------------------- + ----------------- + ----------------- + ----------------- +
| team_name      | team_mascot      | donation_amount      | donor_f_name      | donor_l_name      | sponsor_name      |
+ -------------- + ---------------- + -------------------- + ----------------- + ----------------- + ----------------- +
| Atlanta        | Falcons          | 400000               | Cedric            | Daniels           | Uber Eats         |
| Atlanta        | Falcons          | 420000               | Omar              | Little            | Subway            |
| Atlanta        | Falcons          | 760000               | Paulie            | Galiteri          | Visa              |
| Atlanta        | Falcons          | 800000               | Cedric            | Daniels           | Uber Eats         |
| Carolina       | Panthers         | 1000000              | Logan             | Roy               | Cisco Systems     |
| Carolina       | Panthers         | 2500000              | Logan             | Roy               | Cisco Systems     |
| Detroit        | Lions            | 1000000              | James             | McNulty           | Visa              |
| Jacksonville   | Jaguars          | 900                  | Jay               | Landsman          | DraftKings        |
| Los Angeles    | Rams             | 6969                 | Roman             | Roy               | Cisco Systems     |
| Los Angeles    | Chargers         | 9900                 | Carmela           | Soprano           | Gatorade          |
| New Orleans    | Saints           | 1600000              | Corrado           | Soprano           | Gatorade          |
| New York       | Giants           | 150000               | Corrado           | Soprano           | Gatorade          |
| New York       | Jets             | 8000                 | Josh              | Lyman             | Verizon           |
| Tampa Bay      | Buccaneers       | 6000000              | Tony              | Soprano           | Gatorade          |
+ -------------- + ---------------- + -------------------- + ----------------- + ----------------- + ----------------- +
14 rows

It is important for teams and sponsors to keep track of the flow of donations and where those donations are coming from. By understanding which donors on each team are generally gifting more money, financial linguistics officials will have more concrete reasoning to pursue certain people versus others when looking to fundraise.

Q5.
This query selects teams who have rented a facility for the purpose of practicing or watching film from a previous game, but who also have an offensive coordinator with less than 8 years of experience. The results are ordered by the correlating event date.

> Select teamid, team_name, coach_l_name, event_date, Count(teamid) As inexperienced_coaches 
From event Join rental_of_facility On event_id = event_event_id Join team On 
rental_of_facility.team_teamid = teamid Join coaches On teamid = coaches.team_teamid
Where event_type RegExp 'Practice|^Film'
And Lower(coach_specialty) RegExp 'offensive coordinator'
And coach_experience RegExp '1|2|3|4|5|6|7'
Group BY event_date, team_name, teamid, coach_l_name
Order By event_date

+ ----------- + -------------- + ----------------- + --------------- + -------------------------- +
| teamid      | team_name      | coach_l_name      | event_date      | inexperienced_coaches      |
+ ----------- + -------------- + ----------------- + --------------- + -------------------------- +
| 4           | Tampa Bay      | Canales           | 2023-10-24      | 1                          |
+ ----------- + -------------- + ----------------- + --------------- + -------------------------- +
1 rows

Query 5 allows a person to see when teams are training and how they split that time between practice and film review. The results also show teams where they stand with total experience among coaches. A team may use this information and gain more confidence in its possibilities or cause it to think about hiring new coaching staff to balance the skill set.

Q6.
Query 6 identifies how many injured players a team had before a specified date, and lists the injured players’ ID, date of birth, position, and the severity of the injury. Results are ordered by ascending teamID.

> Select team_name, teamid, Count(Distinct playerid) As players_injured, 
playerid, player_dob, player_position, injury_severity
From team Join player On teamid = team_teamid Join specific_injury On 
playerid = player_playerid Join injury On injury_injuryid = injuryid
Where injury_date < '2023-10-19'
Group By team_name, teamid, player_position, injury_severity, player_dob, playerid
Order By teamid

+ -------------- + ----------- + -------------------- + ------------- + --------------- + -------------------- + -------------------- +
| team_name      | teamid      | players_injured      | playerid      | player_dob      | player_position      | injury_severity      |
+ -------------- + ----------- + -------------------- + ------------- + --------------- + -------------------- + -------------------- +
| Atlanta        | 1           | 1                    | 1             | 1997-12-13      | Safety               | 4-6 Months           |
| Carolina       | 2           | 1                    | 6             | 1996-03-30      | Linebacker           | 6-12 Months          |
| Carolina       | 2           | 1                    | 5             | 2000-05-11      | Offensive Line       | 1-3 Weeks            |
| Carolina       | 2           | 1                    | 5             | 2000-05-11      | Offensive Line       | 6-8 Months           |
| New Orleans    | 3           | 1                    | 8             | 2000-09-01      | Tight End            | 2-4 Weeks            |
| Tampa Bay      | 4           | 1                    | 10            | 2001-11-06      | Defensive Line       | 1-2 Months           |
| Tampa Bay      | 4           | 1                    | 12            | 1998-12-27      | Offensive Line       | 1-2 Months           |
| New York       | 5           | 1                    | 13            | 1994-01-12      | Wide Receiver        | 4-6 Months           |
+ -------------- + ----------- + -------------------- + ------------- + --------------- + -------------------- + -------------------- +
8 rows

Query 6 becomes valuable to a team and coaches by creating a way of determining what players were hurt before a specific date alongside information about the severity of the injury in order to make an estimate on how much longer a specific player might be hurt.

Q7.
This query lists the staffID and name of staff members working for certain teams by relating the team’s name or mascot.

> Select staffid, staff_name From staff 
Where staffid In (Select staff_staffid From team
Where team_name RegExp 'Atlanta|Jacksonville'
or
team_mascot RegExp 'Giants')
Order By staffid

+ ------------ + --------------- +
| staffid      | staff_name      |
+ ------------ + --------------- +
| 55           | Alex Kemp       |
| 97           | Tom Hill        |
| 117          | John Jenkins    |
| NULL         | NULL            |
+ ------------ + --------------- +
4 rows

Team managers will use query 7 to track which staff members are working under which teams. The staff work with many teams and managers may use this information to increase organization and the ease of identifying staff members under a range of teams.

Q8.
This query identifies football teams that have an above-average frequency of equipment checkouts. It counts how many times equipment has been checked out for each team, presenting this number alongside the team’s ID, name, and mascot. The teams included in the results are those where the count of equipment checkouts per team is greater than the average number of checkouts across all teams.

> SELECT team.teamid, team.team_name, team.team_mascot, COUNT(equipment_checkout.checkoutid) as NumberOfEquipmentCheckouts
FROM team, player, equipment_checkout
WHERE team.teamid = player.team_teamid
AND player.playerid = equipment_checkout.player_playerid
GROUP BY team.teamid, team.team_name, team.team_mascot
HAVING COUNT(equipment_checkout.checkoutid) > (
    SELECT AVG(NumberOfEquipmentCheckouts)
    FROM (
        SELECT team.teamid, COUNT(equipment_checkout.checkoutid) as NumberOfEquipmentCheckouts
        FROM team, player, equipment_checkout
        WHERE team.teamid = player.team_teamid
        AND player.playerid = equipment_checkout.player_playerid
        GROUP BY team.teamid
    ) AS calc
)

+ ----------- + -------------- + ---------------- + ------------------------------- +
| teamid      | team_name      | team_mascot      | NumberOfEquipmentCheckouts      |
+ ----------- + -------------- + ---------------- + ------------------------------- +
| 3           | New Orleans    | Saints           | 5                               |
| 4           | Tampa Bay      | Buccaneers       | 4                               |
| 9           | Detroit        | Lions            | 3                               |
+ ----------- + -------------- + ---------------- + ------------------------------- +
3 rows

For a football team manager, this information is crucial for inventory management. Teams with high equipment checkout rates may have higher wear and tear on gear, indicating a potential need for more frequent replacements or the purchase of additional equipment to meet demand.

Q9.
This query tallies the number of donations made to football teams from sponsors identified as tech companies—specifically Verizon, Microsoft, Cisco Systems, and Uber Eats. It shows each team's ID, name, and mascot, along with the total number of donations received, only including teams that have received more than one donation. The results are sorted in descending order of the number of donations.

> SELECT team.teamid, team.team_name, team_mascot, count(donation_amount) as CountOfDonations
FROM team, donation, sponser
WHERE team.teamid = donation.team_teamid
AND sponser.sponserid = donation.sponser_sponserid
AND sponsor_name regexp 'Verizon|Microsoft|Cisco Systems|Uber Eats'
GROUP BY team.teamid
HAVING count(donation_amount) > 1
ORDER BY CountOfDonations desc

+ ----------- + -------------- + ---------------- + --------------------- +
| teamid      | team_name      | team_mascot      | CountOfDonations      |
+ ----------- + -------------- + ---------------- + --------------------- +
| 2           | Carolina       | Panthers         | 5                     |
| 1           | Atlanta        | Falcons          | 3                     |
| 3           | New Orleans    | Saints           | 2                     |
+ ----------- + -------------- + ---------------- + --------------------- +
3 rows

From a team manager's standpoint, this query is useful for recognizing and prioritizing relationships with key sponsors. By understanding which tech companies are most supportive, the manager can focus on nurturing these partnerships, allocating appropriate recognition and engagement efforts to maintain and possibly increase their support.

Q10.
This query retrieves details of players who have borrowed helmets from their football team and have not returned them. It connects player and equipment records, focusing on unreturned helmets by checking for a null return date and lists them along with player and team details, sorting by the date the helmets were borrowed.

> SELECT player_f_name, player_l_name, team_name, team_mascot, checkout_date, player_contact_info
FROM team, player, equipment_checkout, equipment
WHERE team.teamid = player.team_teamid
AND player.playerid = equipment_checkout.player_playerid
AND equipment_checkout.equipment_equipmentid = equipment.equipmentid
AND equipment.equipment_name regexp 'Helmet'
AND equipment_checkout.return_date IS NULL
AND EXISTS (Select * from equipment_checkout, equipment where equipment_checkout.equipment_equipmentid = equipment.equipmentid)
ORDER BY checkout_date

+ ------------------ + ------------------ + -------------- + ---------------- + ------------------ + ------------------------ +
| player_f_name      | player_l_name      | team_name      | team_mascot      | checkout_date      | player_contact_info      |
+ ------------------ + ------------------ + -------------- + ---------------- + ------------------ + ------------------------ +
| Scotty             | Miller             | Los Angeles    | Chargers         | 2023-10-21         | ScottMiller@gmail.com    |
| Bijan              | Robinson           | Los Angeles    | Rams             | 2023-10-26         | Franchiseonmyback@gmail.com |
| Mack               | Hollins            | New York       | Giants           | 2023-10-31         | MackenzieHollins@gmail.com |
+ ------------------ + ------------------ + -------------- + ---------------- + ------------------ + ------------------------ +
3 rows

For a football team manager, this query helps manage equipment efficiently, ensuring helmets are returned on time for use by other players and maintaining safety standards by keeping track of gear usage.

