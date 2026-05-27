# Blazor AI Maps

This project integrate **Azure OpenAI** with the **[Blazor Maps](https://www.syncfusion.com/blazor-components/blazor-map)** component to create AI-powered, interactive maps. From a single text query,the app uses Azure OpenAI to generate a structured list of locations and renders them as customized markers with rich tooltips on an OpenStreetMap-backed map.

## Overview

Asking an AI for a list of places is easy — turning that list into an interactive, zoomable map experience usually isn't. This sample shows how to bridge that gap end-to-end:

1. The user types a free-form query in a search box.
2. The app calls an Azure OpenAI deployment via a typed `AISampleService` and asks for a flat JSON list of 15 places (with name, latitude, longitude, address, and details).
3. The response is deserialized and bound to a `SfMaps` component, which renders custom image markers with template-based tooltips.
4. Built-in zoom, pan, and reset controls let users explore the AI-generated results.

The result is a reusable pattern for adding AI-driven, location-based discovery to any Blazor application.

## Features

- **AI-generated markers** — Convert any natural-language query into 15 geocoded points of interest using Azure OpenAI Chat Completions.
- **Custom marker imagery** — Renders pins with a custom `map_pin.png` image marker on top of OpenStreetMap tiles.
- **Rich tooltip templates** — Tooltips display the place name, address, and a description pulled from the AI response. Hospital-related queries also display a randomized photo from a local image set.
- **Search-driven updates** — A `SfTextBox` with a search icon refreshes the marker collection whenever the query changes.
- **Loading state** — A `SfSpinner` is shown while the AI request is in flight.
- **Zoom toolbar** — Built-in `Zoom`, `ZoomIn`, `ZoomOut`, `Pan`, and `Reset` toolbar items, with a max zoom of 19.
- **Clean separation of concerns** — All Azure OpenAI calls are encapsulated in `AISampleService`, registered as a singleton via DI.

## Prerequisites

- [.NET SDK 8.0](https://dotnet.microsoft.com/download/dotnet/8.0) or later
- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or later
- [Visual Studio Code](https://code.visualstudio.com/)

## Getting Started

### Clone the repository

```bash
git clone https://github.com/SyncfusionExamples/https://github.com/SyncfusionExamples/build-smart-interactive-maps-with-azure-openai.git
cd build-smart-interactive-maps-with-azure-openai
```

### Run with Visual Studio

1. Open the solution file using Visual Studio 2022 or later.
2. Restore the NuGet packages by rebuilding the solution.
3. Build the project to ensure there are no compilation errors.
4. Run the project.

### Run with .NET CLI

```bash
# Restore dependencies
dotnet restore

# Run the project
dotnet run
```
## References

- [Blazor Documentation](https://blazor.syncfusion.com/documentation/introduction)
- [Blazor Maps documentation](https://blazor.syncfusion.com/documentation/maps/getting-started)
- [Blazor Maps online demos](https://blazor.syncfusion.com/demos/maps/default-functionalities)



