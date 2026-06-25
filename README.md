# Feather 🪶

Feather is a lightweight, high-performance service-controller framework built for Roblox. Designed as a modern, "zero-bloat" alternative to monolithic frameworks, Feather focuses on fast bootstrapping and minimal memory overhead, making it ideal for games that require high-speed performance and clean, modular architecture.

## 🧠 Core Philosophy
Feather is built for developers who want the structure of a Service/Controller pattern without the heavy dependency chains found in other libraries. It prioritizes:

*   **Performance:** Optimized for minimal server-side load and rapid initialization.
*   **Modularity:** A strictly decoupled environment that keeps client and server logic clean.
*   **Simplicity:** No unnecessary features. Feather does exactly what it needs to do—bootstrap your services and controllers—and nothing else.

## ✨ Key Features

*   **🚀 Lightweight Bootstrapper:** Reduces game startup times significantly.
*   **🧩 Service/Controller Pattern:** Cleanly separates network-based services from local client controllers.
*   **⚡ High Scalability:** Built to handle the heavy demands of modern sub-genres like RNG simulators and high-fidelity physics games.
*   **🛠️ Easy Integration:** Designed to drop into any workspace with minimal configuration.

## 📦 Installation

Feather is designed for quick implementation. You can integrate it directly into your project workspace.

1. Download the latest release from the repository.
2. Drag the `Feather` module into your `ReplicatedStorage`.
3. Require the module in your scripts to begin creating services and controllers.

For full documentation, API references, and usage guides, visit the official site: [nylonpixelated.github.io](https://nylonpixelated.github.io/feather)

## ⚡ Basic Usage

Feather uses a modular approach. You define your services and controllers using the `CreateService` and `CreateController` methods.

**Creating a Service (Server):**
```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Feather = require(ReplicatedStorage.Packages.Feather)

local MyService = { Client = {} }

function MyService:featherInit()
    print("Service Initialized")
end

function MyService:featherStart()
    print("Service Started")
end

return Feather.CreateService(MyService)
