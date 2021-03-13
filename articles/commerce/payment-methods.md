---
title: Makseviisid
description: Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel. Selles artiklis kirjeldatakse seadistatavaid makse tüüpe ja kirjeldatakse nende seadistamise protsessi.
author: rubencdelgado
manager: AnnBe
ms.date: 06/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 54bff6b7962ade09ea5c1f5f8d7721757dea1fc3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012362"
---
# <a name="payment-methods"></a>Makseviisid

[!include [banner](includes/banner.md)]

Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel. Selles artiklis kirjeldatakse seadistatavaid makse tüüpe ja kirjeldatakse nende seadistamise protsessi.

Jaemüüjad võivad võtta müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega. Kuigi levinuim maksemeetod on sularaha, võivad jaemüüjad võtta tasu ka tšekkide, kaartide, kannetega jne. Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel Dynamics 365 Commerceis. Järgmises loendis kirjeldatakse kõiki maksetüüpe, mille saab seadistada.

- **Sularaha** – raha valuuta füüsilises vormis (nt paberraha ja mündid). Valuuta võib olla ettevõtte valuuta või kaupluse kohalik valuuta.
- **Tšekk** – käibiv vahend, mille alusel saab määratud pangas välja võtta kindlas valuutas kindla summa. Tšekk kehtib tavaliselt kas tähtajatult või kuus kuud pärast väljaandmist, kui ei ole määratud muud kehtivusaega. See periood on erinev olenevalt tšeki koostanud pangast. Tšekke on erinevat tüüpi, nt tellimustšekid, vahetustšekid, esitajatšekid ja krosseeritud tšekid. Saate seadistada tšekid makseviisidena iga poe puhul. Tšekke saab vastu võtta valuutas, mis on määratletud kas ettevõtte või poe tasemel. Peate tšekid makseviisina seadistama, enne kui saate poes tšekki makseviisina aktsepteerida.
- **Valuuta**– peamine makseviis lisaks ettevõtte vaikevaluutale. Mündid ja paberraha on mõlemad valuuta vormid. Valuuta makseviis kajastab kogu valuutat, mida kasutatakse. Enne selle makseviisi kasutamist peate häälestama valuutad ja määrama valuutadele vahetuskursi teabe.
- **Kaart** – igat tüüpi kaardid, mida kasutatakse, nt deebet- ja krediitkaardid. On mõistlik seadistada üks kaardimakseviis organisatsiooni tasemel, et esindada igat tüüpi kaarte. Poe tasemel häälestage makseviis igale kaardile või kaartide komplektile, mida töödeldakse samu sätteid kasutades. Peate häälestama turul saadaolevad tootja kaardid, näiteks deebet- ja krediitkaardid, enne kui neid saab kaupluses makseviisina aktsepteerida.
- **Kreeditarve** – kreeditarved, mida väljastatakse või lunastatakse müügikohas. Kreeditarve võib olla kreedit- või tagastusarve, mis on väljastatud tagastusmüügiga. Kui kreediarveid saab üksnes osaliselt lunastada, väljastab programm uue kreeditarve uue saldo puhul. Uuel kreeditarvel on uus number. Kreediarvet saab kasutada ainult ühe korra ja süsteem peab arvestust kõigi kasutatud numbrite üle. Kirjet saab vaadata lehel **Krediitarve tabel**. Klient ei saa lunastada krediitarve väärtusest suuremat summat.
- **Kinkekaart** – kinkekaardid, mis on müügikohas väljastatud ja lunastatud. Kinkekaartide puhul pole ülemakse lubatud. Kõigil kinkekaartidel peaksid olema kaardinumbri vastendused. 
- **Kliendi konto** – maksed, mida saab esitada kliendi kontole müügi ajal kassaaparaadist. Selle makseviisi abil saate ka koguda müügiteavet või kliendispetsiifilisi allahindlusi, kui klient maksab muud makseviisi kasutades. Sel juhul tuleb teil häälestada kliendispetsiifiline teave.
- **Boonuspunktid** – punktid, mida kliendid koguvad püsikliendiprogrammide. Kui loote püsikliendiprogramme, saavad kliendid teenida punkte ja lunastada neid erineval moel. Näiteks mõne püsikliendiprogrammi puhul saavad kliendid boonuspunkte lunastada allahindluse vormis või lausa makseviisna.

Makseviiside seadistamiseks täitke järgmised ülesanded.

1. Seadistage organisatsioonile makseviisid. Looge makseviisid, mida aktsepteerib kogu organisatsioon.
2. Üleorganisatsiooniliste kaarditüüpide ja kaardi numbrite loomine. Kui aktsepteeritakse krediit- või deebetkaarte, peate looma ühe makseviisi kaartidele ja looma seejärel üleorganisatsioonilised kaarditüübid ja kaardi numbrid.
3. Seadistage kaupluse makseviis. Seostage makseviisid iga kauplusega ja seejärel sisestage iga kaupluse makseviisile kauplusepõhised sätted.
4. Seadistage kauplustele kaardimakseviisid. Tehke kaardiseadistus kõikidele kaardimakseviisidele, mida kauplus aktsepteerib.
