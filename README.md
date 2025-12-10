# keetlink

This project can help you share keet room invite via web (http) link.

Want to host keet invite via your domain? Fork this project & deploy to your site.

## How to use?

Visit http://gasolin.idv.tw/keetlink/

And here are some examples in [Awesome Pears - Keet rooms](https://github.com/gasolin/awesome-pears/blob/main/keet_rooms.md)

## How I turn my invite link to a web link?

1. Click the `How to Add my room?` link in [keetlink](https://gasolin.idv.tw/keetlink/)
2. Copy and paste the invite generate from Keet Room > Room Profile > Invite.

> [!TIP]
> Can copy and paste [PROMPT.txt](https://raw.githubusercontent.com/gasolin/keetlink/main/PROMPT.txt) content to chatGPT and convert

----

## How keetlink works?

Its an single page static html that accept anchor parameters. If no anchor parameter received it will show the [pear community](https://gasolin.idv.tw/keetlink) room link.

### with Anchor

The url composed with 2 parts:

#### Basic url:

`https://gasolin.idv.tw/keetlink/#key=[room key]&title=[room title]`

`https://gasolin.idv.tw/keetlink/#` is the basic url host in github page, no hidden track.

#### Simple format:

`https://gasolin.idv.tw/keetlink/#{room key}`

This format provides a cleaner way to share room invites using just the room key.

#### Simple format with title:

`https://gasolin.idv.tw/keetlink/#{room key}&title={room title}`

This format combines the simple key format with an optional title parameter.


#### title

`title` is used to show room name in the page

Can encode plain text title via `encodeURIComponent`. Or you can ask chatGPT `how  `Bug Bandits🐞` looks like  in url?`

and it will return `Bug%20Bandits%F0%9F%90%9E`. Use this as the title parameter.

#### key

`key` is used to compose keet invite link in the page

Normal keet invite starts from `pear://keet/` prefix, ex: `pear://keet/yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc`

To pass in `key` we strip the prefix and use the room key directly.

#### Basic url:

The url composed with 3 parts:

`https://gasolin.idv.tw/keetlink/#key=[room key]&title=[room title]`

`https://gasolin.idv.tw/keetlink/#` is the basic url host in github page, no hidden track.

The key and title part are the same as above.

#### Final form

The params should composite with `&`, so the final form for `Bug Bandits🐞` room is 
> https://gasolin.idv.tw/keetlink/#key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc&title=Bug%20Bandits%F0%9F%90%9E

or with the simple format:

> https://gasolin.idv.tw/keetlink/#yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc

or with the simple format and title:

> https://gasolin.idv.tw/keetlink/#yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc&title=Bug%20Bandits%F0%9F%90%9E


