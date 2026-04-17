ProductBoard, $800/mois. Des agents IA, quelques centimes. Même résultat.

Sur Superproper, +300 feedbacks structurés en quelques semaines. Feature requests, bugs, retours terrain des équipes sales.

Sans système pour trier, prioriser et fermer la boucle, ça devient ingérable.

En relisant le tweet qui fait le buzz d'Andrej Karpathy sur le "LLM Wiki", j'ai réalisé qu'on applique le même concept depuis 4 mois.

L'idée : un LLM qui ne se contente pas de répondre à des questions, mais qui construit et maintient une base de connaissance persistante. Il ingère, structure, cross-référence.

Le bookkeeping, le truc chiant que tout le monde abandonne au bout de 3 semaines, coûte zéro effort avec un LLM.

Nous c'est pareil. Sauf que c'est pas un wiki. C'est notre base de feedbacks produit.

Concrètement ?

Un message arrive dans Slack. L'équipe CS discute (ou pas) du ticket dans le thread. Un agent ingère le tout et classe le feedback dans une arborescence de fichiers markdown.

Les branches de l'arborescence = les domaines fonctionnels du produit.
Les feuilles = les feedbacks individuels.

Il cross-référence avec les feedbacks similaires déjà existants. Réaction automatique sur le message Slack pour marquer "feedback enregistré".

Un autre agent fait le refinement. Impact x complexité. GO, DISCUSS ou REJECT.

Si discussion nécessaire, il poste dans un channel dédié avec le contexte technique et tag les bonnes personnes.

Et le meilleur : quand le dev est terminé, l'agent poste directement dans le thread Slack d'origine. "C'est déployé."

Le CS voit. Il relaye au client. Le client se sent écouté.

Ça, la plupart des outils de feedback ne le font pas. Cette boucle fermée, du message terrain jusqu'au "c'est en prod", sans qu'un humain fasse le passe-plat.

Le tout connecté en MCP. Slack et Chatwoot aujourd'hui. N'importe quelle source demain.

Un constat au passage : les boîtes avec une culture de l'écrit vont être massivement avantagées. Chaque thread Slack, chaque discussion structurée, c'est du contexte que les agents exploitent directement.

Le texte vaut de l'or. Les équipes qui écrivent bien alimentent des agents qui comprennent mieux, qui trient mieux, qui priorisent mieux.

C'est peut-être ça, la vraie "crise du SaaS" en 2026. Pas la fin des outils. Mais la capacité pour une équipe de cloner la partie utile d'un outil, adaptée exactement à son use case. Rapidement. Pour quasi rien.

Disclaimer : non, on n'a pas remplacé ProductBoard. On a cloné la partie dont on avait besoin, à notre échelle, pour notre use case. Si vous êtes 50 PMs avec 10k feedbacks/mois, c'est pas le même sujet (quoique). Mais si vous êtes une petite équipe produit qui hésite à prendre un outil cher et complet pour utiliser 20% des features, ça vaut le coup de se poser la question.
