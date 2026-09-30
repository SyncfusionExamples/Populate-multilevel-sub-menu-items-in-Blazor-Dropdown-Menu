# Populate Multi-Level Submenu Items in Blazor DropDown Menu

## Overview

This sample demonstrates how to populate and render hierarchical menu structures using Syncfusion [Blazor Dropdown Menu](https://www.syncfusion.com/blazor-components/blazor-dropdown-menu) within a dropdown-style navigation experience. The implementation combines `SfDropDownButton` and `SfContextMenu` components to create a customizable multi-level menu system with nested submenu items. Menu data is defined through a hierarchical model and rendered dynamically using parent-child relationships. 

This approach helps developers build scalable navigation systems where commands and actions can be organized into logical menu groups.

## Key Features

- Uses `SfDropDownButton` to host and display a custom popup menu experience.
- Renders multi-level submenu navigation using `SfContextMenu` and hierarchical menu item collections.
- Defines nested submenu structures through the `ContextMenuItemModel.Items` property.
- Maps menu item text using the `MenuFieldSettings` component with the `Text="Content"` configuration.
- Enables submenu expansion on click using the `ShowItemOnClick="true"` property.
- Handles menu lifecycle events through `MenuEvents`, including:
  - `Created` event to automatically open the context menu when initialized.
  - `OnClose` event to control menu closing behavior.
  - `ItemSelected` event to determine when the menu should remain open or close.
- Uses `DropDownButtonEvents.OnClose` to prevent the DropDown Button popup from closing automatically.
- Implements custom menu state management using the `isClose` flag and `FileButton.Toggle()` method.
- Demonstrates parent and child menu relationships for commands such as **Align**, **Space**, and **Save As**.
- Includes separator items using the `Separator` property to organize menu commands into logical groups.
- Supports multiple submenu levels using nested `ContextMenuItemModel` collections bound directly to the `Items` property.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the `PopulateMultiSubItem.sln` solution file.
3. Restore all NuGet packages.
4. Build the solution.
5. Ensure the Blazor project is selected as the startup project.
6. Run the application using **Ctrl+F5**.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open an integrated terminal.
3. Navigate to the project directory.
4. Restore the project dependencies.

```bash
dotnet restore
```

5. Run the application.

```bash
dotnet run
```

6. Open the local application URL displayed in the terminal after the application starts.

## Project Structure

`Pages/Index.razor` - Implements the multi-level submenu dropdown using `SfDropDownButton`, `SfContextMenu`, custom `ContextMenuItemModel` objects, and menu event handlers.

`Pages/FetchData.razor` - Default Blazor sample page that displays weather forecast data from a service.

`Data/WeatherForecast.cs` - Weather forecast model used by the sample `FetchData` page.

`Data/WeatherForecastService.cs` - Service that generates sample weather forecast data.

`Shared/SurveyPrompt.razor` - Reusable survey prompt component included with the default Blazor template.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the Syncfusion Blazor Context Menu documentation: https://blazor.syncfusion.com/documentation/context-menu/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.