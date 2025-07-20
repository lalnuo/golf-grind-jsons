# Golf Grind Dynamic Content

This repository hosts dynamic JSON content for the Golf Grind mobile app.

## Files

- `drills.json` - Contains drill video data that can be updated without app releases

## Usage

The app fetches content from:
```
https://raw.githubusercontent.com/lallinuorteva/golf-grind-jsons/main/drills.json
```

## Updating Content

1. Edit the JSON files directly on GitHub
2. Changes are reflected in the app within ~5 minutes (GitHub CDN cache)
3. Always validate JSON before committing

## Schema

### drills.json
```json
{
  "version": "1.0.0",
  "lastUpdated": "ISO-8601 timestamp",
  "drills": [
    {
      "id": "unique-drill-id",
      "title": "Drill Title",
      "youtubeId": "YouTube video ID",
      "channelName": "Channel Name",
      "channelUrl": "https://youtube.com/@channel",
      "thumbnail": "https://img.youtube.com/vi/{youtubeId}/maxresdefault.jpg",
      "duration": "M:SS",
      "description": "Drill description",
      "challengeIds": [1, 2, 3]
    }
  ]
}
```

## Challenge IDs

- 1: Short Putts
- 2: Lag Putting  
- 3: Chipping
- 4: Pitching
- (Add more as needed)