import praw

reddit=praw.Reddit(client_id='',
                  client_secret='',
                  username='BobaDayBot',
                  password='',
                  user_agent='bobaDayBot1.0')

subreddit=reddit.subreddit('food')
for post in subreddit.hot(limit=15):
  for comment in post.comments:
    if hasattr(comment,'body'):
      comment_lower=comment.body.lower()
      if ' boba ' or ' bubble tea ' in comment_lower:
        print(comment.body)
        print('----------------------')
        comment.reply('Do you know bubble tea day? 4/30 is national bubble tea day in the US!')
