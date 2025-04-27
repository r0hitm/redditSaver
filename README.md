# redditSaver-Offline

Forked from [erohtar/redditSaver](https://github.com/erohtar/redditSaver). For downloading and saving the post media. 

**Note**: Only downloads the image/video of the post.


## Features
- YAML Frontmatter is downloaded along with the markdown formatted note - supports using it with **Dataview** plugin (see below)
- Notes are saved in `reddit\<subreddit>\<note_title>` hierarchy
- Clickable link to the post/comment is added at the top of the note (besides being saved in Frontmatter)


## Setup
1. Go to [this url](https://ssl.reddit.com/prefs/feeds/) and copy the json link for your saved posts.
2. Clone this repo & copy **settings.sample.json** to **settings.json** and udpate these values:
	- `jsonUrl` : Put above copied link
	- `rootPath` : Your notes target path (use double forward slashes)
	- `overWrite` : If you wish to overwrite your existing note files with latest downloads, set this to 1
```
{
	"jsonUrl": "https://www.reddit.com/user/erohtar/saved.json?feed=xxxxxxxxx&user=erohtar",
	"rootPath": "C:\\ObsidianVault\\Reddit",
	"overWrite": 0
}
```
3. Run the `redditSaver.js` using `node`.


## (modified) Additional Notes
- [ ] Runs the script continuously using the `after` key present on the response data to get all the saved posts data.

