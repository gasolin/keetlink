# Keetlink - an unofficial Keet Groups Directory

A modern, searchable directory for Keet groups and communities. Discover and join encrypted peer-to-peer chat rooms with a beautiful, responsive interface.

## 🚀 Quick Start

Visit [https://gasolin.idv.tw/keetlink/](https://gasolin.idv.tw/keetlink/) to browse and join Keet groups.

## ✨ Features

- **🔍 Smart Search**: Find groups by name, tags, or description
- **📱 Responsive Design**: Works perfectly on desktop and mobile devices
- **🎨 Modern UI**: Dark theme with gradient accents and smooth animations
- **🏷️ Tag System**: Click tags to quickly filter related groups
- **📱 QR Code Support**: Scan QR codes to join groups instantly
- **🔗 Direct Links**: Generate shareable links for any group

## 📱 How to Join a Group

1. Browse the directory or use the search bar to find interesting groups
2. Click on any group card to view details
3. Scan the QR code with your Keet app, or click "Join Group with Keet"
4. If you don't have Keet installed, follow the download link for your platform

## 🏷️ Popular Categories

- **Official**: Pear and Keet official rooms
- **Development**: Developer discussions, bug reports, app development
- **Community**: Social chats, regional communities
- **Crypto**: Bitcoin and cryptocurrency discussions
- **Content**: Music sharing, interesting links, memes

## 🔧 How It Works

The directory is a static HTML page with embedded group data. Each group includes:

- **Name**: Display name of the group
- **Description**: Brief overview of the group's purpose
- **Tags**: Categories for easy filtering
- **Key**: Unique identifier for joining the group

### URL Format

Direct group links use this format:
```
https://gasolin.idv.tw/keetlink/#{room_key}
```

Example:
```
https://gasolin.idv.tw/keetlink/#yfo4afrc46rkykdue9br5zsiyc917eqqpr9oiy8z19xrfj9ffenx69t7eqaz5uuann7bf3pdih51o3neibf199i8cyb8tyexngxt8ug361rw9k4pgfsfxp7xxpkxoufigkz5e8ddizope3mkx5ix4dp7yapkhye
```

## 🏠 Self-Hosting

Want to host your own Keet groups directory?

1. Fork this repository
2. Modify the `rooms` array in `index.html` to include your groups
3. Deploy to any static hosting platform (GitHub Pages, Netlify, Vercel, etc.)

### Adding New Groups

Update the `rooms` array in `index.html`:

```javascript
{
    "name": "Your Group Name",
    "description": "Brief description of your group",
    "key": "your-room-key-here",
    "tags": ["Tag1", "Tag2", "Tag3"]
}
```

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript**: No build process required
- **QRCode.js**: For generating QR codes
- **Responsive Grid Layout**: Adapts to all screen sizes
- **Client-side Search**: Instant filtering without server requests
- **URL Hash Navigation**: Direct links and browser back button support, and no trace by analytics tools

## Reference

Previous version in [v1 branch](https://github.com/gasolin/keetlink/tree/v1)

## 📄 License

MIT, This project helps make Keet more accessible to everyone. Feel free to contribute and improve the directory!
