# Profile

## About the project
The idea is to create some sort of dashboard for a student profile that we can modify as we want. It should allow to add and remove modules (like Sprint, Objectives (hello from the future)), focus attention on important information (like student performance). The project was not finished when my internship ended. So all information presented here is work in progress. Source code can be provided on demand (possibly)

## Team
* Aleksandr Buzdin ([abuzdin](https://profile.intra.42.fr/users/abuzdin) / [medved](https://profile.intra.42.fr/users/medved))

## Tools

* Frontend: HTML, htmx, CSS, SCSS, jQuery, JavaScript
* Backend: Django

## To-do
* Better structure for the stats page?
* New objectives -> new methods
* Better methods/models to assess objective progress
* Graphs to stats

## Models
* ***Objective*** - periodical objective; contains all basic information and methods to assess progress
* ***CoalitionObjective*** - objective instance for a coalition; probably nymano will delete this model
* ***CoalitionMessage*** - messages created by coalition leaders and displayed on the **Coalitions** page

## Pages
* ***Stats*** - page with user stats; stats can be divided into three groups: piscine, school and total (piscine + school); ideally should also have a possibility to create some graphs
* ***Leaderboards*** - top10 leaderboards; I tried to make db calls as much efficient as possible
* ***Coalitions*** - page contains stats about user coalition, its stats in this regard, info about the tournament and the current objective; it also displays a coalition leader message; coalition leaders on this page can update and create new messages; page background depends on user coalition and is set in **coalitions.html**
* ***Calculator*** - level calculator; probably it will be availble, if ever, only for the post common core students; for me it was just a nice exercise to do
* ***Who*** - credits, add yourself on it (via the view) if you contributed
* Other pages are currently empty, including index page

## DB population
* In ***management*** folder you can find my methods to populate DB. To populate/delete a certain model, run in the hub-app: `./manage.py populate_profile populate (or 'delete) [MODEL_NAME]`

## Useful links
* [Ultimate SCSS guide](https://blog.logrocket.com/the-definitive-guide-to-scss/)
* [Article about tricks for CSS variables](https://css-tricks.com/difference-between-types-of-css-variables/#)
* To install scss: sudo npm i -g scss
* To compile css form scss: scss [SCSS FILE] [DESIRED CSS FILE]. Example: `sass static/profile/profile.scss static/profile/profile.css`

## Notes
* I tried to use htmx for navbar, but it feels that htmx there bring more bad than good; currently htmx is used for the spinner (loading icon), leaderboards, stats
* You can change font via navbar; selected font is saved in cookies

## Screenshots
User stats
![stats](https://github.com/baltsaros/profile/blob/main/pics/stats.jpeg)
Leaderboards page
![leaderboards1](https://github.com/baltsaros/profile/blob/main/pics/leaderboards1.jpeg)
Spinner on leaderboard load
![leaderboards1](https://github.com/baltsaros/profile/blob/main/pics/leaderboards2.jpeg)
Loaded leaderboard with open window on user stats regarding this leaderboard
![leaderboards1](https://github.com/baltsaros/profile/blob/main/pics/leaderboards3.jpeg)
Coalitions page. View from the coalition leader point. Other users cannot update/create new messages
![coalitions](https://github.com/baltsaros/profile/blob/main/pics/coalitions.jpeg)
Level calculator
![calculator](https://github.com/baltsaros/profile/blob/main/pics/calculator.jpeg)