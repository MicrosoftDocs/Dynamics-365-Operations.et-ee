---
title: Topeltkirjutuse konfiguratsiooni kontrollimine Finance and Operationsi rakendustes ja Dataverse’is
description: See teema selgitab, kuidas saate määrata, kas kahekordne kirjutamine on Finance and Operationsi rakendustes ja rakendustes konfigureeritud Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3fa16a450032464e445ae166f0699fe0dc388071
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062796"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Topeltkirjutuse konfiguratsiooni kontrollimine Finance and Operationsi rakendustes ja Dataverse’is

[!include [banner](../../includes/banner.md)]





See teema pakub tõrkeotsinguteavet finance and Operationsi rakenduste ja rakenduse kahe kirjutamise integreerimiseks Dataverse. Täpsemalt selgitab see, kuidas saate määrata, kas kahekordne kirjutamine on Finance and Operationsi rakendustes ja rakendustes konfigureeritud Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Veenduge, et kahekordne kirjutamine on Finance and Operationsi rakenduses konfigureeritud

Selleks, et teha kindlaks, kas ridade värskenduse salvestamisel kuvatavad tõrketeated on põhjustatud topeltkirjutusest, kontrollige esmalt, kas topeltkirjutus on konfigureeritud.

+ Kui teil on rakenduses Finance and Operations administraatoriõigused, minge aadressile **Tööruumid \> Andmehaldus** ja valige **Kahekordne kirjutamine** plaat. Kui kuvatakse lingitud keskkondade üksikasjad ja kasutatava tabeli vastenduste loend, konfigureeritakse topeltkirjutus.

    ![Rakenduse Finance and Operations ühenduse kinnitamine, kui teil on administraatoriõigused.](media/verify_fin_ops_1.png)

+ Kui teil ei ole administraatori privileege, kuvatakse tõrketeade *Andmeid ei saa kirjutada üksusele \<entity name\>*. Järgmise illustratsiooni näites ei saa te rakenduses Finance and Operations kliendirida luua, kuna kahekordne kirjutamine on konfigureeritud, kuid kliendirühma ja maksetingimuste viiteandmeid rakenduses pole Dataverse.

    ![Rakenduse Finance and Operations ühenduse kinnitamine, kui teil pole administraatoriõigusi.](media/verify_fin_ops_2.png)

Teavet selle kohta, kuidas Finance and Operationsi rakendustes andmete loomisel probleeme lahendada, vaadake jaotisest [Otsige reaalajas sünkroonimise probleeme](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollimine, kas topeltkirjutus on konfigureeritud Dataverse'is

Kui andmete loomisel kuvatakse Dataverse’i lehtedel veerg **Ettevõte**, on topeltkirjutus konfigureeritud.

![Dataverse'i ühenduse kontrollimine.](media/verify_cds.png)

Lisateavet selle kohta, kuidas lahendada probleeme Dataverse'is andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

Lisateavet selle kohta, kuidas vaadata tõrke üksikasju, kui Dataverse'is andmete loomisel ilmneb tõrkeid, vaadake teemast [Dataverse'is lisandmooduli jälituslogi lubamine ja kuvamine tõrke üksikasjade vaatamiseks](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]