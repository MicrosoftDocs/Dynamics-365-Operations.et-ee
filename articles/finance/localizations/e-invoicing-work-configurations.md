---
title: Konfiguratsioonidega töötamine
description: See artikkel annab ülevaate peamiseks stsenaariumiks globaalsete funktsioonide tööruumist elektroonilise aruandluse (ER) konfiguratsioonide töötamiseks.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283051"
---
# <a name="work-with-configurations"></a>Konfiguratsioonidega töötamine

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
