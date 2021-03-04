---
title: Ohtlikud materjalid
description: See teema annab teavet teie keskkonda talletatud ohtlike materjalide dokumentide ja teabe kohta.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426404"
---
# <a name="hazardous-materials"></a>Ohtlikud materjalid

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Teave ohtlike materjalide kohta on seadistatud toote teabehalduses. Siit moodulist leiate ka laohalduse kaudu prinditavad dokumendid.

Kui saadate materjale, mis on liigitatud ohtlikeks kaupadeks, tuleb saadetistega kaasa panna täiendavat dokumentatsiooni. Ohtlike materjalide funktsioon võimaldab klientidel talletada klassifikatsiooni teavet ja siduda seda lähetatavate kaupadega. Seda teavet saab kasutada saatmisdokumentide ettevalmistamise hõlbustamiseks.

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Managementi ohtlike materjalide funktsioonid pakuvad kasulike tooteteabe väljade ja nendega seotud funktsioonide kogumit, mis aitab salvestada ohtlike toodetega seotud teavet ja viidata sellele. Need funktsioonid aitavad ka luua ja printida saadetise dokumente, mis sisaldavad sama teavet mistahes ohtlike materjalide kohta, mida te lähetate. Siiski ei muuda süsteem teie kaupa automaatselt nõuetele vastavaks teie riigis või piirkonnas kohalduvatele määrustele. Kuigi need tööriistad on ette nähtud selleks, et aidata teil järgida ühiseid määrusi, ei ole need iseenesest piisavad ega nende piisavus pole garanteeritud. Teie organisatsioon vastutab kõigi kohaldatavate määruste ja nende täitmiseks vajalike sammude eest.

Enne kui saate seda funktsiooni kasutada, on vaja teha järgmised seadistused.

- **Toote teabehaldus:** saate seadistada väljastatud toodetele rakendatavaid koode.
- **Laohaldus:** saadetise teabe printimiseks saate kasutada täiendavaid tarnedokumente.

## <a name="product-information-management"></a>Tooteteabe haldus

Toote teabehalduses on olemas valik seadistustabeleid, kus saate lisada viiteteabe, mis on esitatud ohtlike kaupade loendites maantee-, õhu- ja meretranspordi jaoks.

Siin on mõned määrused, millele sageli viidatakse.

- **ADR** – määrused, mis on seotud ohtlike kaupade rahvusvahelise autoveoga
- **CFR 49** – Ameerika Ühendriikide määrused ohtlike kaupade veo kohta
- **IMDG** – rahvusvaheline ohtlike kaupade (IMDG) kood
- **IATA** – Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade määrused

Kõigis neis määrustes on viitekoode sisaldav ohtlike kaupade loend. Iga transporditüübi loendid on kombineeritud rahvusvaheliste ühisklassifikaatoritega. Supply Chain Management pakub nende loendite ühiskasutatavate koodide viitetabeli. Igal loendil on ka mõned unikaalsed koodid, mida saab määratleda.

Selle teabe konfigureerimise alustamiseks looge määrus, mida saate kasutada algsete parameetrite konfigureerimiseks.

## <a name="warehouse-management"></a>Laohaldus

Kui saadetis on ette valmistatud, saab printida mitu uut aruannet. Need aruanded kasutavad teavet, mida olete toote teabehalduses seadistanud.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]