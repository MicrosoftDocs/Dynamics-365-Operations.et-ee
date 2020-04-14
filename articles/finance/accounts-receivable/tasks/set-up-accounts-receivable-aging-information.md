---
title: Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine
description: See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e3c1ec73da27a08aa7a6cd859d1adac772916e4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140169"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine

[!include [banner](../../includes/banner.md)]

See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded. Salvestamisel kasutatakse demoettevõtte USMF-i.


## <a name="create-an-aging-period-definition"></a>Aegumisperioodi määratluse loomine
1. Avage **Navigeerimispaan > Moodulid > Krediit ja sissenõudmised > Häälestus > Aegumisperioodi definitsioonid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Aegumisperioodi definitsioon**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Klõpsake nuppu **Lisa alla**, et sisestada uus aegumisperiood.
6. Sisestage väljale **Periood** kirjeldus aegumisaruannetel kuvamiseks.
7. Sisestage arv väljale **Ühik**.
8. Valige suvand väljal **Intervall**. Pearaamatu periood vastab teie pearaamatu kalendrile. Päev, nädal, kuu, kvartal ja aastad määratlevad kuupäeva tüübi järgi intervalli pikkuse. Valik Piiramatu valib kõik kanded enne või pärast eelmist perioodi, sõltuvalt sellest, kas see on esimene või viimane periood.  
9. Valige suvand väljal **Aegumise näidik**.
10. Valige ruudustiku päisest periood. Aegumisperioodi määratluse vanima perioodi kirjeldamiseks värskendage kirjeldust.
11. Sisestage väljale **Periood** uus aegumisperioodi kirjeldus.
12. Sulgege leht.

## <a name="age-the-balances"></a>Saldode aegunuks märkimine
1. Avage **Krediit ja sissenõudmised > Perioodilised ülesanded > Kliendisaldode ajatamine**.
2. Valige väljal **Aegumisperioodi definitsioon** loodud aegumisperioodi definitsioon.
    + Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis.  
    + Vaikimisi töödeldakse kõiki kliente. Saate seda valikut kasutada ühe kliendikausta sissenõuete arvutamiseks.  
    + Valige kandest kuupäev, mida aegumiseks kasutada.  
    + Valige aegumise jaoks „aegunud seisuga” kuupäev. Vaikimisi on valitud tänane kuupäev, ent kui muudate sellel väljal valikuks Valitud kuupäev, saate valida mistahes kuupäeva. Pakktöötluseks kasutage tänast kuupäeva.  
3. Laiendage **Ettevõtte** vahemikku. Saate valida hetketõmmisesse kaasatavad ettevõtted. Praegune ettevõte on vaikimis valitud.
4. Klõpsake **Ok** hetktõmmise töötlemiseks. See võtab veidi aega, nii et oodake, kuni liugur on kadunud, ja kontrollige, kas sõnumikeskuses on sõnum.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Saldode vaatamine loendis Aegunud saldod ja lehel Sissenõue.
1. Avage **Krediit ja sissenõudmised > Sissenõudmised > Aegunud kliendisaldod**. Loendilehel kuvatakse kliendi saldod. Aegumise ikoon näitab vanima kande aegumisperioodi.  
2. Valige saldoga klient.
3. Laiendage kasti **Aegumise fakt** ala, et näha aegunud saldosid. Kiirinfo aegumisperioodi määratluse kohta võetakse parameetrites määratud aegumisperioodi vaikemääratlusest. Saate seda muuta menüüd Sissenõue kasutades.  

