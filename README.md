# Anime-Images-API Javascript Wrapper

### Basic Usage:
```js
const Anime_Images = require('anime-images-api')
const API = new Anime_Images()
async function getIMG(){
    let { image } = await API.sfw.hug()
    console.log(image)
}
getIMG()
//Or get an NSFW Image:
getNSFWImg()
async function getNSFWImg(){
    let { image } = await API.nsfw.hentai()
    console.log(image)
}
```
Output:
```
https://anime-api.hisoka17.repl.co/images/hug80.gif
```
**The Following Endpoints Are For the `sfw` property**
`API.sfw`:

| Endpoint | Description         |
|----------|---------------------|
| hug()    | Sends a hug Gif     |
| kiss()   | Sends a kiss Gif    |
| slap()   | Sends a slap Gif    |
| punch()  | Sends a punch Gif   |
| wink()   | Sends a winking Gif |
| pat()    | Sends a pat Gif     |
| kill()   | Sends a kill Gif    |
| cuddle() | Sends a cuddle Gif  |
| wafiu()  | Sends a waifu       |

`API.nsfw`:

| Endpoint | Description         |
|----------|---------------------|
| hentai() | Sends a hug Gif     |
| boobs()  | Sends a boob Gif    |



**Other Methods:**
`download`

```js
const API = require('anime-images-api')
const images_api = new API() 

let url = 'https://example.com/file.jpg';
images_api.download(url, path, 'file.jpg')
console.log('Downloaded')

```

Discord Bot example:
```js
const Discord = require('discord.js');
const client = new Discord.Client()
const API = require('anime-images-api')
const images_api = new API() 

client.on('message', function(m){
    if (m.content.startsWith('image')){
        images_api.hug().then(response => {
            m.channel.send(response.image)
        }) 
    }
})
```




