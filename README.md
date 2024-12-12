# Currency Converter Web Application

## Overview
This project is a **Currency Converter Web Application** that allows users to convert an amount from one currency to another using real-time exchange rates. The application fetches live data from a free currency exchange rate API and displays the conversion results along with the appropriate country flags.

## Features
- **Real-time exchange rates**: Fetches live currency exchange rates using the [ExchangeRate API](https://app.currencyapi.com/dashboard).
- **Country Flags**: Displays flags of the selected currencies dynamically.
- **User-friendly Interface**: Simple and intuitive UI for seamless user interaction.
- **Pre-filled Default Values**: Defaults to converting from USD to INR with an initial amount of 1.

## Technologies Used
- **HTML**: For structuring the web page.
- **CSS**: For styling the application.
- **JavaScript**: For functionality and API integration.
- **FontAwesome**: For icons in the interface.

## Files
1. **HTML File**
   - `index.html`: The main structure of the web application.
2. **CSS File**
   - `style.css`: Styles the interface to make it visually appealing.
3. **JavaScript Files**
   - `app.js`: Contains logic to fetch data from the API, handle user input, and update the UI.
   - `code.js`: Additional JavaScript code (if any) for extended functionality.

## Setup Instructions
### Prerequisites
- A web browser (e.g., Chrome, Firefox, Edge).
- Internet connection to fetch data from the API.

### Steps to Run the Application
1. Clone or download the repository.
2. Open the `index.html` file in your web browser.
3. Enter the amount and select the currencies for conversion.
4. Click the "Get Exchange Rate" button to see the conversion result.

### API Integration
The application uses the ExchangeRate API to fetch live currency rates. The base URL for the API is defined in the `app.js` file:
```javascript
const BASE_URL = "https://v6.exchangerate-api.com/v6/80f55b457d4942a587b06313/latest";
```

### Dynamic Country Flags
The application dynamically updates the country flags based on the selected currencies using the `flagsapi.com` service:
```javascript
let newSrc = `https://flagsapi.com/${countryCode}/flat/64.png`;
```

## How It Works
1. **Dropdown Initialization**: Populates the currency dropdowns with currency codes using the `countryList` object.
2. **Event Listener**: Updates the flag when a new currency is selected from the dropdown.
3. **API Fetch**: Fetches conversion rates from the API when the user clicks the "Get Exchange Rate" button.
4. **Conversion Calculation**: Calculates the final converted amount and displays it on the screen.

## Screenshots
### Home Page
- Shows input fields, dropdowns for currency selection, and a result message.

### Example Conversion
- Converts 1 USD to INR and displays the result with corresponding flags.

## Future Enhancements
- Add support for more currencies.
- Improve error handling for invalid API responses or network issues.
- Display historical exchange rate trends using charts.

## License
This project is licensed under the MIT License.

