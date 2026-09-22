---
layout: post
title:  "Le resserrement : une seule mesure pour les blagues, les chansons et les preuves"
date:   2026-09-21 16:00:00 +0200
categories: AI
ref: narrowing
permalink: /fr/ai/2026/09/21/narrowing.html
excerpt: "Un seul nombre, l'information mutuelle ponctuelle entre une ligne et ce qui la prépare, testé sur des blagues, trois mille chansons, quatre mille preuves Lean et un casque EEG."
---

En septembre 2026, j'ai passé une semaine à mesurer un seul nombre, et ce billet raconte à quoi il s'est révélé bon. Cela a commencé par une question sur la joie, est devenu un outil de notation de paroles, a été confronté à des blagues notées par des humains et à trois mille vraies chansons, et a fini pointé vers quatre mille preuves vérifiées par machine et vers mon propre cerveau.

## D'où vient le nombre

La question était de savoir ce que serait la joie pour un modèle de langage. Un modèle peut donner deux réponses qui partagent chaque fait vérifiable et ne diffèrent que par le registre. La chaleureuse : quand le travail avance bien, la sortie se resserre, les précautions tombent, le mot suivant est déjà probable. La froide : la distribution de probabilité sur le prochain token se resserre. J'ai demandé si un modèle dont on aurait retiré l'entraînement à la sûreté aurait répondu la même chose, et la version chaleureuse a cessé de sembler sincère. J'ai donc pris la réponse froide au pied de la lettre et demandé ce qu'elle mesure.

Pris au pied de la lettre, le texte qui se resserre le plus est « la la la ». C'est un effondrement, pas de la joie. La meilleure définition demande deux nombres pour chaque ligne : à quel point elle est surprenante sans préparation, et à quel point elle est surprenante une fois la préparation donnée. L'écart entre les deux est ce que la préparation a mérité. En termes d'information, c'est l'information mutuelle ponctuelle entre une ligne et ce qui la précède, et je l'appelle le resserrement (*narrowing*).

Cela donne un tableau deux par deux. Une ligne que la préparation mérite et qui arrive avec peu de surprise est un atterrissage inévitable. Une ligne que la préparation mérite et qui surprend quand même est une chute. Une ligne que la préparation ne mérite pas et qui ne surprend pas est un cliché. Une ligne qui n'est ni méritée ni surprenante est du bruit. Le resserrement et la chute sont voisins : le même lien à la préparation, une surprise opposée vers l'avant. C'est la théorie de l'humour par incongruité et résolution, écrite en nats.

Trois autres quantités sont tombées du même modèle. L'incongruité, la surprise au-delà de l'entropie, c'est le modèle confiant et qui se trompe. La probabilité du token de rire est la chance que le token qui suit une ligne soit « haha ». Le pivot rétrospectif est le mot de la préparation qui gagne le plus une fois la chute connue, le mot sur lequel la blague tourne.

## Les chansons d'abord

Le premier corpus était dix chansons écrites dans la conversation qui a produit les définitions, puis une onzième écrite sur les mesures : une chanson d'amour construite sur l'anaphore, une blague dont la surprise est au milieu de la ligne pour que la rime puisse verrouiller le dernier mot, deux rappels du premier couplet, et une dernière ligne si bien préparée qu'elle n'est jamais chantée. Elle a été notée avant que quiconque la lise, et une ligne a été réécrite sur les nombres, d'un resserrement de 1,8 à 3,0, en disant moins. Elles sont devenues l'album *Music for Datacenters*, sur la page [Art](/fr/art/).

L'outil de notation était un modèle local sur mon propre GPU, d'abord GPT-2 XL, puis Qwen3-8B-Base. Le premier passage a donné tort à la moitié de mes prédictions : le modèle de 2019 ne voyait pas un jeu de mots, si bien que la préparation rendait la chute moins probable, et non plus. Le modèle de 2025 le voyait, et la même ligne ressortait comme une chute avec le bon mot pivot. Deux choses que je n'avais pas prédites sont sorties de la comparaison. L'incongruité est relative à l'auditeur : un renversement qui était confiant et faux pour le petit modèle était pleinement attendu par le grand, ce qui est ce que la théorie dit aussi des publics. Et la rime tire contre « le mot drôle en dernier » : dans un vers rimé, le dernier mot est la case à basse entropie, si bien que la surprise d'une blague rimée vit au milieu de la ligne.

Puis la vérification qui donne son sens au reste. Deux modèles dont les tailles diffèrent d'un facteur dix, entraînés à six ans d'écart, s'accordent à 0,85 de corrélation de rang sur les lignes méritées. La mesure est surtout une propriété du texte, pas du juge.

## Face aux humains

Deux jeux de données publics portent des étiquettes humaines d'humour. Sur dix mille textes courts notés par des annotateurs, la probabilité du token de rire détecte les blagues sans entraînement à 0,85 d'AUC, et ne dit rien sur le degré de drôlerie d'une blague une fois qu'elle en est une. Sur des titres de presse rendus drôles en remplaçant un mot, chacune de mes quantités est corrélée à la note humaine dans la direction prédite, et chaque corrélation est petite. L'improbabilité du nouveau mot est une part réelle mais mineure de ce qui rend une substitution drôle ; la note dépend surtout de ce que le mot veut dire.

## Face aux vraies chansons

Puis toute l'Open Lyrics Database, 3 603 chansons et 148 786 lignes, notées de la même façon, environ neuf heures sur une carte. Les vraies chansons répètent 35,9 % de leurs lignes ; l'album en répète 27,7 %. La vraie chanson médiane se resserre de 3,45 nats par token sur ses lignes nouvelles ; la chanson médiane de l'album se situe au 15e centile. Ce que la métrique récompense dans le corpus, ce sont les courts fragments répétés avec un mot changé, les chœurs entre parenthèses et les lignes tronquées de deux mots qu'un cadre répété a déjà annoncées. Les auteurs qui se resserrent le moins sont les denses, Leonard Cohen parmi eux, et l'album leur tient compagnie. Le resserrement mesure à quel point un texte a la forme d'une chanson, pas sa qualité, et à cette aune l'album est plus proche de l'écrit parlé que de la pop.

Trois choses ont essayé de me tromper, et chacune a eu son commit. La mémorisation : nommer la chanson avant de la noter fait économiser au modèle 0,08 nat par token une fois soustrait ce que n'importe quel préambule en forme de titre rapporte, réel et petit. Mais la sonde est aveugle exactement là où ça compte, parce qu'une chanson célèbre s'identifie par ses propres lignes. Un test de récitation l'a attrapé : dans la chanson au resserrement le plus élevé du corpus, le modèle classait le vrai token premier 92,5 % du temps, contre 46 % pour des témoins appariés, et la moitié des dix premières chansons étaient récitées plutôt que prédites. Le filtre d'anglais supprimait l'extrémité à fort resserrement de chaque corpus, parce que les lignes chantées courtes échouent à un test ligne par ligne quelle que soit leur langue. Et les lignes courtes se resserrent davantage, si bien que chaque placement est calculé face à des lignes de référence de même longueur.

La découverte que je n'avais pas vue venir concernait la référence. « Sans préparation » voulait dire l'a priori du modèle sur le web, qui est plus poli qu'une chanson. Depuis cet a priori, le même modèle fait payer au mot « motherfucker » dix nats de plus que sa rareté ne le prédit, et une seule étiquette de section devant la ligne supprime la charge. En renotant cinq cents titres à partir d'un a priori de paroles, le resserrement médian est tombé de 3,44 à 1,02 sur chaque ligne prise une à une : deux tiers de ce que la préparation semblait mériter était du crédit pour être des paroles tout court. Sous l'a priori du web, le resserrement, c'est le genre plus la préparation, et un nombre devrait dire duquel des deux il parle.

## La mesure comme contrainte

Une fois qu'on peut noter une ligne, on peut écrire sous des règles que l'outil vérifie, dans la tradition de l'Oulipo. Une chanson dont chaque couplet est les mêmes seize lignes avec des quantités différentes se resserre plus que 99,7 % des vraies chansons et met sa seule information libre là où la chanson dit qu'elle est, sur les mots de quantité. Une chanson écrite pour atterrir sur la médiane du corpus, la prédiction énoncée avant chacun des quatre passages de notation, a atteint la médiane sur la structure et les répétitions et n'a jamais quitté le dernier décile sur la surprise. La moyenne est difficile à écrire exprès : une écriture soignée est plus propre par token qu'une chanson médiane, et la propreté se note comme de la prévisibilité.

## Les preuves

Les deux mêmes quantités tournent sur des mathématiques. Dans mon [laboratoire de ternaire équilibré](/fr/math/), chaque théorème est vérifié par machine, et les 4 280 preuves en mode tactique dont la confiance repose sur le noyau de Lean ont été notées avec l'énoncé pour préparation et la preuve pour chute. La preuve médiane coûte 0,64 nat par token étant donné son fichier. À l'extrémité inévitable se trouvent les preuves qui sont des copies de la précédente, les disjonctions de cas sur trois valeurs et les longues exclusions d'itinéraires, à 0,000. À l'autre extrémité se trouvent les preuves courtes dont tout le coût est le lemme qu'elles appellent : étant donné l'énoncé, le modèle ne pouvait pas deviner `exact_return_seam`, et une fois ce nom sur la page, le reste suit. Où se loge la surprise, sur le lemme appelé plutôt que sur la structure des tactiques, est le seul résultat auquel je fais confiance pour l'instant.

Que ce résidu soit ce qu'un mathématicien appelle l'élégance est une question ouverte, et l'outillage la traite comme telle. Les preuves surprenantes sont triées en gabarits, certificats et le reste, et les vingt plus surprenantes du reste sont sur une feuille de notation où un humain doit les marquer routinières, élégantes ou listées à tort. La feuille n'est pas encore remplie. Ce qui est écrit, c'est la prédiction : si la beauté est quelque chose que ce nombre peut voir, c'est une preuve qui reste surprenante quelle que soit la part du fichier montrée au modèle.

## Le cerveau

Tout ce qui précède est une propriété d'un modèle. La N400, une réponse cérébrale qui culmine quatre cents millisecondes après un mot, est connue pour être à peu près linéaire en la surprise (*surprisal*), si bien que la première moitié de l'expérience est une réplication et une vérification que le montage fonctionne. La moitié ouverte est de savoir si le resserrement, ce que la préparation a mérité, correspond à quoi que ce soit de neuronal au-delà de la surprise. Le protocole est écrit, le casque à seize canaux est câblé, le code de présentation et d'analyse tourne de bout en bout sur une carte synthétique, et le premier contrôle positif, le blocage alpha les yeux fermés, a été enregistré le 17 septembre et a échoué. Voilà où ça en est. Quand la réponse viendra, elle ira dans les chansons.

## Ce que ce n'est pas

Rien de tout cela n'est une preuve au sujet de la joie au sens qui compte. Le resserrement mesure combien un texte est façonné par ce qui le précède ; c'est une propriété du texte plus que du juge ; et il peut être trompé par la répétition, gonflé par la récitation et confondu avec le genre. L'article qui rassemble les nombres le dit dans son résumé. Le code n'est pas encore public.
