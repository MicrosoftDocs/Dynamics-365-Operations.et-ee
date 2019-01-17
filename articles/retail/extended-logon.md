---
title: MPOS-i ja pilve kassa (CPOS) jaoks laiendatud sisselogimise funktsiooni seadistamine
description: "See teema käsitleb võimalusi laiendatud sisselogimise seadistamiseks pilve kassas ja tänapäevases jaemüügikassas (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 4e3f8042871e5e423b559bb0e0dae0006af00194
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>MPOS-i ja pilve kassa (CPOS) jaoks laiendatud sisselogimise funktsiooni seadistamine

[!include [banner](includes/banner.md)]

See teema käsitleb võimalusi laiendatud sisselogimise seadistamiseks pilve kassas ja tänapäevases jaemüügikassas (MPOS).

## <a name="setting-up-extended-logon"></a>Laiendatud sisselogimise seadistamine

Vöötkoodi maskide seadistuse leiate järgmist teed pidi: **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa profiilid** &gt; **Funktsiooniprofiilid**. Kiirkaart **Funktsioonid** sisaldab järgmisi laiendatud sisselogimisega seotud suvandeid.

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

Sisselogimisteenust saab laiendada täiendavate laiendatud sisselogimine seadmete nagu käsiskannerid toetamiseks. Lisateabe saamiseks vt kassa laiendatavuse dokumentatsiooni.

## <a name="using-extended-logon"></a>Laiendatud sisselogimise kasutamine

Kui laiendatud sisselogimine on konfigureeritud ja töötajale on määratud vöötkood või magnetriba, peab töötaja kassa sisselogimislehe kuvamisel tegema ainult kaarditõmbe või ‑skanni. Kui sisselogimise jätkamiseks on kohustuslik ka parool, palutakse töötajal oma parool sisestada.

