# SupaDrawer

SupaDrawer is a real-time multiplayer drawing board application built with React Native. It leverages Supabase's real-time database capabilities to enable multiple users to draw on a shared canvas simultaneously.

## Features

- Real-time collaborative drawing
- Unique user identifiers with random usernames and colors
- Smooth drawing experience using a custom drawing board component
- Easy channel-based drawing sessions

## Tech Stack

- **React Native**: For building the mobile application.
- **Expo**: For development and building the app.
- **Supabase**: For real-time database and user authentication.

## Getting Started

### Prerequisites

- Node.js and npm installed
- Expo CLI installed (`npm install -g expo-cli`)
- Supabase account and project set up

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/tusharpamnani/supaDrawer.git
   cd supaDrawer
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create an `.env` file in the root of your project and add your Supabase URL and Anon Key:

   ```env
   EXPO_PUBLIC_SUPABASE_URL=your-supabase-url
   EXPO_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key
   ```

4. **Run the project:**

   ```bash
   expo start
   ```

## Project Structure

```
SupaDrawer
├── app
│   ├── _layout.tsx           # Layout component
│   ├── index.tsx             # Main entry point
│   └── channel
│       └── [channel].tsx     # Channel-specific drawing screen
├── components
│   └── DrawingBoard.tsx      # Drawing board component
├── .env                      # Environment variables
├── app.json                   
├── README.md                 # This file
├── LICENSE                   # MIT License
└── package.json              # Project metadata and dependencies
```

## Usage

1. **Start a drawing session:**

   Open the app and navigate to a drawing channel by passing the channel name as a parameter in the URL or navigation.

2. **Draw on the canvas:**

   Use your finger or stylus to draw on the canvas. Your drawings will be broadcasted in real-time to other users in the same channel.

3. **Collaborate:**

   Other users joining the same channel will see your drawings and can draw simultaneously on the same canvas.

## File Descriptions

### `app/_layout.tsx`

Defines the layout for the application, setting up the navigation structure.

### `app/index.tsx`

The home screen of the application, where users can navigate to different drawing channels.

### `app/channel/[channel].tsx`

The main drawing screen for a specific channel. This component handles the initialization of the Supabase channel and manages the drawing events.

### `components/DrawingBoard.tsx`

A custom component for the drawing board. It provides the canvas and drawing functionalities, and exposes methods for handling drawing events.

## Demo

Check out the video demo of the main app in action:

| ![SupaDrawer Demo 1](/assets/supa1.gif) | ![SupaDrawer Demo 2](/assets/supa2.gif) |
|:---------------------------------------:|:---------------------------------------:|

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue to improve the project.

## License

This project is licensed under the [MIT](LICENSE) License.

---

Happy drawing! 🎨
