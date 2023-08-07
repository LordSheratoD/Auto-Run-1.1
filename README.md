# New World Resource Gathering Bot

Allows you to run a bot for resource gathering along a pre-defined path. The program doesn't use in-game resources and only interacts with the interface using the OpenCV library.

## Installation:

1. Download and install OverWolf, see the readme in the "ts" folder for more information.

2. Copy the repository into Visual Studio or run the solution.

3. Compile the project in Visual Studio.

4. After compilation, a "bin" folder will be created in the "AutoRun 1.1" folder. Move/Copy the "Images" folder to "..\Auto Run 1.1\bin\Debug\net5.0-windows". The "Images" folder contains templates required for the bot to function during resource gathering.

## Controls:

- F2 Key: Starts the bot.
  
- F4 Key: Stops the program's execution.

- E Key: Initializes the resource gathering point.

- StartStream Button: Initializes the recording of the path while the character moves.

## Description:

At the moment, the bot can only be launched while being on OverWolf's whitelist, as the developer team has disabled the ability to run and test unauthorized applications. OverWolf API allows obtaining the game character's coordinates and writing them to a file, which enables extracting this data and directing the character in the desired direction. There's another method using OCR, but even with filters, this method is not very accurate, and another limitation is the low FPS, around 7-10 frames per second, which is not sufficient for proper functioning.

## Recording the Route:

Before starting, it's necessary to plan the safest route, minimizing obstacles where the bot may get stuck (mountains where jumping or falling from a height is needed, buildings, narrow passages). The route must be cyclic, meaning the starting point should match the ending point of the route. The "StartStream" button initiates the recording of the character's movement, and the file with recorded coordinates is located at the path <username>\Documents\OverwolfAutopath\stream.pos. Pressing the "E" key will record the current location as the resource gathering point. At the end of the route, it's necessary to stop the recording by pressing the "StopStream" button to create the "stream.pos" file with the coordinates of the traversed path.

## Bot Execution:

After the route has been recorded, and the "steam.pos" file has been created, you can directly run the bot. Before starting, ensure to set the resolution to 1280x1024 in windowed mode, as the OpenCV library is used to identify the resource by pattern. There are no templates available for other resolutions, so the bot won't work correctly with a different resolution, ignoring the resource gathering points. Another important aspect is to set the camera speed in the game settings to the minimum. You can start the bot by pressing the F2 key or the "StartBot" button. You can start at any point close to the recorded route. If the character is far from the nearest coordinate, it will run in a straight line, ignoring obstacles, which increases the likelihood of the character getting stuck. You can stop the execution by pressing the F4 key or the "StopBot" button.

## Video:
https://www.youtube.com/watch?v=J6WFTHFlyuw&ab_channel=%D0%94%D0%BC%D0%B8%D1%82%D1%80%D0%B8%D0%B9%D0%94%D0%BE%D0%BD
