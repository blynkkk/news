# Posting news
You can update your customers with any latest news. When new content is available, it will be automatically shown in a popup. Users can close the popup or it will auto-close in 8 seconds.

IMAGE

## Setup
1. Create a new **public** GitHub repository
2. In Your.Console go to Settings -> Application Settings -> News repository -> add a link to your Github news repo

IMAGE

## Working with content

Your repository should have two files:
```
latest_timestamp.md
old.md
```

Content is written using [markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) format. 

Files have a pre-defined structure. You would need to follow it to render news correctly. Here is how it should be structured:

```
### date and time (required)

# Headline (required)

Image (optional). Should always be the same size (640x240)

Body: Short description (optional, but highly recommended)

Links(optional) - for the latest post it will render as a button, for older news it will be rendered as a link (if possible)
```


### Making first post:

1. Create new file: `latest_timestamp.md`, where `timestamp` is a current unix time. To get the timestamp go to: LINK. As a result, file name should look similar to this: `latest_1646642432`
2. Edit the contents of the file:

Example: 

```
### April 1, 2022
# Latest news! We put a man on the moon!

![image](https://user-images.githubusercontent.com/11541426/157123572-8339b3e1-c24d-45c1-94c1-7de66fbf129f.png)

If you believed they put a man on the moon
Man on the moon
If you believed there's nothing up his sleeve
Then nothing is cool

[Link](https://blynk.io)
```

### Making next posts:
When you have an update for your users, you need to update the contents of the `latest` file and move previous content into `old` file. To do that:
1. Copy contents of the `latest` to the top of your `old file` contents
It should look similat to the example below: 

old.md:
```
### April 1, 2022
# Latest news! We put a man on the moon!

![image](https://user-images.githubusercontent.com/11541426/157123572-8339b3e1-c24d-45c1-94c1-7de66fbf129f.png)

If you believed they put a man on the moon
Man on the moon
If you believed there's nothing up his sleeve
Then nothing is cool

[Link](https://blynk.io)


### January 15, 2022
# We just launched!
Welcome to our new IoT portal
```

2. Now update the content of the `latest` file with fresh news
3. Rename the `latest` file by updating to the latest timestamp. 
4. Save changes.
