# Telegram bot API

Local Telegram bot API using an **unofficial** Docker image by [aiogram](https://github.com/aiogram/telegram-bot-api).

## Prerequisites

### Docker

Create a network for the container:

```bash
sudo docker network create telegram-bot-api
```

Create volumes for the container:

```bash
sudo docker volume create telegram-bot-api-data && sudo docker volume create telegram-bot-api-temp
```

### Telegram

Go to your [account](https://my.telegram.org) on the Telegram website and create an application in the **API development tools** section.

## Configuration

| **Name**                           | **Required** | **Default** | **Description**                                                                  |
| ---------------------------------- | ------------ | ----------- | -------------------------------------------------------------------------------- |
| `TELEGRAM_API_ID`                  | Yes          | —           | Numeric application identifier for Telegram API access                           |
| `TELEGRAM_API_HASH`                | Yes          | —           | Application hash for Telegram API access                                         |
| `TELEGRAM_HTTP_PORT`               | No           | `8081`      | Port on which your bot API will run                                              |
| `TELEGRAM_LOCAL`                   | No           | `1`         | Allow the bot API server to handle local requests                                |
| `TELEGRAM_MAX_WEBHOOK_CONNECTIONS` | No           | `100`       | Maximum simultaneous webhook connections per bot                                 |
| `TELEGRAM_MAX_CONNECTIONS`         | No           | `100000`    | Maximum number of open file descriptors                                          |
| `TELEGRAM_VERBOSITY`               | No           | `1`         | Log verbosity level (0 — minimum, 10 — maximum)                                  |
| `TELEGRAM_PROXY`                   | No           | —           | HTTP proxy server for outgoing webhook requests in the format `http://host:port` |
