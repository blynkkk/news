You can update your customers with latest news. When new content is available, it will be automatically shown in a popup. Users can close the popup and return read the news later.

![1_platform-news-popup](https://user-images.githubusercontent.com/24506752/160088511-d8d215a1-bcc3-4663-9152-9400561c8ec4.png)

# Initial Setup
1. Create a new **public** GitHub repository
2. In Your.Console go to Settings -> Application Settings -> News repository -> add a link to your Github news repository

![2_news-link](https://user-images.githubusercontent.com/24506752/160089859-b597f74d-15ec-4e08-a456-949cf57d2e9c.png)

# Working with content
Your repository should have this structure:
<img width="884" alt="image" src="https://user-images.githubusercontent.com/24506752/157888403-5e3e670f-d09c-44b3-b30f-0e4080a6d23d.png">


### config.json
This file stores a list of all news in JSON format. You need to follow the exact structure as described below:

```
"list": [ // list of news
  {
    "path": "/list/second.md", // path to md file. (required)
    "date": "04.09.2022", // date and time of the post (required) FORMAT: MM.DD.YYYY (required)
    "link": "Read more" // Link is optional - for the latest post it will render as a button, for older news it will be rendered as a regular link. 
     "URL": "https://mywebsite.com/news.html" // Link URL. Links will open in new browser tab.
  }
]
```

### news folder
![2_news-list](https://user-images.githubusercontent.com/24506752/160089878-68f9b98e-d15c-4732-85a2-a0478782ef1f.png)

This folder contains individual news files in .md ([markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax))format.



# Making first post:
1. Inside of the `news` folder create new file: `my_first_news.md`. File name can be any.
2. Edit the contents of the file
  - Title (required). Keep it short
  - You can add a cover image (optional) in .png format. Size: 640x120px 
  - Plain text. This is the actual content of the news

Example: 

```
# Title

![image](https://user-images.githubusercontent.com/11541426/157123572-8339b3e1-c24d-45c1-94c1-7de66fbf129f.png)

If you believed they put a man on the moon
Man on the moon
If you believed there's nothing up his sleeve
Then nothing is cool
```

3. Edit `config.json` by adding details about the new post.

Example:
```
{
  "news": [
    {
      "path": "/news/my_first_news.md",
      "date": "04.09.2022",
      "link": "Read more" 
      "URL": "https://mywebsite.com/my_first_news.html"
    }
```
4. Go back to Console and refresh page (F5)

# Making next posts:
1. Inside of the `news` folder create new file: `my_second_news.md`. File name can be any
2. Edit the contents of the file as described above
3. Update `config.json` by adding info about new post to the top of the file

Example: 
```
{
  "news": [
    {
      "path": "/news/second.md",
      "date": "04.09.2022",
      "link": "Read more"  
      "URL": "https://mywebsite.com/my_second_news.html"
    },
    
    {
      "path": "/news/my_second_news.md",
      "date": "07.11.2022",
      "link": "Read more"  
      "URL": "https://mywebsite.com/my_first_news.html"
    }
  ]
}
```

### 🚨🚨🚨 IMPORTANT - news files should only contain content. Date, and URL for button should be placed in config.json 
