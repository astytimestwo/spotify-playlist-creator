# Spotify Playlist Creator

A robust, multi-threaded tool to discover new releases and collaborations from your followed artists on Spotify.

## Features

- **Multi-threaded Discovery**: Processes multiple artists simultaneously for maximum performance.
- **Enhanced Search**: Specifically looks for `Remix`, `Mix`, and `With` collaborations that standard "New Release" feeds often miss.
- **Smart Filtering**: Automatically skips "Greatest Hits" and low-quality compilations.
- **Batched Playlist Creation**: Handles large tracklists by batching API requests.
- **Security First**: Uses environment variables to keep your Spotify credentials safe.

## Setup

1. **Spotify API Setup**:
   - Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard).
   - Create an app to get your `Client ID` and `Client Secret`.
   - Set the Redirect URI to `http://localhost:8888/callback`.

2. **Environment Variables**:
   - Copy `.env.example` to `.env`.
   - Fill in your `SPOTIPY_CLIENT_ID`, `SPOTIPY_CLIENT_SECRET`, and `SPOTIPY_REDIRECT_URI`.

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the script using Python (example below):

```bash
python main.py --start 1 --end 50 --cutoff 2025-10-12
```

### Arguments

- `--start`: Start index of your followed artists (default: 1).
- `--end`: End index of your followed artists (default: all).
- `--cutoff`: Only include tracks released after this date (YYYY-MM-DD).
- `--verbose`: Enable detailed logging.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
