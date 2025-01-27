# Call For Code 2019 - Northstar Front End
## About 
This is the front end iOS app for the Northstar project. It communicates with the backend Northstar cloud to predict wildfires, send alerts and route users to safe locations. In its current state, the app demonstrates the following functionality:
- alerts for wildfire danger and directions to safety
- exploration of and navigation to safe zones near your location
- exploration of potential fire hazards near your location

The app makes internal calls to the backend. Our current integration allows recieving an image of the wildfire using the GRPC protocol. Due to the effort required to setup a local server, the integration has been disabled for this demo. Instead, backend calls are mimicked in the front end. There are also other integrations that are yet to be implemented.

## Requirements
- Mac OS Mojave (v10.14.5) 
- XCode App (v10.2.1)

## Setting up the app
1. Clone this repository
2. Navigate to the repository in your terminal
3. Install Cocoapods
`$ sudo gem install cocoapods`
4. Run Cocoapods to create or update the XCode Workspace file in the repository
`$ pod repo update && pod install`
5. Open the resulting XCode **Workspace** file which will launch the XCode App
6. Build and run the app, an iOS emulator should pop up
![Alt text](/Screenshots/build_run.png?raw=true "Build Location")
7. In the iOS emulator, go to the Debug menu. Select Location > Custom Location ... and enter the following:  
  **Latitude:** 37.220818  
  **Longitude:** -121.782621

If you run into issues please email daxit.agarwal@ibm.com

## Screenshots

Upon launch, the app focuses in on the user's current location.
![Alt text](/Screenshots/current_location.png?raw=true "Current Location")
After ten seconds, an alert pops up alerting the user of a wildfire. In the final version of the app, this alert would trigger when the backend sends a response that there is a wildfire near the user's location.
![Alt text](/Screenshots/wildfire_alert.png?raw=true "Wildfire Alert")
Upon clicking "Start Navigation", the following navigation view is shown to direct the user to the closest safe zone.
![Alt text](/Screenshots/safe_zone_nav.png?raw=true "Safe Zone Navigation")
After exiting the navigation view, the user can explore safe locations near them. The red markers represent safe locations, while the towers represent PG&E towers that are potential fire hazards.
![Alt text](/Screenshots/explore_safe_zones.png?raw=true "Safe Zone Exploration")

