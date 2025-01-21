
# PeerChat

PeerChat is a web-based real-time communication application that allows users to join or create rooms for video and audio communication. The application leverages the Agora RTM SDK for real-time messaging and WebRTC for media streaming.

## Features

- Create or join a room using an invite link.
- Real-time video and audio communication.
- Toggle camera and microphone during the session.
- Leave the room gracefully.

## Project Structure

```
agora-rtm-sdk-1.5.1.js
dist/
icons/
index.html
lobby.css
lobby.html
main.css
main.js
webpack.config.js
package-lock.json
package.json
```

- **agora-rtm-sdk-1.5.1.js**: Agora RTM SDK for real-time messaging.
- **icons/**: Directory containing icons used in the application.
- **index.html**: Main page for the video communication.
- **lobby.css**: Stylesheet for the lobby page.
- **lobby.html**: Lobby page where users can create or join a room.
- **main.css**: Stylesheet for the main page.
- **main.js**: JavaScript file containing the main logic for the application.
- **webpack.config.js**: Webpack configuration file.

## Getting Started

### Prerequisites

- Node.js and npm installed.
- A web browser (Chrome, Firefox, etc.)
- An Agora account to get the App ID and token.

### Setup

1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install deoendencies:
  ```sh
  npm install
  ```

3. Build the project
  ```sh
  npx webpack --config webpack.config.js
  ```  
    
4. Open index.html in your web browser.

### Configuration

Create a .env file in the root of your project and add your Agora App ID:

```sh
APP_ID=YOUR_AGORA_APP_ID
```

## Usage

1. Open lobby.html in your web browser.
2. Enter an invite link to create or join a room.
3. Once in the room, you can:
   - Toggle the camera using the camera button.
   - Toggle the microphone using the mic button.
   - Leave the room using the leave button.

## Code Overview

### Main Functions

- **init()**: Initializes the Agora RTM client and sets up event listeners.
- **toggleCamera()**: Toggles the camera on and off.
- **toggleMic()**: Toggles the microphone on and off.
- **leaveChannel()**: Leaves the current channel gracefully.

### Event Listeners

- `beforeunload`: Calls `leaveChannel` when the window is about to be unloaded.
- `camera-btn`: Calls `toggleCamera` when the camera button is clicked.
- `mic-btn`: Calls `toggleMic` when the mic button is clicked.

## License

This project is licensed under the AGORA, INC. SDK LICENSE AGREEMENT. A copy of this license may be found at [Agora SDK License Agreement](https://www.agora.io/en/sdk-license-agreement/).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Acknowledgements

- [Agora.io](https://www.agora.io) for providing the real-time messaging and media streaming SDKs.

