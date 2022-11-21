---
title: Varude nähtavuse rakendus
description: See artikkel kirjeldab, kuidas kasutada varude nähtavuse rakendust.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9886ddbf0b072283cffd73d4bfdc20835ccb3b7c
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762696"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility rakenduse kasutamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas kasutada varude nähtavuse rakendust.

Varude nähtavus annab visualiseerimiseks mudelipõhise rakenduse. Rakendus sisaldab kolme lehekülge: **Konfiguratsioon**, **Operatiivne nähtavus** ja **Varude kokkuvõte**. Sellel on järgmised funktsioonid.

- See annab kasutajaliidese (UI) vaba kaubavaru konfigureerimiseks ja esialgse reserveerimise konfigureerimiseks.
- See toetab reaalajas vaba kaubavaru päringuid eri dimensioonide kombinatsioonide kohta.
- See annab kasutajaliidese reserveerimistaotluste sisestamiseks.
- See annab vaate toodete vabast kaubavarust koos kõigi dimensioonidega.
- See annab vaate toodete vabast kaubavarust koos eelmääratletud dimensioonidega. Vaba kaubavaru loendi vaade võib olla kas täielik või eellaaditud tulemus vaba kaubavaru päringust.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist installige ja seadistage Inventory Visibility lisandmoodul, nagu on kirjeldatud jaotises [Inventory Visibility installimine ja seadistamine](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a> Ava ja autendi varude nähtavuse rakenduse

Varude nähtavuse rakenduse avamiseks ja autentimiseks järgige neid samme.

1. Logige oma keskkonda Power Apps sisse.
1. Avage varude **nähtavuse** rakendus.
1. Avage vasakul **paanil** töö nähtavuse leht.
1. Valige lehe **ülaosas** nupp Sätted (käigu sümbol).
1. Dialoogiboksis Sätted sisestage kliendi ID, rentniku **ID** **ja kliendi salaväärtused,** **·** **mille märkisite varude nähtavuse installimisel ja häälestamisel.**[...](inventory-visibility-setup.md)
1. Valige värskendamisnupp **välja** **"BearerKen"** kõrvalt. Süsteem loob sisestatud teabe põhjal uue kandja loa.

    ![Vaba kaubavaru päringu sätted.](media/inventory-visibility-query-settings.png "Vaba kaubavaru päringu seaded")

1. Kui saate kehtiva kandjaluba, sulgege dialoogiaken. Kandja luba aegub mõne aja pärast. Seetõttu peate seda aeg-ajalt värskendama, kui peate värskendama konfiguratsiooni, sisestama andmeid või päringu andmeid.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a> Varude nähtavuse rakenduse konfigureerimine

Varude **nähtavuse** rakenduse konfiguratsioonileht aitab seadistada üldise andmehalduse konfiguratsiooni ja funktsioonikonfiguratsiooni. Pärast lisandmooduli installimist sisaldab vaikekonfiguratsioon Microsoft Dynamics 365 Supply Chain Management vaikeseadistust (`fno` andmeallikas). Vaikesätet on võimalik üle vaadata. Hiljem vastavalt teie äritegevuse nõuetele ja välissüsteemi lao sisestusnõuetele saate muuta konfiguratsiooni nii, et see standardiseeriks varude muudatuste sisestamis-, korraldamis- ja päringute viise läbi mitme süsteemi.

Lahenduse konfigureerimise täielikud üksikasjad leiate jaotisest [Inventory Visibility konfigureerimine](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Töö nähtavus

Töö **nähtavuse** leht annab reaalajas vaba kaubavaru päringu, reserveerimise sisestamise ja eraldamise tulemused, mis põhinevad erinevatel dimensioonide kombinatsioonil. Kui funktsioon *OnHandReservation on* sisse [lülitatud](inventory-visibility-configuration.md), saate sisestada reserveerimistaotlusi ka töö nähtavuse **lehelt**.

### <a name="on-hand-query"></a>Vaba kaubavaru päring

Töö **nähtavuse lehe** vaba päringu **vahekaart** võimaldab teha päringuid reaalajas vaba kaubavaru kohta. Päringu häälestamiseks ja käivitamiseks järgige neid samme.

1. Avage varude **nähtavuse** rakendus.
1. Avage vasakul **paanil** töö nähtavuse leht.
1. VahekaardilE **Onhand sisestage** Organisatsiooni **ID,** saidi ID **ja** asukoha ID väärtused **,** mida soovite teha.
1. Sisestage **väljale Toote ID** üks või mitu toote ID-d, et saada oma päringule täpne vaste. Kui jätate toote **ID** välja tühjaks, kaasatakse tulemustesse kõik määratud saidi ja asukoha tooted.
1. Granulaarse tulemuse saamiseks (nt dimensiooniväärtuste kaupa nt värv ja suurus) **valige grupeerimise dimensioonid väljal Grupeerimise tulem alusel**.
1. Kindla dimensiooniväärtusega (nt värv = punane) **kaupade** otsimiseks valige dimensioon väljal Filtreeri dimensioonid ja sisestage seejärel dimensiooni väärtus.
1. Saate valida **päringu**. Saate kas edusõnumi (roheline) või nurjunud (punane) sõnumi. Kui päring nurjub, kontrollige oma päringukriteeriume ja veenduge [, et teie](#open-authenticate) kandja tõend on aegunud.

Teine võimalus vaba kaubavaru päringu loomiseks on teha otse API-taotlusi. Saate kasutada kas ühte `/api/environment/{environmentId}/onhand/indexquery` või.`/api/environment/{environmentId}/onhand` Lisateavet vt varude nähtavuse avalikud [API-d](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Reserveeringu sisestamine

Kasutage reserveerimistaotluse **sisestamiseks** vahekaarti **Töö nähtavuse** sisestamine. Enne kui saate reserveerimistaotluse sisestada, peate lülitama sisse funktsiooni *OnHandReservation*. Lisateavet selle funktsiooni ja selle sisselülitamis kohta vt varude nähtavuse [reserveeringutest](inventory-visibility-reservations.md).

> [!NOTE]
> Võimalus teha täiustatud reserveerimist kasutajaliidese kaudu on mõeldud selleks, et lasta teil katsetada oma funktsiooni. Iga pehme reserveerimistaotlus peab olema seotud kande tellimuse rea muudatusega (loomine, muutmine, kustutamine jne). Seetõttu on soovitatav teha vaid kergeid reserveeringuid, mis on lingitud tagatellimusega. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md).

Järgige neid samme, et sisestada täiustatud reserveerimistaotlus kasutajaliidese abil.

1. Avage varude **nähtavuse** rakendus.
1. Avage vasakul **paanil** töö nähtavuse leht.
1. **Määrake vahekaardi Reserveerimise** sisestamine väljal **Kogus** kogus, mida soovite kergeks reserveerida.
1. Tühjendage **ruut Luba negatiivne laovaru, et** toetada ülemüüdmist, et vältida lao üle- või reserveerimist.
1. **Väljal Operaator** valige andmeallikas ja füüsiline mõõt, mida rakendada soft-reserved kogusele.
1. Sisestage **organisatsiooni ID**, **saidi ID**, asukoha **ID** ja toote ID väärtused **,** mida soovite teha.
1. Granulaarse tulemuse saamiseks valige andmeallikas, dimensioonid ja dimensiooniväärtused.

Teise võimalusena kerge reserveerimise sisestamiseks on teha otsesed API-taotlused. Kasutage mustrit, mida kirjeldatakse jaotises [Ühe reserveerimissündmuse loomine](inventory-visibility-api.md#create-one-reservation-event). Seejärel valige **Sisesta**. Taotluse vastuse üksikasjade vaatamiseks valige suvand **Kuva üksikasjad**. Samuti saate `reservationId` väärtuse vastuse üksikasjadest.

### <a name="allocation"></a>Eraldamine

Lisateavet kasutajaliidesest ja API-dest eralduste haldamise kohta vt varude nähtavuse [varude eraldamine](inventory-visibility-allocation.md).

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Varude kokkuvõte

Varude **kokkuvõtte leht** annab koos kõigi dimensioonidega toodete lao kokkuvõtte. See on kohandatud vaade varude vaba *summa üksuse* jaoks. Lao koondandmed sünkroonitakse perioodiliselt laovarude nähtavuse väljalt.

Varude kokkuvõtte lehe **lubamiseks ja** sünkroonimise sageduse miseks järgige neid samme.

1. Avage lehekülg **Konfiguratsioon**.
1. Avage vahekaart **Funktsioonihaldus >** Sätted.
1. Seadke funktsiooni **OnHandMostSpecificBackgroundService tumblerlüliti** väärtusele *Jah*.
1. Kui see funktsioon on lubatud, **·** **muutub teenuse konfigureerimise jaotis kättesaadavaks ja sisaldab rida OnHandMostSpecificBackgroundService’i** funktsiooni konfigureerimiseks. See säte võimaldab teil valida sageduse, millega lao koondandmed sünkroonitakse. Kasutage veeru **Väärtus** nuppu **üles** ja **alla,** et muuta sünkroonimiste vahelist aega (mis võib olla kuni 5 minutit alla). Seejärel valige nupp **Salvesta**.

    ![Teenuse OnHandMostSpecificBackgroundService säte](media/inventory-visibility-ohms-freq.png "Teenuse OnHandMostSpecificBackgroundService säte")

1. Valige **kõigi muudatuste** salvestamiseks suvand Värskenda konfiguratsiooni.

> [!NOTE]
> Funktsioon *OnHandMostSpecificBackgroundService* jälgib ainult vaba kaubavaru muudatusi, mis ilmnesid pärast funktsiooni sisse lülitamist. Nende toodete andmeid, mis pole muutunud, kuna te funktsiooni sisse lülitasite, ei sünkroonita laoteenuse vahemälust keskkonda Dataverse. Kui teie **varude** kokkuvõtte leht ei näita kogu eeldatavat vaba kaubavaru teavet, avage tarneahela haldus, **minge varude haldusse > Perioodilised ülesanded >** Varude nähtavuse integreerimine, keelake pakett-töö ja keelake see uuesti. See käivitab algse tõuke ja kõik andmed sünkroonitakse *üksusega Varude OnHand Sum* järgmise 15 minuti jooksul. Kui soovite kasutada funktsiooni OnHandMostSpecificBackgroundService *, soovitame selle enne vaba kaubavaru muudatuste tegemist sisse lülitada ja lubada varude nähtavuse* integreerimise pakett-töö **.**

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a> Sujuva kaubavaru päringu eellaadimine

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Tarneahela haldus talletab palju teavet teie praeguse vaba kaubavaru kohta ja muudab selle kättesaadavaks mitmesugustel eesmärkidel. Mitme igapäevaste operatsioonide ja kolmanda osapoole integratsioonide puhul on nende üksikasjade alamkogumiks vaja vaid väike alamkogum ning süsteemist kõigi kohta päringute tegemiseks võib tulemuseks olla suured andmekomplektid, mille koostamine ja ülekandmine võtab aega. Seetõttu saab laovarude nähtavuse teenus perioodiliselt tuua ja talletada laoseisu andmete sujuvamaks komplekti, et teha optimeeritud teave pidevaks kättesaadavaks. Salvestatud vaba kaubavaru üksikasju filtreeritakse konfigureeritavate ärikriteeriumide alusel, et tagada kaasatud on ainult kõige asjakohasem teave. Kuna filtreeritud vaba kaubavaru loendid salvestatakse kohalikult varude nähtavuse teenusesse ja neid uuendatakse regulaarselt, toetavad need kiirjuurdepääsu, nõudmisel andmete eksportimist ja sujuvat integratsiooni välissüsteemidega.

Varude **nähtavuse kokkuvõtte lehe eellaadimine** annab vaate vaba kaubavaru *indeksi päringu eellaadimise tulemuste üksusele*. Erinevalt laoseisu *kokkuvõtte* üksusest annab *vaba* kaubavaru indeksi päringu eellaadimise tulemuste üksus toodetele vaba kaubavaru loendi koos valitud dimensioonidega. Lao nähtavus sünkroonib eellaaditud koondandmed iga 15 minuti järel.

Varude nähtavuse kokkuvõtte vahekaardi eellaadimise andmete vaatamiseks peate lülitama sisse funktsiooni **OnHandIndexQueryPreloadBackgroundService** *konfiguratsioonilehe* vahekaardil **Funktsioonihaldus** **ja seejärel valima konfiguratsiooni värskendamine (vt** ka varude nähtavuse konfigureerimine).**·**[...](inventory-visibility-configuration.md)

> [!NOTE]
> Nagu funktsiooni *OnhandMostSpecificBackgroudService* puhul, *jälgib funktsioon OnHandIndexQueryPreloadBackgroundService* ainult vaba kaubavaru muudatusi, mis toimusid pärast funktsiooni sisse lülitamist. Nende toodete andmeid, mis pole muutunud, kuna te funktsiooni sisse lülitasite, ei sünkroonita laoteenuse vahemälust keskkonda Dataverse. Kui teie **varude** kokkuvõtte leht ei näita kogu eeldatavat vaba laoseisu teavet, **minge varude haldusse > Perioodilised ülesanded >** Varude nähtavuse integreerimine, keelake pakett-töö ja lubage see uuesti. See käivitab algse jaotuse *ja* kõik andmed sünkroonitakse järgmise 15 minuti jooksul vaba kaubavaru indeksi päringu eellaadimise tulemuste üksusega. Kui soovite seda funktsiooni kasutada, **on soovitatav see enne vaba kaubavaru muudatuste tegemist sisse lülitada ja lubada varude nähtavuse integreerimise pakett-töö**.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a> Varude kokkuvõtete filtreerimine ja sirvimine

Kasutades **Täpsemat filtrit**, mida Dataverse pakub, saate luua isikliku vaate, mis näitab teie jaoks olulisi ridu. Täpsema filtri võimalused lasevad teile luua mitmesuguseid vaateid, lihtsatest keerulisteni. Samuti võimaldavad nad filtritele lisada grupeeritud ja pesastatud tingimusi. Täpsema filtri kasutamise kohta lisateabe saamiseks vt teemat Isiklike vaadete [redigeerimine või loomine täpsemate ruudustiku filtrite abil](/powerapps/user/grid-filters-advanced).

Lao **kokkuvõtte lehel** on ruudustiku kohal kolm välja (**vaikedimensioon**, **·** **kohandatud** dimensioon ja mõõt), mida saate kasutada nähtavate veergude juhtimiseks. Samuti saate valida mis tahes veerupäise, et praegust tulemust selle veeru järgi filtreerida või sortida. Järgmine kuvatõmmis tõsteb esile dimensiooni, filtreerimise, tulemuste arvu ja "laadi rohkem" väljad, mis on saadaval lao **kokkuvõtte** lehel.

![Varude kokkuvõtte leht](media/inventory-visibility-onhand-list.png "Varude kokkuvõtte leht")

Kuna olete eelnevalt määratlenud koondandmete laadimisel kasutatavad dimensioonid, **kuvatakse eellaadimise** lao nähtavuse kokkuvõtte lehel dimensiooniga seotud veerud. *Dimensioone ei saa kohandada, süsteem&mdash; toetab vaid eellaaditud vaba kaubavaru loendite saidi- ja asukohadimensioone.* Varude **nähtavuse kokkuvõtte lehe eellaadimine** sisaldab **filtreid**, mis sarnased lao kokkuvõtte leheküljel olevale, v.a dimensioonid on juba valitud. Järgmine kuvatõmmis tõsteb esile filtreerimisväljad, mis on saadaval varude **nähtavuse kokkuvõtte lehel Eellaadimisel**.

![Varude nähtavuse kokkuvõtte lehe eellaadimine](media/inventory-visibility-preload-onhand-list.png "Varude nähtavuse kokkuvõttelehe eellaadimine")

Varude **nähtavuse** **kokkuvõtte** ja laokokkuvõtete eellaadimise allosas leiate teavet nagu "50 kirjet (29 valitud)" või "50 kirjet". See teave viitab praegu laaditud kirjetele **Täpsema filtri** tulemusest. Tekst "29 valitud" viitab kirjete arvule, mis on laaditud kirjete veeru päise filtri abil valitud. Nupp Laadi veel **, mille** abil saate laadida rohkem kirjeid Dataverse. Laaditud kirjete vaikearv on 50. Kui valite **laadi** rohkem, laaditakse vaatesse järgmised 1000 saadaolevat kirjet. Number nupul **Laadi veel** näitab praegu laaditud kirjeid ja **Täpsema filtri** tulemuste kõigi kirjete arvu.
