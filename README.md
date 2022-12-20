# Twitter time data collection and sentiment analysis

**Stack:**  `TwitterAPI + Flask + Nameko + Postgresql + Textblob`

## Objective

1. A POST request is received with instructions on which Twitter accounts to gather.
2. Following that, it establishes a socket connection with the Twitter API and begins to ingest real-time Twitter data.
3. TextBlob used to assign a sentiment score to each tweet.
4. A PostgreSQL database is then used for all data.

### Example of POST request json

```json
{
"duration": 60,
"query": ["America", "BTC", "Cryptocurrency"],
"translate": false
}
```

## Set up

1. Clone or download this repository
2. Create virtual environment and install dependencies
3. Setup PostgreSQL
4. Get your Twitter credentials [You can get your Twitter credentials here](https://apps.twitter.com)
5. Install RabbitMQ:
6. Start RabbitMQ: `sudo rabbitmq-server`
7. Start Nameko: `nameko run service --config ./config.yaml`
8. Run Flask (in a different terminal): `python app.py`
