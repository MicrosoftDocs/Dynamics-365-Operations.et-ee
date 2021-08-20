---
title: EUR-00002 Laadimisaadressi määramine ühendusesisesele kandele
description: See protseduur näitab, kuidas määrata ühendusesisese kaubanduskande puhul laadimisaadressi.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68a62a26be418b7a0cb8e17532d022d76cd552411f438ffc5a0ddad589a9e476
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780789"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002 Laadimisaadressi määramine ühendusesisesele kandele

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas määrata ühendusesisese kaubanduskande puhul laadimisaadressi. Näiteks Saksamaa ettevõte tellib kaupu Saksamaa aadressiga hankijalt. Sellel hankijal on ladu Itaalias ja ta lähetab kaubad sealt. Tarne peab kajastuma intrastati aruandes. Sama kehtib klienditagastuste puhul.
See protseduur kohaldub kõigile Euroopa riikidele/piirkondadele. Ülesande loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Saksamaa, andmeid. Enne selle protseduuri läbimist tuleb konfigureerida intrastati aruandlus. See protseduur on mõeldud raamatupidajatele. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

1. Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus
    * Valige näiteks DE-001. Sellel hankija ettevõttel on Saksamaa aadress.  
4. Klõpsake nuppu OK.
5. Märkige loendis valitud rida.
6. Sisestage või valige väärtus D0001 väljal Kaubakood.
7. Klõpsake nuppu Salvesta.
8. Klõpsake toimingupaanil valikut Vastuvõtt.
9. Klõpsake valikut Transpordi üksikasjad.
10. Sisestage kuupäev ja kellaaeg väljale Laadimise kuupäev ja kellaaeg.
11. Klõpsake valikut Lisa aadress.
12. Klõpsake nuppu Uus ja looge uus aadress eesmärgiga Laadimine.
13. Tippige väljale Nimi või kirjeldus Itaalia.
14. Valige väärtuseks Laadimine.
    * Pange tähele, et aadressi eesmärk peab olema Laadimine  
15. Sisestage või valige väärtus ITA väljal Riik/piirkond.
16. Klõpsake nuppu Salvesta.
17. Sulgege leht.
18. Klõpsake nuppu Salvesta.
    * Kontrollige, et laadimisaadress oleks õige.  
19. Sulgege leht.
20. Klõpsake toimingupaanil valikut Ost.
21. Klõpsake käsku Kinnita.
22. Klõpsake toimingupaanil valikut Arve.
23. Klõpsake valikut Arve.
24. Sisestage väärtus väljale Arv.
25. Sisestage kuupäev väljale Arve kuupäev.
26. Rippdialoogi avamiseks klõpsake valikut Vaikimisi asukohast: toote sissetuleku kogus.
27. Valige Tellitud kogus väljal Ridade vaikekogus.
28. Klõpsake nuppu OK.
29. Klõpsake valikut Transpordi üksikasjad.
    * Kontrollige, et kaubad lähetati Itaaliast. Vajaduse korral saate laadimise üksikasju muuta.  
30. Sulgege leht.
31. Klõpsake valikut Sisesta.
32. Sulgege leht.
33. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.
34. Klõpsake käsku Ülekanne.
35. Tehke väljal Hankija arve valik Jah.
36. Klõpsake nuppu OK.
37. Klõpsake vahekaarti Üldine.
    * Otsige üles äsja loodud rida ja veenduge, et saatja saatis kaubad Itaaliast.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]