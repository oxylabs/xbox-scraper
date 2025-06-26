# Xbox Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=xbox-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/Pds3gBmKMH)

Oxylabs' [Xbox Scraper](https://oxylabs.io/products/scraper-api/ecommerce/xbox?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Xbox website effortlessly. This brief guide showcases how Xbox Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Xbox results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Xbox page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.xbox.com/en-us/games'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/xbox-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n    <html lang=\"en\" dir=\"ltr\" data-platform=\"\">\n      <head>\n          <meta http-eq ... </html>",
      "created_at": "2024-02-20 12:15:29",
      "updated_at": "2024-02-20 12:15:31",
      "page": 1,
      "url": "https://www.xbox.com/en-us/games",
      "job_id": "7165680360011904001",
      "status_code": 200
    }
  ]
}
```
With our Xbox Scraper, you can seamlessly pull public data from any Xbox web page. Gather the necessary product details, including game statistics, user ratings, or game descriptions, to evaluate the gaming industry and remain ahead of your competitors. If you encounter any issues, reach out to our support team through live chat or send an email to us at hello@oxylabs.io.
