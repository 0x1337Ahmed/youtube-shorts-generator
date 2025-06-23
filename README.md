# YouTube Shorts Generator

An automated tool that generates YouTube Shorts videos from text prompts. The tool converts text to speech, finds relevant visuals, and combines them into a vertical video format suitable for YouTube Shorts.

## Features

- Text to Speech conversion using AI
- Automatic visual asset fetching from Pexels
- 9:16 aspect ratio video generation optimized for YouTube Shorts
- Optional background music
- Optional branding/watermark
- Batch processing via CSV upload
- Modern, responsive UI built with Next.js and Tailwind CSS

## Prerequisites

- Node.js 18+ installed
- FFmpeg installed on your system
- API keys for:
  - ElevenLabs (for Text-to-Speech)
  - Pexels (for visual assets)

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env.local` file in the root directory with your API keys:
   ```
   ELEVENLABS_API_KEY=your_elevenlabs_api_key
   PEXELS_API_KEY=your_pexels_api_key
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:8000](http://localhost:8000) in your browser

## Usage

### Single Video Generation

1. Enter your script in the text area
2. Toggle optional features (background music, branding)
3. Click "Generate Video"
4. Wait for the processing to complete
5. Download the generated video

### Batch Processing (CSV)

1. Enable "Batch Mode"
2. Upload a CSV file with the following format:
   ```csv
   prompt,addMusic,addBranding
   "Your first video script",true,false
   "Your second video script",false,true
   ```
3. Click "Generate Video"
4. Download the generated videos

## Technical Details

- Frontend: Next.js with Tailwind CSS and Shadcn UI components
- Video Processing: FFmpeg for combining assets and adding effects
- Text-to-Speech: ElevenLabs API
- Visual Assets: Pexels API
- File Format: MP4 with H.264 video codec and AAC audio codec
- Aspect Ratio: 9:16 (1080x1920) optimized for YouTube Shorts

## Error Handling

The application includes comprehensive error handling for:
- Invalid input text
- Failed API calls
- Video processing errors
- Invalid CSV format
- Missing API keys

## Limitations

- Maximum text length: 1000 characters per video
- Supported video length: Up to 60 seconds (YouTube Shorts limit)
- File size limit: Depends on server configuration
- Supported CSV file size: Up to 1MB

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - feel free to use this project for personal or commercial purposes.
