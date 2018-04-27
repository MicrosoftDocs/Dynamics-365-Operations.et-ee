---
title: Avansisaajad
description: Lugege avansisaaja funktsiooni kohta Microsoft Dynamics 365 for Finance and Operationsis.
author: LizaGolub
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262574
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 84471351555d90c5a297d613abf334a26e896e40
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="advance-holders"></a>Avansisaajad

[!INCLUDE [banner](../includes/banner.md)]

Lugege avansisaaja funktsiooni kohta Microsoft Dynamics 365 for Finance and Operationsis.

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

|      Väli      |                                            Kirjeldus                                            |
|-----------------|---------------------------------------------------------------------------------------------------|
| Sisestusreeglid |               Sisestage avansisaaja sisestusreeglite ID-kood.               |
|   Kirjeldus   |                         Sisestage sisestusreeglite lühikirjeldus.                         |
|    Kehtib    | Valige sisestusreeglite seadistamiseks grupeerimistaseme jaoks järgmised suvandid. |

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

Enne avansisaaja loomist peavad töötajad olema juba seadistatud. Lisateavet vt teemast [Töötaja teabe sisestamine (tegevuse juhis).](../../fin-and-ops/hr/tasks/enter-worker-information.md) Töötaja saate avansisaajana seadistada lehel **Avansisaajad**. Valige töötaja, keda kasutada avansisaajana, klõpsake valikut **Redigeeri** ja seejärel määrake valiku **Avansisaaja** sätteks **Tõene**. Samuti peate täitma järgmised väljad.

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

## <a name="advance-holder-transactions"></a>Avansisaaja kanded

Lugege, kuidas töötada avansisaajate kannetega Microsoft Dynamics 365 for Finance and Operationsis.

Avansisaajast töötajate kandeid saab sisestada avansisaaja kontode abil. Igale avansisaajale määratud töötaja ID alusel saab jälgida kõiki avansisaajate kandeid. See number tuuakse avansisaaja kannete jaoks kontonumbrina lehtedel **Päevaraamatud** ja **Avansisaajate kanded**.

### <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Ostutellimuse loomine ja sisestamine avansisaaja andmetega
Täpsemat teavet ostutellimuste kohta vt teemast [Ostutellimuse ülevaade](../../supply-chain/procurement/purchase-order-overview.md). Hankija arve loomisel ja sisestamisel avansisaaja andmetega sisestatakse avansisaaja saldod töövõtja saldokontole, mitte hankija saldokontole. Ostutellimusele avansisaaja andmete lisamiseks tehke järgmist.

-   Valige jaotises **Hind ja allahindlus** väljal **Maksetingimused** maksetingimus. <!---For more information about **Terms of payment**, see [Define vendor payment terms](accounts-payable/tasks/define-vendor-payment-terms).--> Valige maksetingimus, millel on lehel **Maksetingimused** valitud suvand **Avansisaajalt**. Lisateavet avansisaajate maksetingimuste seadistamise kohta vt teemast [Avansisaajad](emea-advance-holders.md).
-   Valige kiirkaardi **Hind ja allahindlus** väljal **Avansisaaja** ostutellimuse avansisaaja.

Ostutellimuse sisestusprotsess loob kaks hankija kannet vastandsummadega ja ühe avansisaaja kande. Ilma avansisaaja andmetega luuakse ainult üks hankija kanne.

### <a name="settle-advance-holder-balances-via-a-bank"></a>Avansisaaja saldode tasakaalustamine panga kaudu
Avansisaaja saldode tasakaalustamisel panga kaudu luuakse päevaraamatus töölehe sisestused avansisaaja saldode sulgemiseks. Saate seadistada töölehe ja panga koodi lehe **Ostureskontro parameetrid** jaotises **Avansisaajad**. Lisateavet vt teemast [Avansisaajad](emea-advance-holders.md). Avansisaaja saldo sulgemiseks panga kaudu avage **Ostureskontro** &gt; **Avansisaajad** &gt; **Avansisaajad**. Klõpsake toimingupaanil nuppu **Saldo** ja seejärel nuppu **Panga kaudu sulgemine**. Sisestage lehel **Panga kaudu sulgemine** järgmine teave.

| Väli                    | Kirjeldus |
|------------------------------|-------------------|
| **Maksekuupäev**          | Sisestage makse sisestamiseks nõutav kuupäev.|
| **Ülekantav summa** | Sisestage sulgemisel saldo summa. Vormi **Saldo** väljal **Summa** näidatud summa kuvatakse vaikimisi. |
| **Automaatne**                | Märkige ruut **Automaatne**, et luua ja sisestada lehel **Ostureskontro parameetrid** eelseadistatud tööleht.|

### <a name="settle-advance-holder-balances-via-cash"></a>Avansisaaja saldode tasakaalustamine kassa kaudu
Avansisaaja saldode tasakaalustamisel kassa kaudu luuakse saatelehe töölehel sisestused avansisaaja saldode sulgemiseks. Saate seadistada töölehe ja kassa koodi lehe **Ostureskontro parameetrid** vahekaardil **Avansisaajad**. Lisateavet vt teemast [Avansisaajad](emea-advance-holders.md). Avansisaaja saldo sulgemiseks kassa kaudu avage **Ostureskontro** &gt; **Avansisaajad** &gt; **Avansisaajad**. Klõpsake toimingupaanil nuppu **Saldo** ja seejärel nuppu **Kassa kaudu sulgemine**. Sisestage lehel **Kassa kaudu sulgemine** järgmine teave.

| Väli                    | Kirjeldus
|------------------------------|-----------------|
| **Maksekuupäev**          | Sisestage makse sisestamiseks nõutav kuupäev.|
| **Ülekantav summa** | Sisestage sulgemisel saldo summa. Vormi **Saldo** väljal **Summa** näidatud summa kuvatakse vaikimisi. |
| **Automaatne**                | Märkige ruut **Automaatne**, et luua ja sisestada lehel **Ostureskontro parameetrid** eelseadistatud tööleht automaatselt.     |

Kui summa väljal **Ülekantav summa** on negatiivne. luuakse pärast saatelehe töölehe töötlemist avansisaajale väljaminekuorder, kui saldod on suletud. Kui summa väljal **Ülekantav summa** on positiivne, luuakse korvamisorder.

## <a name="additional-resources"></a>Lisaressursid

- [Avansimakse töötajale (Ida-Euroopa)](tasks/advance-payment-employee.md)




