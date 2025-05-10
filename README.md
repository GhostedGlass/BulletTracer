# FPS Bullet Tracer Script

This script adds a bullet tracer effect that appears when the player clicks their mouse. A neon beam is created that extends from the player's position toward the point of impact, creating a visual representation of where the bullet would travel. Additionally, the tracer fades out after 5 seconds and disappears with a 2-second fade-out. 

The script is built to be integrated into an existing exploit framework, and it offers a simple but effective way to add bullet trace visuals for any shooting mechanics already in place.

## Features

-> **Neon Bullet Tracers**: The script generates a glowing neon beam when the player shoots, providing a visual representation of the bullet's trajectory.

-> **Fade-Out Effect**: After a few seconds, the tracer fades out over a smooth 2-second transition, creating a dynamic effect.

-> **Raycasting for Trajectory**: Raycasting is used to detect the bullet's trajectory, ensuring the tracer only appears where the bullet would logically hit, avoiding visual clutter.

-> **Toggleable Tracer**: The tracer effect can be toggled on and off using the 'T' key, giving the user control over when to enable or disable the feature.

-> **Collision Handling**: The script ensures that tracers do not interfere with each other by excluding any existing tracers from raycasting checks, preventing visual overlap.

## How It Works

This script isn't intended to be run standalone - it relies on being integrated into a larger exploit framework that handles the player's shooting mechanics. When a player clicks the mouse, the script uses raycasting to calculate the trajectory of the bullet based on where the mouse pointer is. If the ray hits an object, a neon beam appears at the point of impact, extending from the player's torso.

The tracer stays visible for 5 seconds and then fades out over the next 2 seconds. This fade-out is achieved using tweening to smoothly transition the tracer's transparency.

The real power of the script is its ability to be toggled on and off, making it flexible for use in different situations. If the player presses the 'T' key, the tracer is disabled, and no new tracers will be created. Existing tracers are also removed immediately, which can be useful when needing to stop the effect without restarting the entire script.

## Integration Notes

The script works by attaching to the player’s mouse input and calculating the shooting trajectory using raycasting from the player’s torso. It’s designed for use in a custom exploit framework where the mechanics of shooting (i.e., mouse clicks and bullet impact detection) are already handled by other parts of the framework. 

The tracer’s starting point is the LocalPlayer’s **HumanoidRootPart**, and it will always shoot from this part of the player’s body. This might result in slightly inaccurate tracers if the player’s orientation is at an angle, but it serves its purpose in typical scenarios where precise shooting mechanics are already set up.

### Why This Script Might Be Useful

While this script could function by itself to add visual feedback to the shooting process, it’s primarily designed to be integrated into larger exploit frameworks that already deal with the specifics of shooting mechanics. It's perfect for adding an extra layer of feedback to the player experience without having to reinvent the wheel.

Additionally, the ability to toggle the effect makes it easy to enable or disable the tracer as needed, which can be useful if you want to minimize distractions or enhance the effect for specific game moments.
