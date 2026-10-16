# Niche Internet

A community-driven site for discovering lesser-known YouTube channels and interesting corners of the web. Users submit channels and websites, vote on them, and explore results ranked so that small creators get visibility instead of being buried by big ones.

**Live:** https://nicheinternet.vercel.app

Built during [Hack Club High Seas 2024](https://highseas.hackclub.com).

## Features

- **Submit channels and websites** by URL or @handle, with a short description. Channel name, avatar, subscriber count and keywords are fetched from the YouTube Data API.
- **Voting and ranking.** Submissions are ranked by a score that combines votes, subscriber count (fewer subscribers rank higher) and submission date (new submissions get a temporary boost).
- **Search** across channel names/URLs, @handles, YouTube keywords, and both user-written and YouTube descriptions.

## Tech stack

| Area | Technology |
| --- | --- |
| Framework | SvelteKit |
| Database | PostgreSQL |
| External API | YouTube Data API v3 |
| Hosting | Vercel |

## Getting started

Requirements: Node.js, a PostgreSQL database, and a YouTube Data API key.

```bash
git clone https://github.com/mbarancik/niche-internet.git
cd niche-internet
npm install

cat << 'EOF' > .env
DATABASE_URL=your_connection_string
YOUTUBE_API_KEY=your_api_key
EOF 

npm run dev
```

Environment variables:

| Variable | Description |
| --- | --- |
| `DATABASE_URL` | PostgreSQL connection string |
| `YOUTUBE_API_KEY` | YouTube Data API v3 key |

## License

Third-party licences are listed in [NOTICE.txt](NOTICE.txt).
