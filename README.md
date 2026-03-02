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
- **🌐 Dynamic URL Support**: Support for custom room keys and titles
- **📊 JSON Data Management**: Room data stored in separate JSON file for easy maintenance

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

Direct group links support multiple formats:

**Basic format (for catalog groups):**
```
https://gasolin.idv.tw/keetlink/#{room_key}
```

**Custom format with title (for non-catalog groups):**
```
https://gasolin.idv.tw/keetlink/#{room_key}&title={room_title}
```

**Examples:**
```
# Catalog group
https://gasolin.idv.tw/keetlink/#yfo4afrc46rkykdue9br5zsiyc917eqqpr9oiy8z19xrfj9ffenx69t7eqaz5uuann7bf3pdih51o3neibf199i8cyb8tyexngxt8ug361rw9k4pgfsfxp7xxpkxoufigkz5e8ddizope3mkx5ix4dp7yapkhye

# Custom group with title
https://gasolin.idv.tw/keetlink/#customroomkey&title=My%20Custom%20Group
```

**Note**: Groups not in the official catalog will display "This Group does not in catalog" in the tags section.

## 🏠 Self-Hosting

Want to host your own Keet groups directory?

1. Fork this repository
2. Modify the `datapackage.json` file to include your groups
3. Deploy to any static hosting platform (GitHub Pages, Netlify, Vercel, etc.)

### Adding New Groups

To add a new group to this directory, you can:

1. Join [Keety Links Chat](https://gasolin.idv.tw/keetlink/#yfo9nkga9abx983cannfe8e46mxmmqx711jwabjoh7ourqo7agdaah9s5yguzef4c9ax18wxwgfwsiqnfmq4rytkwr371eemycu75sscmzqduit8q5h34uda6cg8ntyfys5s4zf31m71xegqa1uoguttxkw1eye) and follow the instructions to post the non-expiry link there.
2. Or, update the `datapackage.json` file manually:

```json
{
    "name": "qvac-workbench-dev",
    "title": "QVAC Workbench Dev 🛠️",
    "description": "A developer‑focused room for building and testing QVAC workbenches.",
    "data": [
        {
            "key": "nfotu398boebrse8udixr6sbzwnozbq99diquyq8n3h4uw6a8br41yya7ri333xtp61fucazyjmgaomjwqdjwhn3yi1iwb9bcfudeqfyq6j4wpmuyqayd4bqcsrg1h8n6n88qae9d97ck81j9nd39p6ksmbuayedtjnjgnnjajc3g5sej8bfoaadk3sqk"
        }
    ],
    "keywords": ["Dev", "QVAC"]
}
```

**Data Structure:**
- **name**: identifier of the group
- **title**: Display title of the group
- **description**: Brief overview of the group's purpose  
- **data.key**: Unique identifier for joining the group
- **keywords**: Array of categories for easy filtering

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript**: No build process required
- **QRCode.js**: For generating QR codes
- **Responsive Grid Layout**: Adapts to all screen sizes
- **Client-side Search**: Instant filtering without server requests
- **URL Hash Navigation**: Direct links and browser back button support, and no trace by analytics tools
- **JSON Data Loading**: Asynchronous loading of room data from external file
- **Dynamic Room Handling**: Support for both catalog and non-catalog rooms
- **Error Handling**: Graceful fallback if JSON loading fails

## Reference

Previous version in [v1 branch](https://github.com/gasolin/keetlink/tree/v1)

## 📄 License

MIT

### Contributing

This project helps make Keet more accessible to everyone. Feel free to contribute and improve the directory! By

- 🐛 Report bugs or request features via GitHub issues
- 💡 Suggest new groups to add to the catalog via [Keety Links Chat](https://gasolin.idv.tw/keetlink/#yfo9nkga9abx983cannfe8e46mxmmqx711jwabjoh7ourqo7agdaah9s5yguzef4c9ax18wxwgfwsiqnfmq4rytkwr371eemycu75sscmzqduit8q5h34uda6cg8ntyfys5s4zf31m71xegqa1uoguttxkw1eye)
- 🔧 Improve the UI/UX or add new features
- 📝 Help improve documentation

The directory is designed to be community-driven and welcomes contributions from all Keet users!
