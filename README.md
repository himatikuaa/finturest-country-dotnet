# Finturest Country .NET SDK 🌍

Welcome to the official C# SDK for the Finturest Country API. This library provides easy access to country-related data, supporting .NET Standard 2.0+ and all modern .NET versions. With this SDK, you can retrieve information about countries, including their codes, currencies, flags, languages, and more.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-Click%20Here-brightgreen)](https://github.com/himatikuaa/finturest-country-dotnet/releases)

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Features

The Finturest Country SDK offers the following features:

- **Country Codes**: Access ISO 3166 country codes.
- **Currency Information**: Get details about currencies using ISO 4217.
- **Country Flags**: Retrieve images of country flags.
- **Languages**: Access country languages using ISO 639-1 and ISO 639-2 codes.
- **Country Data**: Fetch comprehensive data about countries.
- **Easy Integration**: Simple methods to access the API data seamlessly.

## Installation

To install the Finturest Country SDK, use NuGet Package Manager. You can run the following command in your project:

```bash
Install-Package Finturest.Country
```

Alternatively, you can add it to your `.csproj` file:

```xml
<PackageReference Include="Finturest.Country" Version="1.0.0" />
```

After installation, you can start using the SDK in your project.

## Usage

Here's a simple example of how to use the Finturest Country SDK in your application.

### Initial Setup

First, you need to create an instance of the `FinturestCountryClient`. Make sure to provide your API key.

```csharp
using Finturest.Country;

var client = new FinturestCountryClient("your_api_key");
```

### Fetching Country Data

You can fetch data for a specific country by its code:

```csharp
var countryData = await client.GetCountryDataAsync("US");
Console.WriteLine($"Country: {countryData.Name}, Currency: {countryData.Currency}");
```

### List All Countries

To get a list of all countries, you can use the following method:

```csharp
var countries = await client.GetAllCountriesAsync();
foreach (var country in countries)
{
    Console.WriteLine(country.Name);
}
```

### Get Country Flag

To retrieve a flag for a specific country:

```csharp
var flagUrl = await client.GetCountryFlagAsync("US");
Console.WriteLine($"Flag URL: {flagUrl}");
```

## API Reference

The SDK provides various methods to interact with the Finturest Country API. Below is a brief overview of the main methods:

- **GetCountryDataAsync(string countryCode)**: Retrieves detailed information about a specific country.
- **GetAllCountriesAsync()**: Fetches a list of all countries with basic information.
- **GetCountryFlagAsync(string countryCode)**: Returns the URL of the flag image for a specified country.
- **GetCountryCurrencyAsync(string countryCode)**: Provides currency details for a specific country.

For more detailed information, please refer to the [API documentation](https://github.com/himatikuaa/finturest-country-dotnet/releases).

## Contributing

We welcome contributions to the Finturest Country SDK. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Create a pull request to the main repository.

Please ensure that your code adheres to our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions, please check the [Releases](https://github.com/himatikuaa/finturest-country-dotnet/releases) section for updates. You can also open an issue in the repository for assistance.

For further information, feel free to reach out to the maintainers through GitHub.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-Click%20Here-brightgreen)](https://github.com/himatikuaa/finturest-country-dotnet/releases)

Thank you for using the Finturest Country SDK! We hope it helps you build amazing applications with country data.