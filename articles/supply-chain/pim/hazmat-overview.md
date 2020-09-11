---
title: Ohtlike materjalide ülevaade
description: Selles teemas antakse ülevaade funktsioonidest, mis on seotud ohtlike materjalide käitlemise ja dokumenteerimisega tooteteabe ja laohalduse ajal.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 227111f4703d9dc381270382dcb796874d7de937
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699605"
---
# <a name="hazardous-materials-overview"></a>Ohtlike materjalide ülevaade

[!include [banner](../includes/banner.md)]

Tarne-ja transpordimääruste nõuetele vastavuse säilitamiseks peavad organisatsioonid, kes tarnivad materjale, mis liigitatakse ohtlikuks kaubaks, lisama saadetistele täiendavaid pabereid. Ohtlike materjalide funktsioon võimaldab klientidel talletada teavet, mis on seotud väljastatud kaupadega. Seda teavet saab kasutada saatmisdokumentide ettevalmistamise hõlbustamiseks. Organisatsioonil, kes tarnib ohtlikke kaupu, peavad saatmisprotsessi haldamiseks olema oma protsessid ja protseduurid. Microsoft Dynamics 365 Supply Chain Management on tööriist, mis aitab genereerida nõutavaid dokumente.

Järgmisel joonisel on kuvatud ohtlike materjalide funktsiooni häälestamise ja kasutamise toimingud.

![Ohtlike materjalide funktsiooni häälestamine ja kasutamine](media/hazmat-overview.png "Ohtlike materjalide funktsiooni häälestamine ja kasutamine")

Ohtlike materjalide funktsioon häälestatakse tooteteabe halduses ja see pakub dokumente, mida saab printida laohalduse kaudu. Seetõttu on need alad laias laastus kaks peamist valdkonda, kus saate üle vaadata, häälestada ja kasutada seda funktsiooni funktsionaalsust.

- **Toote teabehaldus** – saate häälestada väljastatud toodetele rakendatavaid koode.
- **Laohaldus** – töö täiendavate saatedokumentidega, mis prinditakse saadetiste jaoks.

> [!IMPORTANT]
> Supply Chain Managementi ohtlike materjalide funktsioonid pakuvad kasulike tooteteabe väljade ja nendega seotud funktsioonide kogumit, mis aitab salvestada ohtlike toodetega seotud teavet ja viidata sellele. Need funktsioonid aitavad ka luua ja printida saadetise dokumente, mis sisaldavad sama teavet mistahes ohtlike materjalide kohta, mida te lähetate. Siiski ei muuda süsteem teie kaupa automaatselt nõuetele vastavaks teie riigis või piirkonnas kohalduvatele määrustele. Kuigi need tööriistad on ette nähtud selleks, et aidata teil järgida ühiseid määrusi, ei ole need iseenesest piisavad ega nende piisavus pole garanteeritud. Teie organisatsioon vastutab kõigi kohaldatavate määruste ja nende täitmiseks vajalike sammude eest.

## <a name="product-information-management"></a>Tooteteabe haldus

Toote teabehaldus pakub valikut häälestustabeleid, kuhu saate sisestada viiteteabe ohtlike kaupade loenditesse maantee-, õhu- ja meretranspordi jaoks.

Selle funktsiooni väljatöötamisel viidati järgmistele ühistele määrustele.

- **ADR** – määrused, mis on seotud ohtlike kaupade rahvusvahelise autoveoga
- **CFR 49** – Ameerika Ühendriikide määrused ohtlike kaupade veo kohta
- **IMDG** – rahvusvaheline ohtlike kaupade (IMDG) kood
- **IATA** – Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade määrused

Igas määruses on sätestatud ohtlike kaupade ja viitekoodide standardiseeritud loendid. Seetõttu pakub Supply Chain Management nende ühiste koodide loendite viitetabeli. Igal loendil on ka mõned unikaalsed koodid, mida saate määratleda.

Lisateabe saamiseks ohtlike materjalide määruste ja väärtuste häälestamise ja asjakohastele toodetele väärtuste määramise kohta lugege järgmistest teemadest.

- [Ohtlike materjalide häälestamine](hazmat-setup.md)
- [Ohtlikud materjalid toodetes, tellimustes, saadetistes ja koormates](hazmat-items.md)

## <a name="warehouse-management"></a>Laohaldus

Kui valmistate saadetist ette laohalduses, saate printida mitu uut aruannet, mis kasutavad tooteteabe halduses häälestatud teavet. Lisateavet saadaolevate aruannete ja nende kasutamise kohta leiate teemast [Ohtlike materjalide päringud ja aruanded](hazmat-reports.md).