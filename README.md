## What does my tool do?
- Country Explorer fetches data from the REST Countries API and displays countries in a card grid.
- Users can search by country name, capital, or language, and filter by region to control what data they see.
- Users can favorite countries with a star button, and favorites are saved in localStorage.
- The app includes loading and error states so users get clear feedback while data is fetched.

## How to use it (brief instructions)
- Open index.html in your browser.
- Use the Search countries box to find countries by name, capital, or language.
- Use the Filter by region dropdown to narrow the results.
- Click the star on any country card to save it as a favorite.
- Use Show favorites only to browse saved favorites.
- If the API request fails, use the Try again button in the error message box.

### Testing checklist (including mobile)
- Responsive/mobile test:
	1. Open browser DevTools.
	2. Toggle device toolbar (phone/tablet view).
	3. Verify controls stack vertically and cards become single-column on small screens.
- Loading state test:
	1. Open DevTools Network tab and set throttling to Slow 3G.
	2. Refresh the page.
	3. Confirm the spinner and Loading... text appear while data is being fetched.
- Error handling test:
	1. In DevTools Network tab, enable Offline (or block the API request).
	2. Refresh the page.
	3. Confirm the error message is displayed and the Try again button appears.

## Link to live site 
- .....

## What I learned
- How to fetch and render API data dynamically with JavaScript.
- How to combine search and filter UI to improve user control over data.
- How to persist user preferences with localStorage (favorites).
- How to implement loading and error states to improve usability.
- How to handle edge cases like no results, empty search, and API rate limiting.
- How responsive CSS media queries change layout for mobile devices.
