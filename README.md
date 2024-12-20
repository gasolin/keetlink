# keetlink

This project can help you share keet room invite via web (http) link.

Want to host keet invite via your domain? Fork this project & deploy to your site.

## How to use?

Visit http://gasolin.idv.tw/keetlink/

And here are some examples in [Awesome Pears - Keet rooms](https://github.com/gasolin/awesome-pears/blob/main/keet_rooms.md)

## How I turn my invite link to a web link?

2 steps:

1. Copy and paste [PROMPT.txt](https://raw.githubusercontent.com/gasolin/keetlink/main/PROMPT.txt) content to chatGPT
2. Copy and paste the invite generate from Keet Room at the bottom.

----

## How keetlink works?

Its an single page static html that accept url params. If no url param received it will show the [pear community](https://gasolin.idv.tw/keetlink) room link.

### with Anchor

The url composed with 2 parts:

#### Basic url:

`https://gasolin.idv.tw/keetlink/#key=[room key]&title=[room title]`

`https://gasolin.idv.tw/keetlink/#` is the basic url host in github page, no hidden track.


### with URL params

A more schematic correct way is pass invite key and title through URL params, but the path and param might be recorded on server side.


#### title

`title` is used to show room name in the page

Can encode plain text title via `encodeURIComponent`. Or you can ask chatGPT `how  `Bug Bandits🐞` looks like  in url?`

and it will return `Bug%20Bandits%F0%9F%90%9E`. Paste that as `title=Bug%20Bandits%F0%9F%90%9E`

#### key

`title` is used to compose keet invite link in the page

Normal keet invite starts from `pear://keet/` prefix, ex: `pear://keet/yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc`

To pass in `key` we strip the prefix so Paste as `key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc`

#### Basic url:

The url composed with 3 parts:

`https://gasolin.idv.tw/keetlink/#key=[room key]&title=[room title]`

`https://gasolin.idv.tw/keetlink/#` is the basic url host in github page, no hidden track.

The key and title part are the same as above.

#### Final form

The params should composite with `&`, so the final form for `Bug Bandits🐞` room is 
> https://gasolin.idv.tw/keetlink/#key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc&title=Bug%20Bandits%F0%9F%90%9E

or with url params

> https://gasolin.idv.tw/keetlink/?key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc&title=Bug%20Bandits%F0%9F%90%9E
