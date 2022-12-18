# PizzaPlace GitCord

> [This is an updated fork of the original version by Promise Solutions.](https://github.com/biaw/gitcord-forum)

![PizzaPlace Banner](https://raw.githubusercontent.com/PizzaPlace/assets/main/PizzaPlaceBannerButSmaller.png)

## What is this?

This is a middleware that forwards all (or some) GitHub events to a Discord forum post, it allows for a more streamlined way of communicating changes with your community.

## How do I use it?

Simply set up a webhook on your GitHub repository, and set the URL to your Cloudflare Worker route. You'll also need to set a secret, which will be used to verify the request. [You can get a randomly generated secret here.](https://generate-secret.vercel.app/32).

## How do I set it up?

Run the following command in your terminal:

```bash
wrangler publish
wrangler secret put GITHUB_WEBHOOK_SECRET
wrangler secret put DISCORD_WEBHOOK
```

## How do I set up the webhook?

Go to your repository's settings, and click on the "Webhooks" tab. Click "Add webhook", and set the URL to your Cloudflare Worker route. Set the secret to the one you generated earlier. Set the content type to `application/json`, and select some of the event options, or if you want a clean feed select 'Just the push event'.

## Credits

Thanks to the Promise Solutions team for the original version of this project.
