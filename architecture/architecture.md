# Architecture
![architecture](https://github.com/user-attachments/assets/d2648ba4-8bb5-4b8c-b2b1-d89d79c4ee7f)

## Uitleg
### Syncroon
De drie Services kunnen met elkaar communiceren via OpenFeign op een syncrone manier.
### Asyncroon
De drie Services kunnen zich aanmelden bij de eventbus door RabbitMQ.
