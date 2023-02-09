# BNB Chain Program in C#
This repository contains a simple program that demonstrates how to connect to the Binance Smart Chain (BNB) network and retrieve information about the blockchain using C#. The program uses the NBitcoin and NBXplorer libraries to connect to the Binance Smart Chain test network and retrieve the current block height and the block hash of the latest block.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
Before you start, make sure you have the following software installed on your computer:
1. Visual Studio
2. .NET Framework

### Installing
To install the required libraries, follow these steps:
1. Open Visual Studio and create a new Console Application project.
2. Open the NuGet Package Manager Console by going to Tools > NuGet Package Manager > Package Manager Console.
3. Run the following command to install the NBitcoin library:
```csharp
Install-Package NBitcoin
```
4. Run the following command to install the NBXplorer library:
```csharp
Install-Package NBXplorer
```
### Running the Program
1. After installing the required libraries, you can run the program by doing the following:
2. Open the Program.cs file in the project.
3. Replace the contents of the file with the following code:
```csharp
using System;
using NBitcoin;
using NBXplorer;

namespace BNB_Example
{
    class Program
    {
        static void Main(string[] args)
        {
            var network = Network.TestNet;
            var explorer = new NBXplorerClient(network);
            
            Console.WriteLine("Binance Smart Chain (BNB) Program Example");
            Console.WriteLine("Block height: " + explorer.GetStatus().ChainHeight);
            Console.WriteLine("Block Hash: " + explorer.GetBlock(explorer.GetStatus().ChainHeight).BlockId);
            Console.WriteLine("Press any key to exit...");
            Console.ReadLine();
        }
    }
}
```
4. Save the file.
5. Press F5 to run the program in debug mode.
6. The program should connect to the Binance Smart Chain test network and retrieve the current block height and the block hash of the latest block. The results will be displayed in the console window.

### Built With
1. NBitcoin - A library for Bitcoin development in .NET
2. NBXplorer - A blockchain explorer for Bitcoin-based blockchains

### Author
Muhammad Omer Khan - Entrepreneur & Technologist

### License
This project is licensed under the MIT License - see the LICENSE.md file for details.
