## Iteration 1: Fetch and Display
- What does the API response look like? What fields did you use? What was the trickiest part of getting fetch to work? If AI helped, what did it explain about async/await? 
    - The API response returns a list of country objects with specific field, for example: languages and currencies are objects (not arrays), so I needed to use Object.values() to extract them. I used the fields: name, flags, capital, population, region, languages, and cca3. The hardest part I would say was understanding how async/await works; I would havr to await the fetch() call and then await the .json() call separately since they are both promises. AI helped explain that async/await is just a cleaner syntax for handling promises, and that if you do not await them, you get a pending promise instead the actual data.

## Iteration 2: Interactivity and Design
- How did you connect user input to API calls? What CSS layout did you use for displaying data? What design decisions did you make? 
    - I connected user input by adding event listeners to the search bar and region dropdown that call renderCountries() function on every keystroke or selection change. The function filters the already-fetched data client-side so the app does not need to re-fetch from the API everytime. I used CSS Grid auto-fill and minmax(260px, 1fr) for the country cards so the layout automatically adjusts to different screen sizes. Design decisions included using a warm off animations on cards to keep it looking clean and minimalistic.

## Iteration 3: Polish and Extend
- What extension did you add? What edge cases did you handle? What surprised you about working with a real API? 
    - I added a favorites feature using localStorage so users can star countries and filter to show only favorites and those stay even after refreshing the page. Edge cases I handled include: no results found, API rate limiting (with a specific error message and retry button), disabled inputs during loading, and countries with missing data like no language or capitals. I think the most surprising thing about working with a real API was how inconsistent the data can actually be, some countries were missing some fields, so I realized someone ALWAYS has to write defensive code with fallbacks for it (just in case).

