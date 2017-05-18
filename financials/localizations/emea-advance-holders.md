---
title: Avansisaajad
description: Lugege teavet Microsoft Dynamics 365 for Operationsi avansisaajate funktsiooni kohta.
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 0f34bfed64507944cadf5b02e3c7222f17803f92
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="advance-holders"></a>Avansisaajad

[!include[banner](../includes/banner.md)]


Lugege teavet Microsoft Dynamics 365 for Operationsi avansisaajate funktsiooni kohta.

*Avansisaaja* on ettevõtte töövõtja, kes vastutab organisatsiooni pakutud kulusumma eest. Avansisaaja saab olla ainult ettevõtte töötaja. Hanke toimumisel teavitab avansisaaja ettevõtet tehtud kuludest. Ettevõte hüvitab töövõtjale kulusumma. Ettevõte haldab iga avansisaaja saldot. Kasutajad Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal asuvates juriidilistes isikutes saavad kajastada kindlate kannetega kaasnevaid toiminguid ettevõtte töövõtjatega, kes vastutavad organisatsiooni pakutud kulusumma eest.

## <a name="set-up-an-advance-holder"></a>Avansisaaja seadistamine
Avansisaaja seadistamiseks tuleb täita järjest järgmised ülesanded.
1.  Avansisaajate gruppide loomine.
2.  Töövõtja sisestusreeglite seadistamine.
3.  Ostureskontro parameetrite seadistamine.
4.  Avansisaajale kindlate maksetingimuste loomine.
5.  Avansisaaja loomine.

### <a name="advance-holder-groups"></a>Avansisaajate grupid

Avansisaajate grupi saate luua lehel **Avansisaajate grupid**. Saate määrata avansisaajate grupi nime, kirjelduse ja vastaskonto.
### <a name="employee-posting-profile"></a>Töötaja sisestusreeglid

Avansisaaja kannete jaoks saate reeglid luua lehel **Töövõtja sisestusreeglid**. Saate töövõtja sisestusreeglite puhul määrata järgmise teabe.
|Väli |Kirjeldus|
|------|-----------|
|Sisestusreeglid|Sisestage avansisaaja sisestusreeglite ID-kood.|
|Kirjeldus|Sisestage sisestusreeglite lühikirjeldus.|
|Kehtib|Valige sisestusreeglite seadistamiseks grupeerimistaseme jaoks järgmised suvandid. 
**Tabel** – seda valikut kasutatakse sisestusreeglite loomiseks ühele avansisaajale. Väljale Viide peate sisestama avansisaaja koodi.
**Grupp** – seda valikut kasutatakse sisestusreeglite loomiseks avansisaajate grupile. Väljale Viide peate sisestama grupi koodi.
**Kõik** – seda valikut kasutatakse sisestusreeglite seadistamiseks kõigile avansisaajatele.| |Viide|Valige avansisaaja kood, kui väljal Kehtib on tehtud valik Tabel, või valige avansisaajate grupp, kui väljal Kehtib on tehtud valik Grupp.| |Koondkonto|Saate valida kannete sisestamiseks koondkonto.|



### <a name="account-payable-parameters"></a>Ostureskontro parameetrid

Avansisaaja kannete kajastamiseks peate lehel **Ostureskontro parameetrid** jaotises **Avansisaajad** seadistama järgmised parameetrid.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Väli**                                     | **Kirjeldus**                                                                                                                                                                  |
| **Sisestusreeglid**                            | Saate valida vaikeprofiili avansisaajate kannete lõpuleviimiseks.                                                                                                         |
| **Avansisaajate sortimine**                     | Selle valiku korral kuvatakse avansisaajad lehel **Avansisaajad** oleva loendi alguses.                                                                     |
| **Väljasta avatud saldo puhul**                 | Selle valiku korral lubatakse sularahaettemakse avansisaajale, kellel on avatud positiivne saldo.                                                                      |
| **Saldo sulgemine kassa väljagrupi kaudu: Nimi** | Valige kassaorderi töölehe kood. Seda töölehe koodi kasutatakse sularaha korvamisorderite ja väljaminekuorderite loomisel, kui avansisaaja saldod suletakse sularaha kaudu. |
| **Sularaha**                                       | Valige sularahakonto, et määrata avansisaaja saldode sulgemiseks kasutatavad kanded.                                                                 |
| **Saldo sulgemine panga väljagrupi kaudu: Nimi** | Valige kannete jaoks töölehe kood, et sulgeda saldod panga kaudu.                                                                                                   |
| **Konto tüüp**                               | Valige pank, et sulgeda avansisaaja saldod panga kaudu.                                                                                                        |
| **Põhikonto**                               | Valige pangakonto kood, et sulgeda avansisaaja saldod panga kaudu.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Avansisaaja maksetingimused

Ostutellimuse õigesti registreerimiseks ja sisestamiseks avansisaaja kaudu peate kasutama maksetingimusi, mille seadistuses kasutati valiku **Avansisaajalt** puhul sätet **Tõene**.
### <a name="create-an-advance-holder-creation"></a>Avansisaaja loomine

Enne avansisaaja loomist peavad töötajad olema juba seadistatud. Lisateavet vt teemast [Töötaja teabe sisestamine (tegevuse juhis).](http://ax.help.dynamics.com/en/wiki/enter-worker-information/) Töötaja saate avansisaajana seadistada lehel **Avansisaajad**. Valige töötaja, keda kasutada avansisaajana, klõpsake valikut **Redigeeri** ja seejärel määrake valiku **Avansisaaja** sätteks **Tõene**. Samuti peate täitma järgmised väljad.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Väli**      | **Kirjeldus**                                                                             |
| **Grupp**      | Valige avansisaajate grupp.                                                             |
| **Seeria**     | Sisestage avansisaaja isiku kontrollimiseks kasutatava dokumendi seeria. |
| **Number**     | Sisestage avansisaaja isiku kontrollimiseks kasutatava dokumendi number. |
| **Väljaandmise kuupäev** | Valige või sisestage dokumendi väljaandmise kuupäev.                                                    |
| **Väljastaja**  | Sisestage dokumendi väljastanud asutuse või isiku üksikasjad.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Avansisaaja päringud ja aruanded
### <a name="advance-holder-transactions-inquiry"></a>Avansisaaja kannete päring

Avansisaaja kannete loendi kuvamiseks klõpsake lehel **Avansisaajad** nuppu **Kanded**. Kõigi avansisaajate kannete kuvamiseks või kindla päringu loomiseks avansisaajate kannete põhjal klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; Kanded. Klõpsake lehe **Pearaamatu kanded** avamiseks valikut **Kanne**.
### <a name="advance-holder-balance-inquiry"></a>Avansisaaja saldo päring

Avansisaaja saldot saate vaadata lehel **Avansisaajad**. Kõigi avansisaajate saldo kuvamiseks või kindla päringu loomiseks avansisaajate kontode põhjal klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; **Saldo**.
### <a name="advance-holder-balance-report"></a>Avansisaaja saldo aruanne

Avansisaajate saldo teabel põhineva aruande eelvaatamiseks ja printimiseks klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; **Avansisaaja saldoaruanne**.
### <a name="advance-holder-transactions-report"></a>Avansisaaja kannete aruanne

Avansisaajate kannetel põhineva aruande eelvaatamiseks ja printimiseks klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; **Avansisaaja kannete aruanne**.



<a name="see-also"></a>Vt ka
--------

[Avansisaaja kanded](emea-advance-holders-transactions.md)




