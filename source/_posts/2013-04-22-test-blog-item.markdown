---
layout: post
title: "Test blog item"
date: 2013-04-22 18:08
comments: true
categories: 
published: true
---

---
layout: post
title: "Spaces for multi-headed Drupal monsters"
date: 2012-12-21 23:30
comments: true
categories: [Spaces, Drupal 7, Fonkelbox, Presentation, Slides]
---
**Afgelopen woensdag (19 december, 2012) was er [Dinner with Drupal in Enschede](https://www.facebook.com/events/290101954443629). Er waren meerdere sessies, Bram Ten Hove beet het spits af en opende met een presentatie over de [Domain](http://drupal.org/project/domain) module. Daarna was mijn presentatie over de Spaces module en tot slot gaf Bart Feenstra een presentatie over geautomatiseerd testen.**

<!--more-->

Deze editie stond in het teken van multi-headed Drupal en, ter gelegenheid van Serious Request, van non-profits en goede doelen. Dit was mooi terug te zien in alle presentaties, enerzijds de multi headed oplossingen van Bram en mij, waarbij Bram sprak over het beheren van meerdere websites in één backend en ik sprak over interactieve groepen en anderzijds de presentatie van  Bart Feenstra over het testen en hoe dit de continuiteit kan garanderen voor de webprojecten van NGO's.

Nu volgt er een korte beschrijving van mijn presentatie, wanneer er van de andere presentatie linkjes beschikbaar zijn zal ik die hier ook plaatsen.

## De presentatie

### Introductie

Eerst een kleine introductie, ik ben Daniel Beeke, ik ben een drupal developer, ik werk bij Studio Fonkel in Barneveld. Ik werk inmiddels vijf jaar met Drupal. Ik heb een paar grote projecten gedaan en een aantal kleine. Ik ontwikkel voornamelijk aan de back-end. Intergraties, jQuery plugins en custom Drupal modules.

Een beetje over mezelf, ik kan soms wat impulsief zijn, flink wat koppig en ik hou ervan om me ergens in te verdiepen, dat is ook de manier waardoor ik Drupal heb geleerd.

Deze lezing geef ik om developers te motiveren spaces te onderzoeken. Het zal een klein beetje technisch zijn maar anderzijds zal de probleem stelling en de oplossing goed te begrijpen zijn voor niet-drupallers.  Het doel is dus motiveren. Ook zullen we aan de hand van een project waar ik mee bezig ben, kijken hoe je spaces in de praktijk gebruikt.

Wie kent open atrium? Spaces samen met og is de machine achter open atrium. Vandaag zullen we bespreken wat de mogelijkheden zijn van spaces, verder zullen we een use case bekijken en een demo doorlopen.

### Multi headed Drupal

Misschien wel toepasselijk op Drupal, wie heeft al eens een drie koppige draak met drupal willen bouwen?

Soms is er een moment dat je een Drupal site wilt opdelen in verschillende onderdelen, die ieder afzonderlijk eigen specifieke kenmerken heeft. Er zijn binnen de contributed meerdere modules die dit proberen op te lossen, sommige complex andere minder complex. 

Beschikbare oplossingen

*	og_features
*	domain
*	subdomain
*	dominion
*	multi install

Weet je er nog meer?

### Spaces
Vandaag wil ik kijken naar de spaces module, een handige module die je voor veel verschillende doeleinden kunt inzetten.

Je kunt er bijvoorbeeld een *paywall* mee maken of een *sociale groepen structuur met optionele functionaliteiten*. Het zorgt er voor dat het net is alsof je website een andere database heeft op bepaalde momenten. 
Die bepaalde momenten zijn de triggers/contexten. Een context kan bijvoorbeeld een organic group zijn, of het bekijken van een taxonomy term.

Ik zal eerst een praktijk voorbeeld laten zien, aan de hand daarvan zullen het door het concept heen lopen en uiteindelijk aan gekomen bij de techniek zullen we kijken hoe je dan zelf gebruik kunt maken van spaces in combinatie met og.
Spaces theorie

### Concept
De spaces module maakt het mogelijk om contextuele instellingen te gebruiken. In Drupal heb je bijvoorbeeld variabelen. Deze worden gebruikt om te bepalen wat de naam van de site is, wat het default theme is enzovoorts. Spaces kan wanneer er aangegeven wordt dat er een spaces context actief is (active space), alle API calls de contextueele setting geven in plaats van de site instellingen. Het is net als of spaces checkt of er een context actief is en snel een andere database aankoppelt.

In de werkelijke techniek gebeuren er een aantal andere truukjes, en komen er toch nog een paar kleine dingetjes bij kijken. Wanneer je bijvoorbeeld een view maakt zul je moeten aangeven dat er een spaces permissie op moet etc. Maar daar over straks meer. Laten we eerst eens naar een voorbeeld kijken.
Voorbeeld: Fonkelbox

### Fonkelbox

Fonkelbox is de werknaam van het project waar we bij Studio Fonkel mee bezig zijn. Op dit moment is het een set features die samen een organic groups functionaliteit bieden in combinatie met spaces.
Het wordt een installatie profile voornamelijk bedoelt voor organisaties. Specifiek organisaties met een community structuur. Het lijkt veel op open atrium. Het grote verschil van Fonkelbox is dat het wel een publieke voorkant heeft en daardoor prima kan dienen als een website voor een organisatie/vereniging. Publieke berichten worden aan de voorkant getoond, net als publieke evenementen en boeken etc. Prive berichten zitten netjes achter slot en grendel.
Momenteel hebben we drie soort gelijke projecten waardoor we konden beginnen aan dit project.

Toen ik begon met het programeren van Fonkelbox had ik eerst mijn twijfels over spaces, het leek een tikje complex. Nu ben ik er mee bezig gegaan en ben ik er heel erg enthoisiast over. 

Wel heb ik de documentatie goed doorgelezen waarna het duidelijk werd hoe het werkt. Een aantal dingen daarvan wil ik nog even laten zien:

Views spaces permissions,
dropbox access


<embed src="/images/multi-headed-drupal-spaces.svg"></embed>
*Je kunt in de presentatie klikken om naar de volgende slide te gaan ook werken de pijltjes.*