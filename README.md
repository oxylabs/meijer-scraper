# Meijer Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs' [Meijer Scraper](https://oxylabs.io/products/scraper-api/ecommerce/meijer?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Meijer website effortlessly. This brief guide showcases how Meijer Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Meijer results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Meijer page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.meijer.com/grocery-snacks/c/1001'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/meijer-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\" style=\"overflow: visible;\"><head class=\"at-element-marker\"><script ty ... </html>",
      "created_at": "2024-02-20 12:32:30",
      "updated_at": "2024-02-20 12:33:07",
      "page": 1,
      "url": "https://www.meijer.com/grocery-snacks/c/1001",
      "job_id": "7165684640173271041",
      "status_code": 404
    }
  ]
}
```
With our Meijer Scraper, you can seamlessly gather public data from any Meijer web page. Gather critical grocery information like price, customer reviews, or product descriptions to understand the market and stay a step ahead of your competitors in the grocery business. If you have any questions, our support team is ready to help. Reach out to us via live chat or email us at hello@oxylabs.io.
