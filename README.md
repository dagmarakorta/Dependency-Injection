# 🎾 TennisBookings & ServiceLifetimeDemonstration (.NET 6)

This repository contains two ASP.NET Core projects created as part of learning exercises on **Dependency Injection (DI)**, service lifetimes, and clean architecture in .NET 6.

## 🧩 Projects Overview

### 1. **TennisBookings** – Main Demo App  
A sample tennis court booking site demonstrating real-world DI usage:
- Injects services into Razor Pages and controllers via constructor injection
- Demonstrates service registration and lifetime configuration (transient, scoped, singleton)
- Uses **Entity Framework Core**, **ASP.NET Core Identity**, and **hosted services**
- Contains business logic rules like `MemberBookingsMustNotOverlapRule`
- Weather messages on the homepage are provided via `IRandomWeatherForecaster` implementations

### 2. **ServiceLifetimeDemonstration** – Minimal Razor App  
A simplified Razor Pages app showing DI lifetimes:
- Middleware injects `IGuidService` to generate and share a GUID per request
- Services like `GuidTrimmer` show how to consume scoped dependencies
- Registered via `Program.cs` and injected into pages

### 3. **WeatherService.Api**  
A minimal API project demonstrating:
- Lightweight API patterns
- Use of shared models (`TennisBookings.Shared`) to return weather data

## 🧪 Tests  
Located under `/tests/TennisBookings.Tests`, tests focus on Razor page models (e.g., `IndexModel`), verifying behavior like weather-based messaging.

## 🔧 Technologies Used
- .NET 6
- ASP.NET Core Razor Pages & MVC
- EF Core (In-Memory for tests)
- ASP.NET Core Identity
- Dependency Injection & Middleware
- xUnit for testing

## 📚 Purpose
This solution was built as a learning sandbox to:
- Practice **dependency injection patterns**
- Understand **service lifetimes**
- Explore **ASP.NET Core architecture**, including Razor Pages, middleware, and hosted services

---

> ⚠️ Not intended for production – purely educational.
