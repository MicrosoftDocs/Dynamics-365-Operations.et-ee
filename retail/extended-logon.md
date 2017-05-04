---
title: "Pilve kassasse ja MPOS‑i laiendatud sisselogimise funktsiooni seadistamine"
description: "See viki käsitleb võimalusi laiendatud sisselogimise seadistamiseks Cloud POS-is ja Retail Modern POS-is (MPOS)."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Pilve kassasse ja MPOS‑i laiendatud sisselogimise funktsiooni seadistamine

See viki käsitleb võimalusi laiendatud sisselogimise seadistamiseks Cloud POS-is ja Retail Modern POS-is (MPOS).

<a name="setting-up-extended-logon"></a>Laiendatud sisselogimise seadistamine
=========================

Vöötkoodi maskide seadistuse leiate järgmist teed pidi: **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa profiilid** &gt; **Funktsiooniprofiilid**. Kiirkaart **Funktsioonid** sisaldab järgmisi laiendatud sisselogimisega seotud suvandeid.

### <a name="staff-bar-code-logon"></a>Personali vöötkoodi sisselogimine

Kui suvand **Personali vöötkoodiga sisselogimine** on lubatud, saavad töötajad, kelle kassa identimisteabele on määratud laiendatud sisselogimine, vöötkoodi kasutades sisse logida.

### <a name="staff-bar-code-logon-requires-password"></a>Personali vöötkoodiga sisselogimisel on nõutav parool

Kui suvand **Personali vöötkoodiga sisselogimisel on nõutav parool** on lubatud, valib personali vöötkoodiga sisselogimine ainult selle töötaja, kellel on määratud esitatud laiendatud sisselogimine. Kui see suvand on lubatud, peavad töötajad ka parooli sisestama.

### <a name="staff-card-logon"></a>Personali kaardi sisselogimine

Kui suvand **Personali kaardiga sisselogimine** on lubatud, saavad töötajad, kelle kassa identimisteabele on määratud laiendatud sisselogimine, magnetriba kasutades sisse logida.

### <a name="staff-card-logon-requires-password"></a>Personali kaardiga sisselogimisel on nõutav parool

Kui suvand **Personali kaardiga sisselogimisel on nõutav parool** on lubatud, valib personali kaardiga sisselogimine ainult selle töötaja, kellel on määratud esitatud laiendatud sisselogimine. Kui see suvand on lubatud, peavad töötajad ka parooli sisestama.

<a name="assigning-an-extended-logon"></a>Laiendatud sisselogimise määramine
===========================

Vaikimisi saavad töötajatele laiendatud sisselogimist määrata ainult juhid. Laiendatud sisselogimise määramiseks avage kassas valik **Laiendatud sisselogimine**. Seejärel otsige töötajat, sisestades otsinguväljale tema operaatori ID. Valige töötaja ja klõpsake seejärel nuppu **Määra**. Järgmisel leheküljel tehke töötajale laiendatud sisselogimise määramiseks kaaarditõmme või ‑skann. Kui kaarditõmme või ‑skann on edukalt loetud, ilmub nupp **OK**. Töötajale laiendatud sisselogimise salvestamiseks klõpsake nuppu **OK**.

<a name="deleting-an-extended-logon"></a>Laiendatud sisselogimise kustutamine
==========================

Töötajale määratud laiendatud sisselogimise kustutamiseks otsige töötajat toimingu **Laiendatud sisselogimine** abil. Valige töötaja ja klõpsake seejärel nuppu **Eemalda määrang**. Kõik töötajaga seostatud laiendatud sisselogimise identimisteave eemaldatakse.

<a name="extending-extended-logon"></a>Laiendatud sisselogimine laiendamine
========================

Sisselogimisteenust saab laiendada täiendavate laiendatud sisselogimine seadmete nagu käsiskannerid toetamiseks. Lisateabe saamiseks vt kassa laiendatavuse dokumentatsiooni.

<a name="using-extended-logon"></a>Laiendatud sisselogimise kasutamine
====================

Kui laiendatud sisselogimine on konfigureeritud ja töötajale on määratud vöötkood või magnetriba, peab töötaja kassa sisselogimislehe kuvamisel tegema ainult kaarditõmbe või ‑skanni. Kui sisselogimise jätkamiseks on kohustuslik ka parool, palutakse töötajal oma parool sisestada.


