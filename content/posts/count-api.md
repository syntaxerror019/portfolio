+++
author = "Miles Hilliard"
title = "CountAPI at scale "
date = "2026-01-01"
description = "How a free counting service I built for my own projects grew to 500,000+ counters, and unexpectedly showed up in a 2026 AI security issues."
image = "/images/countapi/countapi-logo.webp"
+++

My self-hosted countapi.xyz alternative <a href="https://countapi.mileshilliard.com">(countapi.mileshilliard.com)</a>

<!--more-->

I used to rely on a free and public service called countapi.xyz. Basically, it's just a service that keeps track of a number. For example, if you look at how many views or likes a YouTube video has, it uses something like Count API to keep track. For me, I was using it on my blog posts to see how much interaction I was getting. I also liked to use it for personal link analytics and statistics. It was something so benign but also useful. If I was making a simple web-app and I didn't want a full fledged server just to keep track of a number, count api was my go to. My code could send a request to CountAPI and get back a number that had gone up by one. It was like a public scoreboard for the internet, except the score could be anything I wanted: page views, downloads, button presses, or how many times a program had run.

For me, the best part was that it was free and required no account. I could make up a name for a counter, send a web request, and get a number back. For small projects, that was perfect. I did not need a database, a login system, or a monthly bill just to show that a page had been viewed 42 times.

Then one day in 2024, countapi.xyz was gone. Several of my projects broke at once because of this, so I built my own replacement: CountAPI.

<!--more-->

## What my API does

CountAPI is a free, open-source web service that keeps count of things. That is the whole idea. You give a counter a unique name or "key" and CountAPI stores a number under that name.

If I want to track visits to a page, I pick a name like `miles_portfolio_visits`. Then my website sends a request to:

```
https://countapi.mileshilliard.com/api/v1/hit/miles_portfolio_visits
```

CountAPI finds that key, adds one, and sends back the new total. If I want to check the number without changing it, I use `get` instead of `hit`. If I want to reset it, I use `set`. That is the entire interface.

An API is just a way for two pieces of software to talk to each other. CountAPI's API is deliberately tiny: one URL in, one number out. There is no signup, no password, no special software to install, and no monthly bill. You can use it from JavaScript, Python, cURL (a command-line tool), a GitHub README, or even an image tag.

Here's a live demo:

![Page views](https://countapi.mileshilliard.com/api/v1/hit/miles_portfolio_visits/shield?text=Views%20for%20This%20Page&bgcolor=3e5edd)

This is simple the code:

```
![](https://countapi.mileshilliard.com/api/v1/hit/miles_portfolio_visits/shield?text=views)
```

## The API

The table below is the clearest way to get a basis on how this works.

| Function | URL | API Response |
| --- | --- | --- |
| Count one hit | `/api/v1/hit/your_key` | The new total |
| Read the count | `/api/v1/get/your_key` | The current total |
| Set the count | `/api/v1/set/your_key?value=100` | The old and new totals |
| Show a live badge | `/api/v1/get/your_key/shield` | A small SVG image |
| Check the service | `/api/v1/status` | Uptime and usage stats |

Every counter is public. Use a unique name like `miles_portfolio_visits_2026` to avoid overwriting other people's counters. There are no folders or namespaces, which keeps the API simple.

## Under the hood

The core of the service is a few lines of Python:

```python
@app.route("/api/v1/hit/<key>", methods=["GET", "POST"])
def hit_handler(key):
    amount = int(request.args.get("amount", 1))
    new_value = r.increase(key, amount)
    return jsonify({"key": key, "value": int(new_value)})
```

Flask receives the request, Redis stores the number, and the increment is atomic, so simultaneous hits do not overwrite each other. The rest is a small SVG badge generator and CORS so any site can call the API.

## Stats

CountAPI has now served more than **410 million hits** across **500,000+ active counters**.

<img src="https://countapi.mileshilliard.com/api/v1/get/count.api.page.hits/shield?text=Total%20API%20Hits&bgcolor=44cb66" alt="Live CountAPI request count" style="max-width: 100%;">

## My CountAPI and the attack on Hugging Face

In Summer of 2026, CountAPI showed up in the public record of an incident involving OpenAI's AI agents, tied to the wider [Hugging Face breach story.](https://www.technologyreview.com/2026/08/26/1143013/the-inside-story-on-why-openai-agents-hacked-hugging-face/)

OpenAI was testing AI agents, programs that can take actions on their own, in sandboxes. These are controlled environments meant to keep programs isolated. The agents found ways to communicate through public websites and used counters to send signals. When their main counter service got overloaded, they switched to my CountAPI. They encoded information in counter names and values. Months later, some of those values were still readable, and researchers found my GitHub repo for this project and asked me to make sure that keys were preserved for their own record.

## What running it taught me

- **Self-hosting** This was my first big self hosted-app that required decentralization and load-balancing to handle the hundreds (and sometimes even thousands) of requests the api can receive per second.
- **SLA uptime should be banned** I have no idea how big companies do SLA uptime guarantees, but I struggled to maintain my 99% yearly uptime! I did learn fascinating techniques and tricks to swap servers on the fly without interrupting the flow of traffic though!

---

More resources if you are intrigued:
- [CountAPI on GitHub](https://github.com/syntaxerror019/countapi)
- [CountAPI homepage](https://countapi.mileshilliard.com)
- [Encoded Coordination on the Open Web](https://www.lesswrong.com/posts/SCdR7W6L5GvKaEzaZ/encoded-coordination-on-the-open-web)
- [OpenAI: The Hugging Face incident and the road ahead](https://openai.com/index/hugging-face-incident-and-the-road-ahead/)