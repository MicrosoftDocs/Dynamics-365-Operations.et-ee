---
title: Kalendrid ja koondplaneerimine
description: Selles teemas antakse ülevaade tarneahela kalendritest ja nende mõjust koondplaneerimisele.
author: t-benebo
manager: tfehr
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c32957b0bd234ed14e6333a36a46c6a83ec2e91
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426281"
---
# <a name="calendars-and-master-planning"></a>Kalendrid ja koondplaneerimine

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade tarneahela kalendritest ja nende mõjust koondplaneerimisele.  Selgitatakse erinevaid koondplaneerimise mootoris kasutatavaid kalendreid, sh seda, kuidas need mõjutavad lähetus- ja vastuvõtukuupäevi planeeritud tellimustes. Ühtlasi antakse soovitused kalendrite määramise, kasutamise ja värskendamise kohta.

## <a name="definition-of-a-calendar"></a>Kalendri määratlus

Saate oma organisatsioonis kasutatava kalendri määrata lehel **Organisatsiooni haldus > Seadistus > Kalendrid > Kalendrid**. 

Iga kuupäevakirje kalendris võib olla **avatud**, **suletud** või **põhikalender**. See on määratud lehe **Tööajad** veerus **Juhtimine**. Iga kuupäeva puhul 
- **Avatud** – näitab, et tööd tehakse valitud päeval. Kalendrit värskendatakse vastavalt tööaja mallile.
- **Suletud** – näitab tööd, mida selle päeva jooksul ei tehta. 
- **Põhikalender** – näitab, et teatud kuupäev pärib tööajad ja avatud/suletud oleku põhikalendrist. Seetõttu pärib valitud kalender põhikalendri muutmisel sellest toiminguajad. 

Mis tahes suletud kuupäevade puhul on ruut **Komplekteerimiseks suletud** automaatselt märgitud. Avatud kuupäevade puhul saate suvandi **Komplekteerimiseks suletud** käsitsi valida. See näitab, et tööd tehakse kuupäeval, kuid lähetust ei toimu. 

## <a name="calendars-that-affect-master-planning"></a>Koondplaneerimist mõjutavad kalendrid

### <a name="calendar-for-a-coverage-group"></a>Laovarude grupi kalender
Laovarude grupp näitab antud laovarude gruppi kuuluvate kaupade täiendamiseks kasutatavate parameetrite ühist kogumit. 

Laovarude gruppi kalendri lisamiseks minge jaotisse **Koondplaneerimine > Seadistus > Laovarud > Laovarude grupid**. Leidke laovarude grupp, millele soovite kalendri määrata, ja seejärel valige see väljal **Kalender**.

Laovarude grupi saab määrata järgmistel lehtedel. 
    - Kauba lehel **Väljastatud toote üksikasjad**. Kauba laovarude grupi nägemiseks minge jaotisse **Tooteteabe haldus > Tooted > Väljastatud tooted** ja valige üksus, et avada leht **Väljastatud toodete üksikasjad**. Kauba laovarude gruppi saate vaadata kiirkaardil **Plaan**.
    - Lehel **Kauba laovarud**. Klõpsake väljastatud toodete üksikasjade lehel suvandit **Kauba laovarud**, et avada kauba laovarude leht. Ülevaate vahekaardil näete erinevaid täiendamise parameetreid olenevalt tegevuskohast, laost ja tootedimensioonidest. Iga kauba laovarude grupp päritakse laovarude grupist lehel **Väljastatud toote üksikasjad**. Selle saab tühistada, kasutades suvandit **Kasutuskohased sätted** või **Grupi sätete tühistamine** vahekaardil **Üldine**.
    - Lehel **Koondplaneerimise parameetrid**. Kui kaubale pole eelmistel lehtedel laovarude gruppi määratud, võtab koondplaneerimine üldise laovarude grupi, mis on määratud koondplaneerimise parameetrites. See seadistatakse jaotises **Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid** väljal **Üldine laovarude grupp**. 

### <a name="calendar-for-a-vendor"></a>Hankija kalender
Hankija tööpäevade näitamiseks saate määrata hankijale ostutellimuse kalendri hankija lehel **Ostutellimuse vaikesätted**. 

Hankija kalendri määramiseks peate looma kalendri jaotises **Organisatsiooni haldus > Kalendrid > Kalendrid**. Kalendri loomisel peate selle määrama hankijale. Minge jaotisse **Ostureskontro > Hankijad > Kõik hankijad** ja valige hankija, kellele soovite kasutatava kalendri määrata. Seejärel määrake hankija lehel kiirkaardil **Ostutellimuse vaikesätted** rippmenüü abil uus ostukalender. 

Hankija kalendris on näidatud päevad, millal ta aktsepteerib ostutellimuse esitamise, ja kuupäevad, millal ta saab tellimused teie ettevõttele tarnida. Seega on ostukalendriga hankija ostutellimuse tellimiskuupäevad kalendris avatuna määratletud kuupäevad. Nende tellimuste tarnekuupäevad on samuti avatud päevadel, mis mõjutab seega ostetud kauba täitmisaega. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Ostetud kauba täitmisaja määratlemine

Ostu täitmisaja (ja selle, kas arvesse võetakse ainult tööpäevi) määramiseks peate minema toote tellimuse vaikesätete lehele, valides suvandid **Tooteteabe haldus > Tooted > Väljastatud tooted** ja seejärel **Tellimuse vaikesätted**. 

> [!Note]
> Säte **Tööpäevad** ostutellimuse täitmisajas näitab hankija tööpäevi. Näiteks kalendri puhul, mille kohaselt tarne toimub ainult teisipäeviti, täitmisaeg on 10 päeva ja märkeruut Tööpäevad on valitud, võib kauba kättetoimetamiseks kuluda 10 nädalat (10 teisipäeva).
Seetõttu pole enamasti soovitatav valida ostutellimuse täitmisaegadeks tööpäevi.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Täitmisaegade määratlemine kaubanduslepete lehel

Koondplaneerimise saab seadistada kaasama kõiki hankijate kaubandusleppeid. Kaubanduslepped on fikseeritud hinnad või allahindluslepingud, mis on seadistatud ühe või mitme kliendi või hankija jaoks ühe või mitme toote müügiks või ostuks. Minge jaotisse **Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid** ja valige vahekaardil **Planeeritud tellimused** suvand **Leia kaubanduslepped**, et kaasata planeerimisel kaubanduslepped. Koondplaneerimine saab valida hankija parameetriga **Minimaalne täitmisaeg** või **Madalaim ühikuhind**.

### <a name="calendar-for-a-warehouse"></a>Lao kalender
Saate määrata kalendri laole, et näidata vastuvõtmiseks ja lähetamiseks avatud kuupäevi. Kui laole pole ühtki kalendrit määratud, on eelduse kohaselt kõik päevad avatud. 

> [!Note]
> Kalendri määramisel transiitlaole pole mingit mõju. Transiitladusid kasutatakse üleviimistellimuste toetamiseks. Tellimustele kohalduvad lähetus- või sissetulekukuupäevad määratletakse avatud päevadega lähtelaost ja sihtlaost ning tarneviisi kalendriga.

#### <a name="closed-for-pickup-policy"></a>Komplekteerimiseks sulgemise poliitika
Selleks et näidata, et ladu on vastuvõtmiseks avatud, kuid komplekteerimine pole võimalik, saate kasutada laokalendris suvandit **Komplekteerimiseks sulgemise poliitika**. See kehtib ka kliendi komplekteerimiste kohta. 

### <a name="transport-calendar"></a>Transpordigraafik 
Selleks et näidata kuupäevi, mis on saadaval üleviimistellimuste lähetamiseks **lähtelaost**, saate määrata **transpordikalendri**. Saate seadistada transpordikalendri tarneviisi või tarneviisi ja lähtelao kohta. Transpordikalender seadistatakse jaotises **Müük ja turundus > Seadistus > Jaotus > Tarneviisid**. Valige tarneviis ja klõpsake nuppu **Transpordikalender**.

Iga lao ja tarneviisi kohta saab luua rea ning kalender lisatakse veergu **Transpordikalender**. See määrab transpordikalendri, mida kohaldatakse, kui kaubad lähetatakse laost antud tarneviisi kasutades. Transpordikalendri kohaldamiseks kõigile saadetistele, mis kasutavad antud tarneviisi, saab rea luua ilma ladu määramata.  See mõjutab kõiki antud tarneviisi kasutavaid saadetisi olenemata laost. 

Kui ühtki transpordikalendrit pole määratud, on eelduse kohaselt kõik päevad transpordiks avatud.

### <a name="calendar-for-a-customer"></a>Kliendi kalender
Selleks et näidata kuupäevi, millal klient saab saadetisi vastu võtta, saate määrata kliendile sissetulekukalendri. Kui kalendrile pole ühtki kalendrit määratud, on eelduse kohaselt kliendile tellimuste kättetoimetamine võimalik kõigil päevadel. See mõjutab sissetuleku kuupäeva müügitellimuse ridadel. Kui valite müügitellimuse ridadel kuupäeva, mis ei ole kliendi kalendris avatud, näitab süsteem, et sissetuleku kuupäev on kehtetu. 

Pange tähele, et ühe kliendiga saab kaasata ainult ühe kalendri. Kui soovite kaasata kalendri kliendi igale aadressile, saate luua ühe kliendi aadressi kohta ja seejärel määrata sellele vastava kalendri. 

Nõutavat sissetulekukuupäeva müügitellimuse ridadel mõjutab kliendi kalender ja tarnekuupäeva määramisviis. Lisateavet varaseima tarnekuupäeva arvutamise kohta leiate teemast [Tellimuse lubamine.](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Juriidilise isiku lähetuskalender
Selleks et näidata kuupäevi, millal juriidiline isik saab kaupu lähetada, saate seadistada lähetuskalendri jaotises **Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud**. Valige juriidiline isik ja lisage kalender vahekaardi **Väliskaubandus ja logistika** väljal **Lähetuskalender**. Lähetuskalender toimib juriidilise isiku kõigi laokalendrite vaikesätete allikana. 

## <a name="how-calendars-affect-dates-in-planning"></a>Kalendrite mõju planeerimisele

### <a name="order-date-of-a-planned-purchase-order"></a>Plaanitud ostutellimuse tellimiskuupäev 
Plaanitud ostutellimuse tellimiskuupäev näitab kuupäeva, millal tellimus on esitatud. See on avatud kuupäev nii hankija kalendris kui ka laovarude grupi kalendris. Mõnikord on hankijatel vaja paari varupäeva ostutellimuse kättesaamise ja kaupade lähetamise vahel. Need kuupäevad on näidatud hankija varupäevades. Kui aga ostetud kaup määratakse laovarude grupile varupäevadel, tühistavad need varupäevad hankija varupäevad.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Plaanitud ostutellimuse tarnekuupäev
Ostu vastuvõtukuupäev näitab kuupäeva, millal saate kaubad kätte. See on kalendris avatud kuupäev. Kalendrid, mida võetakse arvesse, et näidata päevi, millal ostutellimusi on võimalik vastu võtta, on tähtsuse järjekorras järgmised (alates tähtsaimast). 
1. Hankija kalender
1. Laovarude grupi kalender
1. Vastuvõtva lao laokalender

Pange tähele, et laovarude grupi kalendri saab määrata erinevatel lehtedel ja nende tähtsusjärjestus on järgmine.
1. Kauba laovarude grupp lehel **Kauba laovarud**
1. Kauba laovarude grupp lehel **Väljastatud toodete üksikasjad**
1. Kauba laovarude vaikegrupp lehel **Koondplaneerimise parameetrid**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Plaanitud üleviimistellimuse lähetuskuupäev
Kahe lao vahel üleviimistellimuse loomisel kaasatakse lähetuskuupäev ja vastuvõtukuupäev üleviimistellimuse päisesse koos lähtelaoga ja sihtlaoga. Nende kahe kuupäeva vaheline erinevus on eeldatav transpordiaeg (päevades) ladude vahel.

Plaanitud üleviimistellimuse lähetuskuupäev näitab kuupäeva, millal kaubad lähtelaost lähetatakse. Saadaolevate lähetuskuupäevade määramiseks kasutatud kalendrite tähtsusjärjestus on järgmine. 
1. Lähtelao laokalender
1. Laovarude grupi kalender (vt selle kalendri taandejärjestust ülalt). Kui laokalender on määratud, on lähetuskuupäev kalendris avatud kuupäev. Kui laokalendrit pole määratud, kasutatakse laovarude grupi kalendrit. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Plaanitud üleviimistellimuse sissetulekukuupäev
Üleviimistellimuse sissetulekukuupäev näitab kuupäeva, millal kaubad sihtlaos vastu võetakse.

Sissetulekukuupäeva määramiseks kasutatud kalendrite tähtsusjärjestus on järgmine. 
1. Laovarude grupi kalender 
1. Sihtlao laokalender. Kui laovarude kalender on määratud, on sissetulekukuupäev kalendris avatud kuupäev. Kui laovarude grupi kalendrit pole määratud, kasutatakse laokalendrit. 

Plaanitud üleviimise lähetus- ja vastuvõtukuupäevade leidmisel võetakse arvesse ka kasutaja määratud varupäevi lähetamiseks ja vastuvõtmiseks. 

## <a name="using-calendars-in-master-planning"></a>Kalendrite kasutamine koondplaneerimises

### <a name="assignment-of-scm-calendars"></a>SCM-kalendrite määramine
Oluline on seada kalendrid tuvastama ettevõtte tööpäevi. Parim viis selleks on seada kalender iga elemendi puhul erinevate tööpäevadega. Teisisõnu kõik ettevõttega seotud välised kalendrid (klient, hankija) ja kõik sisemised (ladu, laovarude grupp ja tarneviis).

### <a name="recommendation-on-warehouse-calendars"></a>Soovitus laokalendrite kohta
Soovitatav on kasutada üht kalendrit lao kohta, et kaasata ainult kindlad ladu mõjutavad muudatused. Näiteks võivad kahel või enamal laol olla samad tööpäevad, kuid erinev komplekteerimispoliitika. Sel juhul on iga lao kalender koos selle vastava komplekteerimispoliitikaga süsteemi jaoks parim viis kaasata plaanitud ostu-, üleviimis- ja tootmistellimuste jaoks sobivaimaid kuupäevi. Kui ühtki laokalendrit pole määratud, saab laokalendri vaikesätete allikana kasutada juriidilise isiku kalendrit. 

### <a name="recommendation-of-coverage-group-calendars"></a>Soovitus laovarude grupi kalendrite kohta
Laovarude grupi kalendri puhul on oluline arvestada, et sellel on seoses koondplaneerimise vastuvõtukuupäevadega tühistamiskäitumine. Seetõttu on soovitatav seda kasutada ettevaatlikult. Eriti kasulik on see juhul, kui täiendamine tuleb teha kindlatel nädalapäevadel. 

### <a name="updating-scm-related-calendars"></a>SCM-iga seotud kalendrite värskendamine
On küll oluline määrata kõik asjaomased kalendrid vastavasse kohta (hankija, klient, ladu, tarneviis või laovarude grupp), kuid samavõrra tähtis on neid värskendada muudatuste kajastamiseks. Süsteem määratleb tootmis-, üleviimis-, ostu- ja müügitellimuste kuupäevad määratud kalendrite kombinatsiooni põhjal. Hea tava on selgitada, kes vastutab oma valdkonna kalendrite määramise ja värskendamise eest. Liigenduse või mis tahes muu ebatavalise muudatuse korral tööpäevades on oluline selle kohaselt kalendreid värskendada. Kõik kalendritest sõltuvad ülesanded, nagu koondplaneerimine ja tootmisgraafiku koostamine, tuleb pärast kalendrite värskendamist uuesti käivitada. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]