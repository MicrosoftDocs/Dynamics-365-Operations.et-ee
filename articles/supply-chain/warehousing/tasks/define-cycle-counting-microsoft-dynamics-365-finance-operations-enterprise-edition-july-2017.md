---
title: 'Tsüklilise inventuuri määratlemine '
description: Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24c4c27745a15f013d20b52efc6e36de848a0251
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916779"
---
# <a name="define-cycle-counting"></a>Tsüklilise inventuuri määratlemine  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada. See tegevuse salvestis näitab, kuidas seadistada inventuuritöö vaikeprioriteeti, lubada mobiilse seadme menüü-üksusel töödelda nii komplekteerimis- kui ka inventuuritoiminguid, lubada inventuuri läve käivitumist, kui asukoht saab tühjaks ja lubada tsüklilise inventuuri plaani teatud kauba kohta kindlas laos. Tavaliselt teeb need toimingud laojuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.


## <a name="set-the-priority-of-counting-work"></a>Inventuuritöö prioriteedi määramine
1. Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Ladu > Laohalduse parameetrid**.
2. Klõpsake vahekaarti **Tsükliline inventuur**.
3. Väljale **Vaikimisi tsüklilise inventuuri töö prioriteet** sisestage arv. See toiming muudab tsüklilise inventuuri töö prioriteeti võrreldes muud tüüpi töödega laos. Kui sisestate väiksema numbri kui muud tüüpi töödele, tõstate tsüklilise inventuuri töö prioriteeti.  
4. Klõpsake valikut **Salvesta**.
5. Sulgege leht.

## <a name="enable-the-mobile-device"></a>Lubage mobiilne seade
1. Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü-üksused**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Menüü-üksuse nimi**.
4. Sisestage väärtus väljale **Pealkiri**.
5. Väljal **Režiim** valige "Töö".
6. Seadke suvandi **Kasuta olemasolevat tööd** väärtuseks Jah. Kui määrate selle suvandi väärtuseks Jah, otsib süsteem olemasolevat tööd, kui kasutatakse mobiilse seadme menüü-üksust.  
7. Väljale **Juhtija** valige "Süsteemi suunatud". "Süsteemi suunatud" valimisel suunatakse laotöötaja tööklassides määratud avatud tööle. (Loome järgmisena need tööklassid.)  
8. Laiendage kiirkaarti **Tööklassid**. Järgmisena loome kaks tööklassi, mida kasutatakse selle mobiilse seadme menüü-üksusega. Menüü-üksuse kasutamisel esitatakse päring nende tööklasside kohta ja kasutajale kuvatakse kõrgeima prioriteediga töö.  
9. Klõpsake valikut **Uus**.
10. Väljale **Tööklassi ID** valige väärtus.
11. Klõpsake valikut **Uus**.
12. Väljale **Tööklassi ID** valige väärtus.
13. Paanil **Toimingupaan** klõpsake **Salvesta**.
14. Sulgege leht.
15. Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü-üksused**.
16. Otsige loendist ja valige soovitud kirje.
17. Valige puul äsjaloodud menüü-üksus.
18. Klõpsake valikut **Redigeeri**.
19. Klõpsake menüü-üksuse menüüsse lisamiseks noolt.
20. Klõpsake valikut **Salvesta**.

## <a name="create-a-counting-threshold"></a>Looge inventuurilävi
1. Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri läved**.
2. Klõpsake valikut **Uus**.
3. Väljale **Tsüklilise inventuuri läve ID** sisestage väärtus.
4. Seadke suvandi **Töötle tsüklilist inventuuri kohe** väärtuseks Jah.
5. Sisestage väärtus väljale **Kirjeldus**.
6. Klõpsake valikut **Salvesta**.
7. Klõpsake **Vali asukohad**.
8. Märkige loendis valitud rida.
9. Väljal **Kriteerium** valige väärtus.
10. Klõpsake valikut **OK**.
11. Sulgege leht.

## <a name="create-a-cycle-count-plan"></a>Looge tsüklilise inventuuri plaan
1. Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri plaanid**.
2. Klõpsake valikut **Uus**.
3. Väljale **Tsüklilise inventuuri plaani ID** sisestage väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Väljale **Maksimaalne tsükliliste inventuuride arv** sisestage arv.
6. Klõpsake valikut **Salvesta**.
7. Klõpsake **Vali asukohad**.
8. Märkige loendis valitud rida.
9. Väljal **Kriteerium** valige väärtus.
10. Klõpsake valikut **OK**.
11. Väljale **Päevi tsükliliste inventuuride vahel** sisestage arv. Näiteks kui väljale **Päevi tsükliliste inventuuride vahel** sisestatud 5, luuakse tsüklilisi inventuure iga viie päeva järel. Kuid kui tsüklilise inventuuri töö töödeldakse kolmandal päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, kaheksandal päeval.  
12. Klõpsake valikut **Salvesta**.
13. Klõpsake valikut **Uus**.
14. Sisestage arv väljale **Järjekorranumber**. Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini. Väärtus peab olema suurem kui 0 (null).  
15. Märkige loendis valitud rida.
16. Sisestage väärtus väljale **Kirjeldus**.
17. Klõpsake valikut **Salvesta**.
18. Klõpsake päringut **Määratle toode**.
19. Märkige loendis valitud rida.
20. Sisestage või valige väärtus väljal **Kriteeriumid**.
21. Klõpsake valikut **OK**.
22. Sulgege leht.

