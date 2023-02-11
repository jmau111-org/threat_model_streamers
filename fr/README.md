#  Modèle de menace simplifié pour les streameurs

Menaces sur les streameurs et moyens efficaces de les mitiger 🧢

[Lire la version anglaise](https://github.com/jmau111-org/threat_model_streamers)

## C'est quoi un modèle de menace

Grosso modo, il s'agit d'adapter les mesure de sécurité à sa situation pour protéger quelque chose de valeur, ce qui n'est pas toujours lié à des problématiques d'argent mais c'est tout de même souvent le cas.

Par example, un utilisateur lambda n'aura pas le même modèle de menace qu'un hacktiviste, ou même un chercheur en sécurité car ses activités peuvent être considérées comme bien moin sensibles.

**Les streameurs sont particulièrement dans le colimateur** en 2023, et c'est encore plus vrai pour les têtes de gondole qui touche un large public (milliers voire centaines de milliers de viewers/abonnés).

Mais même quelques centaines d'abonnés "seulement" sont suffisants pour devenir une cible de premier choix.

## Avertissement

Ce guide simplifié a pour but de vulgariser la notion et ne prétend pas parler avec autorité sur le sujet.

## Pas à pas

### C'est quoi un "streameur" ?

Une personne qui diffuse en temps réel (le fameux streaming) ses parties de jeux vidéos. Les plateformes de référence sont Twitch et YouTube.

Beaucoup d'appelés, très peu d'élus. Le secteur est ultra-concurrentiel. Une élite de streameurs tire son épingle du jeu néanmoins et peut en vivre correctement (voire confortablement dans les meilleurs cas). En général, les grosses têtes d'affiches sont déjà connues pour autre chose (YouTubeurs, artistes, politiques, etc) mais certains arrivent à "percer" uniquement par leurs compétences de jeu.

[Inspiration: computerhope](https://www.computerhope.com/jargon/s/streamer.htm)

### 7 scénarios catastrophe

* les attaquants hackent le compte et suppriment des contenus, ce qui peut faire perdre beacoup d'argent à la victime
* les pirates "leakent" (révèlent publiquement) des données personnelles concernant la victime (PII)
* une attaque par déni de service est lancée contre la connection sans fil de la victime (pas de stream, pas de chocolat)
* la cible est hackée pour diffuser un malware/spyware à sa communauté
* l'objectif n'est pas vraiment la chaîne en elle-même mais plutôt le "merch" (merchandizing) ou d'autres services associés, car ce modèle de business est assez courant chez les streameurs
* la cible est attaquée par un groupe de pirates dans un but politique pour diffuser un message ou un manifeste (assez improbable mais pas impossible)
* l'attaque vise toute la plateforme et non une personne en particulier (très rare, mais souvenez-vous des [Twitch leaks sur 4chan](https://arstechnica.com/information-technology/2021/10/twitch-admits-to-major-leak-exposing-source-code-creator-earnings/))

### 7 techniques d'attaque connues

Parmi les plus crédibles:

* phishing ou spear phishing (phishing plus ciblé)
* envois de code malicieux via les forums et autres chats (cela peut être hors plateforme, comme un site auto-hébergé)
* appels téléphoniques directs si le numéro est leak ou repéré
* attaque par ingénierie sociale sur un collaborateur (ex: community managers, associés) 
* attaque sur les applications servant au merchandizing (encore plus probable si le site est géré/développé par l'équipe de la victime ou juste elle, et non une plateforme reconnue et sécurisée)
* si l'accès est établi sur les machines contenant des documents importants comme la production vidéo, on peut s'attendre à du rançongiciel, des RATs (Remote Access Trojans), ou des reverse shells
* déni de service sur la connection sans fil de la victime si son adresse est repérée et que son installation est vulnérable (les plateformes ont en général des systèmes anti-DDoS mais c'est plus rare à domicile)

### 7 protections qui marchent vraiment

* 2FA/MFA (authentification double/multi-facteurs) partout et pour tous les collaborateurs: via une app ou, encore mieux, une clé de sécurité. Même si le SMS est le moins sécurisé, c'est toujours 10 fois mieux que sans!
* un gestionnaire de mots de passe pour générer et auto-compléter des mots de passe **longs et aléatoires** sur les différents comptes. Eviter le cas du mot de passe réutilisé qui ouvre toutes les portes!
* stratégie de sauvegarde des données efficace **et surtout testée** (peut nécessiter un budget)
* vigilance sur les réseaux pour éviter l'OSINT de base ou plus avancé, ou d'autres techniques d'ingénierie sociale
* navigateur sécurisé avec bloqueur de pubs et l'extension [uBlock origin](https://ublockorigin.com/) activée
* système d'exploitation **et** applications/logiciels à jour
* appareils sécurisés: ne pas connecter n'importe quel object connecté car certains n'ont même pas de cryptage

Ne pas oublier [la short list](#short-list)!

### Menaces complétement sous-estimées

### Santé mentale

**Harcèlement en ligne**: propos haineux, moqueries systématiques, mais également commentaires inappropriés. Certes, les plateformes proposent des systèmes de modération et même de banissement pour les petits malins qui voudraient tester les limites, mais cela peut se contourner assez facilement, notamment via d'autres réseaux sociaux.

Prendre régulièrement des pauses et des vacances peut sembler un luxe pour certaines victimes mais le cerveau humain n'est juste pas conçu pour endurer autant de pression (constante stimulation, _a fortiori_ si c'est du "concentré de négativité").

### Propriété Intellectuelle

Tout ce qui est droit de la propriété intellectuelle et autres DMCA est à connaître sur le bout des doigts. Les contenus se font régulièrement signaler/réclamer par les ayants droit. Certaines boîtes ont même un service dédié pour ça.

Les streameurs ont aussi des droits sur leurs propres contenus. Le plagiat et les techniques qui consistent à "sampler" abusivement les contenus des créateurs, pour les dénigrer ou générer des revenus publicitaires sur leurs dos, peuvent être attaquées en justice ou au moins auprès de la plateforme de diffusion.

Attention car le droit à la critique existe aussi, et il est légal de reprendre un contenu streamé pour le critiquer ou le présenter, ce qui laisse une faille à certains pour y glisser des formes de harcèlement plus subtiles mais tout aussi dangereuses, voire plus.

### Short list

* ne pas utiliser son vrai nom mais un pseudo (mais ça deviendra compliqué à maintenir pour les personnes les plus connues)
* utiliser un email **dédié** au compte de stream
* prioriser les plateformes les plus robustes pour le "merch" (ex: Shopify, Squarespace) même si leurs commissions/frais d'abonnement peuvent être salés
* **paiements sécurisés** voire plans professionels/business pour les plateforme type Paypal
* sécurité des publications: supprimer les data EXIF des documents, en particulier les photos car toutes les plateformes ne le font pas automatiquement, et éviter d'exposer les proches ou les rayer au marqueur noir (éviter les floutages hasardeux qui sont parfois réversibles)
* ne pas divulguer une adresse physique ou sa ville (même si compliqué pour les streameurs les plus en vue)
* avoir une connexion internet solide et sécurisée (ça peut coûter un peu mais une connexion foireuse amène plus de risques)
* utiliser un VPN en permanence pour masquer l'IP publique, surtout celles et ceux qui s'aventurent sur des tchats _alternatifs_
* protection de la vie privée pour éviter un bad buzz lié à d'autres activités sur Internet...
