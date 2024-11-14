# Architecture
![architecture](https://github.com/user-attachments/assets/d2648ba4-8bb5-4b8c-b2b1-d89d79c4ee7f)

## Uitleg
### Syncroon
De drie Services kunnen met elkaar communiceren via OpenFeign op een syncrone manier.
#### US-8 + 9
De ReviewService stuurt een melding naar de PostService of de post in orde is of niet en geeft indien het niet in orde is een opmerking mee wat veranderd moet worden.

### Asyncroon
De drie Services kunnen zich aanmelden bij de eventbus door RabbitMQ.
#### US-7
Na het maken van een Post (US-1) wordt deze op de bus gezet zodat de ReviewService deze kan bekijken voor het goed of afkeuren hiervan.
#### US-10
Bij het plaatsen van een Comment wordt deze op de bus gezet zodat de PostService deze kan afhalen en toevoegen aan de Post.
