---
title: Kontrollige topeltkirjutuse konfiguratsiooni Finance and Operations i rakendustes ja Dataverse’is
description: Selles teemas selgitatakse, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operations i rakendustes ja Dataverse'is.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1f82705f3d8bc11eacbc13d32c14ad1765dcc559
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782623"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kontrollige topeltkirjutuse konfiguratsiooni Finance and Operations i rakendustes ja Dataverse’is

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige selgitab see, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operations i rakendustes ja Dataverse'is.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollimine, kas topeltkirjutus on konfigureeritud Finance and Operations i rakenduses

Selleks, et teha kindlaks, kas ridade värskenduse salvestamisel kuvatavad tõrketeated on põhjustatud topeltkirjutusest, kontrollige esmalt, kas topeltkirjutus on konfigureeritud.

+ Kui teil on administraatori privileegid rakenduses Finance and Operations, avage jaotis **Tööruumid \> Andmehaldus** ja valige paan **Topeltkirjutus**. Kui kuvatakse lingitud keskkondade üksikasjad ja kasutatava tabeli vastenduste loend, konfigureeritakse topeltkirjutus.

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide korral.](media/verify_fin_ops_1.png)

+ Kui teil ei ole administraatori privileege, kuvatakse tõrketeade *Andmeid ei saa kirjutada üksusele \<entity name\>*. Järgmises näites kirjeldatakse, et rakenduses Finance and Operations ei saa kliendi rida luua, sest topeltkirjutus on konfigureeritud, kuid kliendigruppi ja maksetingimuste viiteandmeid pole teenuses Dataverse olemas.

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide puudumise korral.](media/verify_fin_ops_2.png)

Lisateavet selle kohta, kuidas lahendada probleeme rakenduses Finance and Operations andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollimine, kas topeltkirjutus on konfigureeritud Dataverse'is

Kui andmete loomisel kuvatakse Dataverse’i lehtedel veerg **Ettevõte**, on topeltkirjutus konfigureeritud.

![Dataverse'i ühenduse kontrollimine.](media/verify_cds.png)

Lisateavet selle kohta, kuidas lahendada probleeme Dataverse'is andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

Lisateavet selle kohta, kuidas vaadata tõrke üksikasju, kui Dataverse'is andmete loomisel ilmneb tõrkeid, vaadake teemast [Dataverse'is lisandmooduli jälituslogi lubamine ja kuvamine tõrke üksikasjade vaatamiseks](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]