---
title: Käskvekslite seadistamine
description: Selles teemas kirjeldatakse käskvekslite seadistamise etappe.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7f5f62d33f6ffedb3fcefcdd9a83b922c1588df0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442268"
---
# <a name="set-up-bills-of-exchange"></a>Käskvekslite seadistamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse käskvekslite seadistamise etappe.

Pangatäht on kas kirjalik või elektrooniline kliendilt tellimus, mis määrab, et kolmas osapool (tavaliselt pank) peab ettevõttele maksma teatud kindla summa. Kui kasutate pangatähte müügitellimusarve või vaba tekstiga arve maksena, krediteerite kliendi konto. See krediit on kaitstud pangatähe üksusega seni, kuni klient on pangatähe tasunud. Tavaliselt tasakaalustatakse arve tähtajaks pangatähega. Kui saate pangalt teate, et arve on tasutud, saate selle pangatähe sulgeda. Panga kaudu saate pangatähe koostada järgmistel aegadel:

-   Tähtaja päeval. Seda lähenemist nimetatakse kogumiseks mõeldud rahaülekandeks.
-   Enne tähtaega, tavaliselt allahindluse kuupäeval, mis on määratud kliendile seadistatud maksetingimuste alusel. Kande sisestamisel sisestatakse allahindlussumma kulukontole. Ülejäänud summa on teile kohustus, kuni pank saab kliendilt makse. Seda lähenemisviisi nimetatakse allahindluseks mõeldud rahaülekandeks.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Käskvekslite sisestusreeglite seadistamine

Kasutage lehte **Kliendi sisestusreeglid**, et seadistada sisestusreeglid, mida saate kasutada pangatähega, vaidlustatud pangatähega, kogumiseks mõeldud rahaülekandega, allahindluseks mõeldud rahaülekandega. Väljal **Summakonto** valige summakonto, millele pangatähe summasid sisestada. Seda kontot debiteeritakse või krediteeritakse sõltuvalt käskveksli kande tüübist.
-   Pangatähtede korral debiteeritakse seda kontot pangatähe sisestamisel ja krediteeritakse kogumise rahaülekande või allahindluse rahaülekande sisestamisel.
-   Vaidlustatud pangatähe korral debiteeritakse seda kontot vaidlustatud pangatähe sisestamisel.
-   Kogumiseks mõeldud rahaülekannete korral debiteeritakse seda kontot kogumiseks mõeldud rahaülekande sisestamisel.
-   Allahindluseks mõeldud rahaülekannete korral debiteeritakse seda kontot allahindluseks mõeldud rahaülekande sisestamisel.

Väljal **Tasakaalusta konto** valige sularahakonto, millele pangatähe summad sisestada. Seda kontot debiteeritakse pangatähe tasakaalustamisel. Väljal **Käibemaksu ettemaksed** valige summakonto, millele käibemaksu summasid sisestada siis, kui pangatähti kasutatakse ettemaksudeks. Väljal **Allahindluse konto kohustused** valige konto, kuhu soovite sisestada allahindluse rahaülekannete allahindlussumma. Seda kontot krediteeritakse allahindluseks mõeldud rahaülekande sisestamisel.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Käskvekslite jaoks müügireskontro parameetrite seadistamine

Lehel **Müügireskontro parameetrid** sisestatakse käskvekslite jaoks vaikimisi sisestusreeglid vahekaardil **Pearaamat ja käibemaks**. Numbriseeriad määratletakse vahekaardil **Numbriseeriad**.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Seadistage pangatähtede töölehe nimed.


Lehel **Töölehtede nimed** looge käskvekslite kasutamiseks vähemalt viis töölehe nime. Töölehe tüübid on järgmised.
-   **Kliendi koostatud pangatäht** – looge valiku Koosta pangatähe tööleht jaoks töölehe nimi.
-   **Kliendi vaidlustatud pangatäht** – looge valiku Vaidlusta pangatähe tööleht jaoks töölehe nimi.
-   **Kliendi uuesti koostatud pangatäht** – looge valiku Koosta pangatähe tööleht uuesti jaoks töölehe nimi.
-   **Kliendi pangaülekanne** – looge rahaülekande töölehe jaoks töölehe nimi.
-   **Kliendi tasakaalustuse pangatäht** – looge valiku Tasakaalusta pangatähe tööleht jaoks töölehe nimi.

Iga käskveksli töölehe kviitungi lehe vahekaardil **Käskveksel** sisestage teave käskveksli kohta. Pärast käskveksli tööleheridade sisestamist saate vaadata neid lehel **Käskveksli töölehepäringu kuvamine** ja lehel **Pangatähtede statistika**.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Seadistage pangatähele maksemeetod.

Lehel **Makseviisid** seadistage käskvekslite jaoks vähemalt üks makseviis. Kui teil on ärisuhted mitme pangaga, seadistage makseviis, mis vastab rahaülekande vormingule, mida iga pank käskvekslite jaoks nõuab.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Seadistage pangatähe maksetasud.

Maksetasu on klientidelt maksete kogumisprotsessiga seostatud kulu. Iga maksetasuga saab siduda mitu maksetasu seadistusrida. Saate kasutada seadustuse ridu kontrollimaks, kuidas maksetasude vaikesummasid arvutatakse. Näiteks saate luua seadistusread makseviisidele, maksetäpsustustele, valuutadele ja ajaperioodidele. Samuti saate luua seadistusridasid päevaintervallidel põhineva protsendi või summa jaoks. Näiteks saate seadistada viiviseprotsendi, mis põhineb makse tähtaja ületanud ajalisel kestusel. Kui pank määrab erinevate rahaülekannete tüüpidele erinevaid tasusid, nagu **Kogum** või **Allahindlus**, seadistage iga rahaülekande tüübi jaoks eraldi maksetasu rida.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Seadistage ülekandetasud panga rahaülekande failide jaoks

Lehel **Pangakontod** saate seadistada ülekandetasud, mida pank võtab iga loodava ülekandefaili jaoks. Rahaülekande tasud sisestatakse siis, kui ülekanne on kinnitatud ja realiseeritud tasu summad on teada. Ülekandetasud erinevad maksetasudest, mis on klientidelt kogutud ja töölehe reale lisatud.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Seadistage pangatähele dokumendi paigutus.

Lehel **Pangakontod** klõpsake nuppu **Seadistus** ja määrake pangakontole, millele loote prinditud pangatähe dokumente, nõutud dokumendi paigutus.

## <a name="set-up-customers-for-bills-of-exchange"></a>Seadistage käskvekslile kliendid

Lehe **Kliendid** vahekaardil **Makse vaikeandmed** saate iga kliendi jaoks, kes on nõustunud maksma käskvekslit kasutades, seadistada käskveksli vaikimisi makseviisi.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]