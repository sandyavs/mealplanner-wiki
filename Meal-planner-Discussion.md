## Discussion with Greener Village:

1. Is the mealplanner app targeting new clients or only existing clients? That is, is this app open to anyone? If they stumble across the website, will they be able to sign up? If only existing users who already know about the project, then we don’t need a cover page. But if there are new users we would need a cover page with appropriate info.
    
    *Only existing clients. App need not have info on the product as it would be a face to face meeting first. So Login page is enough.*
    
2. Login → For all types of users, we have designed for username and password. We got the info that only client ID will be displayed. Does that mean there would not be any email id associated with the end user client? We are displaying the username in the header. If there is no username do you want the client ID to be displayed?
    1. *Admin only will be creating the logins for all users. Name, Email id, password can be keyed in.*
    2. *temporary password generation  - can be implemented later too.*
    3. *User name can be displayed even for client users after they login.*
3. How many mealplans are there approximately?  We would need to implement search and pagination accordingly. **Please give a sample name of meal plan**
    1. *10s of templates. But with users it may vary.* 
    2. *Generic names like Chris’s 1 week meal plan*
4. As of now our meal plan model has name, description, assignee, tags []. We think tags are like Vegan, Vegetarian, Gluten-free, etc. **Please give a sample of tags as per your usage**. Would you need any filter or search on these meal plans?
    1. *Should be able to filter meal plans based on tags*
    2. *tags can be assigned after designing the meal plan calendar. Not required while creating new meal plan.*
    3. *Tags: Diabetic, Halal, Vegan, Vegetarian. (We can allow the admin to create the tags).*
5. Do you create meal plans based on an existing template or every meal plan is created from scratch? We have implemented duplicate meal plan which copies the existing meal plan and assign to a different user. But I am thinking of merging it while creating a new meal plan as a choice ‘From existing’ or ‘New from scratch’.
    1. *Yes based on existing templates and sometimes from scratch. Sometimes without assigning users.  So new design is good.*
6. Is the date created needed for meal plans list? Planning to have new meal plan button in the meal plans list instead of meal plan calendar page. Is that useful?
    1. *date not required.*
    2. *new meal plan button in the meal plans list is desirable.*
7. My understanding is that the meal catalogue is generic to all users. So, Meal catalogue (Meals page) should not have the client ID mentioned. Is that right? How many meals would be there? We need to implement search and pagination accordingly. **Please give a sample meal.**
    1. *meal catalogue is generic to all users. No client user is assigned to a meal.*
    2. *60 recipes*
    3. *tags is required for a meal recipe* 
8. In Meal page (Meal preparation page), are price and nutrition score required? 
    1. We would need more info on the unit conversion table. 
    2. How do we want to calculate the nutrition rating. 
    3. Would you need a favourites button?
    4. Is “Add to plan” required in meals catalogue page? If so we need a design for the Add to plan modal.
        1. ***Unit conversion table can be provided**. But need not implement as MVP.*
        2. ***Nutrition Score will be provided as part of the recipe write up**. Need not be displayed as part of the image. We can add a numeric field in the data model if required.*
        3. *Favourites button would be great. Not immediately necessary. But good to have.*
        4. *Add to plan is required. Not required in MVP.*
9. As of now we have developed a calendar view kind with days and meals on a weekly basis. As of now it is implemented as only one week view for one user one meal plan. Will there be multiple meal plans for a user? If yes, will there be multiple meal for a given week for the same user?
    1. *existing columnwise meal plan calendar is good.*
    2. *week specifications are not required. Given week is not applicable.*
    3. *There will be multiple meal plans for a user.*
    4. *User should be able to filter based on tags for the meal plans. Eg: Just the vegetarian ones.*
10. How important is the half portion of a meal and shopping list generation based on that? As of now we have implemented only meal entry for a particular day. Portion size is not implemented. 
    1. *half portion not required.* 
    2. *select one or more weekly plans not required. At a time viewing one plan is sufficient.*
11. As of now shopping list is implemented with one meal plan and one user. Do you need a aggregated shopping list for selected meal plans of that user?
    1. *Lot of users are anyway using only one meal plan at a time. So aggregation is not required.*
12. While designing a Meal plan in calendar view, is it specific to a particular user? As of now, we are not capturing the user to be assigned while creating a new meal plan in the modal. Do we need it? Do we need to keep the “new meal plan button” here or in the mealplans list page?
    1. *Need not capture user while creating new meal plan. Can assign later, as we have templates too.*
    2. *New meal plan button can be in both the pages.*
13. We are planning only for meal designer view isn’t it? Or is a client user view required? If yes, what actions can they perform?
    1. User should be able to create their own meal plans. So, existing meal designer view is good for users except that they cannot view other users’ mealplans. They should be able to view meal catalog too.
    2. Only the Admin should be able to create meal recipes. Meal designer can only view the recipes.
14. In the Demo Script the user flow seems to be different from what is currently planned. We’ll discuss the userflow.
    1. *Login Page* 
    2. *→ Meal Plans list page → Meal plan calendar view page*
    3. *→ Meals catalog page → Meal recipe*
    4. *→ User Profile* 
15. Do we need to support bilingual data entry in every field eg: Name, Description. Should they have two different text entry boxes for English and French separately? That is, currently the UI is implemented only in English. Would we need to make provision to write in English and French separately for each data entry? Eg: for name, description, tags, etc. 
    1. *Adding the support for bilingual would be great so we have the option if/when the project expands.*
16. How do you currently represent nutrition score? Is it on a scale of 1 to 5 or 1 to 10. Does it have decimal numbers like 2.5? The problem with decimal is if it is 2.7, I can't show the star accordingly. I was thinking I can provide the nutrition score as another numeric entry field while entering the recipe if it is a standard number.
    1. *I'll reach out to our chefs and nutritionists about the score.  I think a numeric score is the easiest as long as it's clear if it's 1-5 or 1-10 of whatever.*
17. Will this app be used on a mobile screen? As of now it is only designed for laptops with a mouse or a trackpad. If we need to make it work on a mobile we need to design it now appropriately. Supporting mobile screens later would involve a redesign.
    1. *We did plan on it being accessible via mobile devices.*
18. In the Meal planner calendar, we currently have breakfast, lunch, dinner, and snack as categories. Are these 4 categories standard for your use? Or do you have any other category like evening snacks? Basically, I want to freeze on the categories in the data model.
    1. *Perhaps a dessert category, though that's not strictly necessary.  Those four categories are all we really need.*
19. Do you generally have multiple items in one meal category - say does breakfast have two or three items?
    1. *I think with the way the recipes are there could be multiple items in a meal category.  For example a supper could be the meatloaf item and the garlic mashed potatoes item.  I don't think there would be more than 3 in a category though (main, side, side)*
20. Currently user profile has only the logout button. Do we have any other profile information apart from name, email id of the customer. 
    
    **User Profile:**
    
    1. *Cooking skill level*
    2. *Appliances they have*
    3. *Family size - numeric*
    4. *Dietary considerations: Diabetic, Vegetarian, halal, shell-fish allergy.*
    5. He can give a list of dietary considerations.
    
    *Can give user profile later on too. Not required in MVP.*
    

| Action | Admin | Meal Designer | End user |
| --- | --- | --- | --- |
| Create a meal product (recipe) | y | n | n |
| Create a meal plan entry | y | y | y |
| Create a user | y | n | n |
| View a shopping list | y | y | y |

## **Summary:**

### **Current Impact:**

1. Landing page is login page.
2. Users should be able to create their own meal plan, view all their meal plans and print shopping list for a selected meal plan. View all the meals from catalogs. 
3. The only difference between meal designer and user is that meal designer can view, create, edit meal plans for all users, but users can only do such actions in their own meal plan.
4. *Admin only will be creating the logins for all users. Name, Email id, password can be keyed in.*
5.  *Should be able to filter meal plans based on tags*
6. *tags can be assigned after designing the meal plan calendar. Not required while creating new meal plan. So Edit meal plan should have tags as a field.*
7. *We should allow the admin to create the tags..*
8. *Date not required for meal plans list.*
9. *new meal plan button should be there in the meal plans list.*
10. M*eal catalogue is generic to all users. No client user is assigned to a meal.*
11. *60 recipes. So search and pagination is required for meal catalog.*
12. *Tags required for a meal recipe* 
13. P*lan on it being accessible via mobile devices.*
14. There won’t be more than 3 meals in a category per day. So current design seems fine.
15. Search not required in the Mealplan calendar view. Instead search is there in the mealplans list view. We can access the meal plans list from the nav menu and search.

### **Later on:**

1. *temporary password generation*
2. ***Unit conversion table is provided**. This was required for shopping list calculation and the cost of a meal recipe. But need not implement as MVP.*
3. ***Nutrition Score will be provided as part of the recipe write up**. Need not be displayed as part of the image. I suggested we can add a numeric field in the data model if required. He'll reach out to our chefs and nutritionists about the score.  I think a numeric score is the easiest as long as it's clear if it's 1-5 or 1-10 of whatever.*
4. *Favourites button would be great. Not immediately necessary. But good to have.*
5. *Add to plan is required. Not required in MVP.*
6. Bilingual support is required. *So, we have the option if/when the project expands. We need the UI to pick from the right fields in the database based on the selected language (such as nameEn, descriptionFr, tagsEn/tagsFr etc). Admin should be able to enter data bilingually for all the fields. We should decide if we should fall back to english if the data has not been localized yet.*
7. **User Profile:** *Cooking skill level, Appliances they have, Family size - numeric, Dietary considerations: Diabetic, Vegetarian, halal, shell-fish allergy. He can give a list of dietary considerations.*