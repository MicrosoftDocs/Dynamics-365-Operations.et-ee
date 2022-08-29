---
title: Avansisaajate ülevaade
description: See artikkel annab teavet ettemaksu saaja funktsioonide kohta.
author: AdamTrukawka
ms.date: 09/15/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 262574,  ""intro-internal
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
ms.openlocfilehash: 4b4c28c342f82ecd265bc70a51b3aa88dc0d7038
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285763"
---
# <a name="advance-holders-overview"></a>Avansisaajate ülevaade

[!include [banner](../includes/banner.md)]

*Avansisaaja* on ettevõtte töövõtja, kes vastutab organisatsiooni pakutud kulusumma eest. Avansisaaja saab olla ainult ettevõtte töötaja. Hanke toimumisel teavitab avansisaaja ettevõtet tehtud kuludest. Ettevõte hüvitab töövõtjale kulusumma. Ettevõte haldab iga avansisaaja saldot. Kasutajad Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal asuvates juriidilistes isikutes saavad kajastada kindlate kannetega kaasnevaid toiminguid ettevõtte töövõtjatega, kes vastutavad organisatsiooni pakutud kulusumma eest.

## <a name="set-up-an-advance-holder"></a>Avansisaaja seadistamine
Täitke järgmised ülesanded ettemaksu hoidja jaoks. Tehke selles jaotises kirjeldatud ülesanded kindlasti järgnevas järjekorras.

1. Ettemaksu hoidjate gruppide loomine.
2. Töövõtja sisestusreeglite seadistamine.
3. Võlgade parameetrite seadistamine.
4. Ettemaksu hoidjate kindlate maksetingimuste loomine.
5. Ettemaksu hoidjate kindlate maksetingimuste loomine.
6. Avansisaaja loomine.


### <a name="advance-holder-groups"></a>Avansisaajate grupid

Avansisaajate grupi saate luua lehel **Avansisaajate grupid**. Saate määrata avansisaajate grupi nime, kirjelduse ja vastaskonto.
### <a name="employee-posting-profile"></a>Töötaja sisestusreeglid

Avansisaaja kannete jaoks saate reeglid luua lehel **Töövõtja sisestusreeglid**. Saate töövõtja sisestusreeglite puhul määrata järgmise teabe.

|      Väli      |                                            Kirjeldus                                            |
|-----------------|---------------------------------------------------------------------------------------------------|
| **Sisestusreeglid** |  Sisestage avansisaaja sisestusreeglite ID-kood.               |
|   **Kirjeldus**   |  Sisestage sisestusreeglite lühikirjeldus.                         |
|    **Kehtib**    |  Valige sisestusreeglite seadistamiseks grupeerimistaseme jaoks järgmised suvandid. <ul> <li>**Tabel** – seda valikut kasutatakse sisestusreeglite loomiseks ühele avansisaajale. Väljale **Viide** peate sisestama avansisaaja koodi.</li> <li>**Grupp** – seda valikut kasutatakse sisestusreeglite loomiseks avansisaajate grupile. Väljale **Viide** peate sisestama grupi koodi.</li> <li>**Kõik** – seda valikut kasutatakse sisestusreeglite loomiseks kõikidele avansisaajatele.</li></ul> |
| **Viide** | Valige avansisaaja kood, kui suvand **Tabel** on valitud väljas **Kehtib**, või valige avansisaajate grupp, kui suvand **Grupp** on valitud väljas **Kehtib**. |
| **Summakonto** | Valige kannete sisestamiseks koondkonto. |



### <a name="account-payable-parameters"></a>Ostureskontro parameetrid

Ettemaksu hoidjate kannete kajastamiseks peate lehel **Võlgade parameetrid** jaotises **Ettemakse hoidjad** seadistama järgmised väljad.

|  Väli                                         | Kirjeldus       |
|------------------------------------------------|-------------------|
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

### <a name="create-an-advance-holder"></a>Avansisaaja loomine

Enne avansisaaja loomist peavad töötajad olema juba seadistatud. Lisateavet vt teemast [Töötaja teabe sisestamine (tegevuse juhis)](../../human-resources/hr-personnel-enter-worker-information.md). 

1. Avage **Võlad** > **Ettemakse hoidjad** > **Ettemakse hoidjad**.

    > [!NOTE]
    > Töövõtjaid ei saa lehel **Avansisaajad** lisada ega kustutada. Esmalt tuleb töövõtjad moodulis **Inimressurssid** palgata. Lehel **Töövõtja sisestusreeglid** saate seadistada töövõtja sisestusreeglid, mida kasutatakse avansisaajate saldode sisestamiseks.

2. Valige töövõtja ja seejärel suvand **Redigeeri**.
3. Seadke kiirkaardil **Üldine** suvandi **Avansisaaja** sätteks **Jah** näitamaks, et töövõtja on avansisaaja.
4. Valige väljal **Grupp** avansisaajate grupp, kuhu töövõtja kuulub.
5. Jaotises **Isikutunnistus** sisestage isikut tõendava dokumendi üksikasjad.
    - **Seeria**: Sisestage ettemaksu hoidja isiku kontrollimiseks kasutatava dokumendi seeria.
    - **Number**: Sisestage ettemaksu hoidja isiku kontrollimiseks kasutatava dokumendi number.
    - **Väljaandmise kuupäev**: Valige või sisestage dokumendi väljaandmise kuupäev.
    - **Väljastaja**: Sisestage dokumendi väljastanud asutuse või isiku üksikasjad.
6. Valige käsk **Salvesta** või sulgege leht.

> [!NOTE]
> Kui lehel **Ostureskontro parameetrid** on suvandi **Avansisaajate sortimine** sätteks valitud **Jah**, kuvatakse avansisaajad lehel **Avansisaajad** ruudustiku ülaosas.


## <a name="advance-holder-inquiries-and-reports"></a>Avansisaaja päringud ja aruanded

### <a name="advance-holder-transactions-inquiry"></a>Avansisaaja kannete päring

Ettemaksu hoidja kannete loendi kuvamiseks valige lehel **Ettemaksu hoidja** nuppu **Kanded**. Kõigi ettemaksu hoidjate kannete kuvamiseks või kindla päringu loomiseks avansisaajate kannete põhjal klõpsake valikuid **Võlad** > **Päringud ja aruanded** > **Ettemaksu hoidjate päringud ja aruanded** > **Kanded**. Klõpsake lehe **Vautšer kanded** avamiseks valikut **Vautšer**.

### <a name="advance-holder-balance-inquiry"></a>Avansisaaja saldo päring

Avansisaaja saldot saate vaadata lehel **Avansisaajad**. Kõigi avansisaajate saldo kuvamiseks või kindla päringu loomiseks avansisaajate kontode põhjal klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; **Saldo**.
### <a name="advance-holder-balance-report"></a>Avansisaaja saldo aruanne

Avansisaajate saldo teabel põhineva aruande eelvaatamiseks ja printimiseks klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; **Avansisaaja saldoaruanne**.
### <a name="advance-holder-transactions-report"></a>Avansisaaja kannete aruanne

Avansisaajate kannetel põhineva aruande eelvaatamiseks ja printimiseks klõpsake valikuid **Ostureskontro** &gt; **Päringud ja aruanded** &gt; **Avansisaajate päringud ja aruanded** &gt; **Avansisaaja kannete aruanne**.

## <a name="advance-holder-transactions"></a>Avansisaaja kanded

Ettemaksu hoidja töötajate kandeid saab sisestada ettemakse hoidjate kontode abil. Igale avansisaajale määratud töötaja ID alusel saab jälgida kõiki avansisaajate kandeid. See number tuuakse ettemaksu hoidjate kannete jaoks kontonumbrina lehtedel **Päevaraamatud** ja **Ettemaksu hoidjate kanded**.

### <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Ostutellimuse loomine ja sisestamine avansisaaja andmetega
Täpsemat teavet ostutellimuste kohta vt teemast [Ostutellimuse ülevaade](../../supply-chain/procurement/purchase-order-overview.md). Hankija arve loomisel ja sisestamisel avansisaaja andmetega sisestatakse avansisaaja saldod töövõtja saldokontole, mitte hankija saldokontole. Ostutellimusele avansisaaja andmete lisamiseks tehke järgmist.

1. Valige jaotises **Hind ja allahindlus** väljal **Maksetingimused** maksetingimus. Lisateabe saamiseks **Maksetingimuste** kohta vaata [Hankija maksetingimuste määratlemine](../accounts-payable/tasks/define-vendor-payment-terms.md). 
2. Valige maksetingimus, millel on suvand **Avansisaajalt** valitud lehel **Maksetingimused**. 
3. Kiirkaardil **Hind ja allahindlus** valige **Ettemaksu hoidja** väljal ostutellimuse ettemaksu hoidja.

Ostutellimuse sisestusprotsess loob kaks hankija kannet vastandsummadega ja ühe avansisaaja kande. Ilma avansisaaja andmetega luuakse ainult üks hankija kanne.

### <a name="settle-advance-holder-balances-by-using-the-bank"></a>Ettemaksu hoidjate saldode tasakaalustamine panga abil
Ettemaksu hoidjate saldode tasakaalustamisel panga kaudu luuakse päevaraamatus töölehe sisestused avansisaaja saldode sulgemiseks. Saate seadistada töölehe ja panga koodi lehe **Ostureskontro parameetrid** jaotises **Avansisaajad**. 

1. Ettemaksu hoidjate saldo sulgemiseks panga abil minge **Võlad** > **Ettemaksu hoidjad** > **Ettemaksu hoidjad**. 
2. Toimingupaani puhul valige **Saldo** > **Panga kaudu sulgemine**. 
3. Sisestage lehel **Panga kaudu sulgemine** järgmine teave.

    | Väli                    | Kirjeldus |
    |------------------------------|-------------------|
    | **Maksekuupäev**          | Sisestage makse sisestamiseks nõutav kuupäev.|
    | **Ülekantav summa** | Sisestage sulgemisel saldo summa. Lehe **Saldo** väljal **Summa** näidatud summa kuvatakse vaikimisi. |
    | **Automaatne**                | Märkige ruut **Automaatne**, et automaatselt luua ja sisestada lehel **Võlgade parameetrid** eelseadistatud tööleht automaatselt.|

### <a name="settle-advance-holder-balances-by-using-cash"></a>Ettemaksu hoidjate saldode tasakaalustamine sularaha abil
Avansisaaja saldode tasakaalustamisel sularaha abil luuakse saatelehe töölehel sisestused avansisaaja saldode sulgemiseks. Saate seadistada töölehe ja kassa koodi lehe **Ostureskontro parameetrid** vahekaardil **Avansisaajad**. 

1. Ettemaksu hoidjate saldo sulgemiseks sularaha abil minge **Võlad** > **Ettemaksu hoidjad** > **Ettemaksu hoidjad**. 
2. Toimingupaani puhul valige **Saldo** > **Sularaha abil sulgemine**. 
3. Sisestage lehel **Kassa kaudu sulgemine** järgmine teave.

    | Väli                    | Kirjeldus
    |------------------------------|-----------------|
    | **Maksekuupäev**          | Sisestage makse sisestamiseks nõutav kuupäev.|
    | **Ülekantav summa** | Sisestage sulgemisel saldo summa. Lehe **Saldo** väljal **Summa** näidatud summa kuvatakse vaikimisi. |
    | **Automaatne**                | Märkige ruut **Automaatne**, et automaatselt luua ja sisestada lehel **Võlgade parameetrid** eelseadistatud tööleht automaatselt.     |

Kui summa väljal **Ülekantav summa** on negatiivne. luuakse pärast saatelehe töölehe töötlemist avansisaajale väljaminekuorder, kui saldod on suletud. Kui summa väljal **Ülekantav summa** on positiivne, luuakse korvamisorder.

## <a name="additional-resources"></a>Lisaressursid

- [Avansimakse töövõtjale (Ida-Euroopa)](tasks/advance-payment-employee.md)
- [Venemaa avansisaajate ülevaade](rus-advance-holders.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
