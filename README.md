# keetlink

share keet room invite via http link

## How it works

Its an single page static html that accept url params. If no url param received it will show the [pear community](https://gasolin.idv.tw/keetlink) room link.

### Basic url: https://gasolin.idv.tw/keetlink/

The url composed with 3 parts:

`https://gasolin.idv.tw/keetlink/?title=[room title]&key=[room key]`

`https://gasolin.idv.tw/keetlink/` is the basic url host in github page, no hidden track.

### title

`title` is used to show room name in the page

Can encode plain text title via `encodeURIComponent`. Or you can ask chatGPT `how  `Bug Bandits🐞` looks like  in url?`

and it will return `Bug%20Bandits%F0%9F%90%9E`. Paste that as `title=Bug%20Bandits%F0%9F%90%9E`

### key

`title` is used to compose keet invite link in the page

Normal keet invite starts from `pear://keet/` prefix, ex: `pear://keet/yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc`

To pass in `key` we strip the prefix so Paste as `key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc` 

### Final form

The params should composite with `&`, so the final form for `Bug Bandits🐞` room is https://gasolin.idv.tw/keetlink/?title=Bug%20Bandits%F0%9F%90%9E&key=yryskxsgye5j6se8mzzxqoygzion3zyo93iphxhew4pznn7sdbeat17cr5gaquoawe9iq7eipkez99qm6zpkouckg8sacci8bdkgmcdtoc
