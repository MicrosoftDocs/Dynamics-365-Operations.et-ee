---
title: Makseviisid
description: "Iga makse tüüp, mida jaemüüja nõustub peab olema konfigureeritud jaemüügi-ja kaubanduse Microsoft Dynamics 365 toiminguteks, kui süsteem on seadistatud. Selles artiklis kirjeldatakse seadistatavaid makse tüüpe ja kirjeldatakse nende seadistamise protsessi."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: MargoC
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b887fc5d03ea8982515e92725ce98cc416e56f9e
ms.openlocfilehash: 011beec07bf1ab858892ab1c374f1acf3839e877
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods"></a>Makseviisid

Iga makse tüüp, mida jaemüüja nõustub peab olema konfigureeritud jaemüügi-ja kaubanduse Microsoft Dynamics 365 toiminguteks, kui süsteem on seadistatud. Selles artiklis kirjeldatakse seadistatavaid makse tüüpe ja kirjeldatakse nende seadistamise protsessi.

Jaemüüjad võivad võtta müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega. Kuigi levinuim maksemeetod on sularaha, võivad jaemüüjad võtta tasu ka tšekkide, kaartide, kannetega jne. Iga mis vahendaja aktsepteerib liik peab olema konfigureeritud Dynamics 365 toiminguteks - jaemüügi kui süsteem on seadistatud. Järgmises loendis kirjeldatakse iga makse tüüp, mis võib luua Dynamics 365 toiminguteks - jaemüük:

-   **Sularaha** – raha valuuta füüsilises vormis (nt paberraha ja mündid). Valuuta võib olla ettevõtte valuuta või kaupluse kohalik valuuta.
-   **Tšekk ** – käibiv vahend, mille alusel saab määratud pangas välja võtta kindlas valuutas kindla summa. Tšekk kehtib tavaliselt kas tähtajatult või kuus kuud pärast väljaandmist, kui ei ole määratud muud kehtivusaega. See periood on erinev olenevalt tšeki koostanud pangast. Tšekke on erinevat tüüpi, nt tellimustšekid, vahetustšekid, esitajatšekid ja krosseeritud tšekid. Saate seadistada tšekid makseviisidena iga poe puhul. Tšekke saab vastu võtta valuutas, mis on määratletud kas ettevõtte või poe tasemel. Peate tšekid makseviisina seadistama, enne kui saate poes tšekki makseviisina aktsepteerida.
-   **Valuuta **– peamine makseviis lisaks ettevõtte vaikevaluutale. Mündid ja paberraha on mõlemad valuuta vormid. Valuuta makseviis esindab kogu valuutat, mida kasutatakse jaotises Jaemüük ja kaubandus. Enne selle makseviisi kasutamist peate häälestama valuutad ja määrama valuutadele jaemüügi vahetuskursi teabe.
-   **Kaart** – igat tüüpi kaardid, mida kasutatakse jaotises Jaemüük ja kaubandus, nt deebet- ja krediitkaardid. On mõistlik seadistada üks kaardimakseviis organisatsiooni tasemel, et esindada igat tüüpi kaarte. Poe tasemel häälestage makseviis igale kaardile või kaartide komplektile, mida töödeldakse samu sätteid kasutades. Peate häälestama turul saadaolevad tootja kaardid, näiteks deebet- ja krediitkaardid, enne kui neid saab kaupluses makseviisina aktsepteerida.
-   **Kreeditarve** – kreeditarved, mida väljastatakse või lunastatakse müügikohas. Kreeditarve võib olla kreedit- või tagastusarve, mis on väljastatud tagastusmüügiga. Kui kreediarveid saab üksnes osaliselt lunastada, väljastab programm uue kreeditarve uue saldo puhul. Uuel kreeditarvel on uus number. Kreediarvet saab kasutada ainult ühe korra ja süsteem peab arvestust kõigi kasutatud numbrite üle. Kirjet saab vaadata lehel **Krediitarve tabel**. Klient ei saa lunastada krediitarve väärtusest suuremat summat.
-   **Kinkekaart** – kinkekaardid, mis on müügikohas väljastatud ja lunastatud. Kinkekaartide puhul pole ülemakse lubatud.
-   **Kliendi konto** – maksed, mida saab esitada kliendi kontole müügi ajal kassaaparaadist. Selle makseviisi abil saate ka koguda müügiteavet või kliendispetsiifilisi allahindlusi, kui klient maksab muud makseviisi kasutades. Sel juhul tuleb teil häälestada kliendispetsiifiline teave.
-   **Punkte** – punkti, mis on hotelli koguneda kaudu lojaalsuse programmid. Kui loote lojaalsuse programmid, hotelli teenida punkte ja pereisa erineval viisil. Näiteks mõne püsikliendiprogrammi puhul saavad kliendid boonuspunkte lunastada allahindluse vormis või lausa makseviisna.

Jaotises Jaemüük ja kaubandus makseviiside seadistamiseks peate täitma järgmised ülesanded.

1.  Seadistage organisatsioonile makseviisid. Looge makseviisid, mida aktsepteerib kogu organisatsioon.
2.  Luua kogu asutuses kehtivaid tüübid ja numbreid. Kui krediit- või deebetkaarte aktsepteeritakse, peate looma ühe makseviisi kaarte ja seejärel luua kogu asutuses kehtivaid tüübid ja numbreid.
3.  Poe makseviisi seadistamine Seostada iga poe makseviisid ja sisestage poe omaseid sätteid iga makseviisi jaoks.
4.  Saate seadistada kaardi makseviisid kauplustes. Iga kaardi makseviise poest endale, kaardi installimise lõpule.



