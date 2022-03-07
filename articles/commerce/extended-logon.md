---
title: MPOS-i ja pilve kassa (CPOS) jaoks laiendatud sisselogimise funktsiooni seadistamine
description: See teema käsitleb võimalusi laiendatud sisselogimise seadistamiseks pilvekassas ja Retail Modern POS-is (MPOS).
author: boycezhu
ms.date: 09/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0cc3d3a3cadbc614e82b8cc7ae0b78406247cece
ms.sourcegitcommit: efcb853a68a77037cca23582d9f6f96ea573727a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7478667"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>Cloud MPOS ja Cloud POS‑i laiendatud sisselogimisfunktsiooni seadistamine

[!include [banner](includes/banner.md)]

See teema käsitleb võimalusi laiendatud sisselogimise seadistamiseks pilvekassas ja Retail Modern POS-is (MPOS).

## <a name="setting-up-extended-logon"></a>Laiendatud sisselogimise seadistamine

Vöötkoodi maskide seadistuse leiate järgmist teed pidi: **Jaemüük ja kaubandus** &gt; **Kanali häälestus** &gt; **Kassa seadistus** &gt;**Kassa profiilid** &gt; **Funktsiooniprofiilid**. Kiirkaart **Funktsioonid** sisaldab järgmisi laiendatud sisselogimisega seotud suvandeid.

### <a name="staff-bar-code-logon"></a>Personali vöötkoodi sisselogimine

Kui suvand **Personali vöötkoodiga sisselogimine** on lubatud, saavad töötajad, kelle kassa identimisteabele on määratud laiendatud sisselogimine, vöötkoodi kasutades sisse logida.

### <a name="staff-bar-code-logon-requires-password"></a>Personali vöötkoodiga sisselogimisel on nõutav parool

Kui suvand **Personali vöötkoodiga sisselogimisel on nõutav parool** on lubatud, valib personali vöötkoodiga sisselogimine ainult selle töötaja, kellel on määratud esitatud laiendatud sisselogimine. Kui see suvand on lubatud, peavad töötajad ka parooli sisestama.

### <a name="staff-card-logon"></a>Personali kaardi sisselogimine

Kui suvand **Personali kaardiga sisselogimine** on lubatud, saavad töötajad, kelle kassa identimisteabele on määratud laiendatud sisselogimine, magnetriba kasutades sisse logida.

### <a name="staff-card-logon-requires-password"></a>Personali kaardiga sisselogimisel on nõutav parool

Kui suvand **Personali kaardiga sisselogimisel on nõutav parool** on lubatud, valib personali kaardiga sisselogimine ainult selle töötaja, kellel on määratud esitatud laiendatud sisselogimine. Kui see suvand on lubatud, peavad töötajad ka parooli sisestama.

## <a name="assigning-an-extended-logon"></a>Laiendatud sisselogimise määramine

Vaikimisi saavad töötajatele laiendatud sisselogimist määrata ainult juhid. Laiendatud sisselogimise määramiseks avage kassas valik **Laiendatud sisselogimine**. Seejärel otsige töötajat, sisestades otsinguväljale tema operaatori ID. Valige töötaja ja klõpsake seejärel nuppu **Määra**. Järgmisel leheküljel tehke töötajale laiendatud sisselogimise määramiseks kaaarditõmme või ‑skann. Kui kaarditõmme või ‑skann on edukalt loetud, ilmub nupp **OK**. Töötajale laiendatud sisselogimise salvestamiseks klõpsake nuppu **OK**.

## <a name="deleting-an-extended-logon"></a>Laiendatud sisselogimise kustutamine

Töötajale määratud laiendatud sisselogimise kustutamiseks otsige töötajat toimingu **Laiendatud sisselogimine** abil. Valige töötaja ja klõpsake seejärel nuppu **Eemalda määrang**. Kõik töötajaga seostatud laiendatud sisselogimise identimisteave eemaldatakse.

## <a name="extending-extended-logon"></a>Laiendatud sisselogimine laiendamine

Laiendatud sisselogimine lubab ainult viit olulist märki, et olla boksist väljas kordumatu ID. Näiteks kui konfigureerite kaks kaarti ID-dega "1234567" ja "1234578", peetakse neid mõlemaid kui "12345". Võite luua laiendi, mis toetab rohkem märke. Üksikasjalikke juhiseid vaadake [MPOS-i ja pilve kassa laiendatud sisselogimise funktsioonide laiendamisest](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Sisselogimisteenust saab laiendada täiendavate laiendatud sisselogimine seadmete nagu käsiskannerid toetamiseks. Lisateabe saamiseks vt kassa laiendatavuse dokumentatsiooni.

## <a name="using-extended-logon"></a>Laiendatud sisselogimise kasutamine

Kui laiendatud sisselogimine on konfigureeritud ja töötajale on määratud vöötkood või magnetriba, peab töötaja kassa sisselogimislehe kuvamisel tegema ainult kaarditõmbe või ‑skanni. Kui sisselogimise jätkamiseks on kohustuslik ka parool, palutakse töötajal sisestada oma parool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
