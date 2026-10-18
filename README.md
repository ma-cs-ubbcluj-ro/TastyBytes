# TastyBytes
A digital cook book

1. Description 

I want to build a simple mobile app called TastyBytes that helps me keep all my favorite cooking recipes in one place. Right now, my recipes are scattered across paper notes, saved screenshots and bookmarks. This app will act as my digital cookbook. I want to easily add new recipes, view my existing ones, edit ingredients or cooking steps whenever I improve a dish and delete recipes I don't use anymore. The app must be clean, very easy to use while cooking in the kitchen and let me quickly snap a photo of my meal directly with my phone camera. 


 
2. Domain Details (Recipe Entity) 

The main item in the app is a Recipe. Each recipe will have 6 simple fields: 

Title (Text): The name of the dish (ex: "Pasta Carbonara"). 

Category (Text): Meal type like Breakfast, Lunch, Dinner or Dessert. 

Preparation Time (Number): How many minutes it takes to cook. 

Ingredients (List): What I need to make it (ex: "2 eggs, 100g bacon, pasta"). 

Cooking Steps (Text): Step-by-step instructions on how to cook it. 

Dish Photo (Camera / Image): A photo of the dish, taken directly with the phone camera or selected from the gallery. 

 

3. CRUD Operations 

Create (Add a Recipe) 

Client Expectation: I tap the + button to open a form. I fill in the name, category, cooking time, ingredients and steps. I can press a camera icon to open my phone's camera, take a quick photo of my dish and attach it. 

Result: Tapping "Save" adds the new recipe straight to my list. 

Read (View Recipes) 

Client Expectation: On the home screen, I see a full list of all my saved recipes with pictures, titles and cooking times. Tapping on any recipe opens it up to show the full list of ingredients and detailed cooking steps. 

Update (Edit a Recipe) 

Client Expectation: If I want to change something, I tap the Edit button on a recipe screen. I can update the ingredients, change the cooking time, rewrite the steps, or retake the photo using my camera. 

Result: Tapping "Save Changes" updates the recipe. 

Delete (Remove a Recipe) 

Client Expectation: I tap the Delete trash icon on a recipe. The app asks "Are you sure you want to delete this recipe?". 

Result: Once I confirm, the recipe is completely removed from my app. 

 

4. Persistence Details 

To make sure I never lose my recipes, all main operations save both locally on my phone and on the online server: 

Create Operation (Server & Local DB): When I add a recipe, it saves to my phone's local storage and uploads to the server. 

Update Operation (Server & Local DB): Editing a recipe updates the details on my phone and updates the server database as well. 

Delete Operation (Server & Local DB): Deleting a recipe removes it from my phone and deletes it from the server. 

Read Operation (Server & Local DB): The app loads recipes instantly from my phone's local database and syncs with the server in the background. 

 

5. Offline Behavior Scenarios 

I often cook in places with bad Wi-Fi or no signal, so the app must work smoothly offline: 

Offline READ Scenario: 

If I open the app without internet, I can still see and read all my previously saved recipes, ingredients and photos directly from my phone. 

Offline CREATE Scenario: 

If I add a recipe and take a photo while offline, the app saves everything locally on my phone. Once my phone gets internet connection again, it automatically uploads the new recipe and picture to the server. 

Offline UPDATE Scenario: 

If I edit a recipe without internet, the changes save immediately on my phone. The app remembers this edit and syncs it with the server as soon as I am back online. 

Offline DELETE Scenario: 

If I delete a recipe while offline, it disappears from my phone right away. The app sends the delete command to the server automatically when the connection comes back. 

 

6. App Mockups 

The mockup images are placed in the repository right next to this README.md file: 

 

 
