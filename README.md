# [<img src="https://s3.internetdata.io/internetdata-public/brand/mark.svg" alt="InternetData" height="28"/>](https://internetdata.io/) InternetData Cloudflare Worker

[![release](https://img.shields.io/github/v/release/internetdata/cloudflare-plugin)](CHANGELOG.md)
[![license](https://img.shields.io/github/license/internetdata/cloudflare-plugin)](LICENSE)

The official [InternetData](https://internetdata.io) Worker for Cloudflare looks up every visitor at Cloudflare's edge, on any plan, and passes the answer to your site.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/internetdata/cloudflare-plugin)

## Getting Started

1. Create an API key in the [InternetData console](https://app.internetdata.io).
2. Click **Deploy to Cloudflare** above. Cloudflare copies this repository into your GitHub or GitLab account, asks for your API key, and deploys the Worker.
3. In the Cloudflare dashboard, open **Workers & Pages**, select **internetdata**, then **Settings** > **Domains & Routes** > **Add** > **Route**. Pick your zone, enter `example.com/*` with your own domain, and select **Add route**.

Every request on the route then reaches your site with the answer in the `X-InternetData` header, as JSON. The Worker deletes any copy of the header a visitor sends, so your site can trust it.

## What it sends

The Worker calls the InternetData API at `https://api.internetdata.io` with your API key and the visitor's IP address.

## About InternetData

Geolocation, anonymity, ownership, network, service and domain data for any IP address, AS or domain, by API or as databases you download.

[<img src="https://s3.internetdata.io/internetdata-public/brand/mark.svg" alt="InternetData" height="64"/>](https://internetdata.io/)

## License

This project is licensed under the [MIT License](LICENSE).
