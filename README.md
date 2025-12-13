# KeetLink

A simple web tool to share Keet room invites via HTTP links. Transform your `pear://keet/` URLs into shareable web links that anyone can access.

## 🚀 Quick Start

Visit [https://gasolin.idv.tw/keetlink/](https://gasolin.idv.tw/keetlink/)

See examples in [Awesome Pears - Keet rooms](https://github.com/gasolin/awesome-pears/blob/main/keet_rooms.md)

## 📝 How to Create a Web Link

1. Visit [KeetLink](https://gasolin.idv.tw/keetlink/) and click "How to Add my room?"
2. Copy your Keet invite from: **Room Profile > Invite**
3. Paste it into the form to generate your web link

> [!TIP]
> Use [PROMPT.txt](https://raw.githubusercontent.com/gasolin/keetlink/main/PROMPT.txt) with ChatGPT for automated conversion

## 🔧 How It Works

KeetLink is a static HTML page that accepts URL parameters. Without parameters, it displays the default [Pear Community](https://gasolin.idv.tw/keetlink) room.

### URL Formats

#### 1. Basic Format
```
https://gasolin.idv.tw/keetlink/#key=[room_key]&title=[room_title]
```

#### 2. Simple Format (Key Only)
```
https://gasolin.idv.tw/keetlink/#{room_key}
```

#### 3. Simple Format with Title
```
https://gasolin.idv.tw/keetlink/#{room_key}&title={room_title}
```

### Parameters

#### `key` (Required)
The room identifier extracted from your Keet invite URL.

**Example:** From `pear://keet/yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc`

Use: `yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc`

#### `title` (Optional)
The display name for your room. Use `encodeURIComponent()` for special characters.

**Example:** `Bug Bandits🐞` becomes `Bug%20Bandits%F0%9F%90%9E`

### Complete Examples

**Basic format:**
```
https://gasolin.idv.tw/keetlink/#key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc&title=Bug%20Bandits%F0%9F%90%9E
```

**Simple format:**
```
https://gasolin.idv.tw/keetlink/#yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc
```

**Simple format with title:**
```
https://gasolin.idv.tw/keetlink/#yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc&title=Bug%20Bandits%F0%9F%90%9E
```

## 🏠 Self-Hosting

Want to host KeetLink on your own domain? Simply fork this repository and deploy to your preferred hosting platform.
