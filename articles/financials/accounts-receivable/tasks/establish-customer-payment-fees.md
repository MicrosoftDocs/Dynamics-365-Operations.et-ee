--- 
title: "Kliendi maksetasude määramine"
description: Looge kliendimaksete maksetasud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 659f4560747cea73c61a9b748a980946ca252bd6
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-fees"></a>Kliendi maksetasude määramine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Looge kliendimaksete maksetasud.

See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Müügireskontro > Maksete seadistus > Maksetasu.
2. Klõpsake valikut Uus.
3. Sisestage tasu ID väljale Tasu ID.
    * Tasu ID kuvatakse makse töölehtedel, mistõttu muutke see kirjeldavaks, et aru saada, millist tasu hinnatakse.  
4. Sisestage tasu nimi väljale Nimi.
5. Sisestage tasu kirjeldus väljale Tasu kirjeldus.
6. Valige, kas tasu määratakse kliendi või pearaamatu kontole.
    * Kui hinnatakse kliendi tasu, valige suvand Klient. Kui tasu hinnatakse teie organisatsiooni kuluna, valige Pearaamat. Selle ülesande puhul valige Klient.  
7. Valige töölehe tüüp, mis saab seda maksetasu kasutada.
    * Nende tasude kasutamisel kliendimakseteks on töölehe tüübiks tõenäoliselt Kliendimakse.  
8. Klõpsake nuppu Salvesta.
9. Klõpsake suvandit Maksetasu seadistus.
    * Makse tasu seadistust kasutatakse kriteeriumide määratlemiseks, mil maksetasu hinnatakse.  Näiteks saate määrata, et tasu arvutatakse, kui pangakontoks on USMF OPER ja makseviisiks on tšekk.  
10. Valige kas Tabel, Grupp või Kõik, et määratleda, millistele pangakontodele see tasu määratakse.
    * Kui valite suvandi Kõik, võidakse seda tasu hinnata kõigil pangakontodel.  Valides suvandi Tabel, võidakse seda tasu hinnata ainult teie valitud pangakontol. Suvandi Grupp valimisel võidakse seda tasu hinnata ainult valitud pangagrupi pangakontodel.  
11. Valige kas pangagrupp või pangakonto.
    * Suvandi Tabel valimisel kuvab otsing pangakontod. Suvandi Grupp valimisel kuvab otsing pangagrupid.  
12. Klõpsake loendis valitud real olevat linki.
13. Valige Makseviis, mis selle tasu puhul määratakse.
    * Näiteks võite määrata tasu klientidele, kui nad saadavad makseid pigem tšekina kui elektroonilise maksena.  
14. Otsige loendist ja valige soovitud kirje.
15. Vajaduse korral sisestage makse valuuta.
    * Makse valuutat kasutatakse tasu määramise täiendavate kriteeriumidena.  Näiteks võib teie pank nõuda lisatasu USA dollarites saadud maksete eest, kuna nad teevad üldjuhul tehinguid ainult eurodes.  
16. Valige, kas tasu on protsent, summa või intervall.
17. Sisestage kas tasu protsent või summa.
    * Kui välja Protsent/summa väärtuseks on Protsent, on siin sisestatud väärtus protsent. Kui välja Protsent/summa väärtuseks on Summa, on siin sisestatud väärtus summa. Kui välja Protsent/summa väärtuseks on Intervall, kasutage kihtide määratlemiseks vahekaarti Intervall.  
18. Valige tasu valuuta väljalt Tasu valuuta.
    * See on valuuta, milles tasu luuakse.  
19. Klõpsake nuppu Salvesta.


