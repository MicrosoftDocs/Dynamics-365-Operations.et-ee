---
title: Tehnilise muudatuse haldamise parameetrid
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Supply Chain Managementis tehnilise muudatuse haldamise funktsioone.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 106c3a79236bcb8112ecbd48e29f3f5f3148a867
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7581004"
---
# <a name="engineering-change-management-parameters"></a>Tehnilise muudatuse haldamise parameetrid

[!include [banner](../includes/banner.md)]

Leht **Tehnilise muudatuse haldamise parameetrid** sisaldab seadistusparameetreid, mis muudavad vaikekäitumist, mis on seotud väljastatava toote struktuuri ja tehnilise muudatuse haldamise protsessidega.

## <a name="open-the-engineering-change-management-parameters-page"></a>Tehnilise muudatuse haldamise parameetrite lehe avamine

Lehe **Tehnilise muudatuse haldamise parameetrid** avamiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamise parameetrid**. Seejärel saate seada väljad nii, nagu on kirjeldatud selle teema ülejäänud osades.

## <a name="release-control-tab"></a>Väljastamise juhtimise vahekaart

Järgmine tabel kirjeldab välju, mis on saadaval lehe **Tehnilise muudatuse haldamise parameetrid** vahekaardil **Väljastamise juhtimine**. Need väljad mõjutavad tootestruktuuri väljastamise protsessi.

| Väli | Kirjeldus |
|---|---|
| Kaubakoodi reegel | Valige, kuidas kaubakood tuleks määratleda, kui toode väljastatakse juriidilisele isikule. Valige *Tehnilise toote number*, kui vastuvõtva juriidilise isiku tootenumber peab ühtima tehnikaettevõtte tootenumbriga. Valige *Kohaliku kauba numbriseeria*, kui toode peab vastuvõtva juriidilise isiku tootenumbri puhul saama numbriseerias järgmise numbri. |
| Koosluse nime reegel | Valige, kuidas koosluse (BOM) nimi määratletakse, kui toode võetakse juriidilises isikus vastu (väljastatakse). Valige kas *Tehniline nimi* või *Vastuvõttev kaubakood*. |
| Protsessi nime reegel | Valige, kuidas protsessi nimi määratletakse, kui toote protsess võetakse juriidilises isikus vastu (väljastatakse). Valige kas *Tehniline nimi* või *Vastuvõttev kaubakood*. |
| Käivita koosluse kontroll | Valige, kas koosluse kontroll käivitatakse, kui toode võetakse juriidilises isikus vastu (väljastatakse). |
| Passiivse koosluse väljastuse käitumine | Valige, kas toodet saab väljastada, kui sellel on passiivne kooslus. Valige *Nõustu*, *Ainult hoiatus* või *Pole lubatud*. |
| Passiivse protsessi väljastuse käitumine | Valige, kas toodet saab väljastada, kui sellel on passiivne protsess. Valige *Nõustu*, *Ainult hoiatus* või *Pole lubatud*.|
| Toote aktsepteerimine | Valige, kas enne toote väljastamist juriidilises isikus on nõutav täiendav nõustumisetapp. Valige *Käsitsi*, et lisada nõustumisetapp. Sel juhul kuvatakse lehel **Avatud tooteväljastused** tooted. Valige *Automaatne*, et näidata toodet otse lehel **Väljastatud tooted** sihtmärgiks olevas juriidilises isikus kohe pärast toote väljastamist koos väljastatud toote struktuuriga. |

## <a name="engineering-change-management-tab"></a>Tehnilise muudatuse haldamise vahekaart

Järgmine tabel kirjeldab välju, mis on saadaval lehe **Tehnilise muudatuse haldamise parameetrid** vahekaardil **Tehnilise muudatuse haldamine**. Need sätted mõjutavad tehnilise muudatuse haldamise protsessi.

| Väli | Kirjeldus |
|---|---|
| Kategooria | Tehnilise muudatuse taotluse loomisel kasutatav vaikekategooria. |
| Prioriteet | Tehnilise muudatuse taotluse loomisel kasutatav vaikeprioriteet. |
| Raskusastme reegel | Valige, kuidas tuleks kindlaks määrata tehnilise muudatuse tellimuse raskusaste. Valige *Käsitsi*, kui kasutaja peaks sisestama väärtuse väljale **Raskusaste**. Valige *Arvuta*, et süsteem arvutaks välja **Raskusaste** väärtuse, kui valite tehnilise muudatuse tellimuse toimingupaanil suvandi **Arvuta raskusaste**. Sel juhul kasutab süsteem raskusastme reegleid, mis on määratud lehel **Raskusastme reeglid**. Valige *Arvuta automaatselt*, et välja **Raskusaste** väärtus arvutataks automaatselt ja täidetaks raskusastme reeglite järgi. |
| Mõjutatud toodete uuesti väljastamine | See väli on asjakohane, kui te väljastate tooteid uuesti tehnilise muudatuse tellimuse kaudu. Saate valida, kas dialoogiboksis **Väljastamised** pakutakse kõiki tooteid või ainult mõjutatud tooteid. |
| Väljastatavad kooslusetasemed | Väljastatava kooslusetaseme sügavus. Kui kooslusel on siin määratletud väärtusest rohkem tasemeid (st kui see on sügavam), väljastatakse tasemed ainult määratletud väärtuseni. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]