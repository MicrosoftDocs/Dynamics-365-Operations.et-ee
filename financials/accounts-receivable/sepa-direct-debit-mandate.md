---
title: "SEPA otsedeebeti loa häälestamine"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA otsedeebeti loa häälestamine



Ühtse euromaksete piirkonna (Single Euro Payment Area, SEPA) otsekorraldus võimaldab kreeditoril võtta vahendeid kliendi pangakontolt eeldusel, et klient on andnud kreeditorile allkirjastatud loa. Kliendi allkirjastatud luba volitab kreeditori makset koguma ja annab kliendi pangale juhise see välja maksta. See teema on korraldatud näidata SEPA otsekorralduse volituste loomise protsessi.

## <a name="prerequisites"></a>Eeltingimused
Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

| Kategooria       | Eeltingimus                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Riik/regioon | Juriidilise isiku peamine aadress peab olema järgmistes riikides/regioonides: Austria, Belgia, Saksamaa, Hispaania, Prantsusmaa, Itaalia või Holland. |

1. Otsekorralduse volituste numbriseeria seadistatud iga direct debit mandaadi peab olema kordumatu number. Looge lehel **Numbriseeriad** otsekorralduse lubade numbriseeria. Selle identifikaatoriga määrate numbriseeria otsekorralduse lubade süsteemile lehel **Müügireskontro parameetrid**.

2. Seadista Müügireskontro parameetrid otsekorralduse volituste kasutamise eest ning **Müügireskontro parameetrid** lehe otsekorralduse volituste parameetrite seadistamiseks. Saate seadistada parameetreid, edasi on **otse** sakk, muuta väärtused, kui vaja. Siis on **Numbriseeriad** vahekaardil, muudetud on **otsene deebet mandaadi ID** numbriseeriaga, mille seadistasite varem välja.

3. Koostatud maksevahendina, otsekorralduse mandaatide te peate seadistama otsekorralduse volituste maksmise meetod. Selle makseviisiga saate teha päringuid arvete kohta, mille jaoks loote otsekorralduse makseid. Seadistage lehel **Makseviisid** makseviis. Otsekorralduse lubadele makseviisi seadistamiseks tuleb järgida makseviisi puhul neid lisajuhiseid.

-   Tehke väljal **Makse tüüp** valik **Elektrooniline makse**.
-   Valikuline: Kui iga teie klientidel on mitu mandaatide, mis on **perioodi** valige **arve**. Iga arve kohta luuakse tasuma eraldi ja iga makse kasutab volitusi, mis on määratud arve.
-   Valige **Nõua luba** maksete loomiseks otsekorralduse lubadega. Valik **Nõua luba** on saadaval ainult juhul, kui teete valiku **Elektrooniline makse** väljal **Makse tüüp**.

Vt ka [otsekorralduse ülevaade](sepa-direct-debit-overview.md) 

