# Reddit Comment and Thread Datas

Around 260,000 threads / comments scraped from Reddit. Useful dataset for NLP projects.

## Quick Start

Scraped using [omega-red](github.com/linanqiu/omega-red)

The `.csv`s are named `<metareddit>_<subreddit>.csv`. The headers are described here and in `headers.txt`.

Headers are:

```
text,id,subreddit,meta,time,author,ups,downs,authorlinkkarma,authorkarma,authorisgold
```

- `text`: Text of the comment / thread
- `id`: Unique reddit id for the comment / thread
- `subreddit`: Subreddit that the comment / thread belongs to
- `meta`: Metareddit that the comment / thread belongs to. Subreddits belong to metareddits. A subreddit can be `leagueoflegends`. The metareddit for that subreddit would be `gaming`, which can also include the subreddit `dota2`
- `time`: UNIX timestamp of the comment / thread
- `author`: Username of the author of the comment / thread
- `ups`: Number of upvotes the comment / thread received
- `downs`: Number of downvotes the comment / thread received
- `authorlinkkarma`: The author's link karma. [What is Link Karma?](https://www.reddit.com/r/NoStupidQuestions/comments/2idfhk/what_is_link_karma/)
- `authorkarma`: The author's karma. [Reddit FAQ](https://www.reddit.com/wiki/faq) explaining karma.
- `authorisgold`: Boolean indicator for the gold status of the user. `1` for gold users, `0` for non-gold (normal) users. [Reddit FAQ](https://www.reddit.com/wiki/faq) explaining gold status.

## Original Texts

If you prefer the texts with punctuation, they are included (as the original output files from [omega-red](github.com/linanqiu/omega-red)) at [https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w](https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w)

### Threads

are in `/threads.csv` at [https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w](https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w)

Headers are:

```
'text', 'title', 'url', 'id', 'subreddit', 'meta', 'time', 'author', 'ups', 'downs', 'authorlinkkarma', 'authorcommentkarma', 'authorisgold'
```

- `text`: text of the thread
- `title`: title of the thread
- `url`: url of the thread
- `id`: unique ID of the thread
- `subreddit`: subreddit that the thread belongs to
- `meta`: meta tag assigned to the subreddit of the thread in `config.json`
- `time`: timestamp of the thread
- `author`: username of the author of the thread
- `ups`: number of ups the thread has received
- `downs`: number of downs the thread has received
- `authorlinkkarma`: the author's link karma
- `authorcommentkarma`: the author's comment karma
- `authorisgold`: `1` if the author has gold status, `0` otherwise

### Comments

are in `comments.csv` at [https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w](https://mega.nz/#F!NtsCGTgD!urXdXLJ6yITYdWEdWN-H1w)

Heades are (different from `threads.csv`)

```
'text', 'id', 'subreddit', 'meta', 'time', 'author', 'ups', 'downs', 'authorlinkkarma', 'authorcommentkarma', 'authorisgold'
```

- `text`: text of the comment
- `id`: unique ID of the comment
- `subreddit`: subreddit that the thread belongs to
- `meta`: meta tag assigned to the subreddit of the thread in `config.json`
- `time`: timestamp of the thread
- `author`: username of the author of the thread
- `ups`: number of ups the thread has received
- `downs`: number of downs the thread has received
- `authorlinkkarma`: the author's link karma
- `authorcommentkarma`: the author's comment karma
- `authorisgold`: `1` if the author has gold status, `0` otherwise

All text is normalized to lower case, tokenized using a TreebankTokenizer from [natural](https://github.com/NaturalNode/natural), then joined with spaces. This results in punctuation being separated from words, a desired effect.

---

The MIT License (MIT)

Copyright (c) 2016, Linan Qiu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
