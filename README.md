# takeit
takeit is a reddit script that downloads an arbitrary number of submissions from a subreddit into an arbitrary folder.

# Usage
```
python takeit.py [sub] [amount of submissions] [folder to download them] [--nsfw]
```

# Why should i use this over any other reddit downloader?

- nsfw filtering
- fast. (1.7s on modern wifi (354.9 MB), 10 submissions from [r/unixporn](https://reddit.com/r/unixporn))
- only ONE dependency!

# Demo
![demo](./demo.gif)

# how to "self host"?

In a way, takeit is selfhosted. How is it selfhosted? You need to create an app [here](https://www.reddit.com/prefs/apps). Here are steps (after you've made an app in reddit):
1. In the directory that you've cloned `takeit`, add this to a `.env` file:
```env
# please don't copy paste this exactly, and then run it, and then get angry at me that it doesn't work.
REDDIT_SECRET="[YOUR REDDIT APP SECRET]"
REDDIT_ID="[YOUR REDDIT APP ID]"
```
2. Install the dependencies for `takeit` via `pip install -r requirements.txt` or `py -m pip install -r requirements.txt` depending on your operating system.

# Running

For example, let's say we want to download 10 submissions from [r/196](https://www.reddit.com/r/196), we would run something like this:
```
python takeit.py 196 10 test
```
This'll download 10 submissions (images, videos, and gifs) to the `test` directory.
