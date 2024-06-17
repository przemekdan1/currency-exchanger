# Currency Exchanger

Currency Exchanger is a C# console application that fetches and displays exchange rates for various currencies against the Polish złoty (PLN). It allows users to convert amounts between different currencies using the latest exchange rates from the National Bank of Poland (NBP) API.

## Features

- Fetches exchange rates from the NBP API.
- Displays exchange rates for various currencies.
- Converts amounts between different currencies.
- Implements Singleton pattern for the currency converter.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/currency-exchanger.git
    ```
2. Navigate to the project directory:
    ```sh
    cd currency-exchanger
    ```

## Usage

1. Open the project in your preferred C# IDE (e.g., Visual Studio).
2. Run the application.
3. Follow the on-screen instructions to view exchange rates and perform currency conversions.

## Code Structure

### Main Classes

- **Currency**: Represents a currency with its name, code, rate, and converter.
- **XMLDataProvider**: Handles fetching and parsing JSON data from the NBP API.
- **UserInterface**: Manages user input and displays output.
- **CurrencyConverterSingleton**: Implements the Singleton pattern for currency conversion logic.

### UML 

![image](https://github.com/przemekdan1/currency-exchanger/assets/101727232/87b6c2b2-391b-4970-82bb-c3fe223a6051)


### Example Methods

- **LoadDataFromJsonAsync(string url)**: Fetches JSON data from the provided URL.
- **LoadCurrencies()**: Parses the fetched JSON data and populates the currencies dictionary.
- **GetUserInputAsync()**: Manages user input and displays conversion results.

## Example Output

```
Currency code: USD, Name: dolar amerykański, Rate: 3.9843
Currency code: EUR, Name: euro, Rate: 4.2923
...
Enter currency: USD
Enter target currency: EUR
Enter available funds: 100
100 USD = 93.09 EUR
dolar amerykański -> euro
```

## Dependencies

- .NET 5.0 or higher
- System.Net.Http
- System.Text.Json
