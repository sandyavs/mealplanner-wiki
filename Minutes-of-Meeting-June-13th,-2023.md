1. Riya favourites feature (issue #455):Code review finished, must create graphQL query, and make a MR
2. Mayomi's bug (issue #355) where empty meals are being created: initial solution involves making every field as required so that empty meals cannot be created, but code and name_en is mandatory, the rest of the fields are not mandatory. Must fix this in the solution.
3. Getting familiarized with reactJS
    - Mayomi, Bo, Pujitha, Tulio must do a sample project (different project for each members) in react. Push code to github.
    - To be complete by Friday/Saturday
    - can use material UI (MUI) instead of css, bootstrap 
    - https://mui.com/
4. Sebastian is awaiting code review for his issue
5. Bo is to create a MR for bug where username is not showing up when meal is not assigned to a user (issue #456)
6. Duplicate meal plan feature (issue #377) assigned to Pujitha
7. New feature: In mealplanner Admin UI (localhost:2000), be able to search particular meals in meal table
    - assigned to Tulio
    - Tulio must create new feature issue on github
8. Print Meal plan calendar is broken when in portrait view bug (issue #345) assigned to Mayomi
9. New bug: on the meal plans page, change trash and shopping cart icon colours to green when hovering the mouse over
     - assigned to Bo
     - Bo must create new bug issue
10. New bug: on the meal plans page, on click delete, must have confirmation dialogue.
     - assigned to Bo
     - Bo must create a new bug issue

11. Steps on how to push code and create MR
     - git checkout v2
     - git checkout -b {issue#}-{descriptionofissue}
         - ex: git checkout -b 456-display-username
     - git commit -m "description of what your code acheives"
         - ex: git commit -m "username will be displayed as no user assigned in the mealplanner calendar"
     - git push origin {yourbranchname}
         - ex: git push origin 456-display-username
     - create MR: select V2, not develop
     - assign MR to Shanthi


