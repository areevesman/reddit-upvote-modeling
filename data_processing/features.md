### Original Features

- `created_utc`: the time (in seconds) when the comment was posted 
- `ups`: number of upvotes on the comment
- `subreddit_id`: id of the specific subreddit
- `link_id`: id of the particular comment thread
- `name`: name of the comment
- `score_hidden`: 1 if the score of the comment was hidden; 0 else
- `author_flair_css_class`: CSS class for the comment flair
- `author_flair_text`: flair text for the comment
- `id`: id of the comment (basically the same as comment name)
- `removal_reason`: reason a comment was removed (either `legal` or `None`)
- `gilded`: the number of gilded tags (~ premium likes) on the comment 
- `downs`: number of downvotes on the comment
- `archived`: if the thread was archived (no new comments, no new likes) 
- `author`: author's reddit username
- `score`: number of upvotes
- `retrieved_on`: The time (in seconds) when the comment was pulled to create the dataset. 
- `body`: the comment itself
- `distinguished`: the type of user on the page. Either `moderator`, `admin`, or `None`. 
- `edited`: whether (1) or not (0) the comment has been edited
- `controversiality`: a Boolean indicating whether (1) or not (0) a comment is controversial -- i.e., popular comments that are getting closely the same amount of upvotes as downvotes. 
- `parent_id`: the id of the comment that this comment was replying to. `None` if the comment is not a reply


### Benchmark v1 Features

- `time`: time comment was posted
- `time_lapse`: time since first comment on thread
- `hour_of_comment`: hour of day comment was posted
- `weekday`: day of week comment was posted
- `is_flair`: Whether or not there is flair text for the comment
- `is_flair_css`: Whether or not there is a CSS class for the comment flair
- `depth`: depth of comment in thread
- `parent_score`: score of parent comment (NaN if comment doesn't have a parent)
- `time_since_parent`: time since parent comment was posted
- `linked_sr`: subreddits linkecd d in the comment
- `linked_urls`: urls linked in the comment
- `no_of_linked_sr`: number of subreddits mentioned in the comment
- `no_of_linked_urls`: number of urls linked in the comment
- `subjectivity`: number of instances of "I"
- `is_edited`: whether or not the comment has been edited
- `is_quoted`: whether or not comment quotes another
- `no_quoted`: number of quotes in the comment
- `senti_neg`: negative sentiment score
- `senti_neu`: neutral sentiment score
- `senti_pos`: positive sentiment score
- `senti_comp`: compound sentiment score
- `word_counts`: Number of words in the comment


### Benchmark v2 Features

Scraped
- `url`: url of thread comment is on
- `num_comments`: number of comments on thread comment is on
- `over_18`: Whether or not the thread has been marked as NSFW
- `link_score`: upvotes of on thread comment is on
- `selftext`: selftext of thread if it exists
- `title`: title of thread
- `upvote_ratio`: The percentage of upvotes from all votes on the thread
- `link_ups`: number of upvotes on thread

Engineered from scraped data
- `link_created_time`: time thread was created
- `time_since_link`: time since the thread was created
- `is_root`: whether or the comment is a parent
- `is_selftext`: whether or not thread comment is on had selftext
- `parent_cos_angle`: consine similarity between comment and its parent comment's embeddings
- `title_cos_angle`: consine similarity between comment and its thread's title's embeddings

### Benchmark v3 Feautures
- `no_past_comments`: number of comments on thread before this comment was posted
- `score_till_now`: score of thread at the time this comment was posted
