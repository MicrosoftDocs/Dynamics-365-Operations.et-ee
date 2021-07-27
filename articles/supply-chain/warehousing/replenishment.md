---
title: Täiendamise ülevaade
description: Selles teemas kirjeldatakse täiendamisstrateegiaid, mis on saadaval ladude puhul, milles seda laohalduse moodulis saadaolevat funktsiooni kasutatakse.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "90043"
- intro-internal
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e381af433eb3041d92ddfe375e6b4c75c1feb7c2
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335816"
---
# <a name="replenishment-overview"></a>Täiendamise ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse täiendamisstrateegiaid, mis on saadaval ladude puhul, milles seda laohalduse moodulis saadaolevat funktsiooni kasutatakse. Selle teema teave ei kehti moodulis Varude haldus oleva ladustamislahenduse puhul.

Saadaval järgmised täiendamise strateegiad.

- **Täiendamine voo nõudmise põhjal** – see strateegia loob täiendamistöö väljaminevatele tellimustele või koormatele, kui töö luuakse vooga ja varud ei ole saadaval. Näiteks saab täiendamistöö luua, kui müügitellimuse jaoks vajalik kogus pole voo töötlemisel saadaval.
- **Min/max täiendamine** – see strateegia kasutab minimaalset ja maksimaalset ladustamispiirangut määramiseks, millal asukohti tuleks täiendada. Kauba ja asukoha kriteeriumid määravad varud, mida täiendamiseks hinnatakse. Min/max täiendamise mallid on põhimehhanism komplekteerimiskohtades optimaalsete tasemete säilitamiseks. Tagamaks piisavate komplekteerimisvarude olemasolu voo nõudlusele vastamiseks võite kasutada Min/max täiendamistsüklite vahel nõudluse tõttu täiendamist.
- **Koorma nõudluse tõttu täiendamine** – see strateegia summeerib nõudluse mitme koorma järele ja loob täiendamistöö, mis on vajalik vastavate komplekteerimiskohtade varustamiseks. See strateegia aitab tagada, et loodud koormaid saab pärast nende väljastamist laos komplekteerida.
- **Viivitamatu täiendamine** – see strateegia täiendab varusid enne voo käitamist, kui eraldamine nurjub asukohakorralduse rea puhul, millel on täiendamise mall. 

Kõik neli strateegiat loovad täiendamistöö täiendamismalli põhjal.

## <a name="wave-demand-replenishment"></a>Voo nõudluse tõttu täiendamine
Voo nõudluse tõttu täiendamine loob nõudlusel põhineva täiendamistöö, kui tootmistellimuste, kanbanide, väljaminevate tellimuste või koormate jaoks vajalikku kogust pole saadaval, kui voog töö loob. Täiendamismall sisaldab teavet kauba kriteeriumide kohta, mõõtühikut, nõudluse juurdekasvu ja asukohta. 

Määramiseks, millist asukohta tuleks täiendada, kasutatakse asukohakorraldusi. Need asukohakorraldused saab siduda täiendamismalliga, kasutades välja **Korralduse kood**. Kui välja **Korralduse kood** pole määratud, kasutatakse päringuid määramiseks, millist asukohakorraldust tuleks kasutada. Arvestage, et kui täiendamismallis pole korralduse koodi määratud ja asukohakorraldusel on korralduse koos, eiratakse asukohakorraldust, isegi kui asukohakorralduse päring on õige. Täiendamiseks varude hankimise koha määratlemiseks kasutatakse komplekteerimise asukohakorraldusi. 

Lisaks malli loomisele tuleb voomallis määrata mõned täiendamise sätted. Voomallid peaksid sisaldama täiendamise vooetappi, mis käivitatakse ainult juhul, kui kauba eraldamine ei õnnestunud. See täiendamise vooetapp kasutab vooetapi koodi määramiseks, millist täiendamismalli tuleks kasutada. Lisaks vooetapi olemasolule täiendamiseks peate veenduma, et on tehtud valik **Täienda** voomalli jaotises **Meetodid**. 

Lehel **Täiendamise mall** on märkeruut **Luba voo nõudel kasutada reserveerimata koguseid**. Märkige see ruut, kui nõudluse tõttu täiendamine peaks võimaldama reserveerimata koguste mahaarvamist valitud täiendamise malli põhjal loodud tööst. Selleks, et lubada nõudluse tõttu täiendamise mallidel seda loogikat kasutada, märkige see ruut iga olemasoleva täiendamismalli jaoks. Kui laos käivitatakse nõudluse tõttu täiendamine, arvestatakse maha nõudlus reserveerimata kogustega olemasolevatest täiendamistöödest, kui töö pärineb täiendamismallidest, millel on märgitud ruut **Luba voo nõudel kasutada reserveerimata koguseid**.

**Täiendamise ühik** on minimaalne ühik täiendamiseks. See peab olema täisarv, mis on seadme kordaja. Süsteem ümardab töö loomisel suurima võimaliku ühikuni.

Nõudluse täiendamist toetatakse müügitellimuste, üleviimistellimuste, tootmistellimuste ja kanbanide puhul. 

## <a name="minmax-replenishment"></a>Min/max täiendamine
Min/max täiendamise puhul täiendatakse varusid nii, et need oleksid määratud miinimum- ja maksimumpiiri vahel. Tavaliselt toimub see protsess kord päevas, et tagada kõigi komplekteerimiskohtade maksimumtasemel täitmine enne komplekteerimise algust. 

Miinimum- ja maksimumkogused määratakse täiendamismallis. Paljud muud malli sätted sarnanevad voo nõudluse tõttu täiendamises kasutatavate mallide sätetele. Mall peaks sisaldama ühte rida iga kauba ja asukoha kohta. Kui käivitate täiendamise pakett-töö abil, hindab süsteem ridade korraldamise seeriat kasutades, kas täiendamine on nõutav. 

Pange tähele, et min/max täiendamise strateegia ei saa täiendada tühja asukohta, kui asukoht pole määratud kauba puhul fikseeritud asukohaks. Kui asukoht, mida peab täiendama, pole fikseeritud asukoht, ei saa süsteem määratleda, millist kaupa tuleks täiendada. Seetõttu on enne täiendamist vaja vähemalt mingisugust vaba kaubavaru.

## <a name="load-demand-replenishment"></a>Nõudmise tõttu laovarude täiendamise laadimine
Koorma nõudluse tõttu täiendamine summeerib nõudluse mitme koorma järele ja loob täiendamistöö, mis on vajalik vastavate komplekteerimiskohtade varustamiseks. Koorma nõudluse tõttu täiendamine sarnaneb mitmel moel voo nõudluse tõttu täiendamisele. Peamine erinevus on see, kuidas ja millal koorma nõudluse tõttu täiendamine ja voo nõudluse tõttu täiendamine käivitatakse. Sarnaselt min/max täiendamisele käivitatakse koorma nõudluse tõttu täiendamine pakett-töö abil. Pakett-töö seadistamiseks valige lehelt **Koorma nõudluse tõttu täiendamine**, valige täiendamismall, mida kasutada, ja määrake filtri päring täpsustamiseks, milliseid koormaid nõudluse määramiseks kasutatakse. Asukoha päring määratleb asukohad, millest saadaolevad kogused lahutatakse, et koormate kogunõudlust täita.

## <a name="immediate-replenishment"></a>Viivitamatu täiendamine
Selle asemel, et võtta nõudlus eraldamisprotsessi lõppemisel kokku ja täiendada summeeritud koguse põhjal, saate rakendada viivitamatu täiendamise strateegiat. Selle strateegia kasutamisel saab varusid täiendada kohe pärast asukohakorralduse rea nurjumist. Seetõttu saate seadistada täiendamise nii, et see on piiratud konkreetsete üksustega ja kasutab konkreetsetele asukohtadele määratud koguseid.

## <a name="replenishment-prerequisites"></a>Täiendamise eeltingimused

|      Eeltingimus       |                                                                                                                                Kirjeldus                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Kaup           |                                                                                                        Kauba puhul peavad olema lubatud laohaldusprotsessid.                                                                                                        |
|        Ladu        | Laos peavad olema lubatud laohaldusprotsessid. Laohaldusprotsesside lubamiseks laos valige ladu lehelt <strong>Laod</strong> ja märkige seejärel valik <strong>Kasuta laohaldusprotsesse</strong>. |
| Täiendamise mallid |                                                                   Min/max täiendamise, voo nõudluse tõttu täiendamise või koormuse nõudluse tõttu täiendamise jaoks tuleb seadistada vähemalt üks täiendamismall.                                                                   |
|        Asukohad        |                                                                                                       Tuleb luua asukohad ja ühendada need asukohaprofiiliga.                                                                                                       |
|    Asukoha profiilid    |                                                                                                        Asukohtade loomiseks on vajalikud asukohaprofiilid.                                                                                                        |
|   Asukoha korraldus   |                                                       Asukohakorraldusi on vaja selleks, et juhtida töö asukohtadesse, kus täiendamine on vajalik, ja asukohtadesse, kust varusid hangitakse.                                                        |
|     Töömallid      |                                                   Töömallid tüübiga <strong>Täiendamine</strong> on vajalikud täiendamistöö loomiseks, et varud saaks soovitud asukohtadesse viia.                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]