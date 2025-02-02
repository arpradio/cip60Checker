# VS Code CIP-60 Validator

A Visual Studio Code extension for validating Cardano CIP-60 (Music Token Metadata Standard) JSON metadata.

## Features

- Validates metadata against CIP-60 versions 1, 2, and 3
- Real-time error reporting with detailed messages
- Enforces string length limits (64 characters)
- Validates ISO8601 duration formats
- Checks structure based on release type (Single/Multiple/Album)

## Usage

1. Open a JSON file containing CIP-60 metadata
2. Use one of the following methods to validate:
   - Press `Ctrl+Alt+V` (`Cmd+Alt+V` on Mac)
   - Right-click and select "Validate CIP-60 Metadata"
   - Open Command Palette (Ctrl+Shift+P) and type "Validate CIP-60"

## Validation Rules

The extension checks for:

- Correct metadata version format (must be integer 1, 2, or 3)
- Required fields based on version and release type
- Proper format for song durations (ISO8601)
- String length limits (max 64 characters)
- Array format for artists and genres
- Proper structure for audio file metadata

## Error Reporting

Errors are displayed in two ways:
- In-editor highlighting of problematic sections
- Detailed error messages in the Problems panel

## Example

For a version 1 Multiple release type, audio files must contain:
```json
{
  "song_title": "Track Name",
  "track_number": 1,
  "song_duration": "PT3M30S",
  "genres": ["Genre1", "Genre2"],
  "artists": ["Artist Name"]
}
```

## Requirements

- Visual Studio Code version 1.60.0 or higher

## Installation

1. Download the .vsix file
2. In VS Code, go to Extensions
3. Click "..." at the top of Extensions panel
4. Select "Install from VSIX..."
5. Choose the downloaded file

## License

MIT

## Contributing

Issues and pull requests welcome on GitHub.
