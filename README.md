# Windows Server DNS Monitoring
------

Ce dépôt contient une vue personnalisée pou l'Observateur d'évenemnts de Windows Server, permettent de surveiller les événements DNS
 critiques.

## Critères de surveillance
------
- 1) Ils proviennent de l'un des journaux suivants :

  ``Application, Security, Setup, System, ForwardedEvents.``
- 2) Leur ``ID`` d'événement doit être l'un des suivants :
    - **ID 2** : (Peut-être un événement spécifique lié à une ``erreur`` ou une ``situation dans un service particulier``).
    - **4** : (Un événement généralement lié à une ``erreur`` ou un ``problème plus grave``).
    - **409** : Cela pourrait être un événement relatif à des ``erreurs`` dans un ``service système ou des erreurs DNS spécifiques``.
    - **501-502** : (Plage d'événements indiquant des ``erreurs`` ou des ``avertissements qui peuvent être liés à des problèmes de                 réseau, de serveur, ou de services sur un serveur Windows``).
    - **6001-6002** : Cela peut faire référence à des événements du service DNS ou à des problèmes de configuration dans le système DNS.
