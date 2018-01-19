--- 
title: " Järjepidevuse graafikute määratlemine"
description: "See teema selgitab järjepidevusprogrammi (teisisõnu korduvate tellimuste) seadistamist."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f99b3b71e46aae1e510cc24efe2f99f1a258fa1
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="define-continuity-schedules"></a> Järjepidevuse graafikute määratlemine

[!include[task guide banner](../includes/task-guide-banner.md)]

See teema selgitab järjepidevusprogrammi (teisisõnu korduvate tellimuste) seadistamist. Selles teemas kasutatakse demoettevõtte USRT andmeid.


## <a name="create-continuity-program"></a>Järjepidevusprogrammi loomine
1. Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevusprogrammid.
2. Klõpsake valikut Uus.
3. Tippige väljale Graafiku ID järjepidevuse graafiku ID
4. Tehke väljal Tellimuse algus valik Esimene sündmus.
    * Kui klient esitab uue järjepidevusprogrammi tellimuse, on toote lähetamiseks kaks võimalust. 1. Esimene sündmus: saadetakse järjepidevusprogrammi esimene toode.  2. Praegune sündmus: saadetakse praegune toode. Näide. Kolme kuu programm, klient saab programmi kolmanda toote.  
5. Valige Jah, et küsitaks tellimuse alguskuupäeva.
6. Klõpsake käsku Lisa rida.
7. Tippige väljale Kaubakood esimese toote kaubakood (0013).
8. Tüüp PP.
9. Sisestage kuupäev, millal esimene toode on tellimiseks valmis.
10. Klõpsake käsku Lisa rida.
11. Sisestage väljale Kaubakood väärtus 0014.
12. Eemaldage väljalt Kuupäevaintervalli kood väärtus, et väli oleks tühi.
    * Selle protseduuri puhul kustutage kuupäevaintervall. Kuupäev määratakse astmeliselt esimese kauba alguskuupäevast.  
13. Siia saab sisestada toodete tarnimise intervalli. Tippige 30.
    * Igakuise programmi puhul sisestatakse intervalliks 30 päeva.  
14. Klõpsake käsku Lisa rida.
15. Sisestage väljale Kaubakood väärtus 0015.
16. Tippige Lõpp.
17. Klõpsake nuppu Salvesta.

## <a name="assign-to-continuity-item"></a>Järjepidevale kaubale määramine
1. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
2. Valige kaup 0016.
    * Selle protseduuri puhul valige kauba number 0016. Tavaliselt olete loonud väljastatud toote, millele on rakendatud järjepidevuse äriloogika, kui see pannakse kõnekeskuses müügitellimusse.  
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake nuppu Redigeeri.
5. Laiendage või ahendage jaotist Müük.
6. Siia saate sisestada järjepidevusprogrammi, mida see kaup esindab. Tippige varem loodud graafiku ID.
    * Kui see kaup kõnekeskuses müüakse, rakendatakse valitud järjepidevusprogrammist täiendav äriloogika.  
7. Klõpsake nuppu Salvesta.


