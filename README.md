# Horoscopes
Here is a light outline that you can reference to build the Horoscopes app. 

## Setup

1. Create a blank new React project with Vite
1. Copy the assets folder, the README.md file and the .gitignore file from this github repo into your new blank project
1. Remove all the extra code rendered from the Vite template. That includes removing all the JSX from the App component's return statement, the import statements in the App component, the CSS code in the App.css and index.css files

## Starting to code the About Today section

1. Let's set up the initial JSX in our App component. Make an h1 titled "Horoscopes" and a section with an h2 titled "About Today". Give the section a class of "today-info".
1. Add a p tag that displays today's date using a Javascript Date object. 
1. Format the date so it reads nicely as text, i.e. "Today is Friday, May 3, 2024"
1. Import the astrology sign data from the data.js file. Let's name it horoscopeData in our import statement.
2. Create a variable called astroSigns in your app component that holds the astroSigns object from the imported astrology signs data 
1. Write a findSign() function that takes in a date as input. It should return the corresponding zodiac sign by checking which zodiac sign's date range aligns with the inputted date. 
1. Create another p tag to display the current Zodiac sign in JSX

## Styling the text and sections
1. Start by styling the body tag. Add a background color and a text color. Style the text using font properties as well.
1. Style the #root by adding a max-width, margin and centering the text with text-align.
2. Style the sections by adding a border, border-radius, and some padding/margin. Add a background color.
3. Style the h1 and h2 text.

## Coding the zodiac sign buttons

1. Create a section tag in the JSX that has a class of "sign-picker". This will hold all of our sign buttons so the user can learn more about the zodiac signs. If the user clicks on one of these buttons, this sign picker section will also hold information about a selected zodiac sign.
1. Map over all the signs and display their signNames as button tags in the JSX. Don't forget to add a key when you are mapping. 
1. Now we want to be able to click on all of these SignButtons to display more information about that sign. So we need to add an onClick handler function to our button tags. For now, let's make our onClick handler function display the signName of the sign button that was clicked on.
1. We need to track which sign was selected. We can do this by saving the selected sign in our app's memory using useState. So, let's create a new state variable called selectedSign. Then change our onClick handler function to call setSelectedSign. 
1. We want our sign-buttons and sign-info to occupy the same place — in our sign-picker. When the user selects a sign, the sign's info should get displayed. And when no sign is selected, the sign-buttons should get displayed. Let's write a ternary statement in our JSX so that when selectedSign has a value, show the selected sign name, but if it's null, show the sign buttons.

## Coding the SignInfo div
1. Now let's create another div tag with the class "sign-info". In its JSX, it should display the signName as an h2 and a div. Inside that div, it should show the startDate and endDate, its luckyNumbers, key traits, and the daily horoscope for that sign.

## Coding the Welcome screen
1. Create a new state variable called showWelcomePage.  
2. In the JSX, create a section tag with class "welcome". It should say Welcome. "Click enter to learn about the twelve zodiac signs and their daily horoscopes." It should have an Enter button that sets showStart to false.
3. Write a ternary statment that will determine whether the welcome screen should be displayed or the main website content.

## Coding the Divider 
1. This is an optional bonus feature if you have time! See if you can create a divider that displays all of the zodiac images in a row in small icon sizes. 

## Adding a Form with a Date Picker input for the user to find their sign 
1. Create a "What's Your Sign?" Section that allows the user to input their birthday and learn more info about their zodiac sign. 

## Fetching Horoscope information via an API 
1. https://rapidapi.com/soralapps/api/best-daily-astrology-and-horoscope-api
2. https://rapidapi.com/ashutosh.devil7/api/horoscope19/
