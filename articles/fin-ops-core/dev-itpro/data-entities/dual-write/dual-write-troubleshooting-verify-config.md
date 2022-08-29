---
title: Topeltkirjutuse konfiguratsiooni kontrollimine finants- ja äritoimingute rakendustes ja Dataverse’is
description: See artikkel selgitab, kuidas saate otsustada, kas topeltkirjutused on konfigureeritud finantside ja toimingute rakendustes ja rakenduses Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289386"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Topeltkirjutuse konfiguratsiooni kontrollimine finants- ja äritoimingute rakendustes ja Dataverse’is

[!include [banner](../../includes/banner.md)]





See artikkel pakub tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning Dataverse. Täpsemalt selgitab see, kuidas saate otsustada, kas topeltkirjutust konfigureeritakse finantside ja operatsioonide rakendustes ja rakenduses Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollige, kas topeltkirjutus on konfigureeritud finantside ja toimingute rakenduses.

Selleks, et teha kindlaks, kas ridade värskenduse salvestamisel kuvatavad tõrketeated on põhjustatud topeltkirjutusest, kontrollige esmalt, kas topeltkirjutus on konfigureeritud.

+ Kui teil on finantside ja toimingute rakenduses administraatori privileegid, minge tööruumide **\> andmehalduse ja** valige topeltkirjutuse **paani**. Kui kuvatakse lingitud keskkondade üksikasjad ja kasutatava tabeli vastenduste loend, konfigureeritakse topeltkirjutus.

    ![Finantside ja toimingute rakenduse ühenduse kontrollimine, kui teil on halduse privileegid.](media/verify_fin_ops_1.png)

+ Kui teil ei ole administraatori privileege, kuvatakse tõrketeade *Andmeid ei saa kirjutada üksusele \<entity name\>*. Järgmises illustratsioonis toodud näites ei saa finantside ja toimingute rakenduses luua kliendi rida, kuna topeltkirjutus on konfigureeritud, kuid kliendigrupi ja maksetingimuste viiteandmeid pole olemas Dataverse.

    ![Finantside ja toimingute rakenduse ühenduse kontrollimine, kui teil ei ole halduseõigusi.](media/verify_fin_ops_2.png)

Teavet probleemide lahendamise kohta finantside ja toimingute rakendustes andmete loomisel vt reaalajas [sünkroonimisprobleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollimine, kas topeltkirjutus on konfigureeritud Dataverse'is

Kui andmete loomisel kuvatakse Dataverse’i lehtedel veerg **Ettevõte**, on topeltkirjutus konfigureeritud.

![Dataverse'i ühenduse kontrollimine.](media/verify_cds.png)

Lisateavet selle kohta, kuidas lahendada probleeme Dataverse'is andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

Lisateavet selle kohta, kuidas vaadata tõrke üksikasju, kui Dataverse'is andmete loomisel ilmneb tõrkeid, vaadake teemast [Dataverse'is lisandmooduli jälituslogi lubamine ja kuvamine tõrke üksikasjade vaatamiseks](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
