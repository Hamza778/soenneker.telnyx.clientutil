# Soenneker Telnyx Client Util 🛠️

![GitHub Release](https://img.shields.io/github/release/Hamza778/soenneker.telnyx.clientutil.svg)
![GitHub Issues](https://img.shields.io/github/issues/Hamza778/soenneker.telnyx.clientutil.svg)
![GitHub Stars](https://img.shields.io/github/stars/Hamza778/soenneker.telnyx.clientutil.svg)

Welcome to the **Soenneker Telnyx Client Util** repository! This project provides an async thread-safe singleton for the Telnyx OpenApiClient, designed to simplify your telephony integration. 

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Introduction

The Soenneker Telnyx Client Util is a powerful tool for developers looking to integrate with the Telnyx API. By using this singleton design pattern, you ensure that only one instance of the client is active at any time, which helps manage resources efficiently in asynchronous environments. This utility is built in C# and leverages .NET’s capabilities to provide a seamless experience.

## Features

- **Thread-Safe**: The singleton implementation ensures that your application remains stable under concurrent access.
- **Asynchronous Operations**: Built to handle async calls, making it suitable for modern applications.
- **Easy Integration**: Simple setup process to get started with the Telnyx API.
- **Robust Error Handling**: Built-in mechanisms to manage API errors gracefully.
- **Extensive Documentation**: Clear guidelines and examples to help you understand and utilize the client effectively.

## Installation

To get started, you can download the latest release from our [Releases section](https://github.com/Hamza778/soenneker.telnyx.clientutil/releases). Download the necessary files, and follow the setup instructions provided there.

### Prerequisites

Before you begin, ensure you have the following:

- .NET SDK installed (version 5.0 or later)
- A Telnyx account with an API key

## Usage

To use the Soenneker Telnyx Client Util in your project, follow these steps:

1. **Add the Client Util to Your Project**:
   Add the package to your project using NuGet:

   ```bash
   dotnet add package Soenneker.Telnyx.ClientUtil
   ```

2. **Initialize the Client**:
   In your application, you can initialize the Telnyx client as follows:

   ```csharp
   using Soenneker.Telnyx.ClientUtil;

   var telnyxClient = TelnyxClient.Instance;
   ```

3. **Making API Calls**:
   You can now use the client to make API calls. For example, to send a message:

   ```csharp
   var message = await telnyxClient.Messages.CreateAsync(new MessageOptions
   {
       To = "+1234567890",
       From = "+0987654321",
       Text = "Hello from Telnyx!"
   });
   ```

4. **Error Handling**:
   Ensure to handle exceptions appropriately:

   ```csharp
   try
   {
       // API call
   }
   catch (TelnyxException ex)
   {
       Console.WriteLine($"Error: {ex.Message}");
   }
   ```

## Contributing

We welcome contributions to improve the Soenneker Telnyx Client Util. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

Please ensure your code adheres to our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest updates and releases, please visit our [Releases section](https://github.com/Hamza778/soenneker.telnyx.clientutil/releases). Here, you can find the latest versions and any important updates.

## Conclusion

The Soenneker Telnyx Client Util aims to simplify your integration with the Telnyx API. With its thread-safe, async capabilities, it offers a robust solution for modern telephony applications. We encourage you to explore the repository, contribute, and enhance this tool for the community.

Thank you for your interest in the Soenneker Telnyx Client Util!