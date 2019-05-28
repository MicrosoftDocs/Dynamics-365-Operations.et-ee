---
title: Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine
description: See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fd8738cfd3466464c9fec1760e9a369ff3a4a67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568231"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded. Salvestamisel kasutatakse demoettevõtte USMF-i.


## <a name="create-an-aging-period-definition"></a>Aegumisperioodi määratluse loomine
1. Tehke valik Krediit ja sissenõuded > Seadistus > Aegumisperioodi määratlused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Aegumisperioodi määratlus.
4. Sisestage väärtus väljale Kirjeldus.
5. Uue aegumisperioodi lisamiseks klõpsake käsku Lisa allolevad.
6. Sisestage aegumisaruannetel kuvatav kirjeldus väljale Periood.
7. Sisestage arv väljale Ühik.
8. Valige suvand väljal Intervall.
    * Pearaamatu periood vastab teie pearaamatu kalendrile. Päev, nädal, kuu, kvartal ja aastad määratlevad kuupäeva tüübi järgi intervalli pikkuse. Valik Piiramatu valib kõik kanded enne või pärast eelmist perioodi, sõltuvalt sellest, kas see on esimene või viimane periood.  
9. Valige suvand väljal Aegumise indikaator.
10. Valige ruudustiku päisest periood. Aegumisperioodi määratluse vanima perioodi kirjeldamiseks värskendage kirjeldust.
11. Sisestage aegumisperioodi uus kirjeldus väljale Periood.
12. Sulgege leht.

## <a name="age-the-balances"></a>Saldode aegunuks märkimine
1. Tehke valik Krediit ja sissenõuded > Perioodilised ülesanded > Klientide saldode aegumine.
2. Valige loodud aegumisperioodi määratlus väljal Aegumisperiood.
    * Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis.  
    * Vaikimisi töödeldakse kõiki kliente. Saate seda valikut kasutada ühe kliendikausta sissenõuete arvutamiseks.  
    * Valige kandest kuupäev, mida aegumiseks kasutada.  
    * Valige aegumise jaoks „aegunud seisuga” kuupäev. Vaikimisi on valitud tänane kuupäev, ent kui muudate sellel väljal valikuks Valitud kuupäev, saate valida mistahes kuupäeva. Pakktöötluseks kasutage tänast kuupäeva.  
3. Laiendage valikut Ettevõtete vahemik. Saate valida hetketõmmisesse kaasatavad ettevõtted. Praegune ettevõte on vaikimis valitud.
4. Klõpsake nuppu OK hetketõmmise töötlemiseks. See võtab veidi aega, nii et oodake, kuni liugur on kadunud, ja kontrollige, kas sõnumikeskuses on sõnum.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Saldode vaatamine loendis Aegunud saldod ja lehel Sissenõue.
1. Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.
    * Loendilehel kuvatakse kliendi saldod. Aegumise ikoon näitab vanima kande aegumisperioodi.  
2. Valige saldoga klient.
3. Laiendage jaotise Aegumine kiirinfo ala, et näha aegunud saldosid.
    * Kiirinfo aegumisperioodi määratluse kohta võetakse parameetrites määratud aegumisperioodi vaikemääratlusest. Saate seda muuta menüüd Sissenõue kasutades.  

