---
title: Tööta konfiguratsioonidega
description: Selles teemas antakse ülevaade põhistsenaariumi töötamiseks globaliseerimisfunktsiooni tööruumist elektroonilise aruandluse (ER) konfiguratsioonide abil.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371905"
---
# <a name="work-with-configurations"></a>Tööta konfiguratsioonidega

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) konfiguratsioonid on üks elektrooniliste arveldusfunktsiooni komponentide põhikomplektidest. ER-i konfiguratsioon sisaldab failistruktuuri seadistust ja teisendusreeglite kogumeid andmete teisendamiseks kahel viisil:

- **Saate eksportida ER-vormingu** konfiguratsiooni – see konfiguratsioon teisendab andmed ühtsest sisestruktuurist (ER-mudel) elektroonilisesse failivormingusse.
- **ER-vormingu konfigureerimine** – see konfiguratsioon teisendab andmed elektroonilisest failivormingust ühtsesse sisestruktuuri (ER-mudel).

Lisaks väljaminevate elektrooniliste failide loomisele eelmääratletud vormingus kasutatakse ER-i konfiguratsioone üldiselt väliste veebiteenuste teadete sõelumiseks vastustena. See funktsioon aitab teil koostada konfigureeritava loogika, et saada kommunikatsiooni tulemusi väliskanalitega, teisendada need tulemused (koodid, sõnumid ja logid) kasutaja loetavaks struktuuriks ja seejärel edastada see teave klientrakendusele.

Elektroonilise arveldamise funktsioonis **ER**-konfiguratsioonide kasutamise alustamiseks peate need oma funktsiooniga seostama ja tegema need kättesaadavaks vahekaardil Konfiguratsioonid praeguse funktsiooniversiooni jaoks. Lingitud ER-i konfiguratsiooniga saate töötada, valides suvandi **Lisa** **, Kustuta**, **Redigeeri** või **Kuva**.

Enne kui saate lisada lingi ER-konfiguratsioonile, peab konfiguratsioon olemas olema teie Regulatiivse konfiguratsiooniteenuse (RCS) hoidlas. ER konfiguratsioonide ülevaatamiseks, mis on saadaval teie RCS-i hoidlas, järgige neid samme.

1. Logige oma RCS-i kontole sisse.
2. Valige tööruumis **Elektrooniline aruandlus** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.

Lisateavet selle kohta, kuidas luua uus ER konfiguratsioon või importida olemasolev ER konfiguratsioon globaalsest hoidlast, vt elektroonilist [aruandlust](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Seotud ER-i konfiguratsiooni kohandamiseks valige **vahekaardil** **Konfiguratsioonid** suvand Redigeeri praeguse elektroonilise arveldamise funktsiooni jaoks. Süsteem loob automaatselt ER-i konfiguratsiooni versiooni. Kui aktiivne konfiguratsioonipakkuja ei loonud praegust versiooni, loob süsteem tuletatud versiooni, mis kasutab teie konfiguratsioonipakkujat. Kui aktiivse konfiguratsioonipakkuja lõi praeguse versiooni, loob süsteem uue versiooni. Mõlemal juhul saate muuta loodud versiooni ja seejärel teha automaatselt kõik vajalikud uuendused.
