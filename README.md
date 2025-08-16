# YouTube Watchlist 📺

A modern, feature-rich YouTube watchlist application that helps you organize and track videos you want to watch. Built as a single HTML file with no dependencies, making it easy to use offline or host anywhere.

## ✨ Features

### Core Functionality
- **Add Videos**: Paste YouTube URLs or video IDs to add videos to your watchlist
- **Auto-fetch Metadata**: Automatically retrieves video titles, channel names, and thumbnails
- **Mark as Watched**: Keep track of which videos you've already seen
- **Remove Videos**: Delete videos from your list with undo functionality
- **Search & Filter**: Search by title or channel name
- **Multiple Sort Options**: Sort by date added, title, or scheduled watch date

### Advanced Features
- **Schedule Videos**: Set "watch by" dates with visual indicators for overdue/upcoming videos
- **Video Preview**: Built-in YouTube player for quick previews
- **Dark/Light Theme**: Toggle between themes with system preference detection
- **Grid/List View**: Switch between compact list and detailed grid layouts
- **Data Management**: Import/export your watchlist as JSON files
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Offline Storage**: All data stored locally in your browser

## 🚀 Getting Started

### Quick Start
1. Download the `index.html` file
2. Open it in any modern web browser
3. Start adding YouTube videos to your watchlist!

### Adding Videos
- Paste a full YouTube URL: `https://youtube.com/watch?v=VIDEO_ID`
- Use short URLs: `https://youtu.be/VIDEO_ID`
- Or just the video ID: `VIDEO_ID` (11 characters)

## 🎯 How to Use

### Basic Operations
1. **Add a Video**: Paste a YouTube URL in the input field and click "Add Video"
2. **Mark as Watched**: Click the checkmark icon on any video card
3. **Preview Video**: Click the play button to watch in the built-in player
4. **Remove Video**: Click the trash icon (with undo option)
5. **Search Videos**: Use the search bar to filter by title or channel

### Scheduling System
- Click the calendar icon on any video to set a "watch by" date
- Videos are color-coded:
  - 🔴 **Red (Overdue)**: Past the scheduled date
  - 🟡 **Yellow (Today)**: Scheduled for today
  - 🔵 **Blue (Upcoming)**: Future scheduled date

### Data Management
1. Open Settings → Manage Data
2. **Export**: Save your watchlist as a JSON file
3. **Import**: Load a previously exported watchlist
4. **Backup**: Copy data to clipboard for manual backup

## ⚙️ Settings & Preferences

### Theme Options
- **Light Mode**: Clean, bright interface
- **Dark Mode**: Easy on the eyes for night viewing

### Layout Options
- **Grid View**: Card-based layout with large thumbnails
- **List View**: Compact list for quick scanning

### Other Preferences
- **Autoplay Previews**: Control whether embedded videos start automatically
- **Sort Preferences**: Your preferred default sorting method

## 💾 Data Storage

### Local Storage
- All data is stored in your browser's local storage
- No data is sent to external servers (except for fetching video metadata)
- Your watchlist persists between browser sessions

### Data Format
The app stores minimal data for each video:
```json
{
  "originalUrl": "https://youtube.com/watch?v=VIDEO_ID",
  "title": "Video Title",
  "channel": "Channel Name",
  "thumbnail": "https://...",
  "watched": false,
  "scheduledDate": "2025-01-15"
}
```

## 🔧 Technical Details

### Browser Compatibility
- **Modern Browsers**: Chrome 70+, Firefox 65+, Safari 12+, Edge 79+
- **Mobile**: iOS Safari, Chrome Mobile, Firefox Mobile
- **Features Used**: ES6+, CSS Grid, Flexbox, Local Storage

### Dependencies
- **None!** - Pure HTML, CSS, and JavaScript
- **External Resources**:
  - Google Fonts (Inter)
  - Font Awesome icons
  - NoEmbed API for video metadata

### File Structure
```
youtube-watchlist.html    # Complete standalone application
├── HTML structure
├── CSS styling (embedded)
└── JavaScript functionality (embedded)
```

## 🛠️ Customization

### Modifying Colors
Edit the CSS custom properties in the `:root` section:
```css
:root {
  --accent-color: #e52d27;  /* YouTube red */
  --bg-primary: #f8f9fa;    /* Light background */
  /* ... other colors */
}
```

### Adding New Features
The app uses a modular JavaScript architecture:
- `App.state`: Application state management
- `App.DOM`: Cached DOM elements
- `App.render()`: Main rendering function
- Event handlers for user interactions

## 🚨 Troubleshooting

### Common Issues
1. **Videos Not Loading**: Check internet connection for metadata fetching
2. **Dark Mode Not Saving**: Ensure local storage is enabled
3. **Import Failing**: Verify JSON format matches export structure
4. **Preview Not Working**: Some videos may have embedding restrictions

### Error Messages
- **"Invalid YouTube URL"**: Check the URL format
- **"Video already in watchlist"**: Duplicate detection is working
- **"Import failed"**: JSON format error or corrupted data

## 🔒 Privacy & Security

### Data Privacy
- No user data is collected or transmitted
- Video metadata fetched from public APIs only
- All personal data stays in your browser

### Security Features
- No eval() or unsafe JavaScript practices
- Content Security Policy compatible
- Safe HTML generation without innerHTML vulnerabilities

## 📱 Mobile Experience

### Touch-Friendly
- Large touch targets for mobile users
- Responsive grid that adapts to screen size
- Optimized modal dialogs for mobile

### Mobile Specific Features
- Pull-to-refresh feel with smooth animations
- Mobile-optimized video preview player
- Thumb-friendly button sizes

## 🎨 Design Philosophy

### Modern UI
- Clean, minimalist interface
- Smooth animations and transitions
- Consistent visual hierarchy
- Accessibility-first design

### User Experience
- Intuitive navigation
- Clear visual feedback
- Forgiving error handling
- Progressive enhancement

## 📈 Performance

### Optimizations
- Lazy loading for video thumbnails
- Efficient DOM manipulation
- Minimal memory footprint
- Fast startup time

### Scalability
- Handles hundreds of videos smoothly
- Efficient search and filtering
- Optimized rendering pipeline

---

**Made with ❤️ for YouTube enthusiasts who want to organize their viewing experience.**
