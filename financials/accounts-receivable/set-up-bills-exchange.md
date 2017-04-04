---
title: "Käskvekslite seadistamine"
description: "Teema käsitleb pangatähtede kuni häälestuse sammud."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Käskvekslite seadistamine

Teema käsitleb pangatähtede kuni häälestuse sammud.

Pangatäht on kirjalik või elektroonne tellimus kliendilt, mis määrab, et teine pool, enamasti pank peab maksma deklareeritud kogusest ettevõttele. Kui kasutate pangatähte müügitellimusarve või vaba tekstiga arve maksena, krediteerite kliendi konto. See krediit on kaitstud pangatähe üksusega seni, kuni klient on pangatähe tasunud. Tavaliselt näidatakse tasakaalustada arve veksli maksetähtpäeval. Kui saate pangalt teate, et arve on tasutud, saate selle pangatähe sulgeda. Joonistate veksli läbi oma panga emba-kumba järgnevatel aegadel:

-   Tähtaja päeval. Selline lähenemine on tuntud töövaldkonda kogumiseks.
-   Enne tähtaega, tavaliselt määratud maksetingimused, mis on loodud Kliendi hinnaalandi kuupäeva. Kande sisestamisel sisestatakse allahindlussumma kulukontole. Ülejäänud summa on teile kohustus, kuni pank saab kliendilt makse. Selline lähenemine on tuntud töövaldkonda allahindlust.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Käskvekslite sisestusreeglite seadistamine
Kasutada ka **kliendi sisestusreeglite** lehel saate seadistada sisestusreeglite, pangatähtede, protesti pangatähtede, rahaülekanded kogumiseks ja rahaülekanded allahindlust kasutatavad. Aastal ning **konto** number pärast veksli summade koondsumma,. See konto debiteerimise või krediteerimise pangatähe kande liigist olenevalt:
-   Pangatähtede, seda kontot debiteeritakse kui käskveksel on sisestatud ja kui sisestatakse rahaülekande allahindluse või rahaülekanne kogumiseks krediteeritakse.
-   Vaidlustatud pangatähe korral debiteeritakse seda kontot vaidlustatud pangatähe sisestamisel.
-   Kogumiseks mõeldud rahaülekannete korral debiteeritakse seda kontot kogumiseks mõeldud rahaülekande sisestamisel.
-   Allahindluseks mõeldud rahaülekannete korral debiteeritakse seda kontot allahindluseks mõeldud rahaülekande sisestamisel.

Aastal ning **lahendada konto** raha, kuhu soovite sisestada pangatähe summad number,. Seda kontot debiteeritakse pangatähe tasakaalustamisel. Aastal ning **käibemaksu ettemaksed** Millal pangatähti kasutatakse ettemaksed käibemaksusummade sisestamiseks konto number. Aastal ning **allahindluse konto passivat** number, kuhu soovite sisestada hinnaalandi summa rahaülekannete et hinnaalandit. Seda kontot krediteeritakse allahindluseks mõeldud rahaülekande sisestamisel.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Seadista Müügireskontro parameetrid mitteresidendi
Kohta ning **Müügireskontro parameetrid** lehekülg, sisestusreeglite jaoks pangatähed sisestatakse vaikimisi ning **pearaamatu ja käibemaksu** vahekaart. Numbriseeriad määratletud ning **Numbriseeriad** vahekaart.
Seadistage pangatähtede töölehe nimed.
------------------------------------------

Kohta ning **töölehtede nimed** lehekülg, vekslite kasutada viie töölehenimede loomist. Järgnevalt töölehega.
-   **Kliendi juhtida veksli** – luua juhtida Pangatähe tööleht töölehe nimi.
-   **Kliendi vaidlustatud pangatäht** – Loo töölehe nimi vaidlusta Pangatähe tööleht.
-   **Kliendi värskendatakse veksli** – Loo töölehe nimi värskendatakse Pangatähe tööleht.
-   **Kliendi Panga rahaülekanne** – Loo töölehe rahaülekande tööleht nimi.
-   **Kliendi settle veksli** – Loo töölehe nimi Settle Pangatähe tööleht.

Iga Pangatähe tööleht töölehe kanne lehel, sisestada teavet maksja kohta on **veksli** vahekaart. Pangatähe töölehe read on konteeritud, kuvatakse nende kohta on **pangatähe töölehe uurimise** leht ja **pangatähtede statistika** lehel.
Seadistage pangatähele maksemeetod.
-----------------------------------------------

Kohta ning **makseviisid** lehele, luua vähemalt üks makse mitteresidendi meetod. Kui tegutsete rohkem kui ühe pangaga, mis vastab iga pangale mitteresidendi rahaülekande vormingu seadistamine.
Seadistage pangatähe maksetasud.
-----------------------------------------

Maksetasu on klientidelt maksete kogumisprotsessiga seostatud kulu. Mitu maksetasu seadistus ridadel võib olla seotud iga makse tasu. Saate kontrollida, kuidas maksetasude vaikimisi summad arvutatakse seadistuse read. Näiteks saate luua seadistusread makseviisidele, maksetäpsustustele, valuutadele ja ajaperioodidele. Luua seadistuse read protsent või summa, mis põhineb päevase intervalliga. Näiteks saate seadistada viivise protsent, mis põhineb aeg, mille maksetähtaeg on ületatud. Kui panga kulud erinevad tasud erinevatele rahaülekande tüüpidele, nagu **kollektsiooni** või **Soodus**, seadistada eraldi makse tasu rida iga rahaülekande tüübi.
Seadistage ülekandetasud panga rahaülekande failide jaoks
------------------------------------------------

Kohta ning **panga** lehe, saate seadistada pangakulude iga rahaülekande faili, mis on loodud ülekandetasusid. Rahaülekande tasud sisestatakse siis, kui ülekanne on kinnitatud ja realiseeritud tasu summad on teada. Ülekande tasu erineda maksetega seotud tasud, mis on kogutud klientidelt ja töölehe ridadega.
Seadistage pangatähele dokumendi paigutus.
---------------------------------------------

Kohta ning **panga** klõpsake valikul **loodud**, ja määrake dokumendi paigutus, mis on vajalik kõigi pangakontode, et te luua trükitud pangatähtede dokumente.
Seadistage käskvekslile kliendid
--------------------------------------

Kohta ning **hotelli** lehekülg, iga kliendi kohta, kes on nõustunud veksli abil saate seadistada vaikimisi meetod makse mitteresidendi kohta ning **maksehäired** vahekaart.




