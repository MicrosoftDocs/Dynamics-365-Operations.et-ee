---
title: "Täiendamine"
description: "Selles artiklis kirjeldatakse täiendamisstrateegiaid, mis on saadaval ladude puhul, milles seda laohalduse moodulis saadaolevat funktsiooni kasutatakse."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c808ec202bdb271f08a36a2b25ebed22a9477414
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="replenishment"></a>Täiendamine

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse täiendamisstrateegiaid, mis on saadaval ladude puhul, milles seda laohalduse moodulis saadaolevat funktsiooni kasutatakse.

Selles artiklis kirjeldatakse täiendamisstrateegiaid, mis on saadaval ladude puhul, milles seda laohalduse moodulis saadaolevat funktsiooni kasutatakse. See teave ei kehti moodulis Varude haldus oleva ladustamislahenduse puhul. Saadaval on kolm täiendamise strateegiat.

-   **Täiendamine voo nõudmise põhjal** – see strateegia loob täiendamistöö väljaminevatele tellimustele või koormatele, kui töö luuakse vooga ja varud ei ole saadaval. Näiteks saab täiendamistöö luua, kui müügitellimuse jaoks vajalik kogus pole voo töötlemisel saadaval.
-   **Min/max täiendamine** – see strateegia kasutab minimaalset ja maksimaalset ladustamispiirangut määramiseks, millal asukohti tuleks täiendada. Kauba ja asukoha kriteeriumid määravad varud, mida täiendamiseks hinnatakse. Min/max täiendamise mallid on põhimehhanism komplekteerimiskohtades optimaalsete tasemete säilitamiseks. Tagamaks piisavate komplekteerimisvarude olemasolu voo nõudlusele vastamiseks võite kasutada Min/max täiendamistsüklite vahel nõudluse tõttu täiendamist.
-   **Koorma nõudluse tõttu täiendamine** – see strateegia summeerib nõudluse mitme koorma järele ja loob täiendamistöö, mis on vajalik vastavate komplekteerimiskohtade varustamiseks. See strateegia aitab tagada, et loodud koormaid saab pärast nende väljastamist laos komplekteerida.

Kõik kolm strateegiat loovad täiendamistöö täiendamismalli põhjal.

## <a name="wave-demand-replenishment"></a>Voo nõudluse tõttu täiendamine
Voo nõudluse tõttu täiendamine loob nõudlusel põhineva täiendamistöö, kui väljaminevate tellimuste või koormate jaoks vajalikku kogust pole saadaval, kui voog töö loob. Täiendamismall sisaldab teavet kauba kriteeriumide kohta, mõõtühikut, nõudluse juurdekasvu ja asukohta. 

Määramiseks, millist asukohta tuleks täiendada, kasutatakse asukohakorraldusi. Need asukohakorraldused saab siduda täiendamismalliga, kasutades välja **Korralduse kood**. Kui välja **Korralduse kood** pole määratud, kasutatakse päringuid määramiseks, millist asukohakorraldust tuleks kasutada. Arvestage, et kui täiendamismallis pole korralduse koodi määratud ja asukohakorraldusel on korralduse koos, eiratakse asukohakorraldust, isegi kui asukohakorralduse päring on õige. Täiendamiseks varude hankimise koha määratlemiseks kasutatakse komplekteerimise asukohakorraldusi. 

Lisaks malli loomisele tuleb voomallis määrata mõned täiendamise sätted. Voomallid peaksid sisaldama täiendamise vooetappi, mis käivitatakse ainult juhul, kui kauba eraldamine ei õnnestunud. See täiendamise vooetapp kasutab vooetapi koodi määramiseks, millist täiendamismalli tuleks kasutada. Lisaks vooetapi olemasolule täiendamiseks peate veenduma, et on tehtud valik **täienda** voomalli jaotises **Meetodid**. 

Lehel **Täiendamise mall** on märkeruut **Luba voo nõudel kasutada reserveerimata koguseid**. See märkeruut tuleb valida, kui soovite lubada nõudluse tõttu täiendamise, et reserveerimata kogused valitud täiendamise malli põhjal loodud tööst maha arvata. Selleks, et lubada nõudluse tõttu täiendamise mallidel seda loogikat kasutada, peate määrama märkeruudu iga olemasoleva täiendamismalli jaoks. Kui laos käivitatakse nõudluse tõttu täiendamine, arvestatakse maha nõudlus reserveerimata kogustega olemasolevatest täiendamistöödest, kui töö pärineb täiendamismallidest, millel on märgitud ruut **Luba voo nõudel kasutada reserveerimata koguseid**.

## <a name="minmax-replenishment"></a>Min/max täiendamine
Min/max täiendamise puhul täiendatakse varusid nii, et need oleksid määratud miinimum- ja maksimumpiiri vahel. Tavaliselt toimub see protsess kord päevas, et tagada kõigi komplekteerimiskohtade maksimumtasemel täitmine enne komplekteerimise algust. 

Miinimum- ja maksimumkogused määratakse täiendamismallis. Paljud muud malli sätted sarnanevad voo nõudluse tõttu täiendamises kasutatavate mallide sätetele. Mall peaks sisaldama ühte rida iga kauba ja asukoha kohta. Kui käivitate täiendamise pakett-töö abil, hindab Microsoft Dynamics 365 for Operations, kas ridade korraldamise seerias on täiendamine nõutav. 

Pange tähele, et min/max täiendamise strateegia ei saa täiendada tühja asukohta, kui asukoht pole määratud kauba puhul fikseeritud asukohaks. Kui asukoht, mida peab täiendama, pole fikseeritud asukoht, ei saa Dynamics 365 for Operations määratleda, millist kaupa täiendada. Seetõttu on enne täiendamist vaja vähemalt mingisugust vaba kaubavaru.

## <a name="load-demand-replenishment"></a>Nõudmise tõttu laovarude täiendamise laadimine
Koorma nõudluse tõttu täiendamine summeerib nõudluse mitme koorma järele ja loob täiendamistöö, mis on vajalik vastavate komplekteerimiskohtade varustamiseks. Koorma nõudluse tõttu täiendamine sarnaneb mitmel moel voo nõudluse tõttu täiendamisele. Peamine erinevus on see, kuidas ja millal koorma nõudluse tõttu täiendamine ja voo nõudluse tõttu täiendamine käivitatakse. Sarnaselt min/max täiendamisele käivitatakse koorma nõudluse tõttu täiendamine pakett-töö abil. Pakett-töö seadistamiseks valige lehelt **Koorma nõudluse tõttu täiendamine**, valige täiendamismall, mida kasutada, ja määrake filtri päring täpsustamiseks, milliseid koormaid nõudluse määramiseks kasutatakse. Asukoha päring määratleb asukohad, millest saadaolevad kogused lahutatakse, et koormate kogunõudlust täita.

## <a name="replenishment-prerequisites"></a>Täiendamise eeltingimused
| Eeltingimus            | Kirjeldus                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kaup                    | Kauba puhul peavad olema lubatud laohaldusprotsessid.                                                                                                                                                                                       |
| Ladu               | Laos peavad olema lubatud laohaldusprotsessid. Laohaldusprotsesside lubamiseks laos valige ladu lehelt **Laod** ja märkige seejärel valik **Kasuta laohaldusprotsesse**. |
| Täiendamise mallid | Min/max täiendamise, voo nõudluse tõttu täiendamise või koormuse nõudluse tõttu täiendamise jaoks tuleb seadistada vähemalt üks täiendamismall.                                                                                                             |
| Asukohad               | Tuleb luua asukohad ja ühendada need asukohaprofiiliga.                                                                                                                                                                                     |
| Asukoha profiilid       | Asukohtade loomiseks on vajalikud asukohaprofiilid.                                                                                                                                                                                       |
| Asukoha korraldus     | Asukohakorraldusi on vaja selleks, et juhtida töö asukohtadesse, kus täiendamine on vajalik, ja asukohtadesse, kust varusid hangitakse.                                                                                     |
| Töömallid          | Töömallid tüübiga **Täiendamine** on vajalikud täiendamistöö loomiseks, et varud saaks soovitud asukohtadesse viia.                                                                                           |






