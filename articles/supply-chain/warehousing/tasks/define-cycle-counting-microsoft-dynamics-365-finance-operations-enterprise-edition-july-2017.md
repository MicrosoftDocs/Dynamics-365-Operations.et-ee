--- 
title: "Tsüklilise inventuuri määratlemine "
description: "Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="define-cycle-counting"></a>Tsüklilise inventuuri määratlemine  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada. See tegevuse salvestis näitab, kuidas seadistada inventuuritöö vaikeprioriteeti, lubada mobiilse seadme menüü-üksusel töödelda nii komplekteerimis- kui ka inventuuritoiminguid, lubada inventuuri läve käivitumist, kui asukoht saab tühjaks ja lubada tsüklilise inventuuri plaani teatud kauba kohta kindlas laos. Tavaliselt teeb need toimingud laojuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.


## <a name="set-the-priority-of-counting-work"></a>Inventuuritöö prioriteedi määramine
1. Avage Laohaldus > Seadistus > Laohalduse parameetrid.
2. Klõpsake vahekaarti Tsükliline inventuur.
3. Sisestage number väljale Tsüklilise inventuuri töö vaikeprioriteet.
    * See toiming muudab tsüklilise inventuuri töö prioriteeti võrreldes muud tüüpi töödega laos. Kui sisestate väiksema numbri kui muud tüüpi töödele, tõstate tsüklilise inventuuri töö prioriteeti.  
4. Klõpsake nuppu Salvesta.
5. Sulgege leht.

## <a name="enable-the-mobile-device"></a>Lubage mobiilne seade
1. Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Menüü-üksuse nimi.
4. Sisestage väärtus väljale Pealkiri.
5. Valige väljal Režiim suvand Töö.
6. Valige suvandi Kasuta olemasolevat tööd sätteks Jah.
    * Kui määrate selle suvandi väärtuseks Jah, otsib süsteem olemasolevat tööd, kui kasutatakse mobiilse seadme menüü-üksust.  
7. Valige väljal Suunaja suvand Süsteemi suunatud.
    * "Süsteemi suunatud" valimisel suunatakse laotöötaja tööklassides määratud avatud tööle. (Loome järgmisena need tööklassid.)  
8. Laiendage või ahendage jaotist Töö klassid.
    * Järgmisena loome kaks tööklassi, mida kasutatakse selle mobiilse seadme menüü-üksusega. Menüü-üksuse kasutamisel esitatakse päring nende tööklasside kohta ja kasutajale kuvatakse kõrgeima prioriteediga töö.  
9. Klõpsake valikut Uus.
10. Valige väärtus väljal Tööklassi ID.
11. Klõpsake valikut Uus.
12. Valige väärtus väljal Tööklassi ID.
13. Klõpsake nuppu Salvesta.
14. Sulgege leht.
15. Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü.
16. Otsige loendist ja valige soovitud kirje.
17. Valige puul äsjaloodud menüü-üksus.
18. Klõpsake nuppu Redigeeri.
19. Klõpsake menüü-üksuse menüüsse lisamiseks noolt.
20. Klõpsake nuppu Salvesta.

## <a name="create-a-counting-threshold"></a>Looge inventuurilävi
1. Avage Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri läved.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tsüklilise inventuuri läve ID.
4. Valige suvandi Töötle tsüklilist inventuuri kohe sätteks Jah.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Klõpsake nuppu Salvesta.
7. Klõpsake suvandit Valige asukohad.
8. Märkige loendis valitud rida.
9. Valige väärtus väljal Kriteeriumid.
10. Klõpsake nuppu OK.
11. Sulgege leht.

## <a name="create-a-cycle-count-plan"></a>Looge tsüklilise inventuuri plaan
1. Avage Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri plaanid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tsüklilise inventuuri plaani ID.
4. Sisestage väärtus väljale Kirjeldus.
5. Sisestage number väljale Tsükliliste inventuuride maksimumarv.
6. Klõpsake nuppu Salvesta.
7. Klõpsake suvandit Valige asukohad.
8. Märkige loendis valitud rida.
9. Valige väärtus väljal Kriteeriumid.
10. Klõpsake nuppu OK.
11. Sisestage number väljale Päevi tsükliliste inventuuride vahel.
    * Näiteks kui välja Päevi tsükliliste inventuuride vahel väärtuseks on määratud 5, luuakse tsüklilise inventuuri töö iga viie päeva järel. Kuid kui tsüklilise inventuuri töö töödeldakse kolmandal päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, kaheksandal päeval.  
12. Klõpsake nuppu Salvesta.
13. Klõpsake valikut Uus.
14. Sisestage number väljale Seerianumber.
    * Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini. Väärtus peab olema suurem kui 0 (null).  
15. Märkige loendis valitud rida.
16. Sisestage väljale Kirjeldus soovitud väärtus.
17. Klõpsake nuppu Salvesta.
18. Klõpsake valikut Määratle tootepäring.
19. Märkige loendis valitud rida.
20. Sisestage või valige väärtus väljal Kriteeriumid.
21. Klõpsake nuppu OK.
22. Sulgege leht.


