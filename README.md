# Capterra Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Capterra Scraper](https://oxylabs.io/products/scraper-api/web/capterra?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Capterra website effortlessly. This brief guide explains how an Capterra Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Capterra results by providing your own URLs to our service. We can return the HTML for any Capterra page you like.

#### Python code example

The example below illustrates how you can get HTML of Capterra page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.capterra.com/categories/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/capterra-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": " ... </html>",
      "created_at": "2023-12-18 11:09:47",
      "updated_at": "2023-12-18 11:10:00",
      "page": 1,
      "url": "https://www.capterra.com/categories/",
      "job_id": "7142471001849260033",
      "status_code": 613
    }
  ]
}
```
With our Capterra Scraper, you can easily extract public data from any Capterra web page. Gather the necessary software details, such as feature lists, customer ratings, or vendor information, to gain a competitive edge in your market research. If you need assistance, our support team is ready to help through live chat or you can email us at hello@oxylabs.io.