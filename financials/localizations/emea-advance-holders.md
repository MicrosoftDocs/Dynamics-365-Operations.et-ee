---
title: Avansisaajad
description: Siin on teavet eelnevalt omaniku funktsiooni Microsoft Dynamics 365 toiminguteks.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262574
ms.assetid: 87924785-6032-4125-8279-5b1a758f4d80
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 8cfe98e3859778e4fdc61f22b437cb1b4d004549
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holders"></a>Avansisaajad

Siin on teavet eelnevalt omaniku funktsiooni Microsoft Dynamics 365 toiminguteks.

On *Avansisaajate* on ettevõte, kes vastutab kulu summa, mis on sätestatud organisatsiooni töötaja. Ainult ettevõtte töötaja võib Avansisaaja. Hanke juhul Avansisaaja aruanded ettevõttele tehtud kulutuste kohta. Firma hüvitab töötaja kulu summa. Ettevõte kontrollib iga Avansisaajate tasakaal. Eesti, Läti, Leedu, Poola, Tšehhi, Ungari ja Venemaa juriidiliste isikute kasutajatele võib kajastada konkreetsete tehingute kaasnevad toimingud ettevõtte töötajatele, kes vastutavad organisatsiooni poolt antud kulusumma.

## <a name="set-up-an-advance-holder"></a>Avansisaaja seadistamine
Avansisaaja seadistamiseks tuleb täita järgmised ülesanded järjekorras.
1.  Loo ettemakse grupid.
2.  Saate seadistada töötaja sisestusreeglid.
3.  Konto Ostureskontro parameetrite seadistamine
4.  Loo ettemakse antava tegemise konkreetsed tingimused.
5.  Avansisaaja luua.

### <a name="advance-holder-groups"></a>Avansisaajate grupid

Kasutamine ning **ette grupid** ette omanik koostamise lehekülg. Saate määrata nime, kirjelduse ja eelnevalt omaniku nimel vastaskonto.
### <a name="employee-posting-profile"></a>Töötaja sisestusreeglid

Kasutamine ning **sisestusreeglite töötaja** lehe luua profiili avansisaaja kanded. Saate määrata järgmised andmed töötaja sisestusreeglid.
|Väli |Kirjeldus|
|------|-----------|
|Sisestusreeglid|Sisestage ettemakse omanik postitad profiili tunnuskood.|
|Kirjeldus|Sisestage selle sisestusreegli lühikirjeldus.|
|Kehtib|Valige üks järgmistest suvanditest sisestusreeglite seadistamine grupeerimise taseme puhul: 
**Tabelis** – seda valikut kasutatakse ühe Avansisaajate jaoks seadistada. Peate määrama selle Avansisaaja kood väljale viitenumber.
**Rühma** – seda valikut kasutatakse Avansisaajate grupi sisestusreegli luua. Peate määrama selle tähise väljale viitenumber.
**Kõik** – seda valikut kasutatakse määrata sisestusreegli jaoks kõik Avansisaajate. | | Viide | Kehtiv välja valitud tabeli valimine on Avansisaaja kood või kehtiv välja valitud rühma eelnevalt omanik rühma valimine. | | Summakonto | Valige konto tehingute konteerimisel. |



### <a name="account-payable-parameters"></a>Konto Ostureskontro parameetrid

Avansisaaja kanded vastavalt seadistama järgmise on **moodustavad Ostureskontro parameetrid** lehe ning **ette alused** lõik.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Field**                                     | **Description**                                                                                                                                                                  |
| **Posting profile**                            | •Valige vaikimisi profiil Avansisaajate tehingute lõpuleviimiseks.                                                                                                         |
| **Advance holder sorting**                     | Märkimisel Avansisaajate kuvatakse loendi alguses ning **ette alused** lehel.                                                                     |
| **Issue when balance is open**                 | Kui valitud, lubatakse raha ette eelnevalt omanikule, kes on avatud positiivne saldo väljaandmine.                                                                      |
| **Saldo sulgemine kaudu raha välja rühm: nimi** | Valige raha saatelehe töölehe kood. Selle töölehe kood saab luua Kassa Väljaminekuorderid ja korvamisorderite Avansisaaja 's nõuded läbi raha sulgemisel. |
| **Cash**                                       | Valige sularahakonto kanded, mida kasutatakse saldode sulgemiseks antava eelneva määramiseks.                                                                 |
| **Saldo sulgemine panga väljagrupi kaudu: nimi** | Tehingute panga kaudu saldode sulgemiseks valige töölehe.                                                                                                   |
| **Account type**                               | Valige Pank sulgeda saldod Avansisaaja panga kaudu.                                                                                                        |
| **Main account**                               | Valige pangakonto kood sulgeda saldod Avansisaaja panga kaudu.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Avansisaajate maksetingimused

Õigesti registreerida ja postitada kaudu Avansisaaja ostutellimuse, kasutage tegemise, mis loodi tingimused on **avansisaajalt** valik seatud **True**.
### <a name="create-an-advance-holder-creation"></a>Loo ettemakse omanik loomine

Avansisaaja loomiseks peab juba seadistatud töötajad. Lisateabe saamiseks vaadake [sisestage töötaja teave (tööülesande juhised).](http://ax.help.dynamics.com/en/wiki/enter-worker-information/) Kasutamine ning **ette alused** lehe luua töötaja on Avansisaaja. Valige töötaja Avansisaaja kasutada, klõpsake **muuta**, seadnud selle **Avansisaajate** võimalus **True**. Peate täitma järgmised väljad.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Field**      | **Description**                                                                             |
| **Group**      | Eelnev omanik rühma valimine.                                                             |
| **Series**     | Sisestage ettemakse omaniku tuvastamisel kasutatava dokumendi seeria. |
| **Number**     | Sisestage ettemakse omaniku tuvastamisel kasutatava dokumendi number. |
| **Issue date** | Valige või sisestage dokumendi kuupäev.                                                    |
| **Issued by**  | Sisestage asutuse või dokumendi väljastaja andmed.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Omanik päringud ja aruanded
### <a name="advance-holder-transactions-inquiry"></a>Eelnev omanik tehingute uurimine

Loetelu avansisaaja kanded, klõpsake selle **tehingute** nupuga ning **ette alused** lehel. Vaadata kõik eelnevalt alused või konkreetse päringu aluseks on eelnevalt omaniku kanded, klõpsake **arved**&gt;**päringute ja aruannete**&gt;**ette alused päringute ja aruannete**&gt; tehingud. Klõpsake **kanne** avamiseks ning **kande** lehel.
### <a name="advance-holder-balance-inquiry"></a>Eelnev omanik Saldopäring

Kuvamiseks kasutage Avansisaaja saldo on **ette alused** lehel. Näha tasakaalu kõigi eelnevalt alused või konkreetse päringu vastavalt eelnevalt omaniku kontode loomiseks klõpsake **arved**&gt;**päringute ja aruannete**&gt;**ette alused päringute ja aruannete**&gt;**tasakaalu.**
### <a name="advance-holder-balance-report"></a>Avansisaaja saldo aruanne

Eelvaade ja eelnevalt omaniku tasakaalu saamiseks kasutada, klõpsake **arved**&gt;**päringute ja aruannete**&gt;**ette alused päringute ja aruannete**&gt;**omanik jääksumma Ettemaksuaruande**.
### <a name="advance-holder-transactions-report"></a>Avansisaaja kannete aruanne

Eelvaade ja eelnevalt omaniku tehingute põhjal aruande, klõpsake nuppu **arved**&gt;**päringute ja aruannete**&gt;**ette alused päringute ja aruannete**&gt;**Ettemaksuaruande omanik tehingute**.



<a name="see-also"></a>Vt ka
--------

[Advance holder transactions](emea-advance-holders-transactions.md)


