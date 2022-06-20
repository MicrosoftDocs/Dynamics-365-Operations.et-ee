---
title: Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga
description: See artikkel kirjeldab, kuidas kasutada Hinnakujunduse mootorit Microsoftis Dynamics 365 Supply Chain Management alates Microsoft Dynamics 365 Müügist.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 259bdd5f868945c3857b045fbd3cbd4fceb26951
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862215"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisaldab hinnakujunduse mootorit, mis tegeleb kaubanduslepete, hinnakirjade, püsikliendi rogrammide, kampaaniate ja allahindlustega. Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks. Kui kasutate topeltkirjutust, **·** **·** Microsoft Dynamics kasutate staatilist hinnakujundust või tarneahela halduse hinnakujundusmootorit pakkumise ja tellimuse lehtedel 365 müügis.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Supply Chain Managementi hinnakujunduse mootori kasutamine Salesis

1. Avage Salesis **Müük \> Tellimused**.
1. Uue tellimuse loomiseks või olemasolema valimiseks tehke loendis **Minu tellimused** valik **Uus**.
1. Uue tellimusrea lisamine.
1. Uue tellimuse loomisel valige tegevuspaanil **hinnatellimus**. Kui värskendate olemasolevat tellimust, valige tegevuse paanil suvand **Uuestiarvutamine**.
1. Järgmised veerud täidetakse automaatselt.

    - Üksikasjalik summa
    - Allahindlus %
    - Allahindlus
    - Transpordieelne summa
    - Transpord summa
    - Kogumaks
    - Kogusumma

> [!NOTE]
> Sarnane protsess rakendub pakkumiste loomisel.

## <a name="how-it-works"></a>Toimimisviis

Kui loote tellimuse müügis, sünkroonitakse tellimus tarneahela haldusega kohe, kasutades müügisse sisestatud väärtusi. Kui valite **müügis** **hinnatellimuse** või hinnapakkumise, arvutab tarneahela haldus iga tellimuse rea hinna ja kogutellimuse, mis põhineb tarneahela halduses määratletud kaubanduslehel määratud reeglitel. Uued arvutatud väärtused sünkroonitakse seejärel tagasi müügiga.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Kaubanduslelepingu hindamissuvandite määramine tarneahela halduses

Saate konfigureerida tarneahela halduse, et arvesse võtta või eirata kaubandusleppeid, kui see arvutab müügis loodud tellimuse hinna. Järgige neid samme selle suvandi häälestamiseks.

1. Logige sisse oma tarneahela haldamise keskkonda.
1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
1. Lisage või **eemaldage** vahekaardi Hinnad **kiirkaardil** **Kaubanduslelepingu hindamine vajaduse korral rida käsitsi sisestamise** poliitika jaoks. Selle poliitika olemasolu või puudumine kontrollib, kas tarneahela haldamise hinnakujunduse mootor alistab automaatselt müügisse sisestatud müügihinna.

    - Kui kaubanduslehel **hindamise** *seadistuses* ei ole käsitsi **sisestamise poliitikat**, on tarneahela haldus hinnaeaviis. **·** **Kui** kasutaja valib müügi tegevuspaanil hinnatellimuse või hinnapakkumise, kutsutakse tarneahela haldamise hinnakujunduse mootor ja müügisse sisestatud müügihind kirjutatakse üle, kui see ei võrdu tarneahela halduses arvutatud müügihinnaga.
    - Kui kaubanduslelepingu **hindamise** *seadistuses* on olemas **käsitsi sisestamise poliitika**, on müük hinna koond. Müügisse sisestatud müügihinda ei saa **automaatselt** **üle** kirjutada, kui kasutaja valib müügi tegevuspaanil hinnatellimuse või hinnapakkumise.
    - Tellimuseridu ja pakkumise ridu, mille **ühiku hind ja/** **või** müügi allahindlusväärtus on 0 *(null), käsitletakse erijuhtumina.* Kui saadaval on vastav kaubanduslelepingu hind, rakendab *tarneahela* haldus seda alati nendele väljadele, olenemata **kaubanduslelepingu hindamisseadistusest**.

    Iga juhtumi näite puhul vaadake järgmisi stsenaariume.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Näide 1. stsenaarium: kaubanduslelepingu hindamine käsitsi sisestamise suvandita

Selle stsenaariumi korral ei sisalda **tarneahela haldamise** kaubanduslelepingu hindamise *häälestus* käsitsi **sisestamise** poliitikat. Müügi kasutaja sisestab tellimuserea, mille müügihind pole müügis null ja kauba jaoks pole tarneahela halduses müügihinda määratletud.

1. Müügis loob kasutaja tellimuserea, mille ühiku hinnaks **on** 1 USA dollar (USD).
1. Tellimuse rida sünkroonitakse tarneahela haldusega müügitellimuse 1 USD.
1. Müügis valib kasutaja tegevuspaanil **hinnatellimuse**.
1. Tarneahela haldus otsib asjakohaseid hindu ja allahindlusi ning arvutab seejärel kogusummad. Kuna kaubal ei ole tarneahela halduses müügihinda, uuendab kalkulatsioon rida nii, et kaubal oleks 0 USD.
1. Rea uus müügihind sünkroonitakse tagasi müügiga.
1. Selle tulemuseks on müügitellimuse rida, mille müügihind on 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Näide 2. stsenaarium: kaubanduslelepingu hindamine käsitsi sisestamise suvandiga

Selle stsenaariumi korral sisaldab tarneahela **haldus kaubanduslelepingu** hindamise häälestus *käsitsi* **sisestamise** poliitikat. Müügi kasutaja sisestab tellimuserea, mille müügihind pole null. Tarneahela haldus hõlmab kaubanduslelepingut, mis määrab 2 USD kaubale müügihinna.

1. Müügis loob kasutaja tellimuserea kaubale, mille **ühiku hind on** 1 USD.
1. Tellimuse rida sünkroonitakse tarneahela haldusega müügitellimuse 1 USD.
1. Müügis valib kasutaja tegevuspaanil **hinnatellimuse**.
1. Kuna kaubanduslelepingu **hindamisseadistus** **tarneahela** halduses sisaldab käsitsi sisestamise poliitikat, ei muutu müügihind, kuigi rakendatavas kaubanduslehel on määratud mõni muu müügihind.
1. Müügihinda ei muudeta müügis ja tarneahela halduses.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Näide 3. stsenaarium: kauba, mille müügihind müügis on null, hindamine

Selle stsenaariumi korral sisaldab tarneahela **haldus kaubanduslelepingu** hindamise häälestus *käsitsi* **sisestamise** poliitikat. Müügi kasutaja sisestab tellimuserea, mille müügihind müügis on 0 (null). Tarneahela haldus hõlmab kaubanduslelepingut, mis määrab 2 USD kaubale müügihinna.

1. Müügis loob kasutaja **tellimuserea**, mille ühiku hind on 0 USD **ja** rea allahindluse väärtus 0 USD.
1. Tellimuse rida sünkroonitakse tarneahela haldusega müügitellimuse 0 USD.
1. Kuna ta sai tellimuserea, mille müügihind on 0 (null), kutsub tarneahela haldus selle hinnakujundusmootorit, **kuigi valik Käsitsi sisestus** on lubatud. Hinnakujundusmootor tagastab kaubanduslelepinguga 2 USD loodud müügihinna ja uuendab tarneahela halduses tellimuserida.
1. Värskendatud müügihind ei ole veel müügis tellimusereaga sünkroonitud.
1. Müügis valib kasutaja tegevuspaanil **hinnatellimuse**.
1. Tarneahela halduse tellimuserida säilitab oma müügihinna 2 USD, mis sünkroonitakse nüüd tagasi müügiga. Seetõttu uuendatakse **müügitellimuse** rea hind ühiku kohta väärtusest 0 USD 2 USD.
1. Müügis sisestab kasutaja uue rea allahindluse **väärtuse**, 0.50 USD. Müük arvutab nüüd, et **rea laiendatud** summa väärtus on 1.50 USD.
1. Tellimuse rida sünkroonitakse tarneahela haldusega rea allahindluse **väärtusega** 0.50 USD.
1. Müügis valib kasutaja tegevuspaanil **hinnatellimuse**.
1. Müügi tellimuserea hinnad ja allahindlused ei muutu.

## <a name="limitations"></a>Kitsendused

Kui Salesi veerud on täidetud, kehtivad järgmised piirangud.

- Supply Chain Managementi tasude ja tasu eraldamise seadistusi ei kopeerita Salesi.
- Hinnakujundus ei arvesta Supply Chain Managementi müügitellimuse rea lehe veerus **Jaemüügi kanal** määratletud jaemüügi erihinnakujundust.
- Supply Chain Managementi jaotises **Kaubandushüvitise haldus** määratletud allahindlusi ei arvestata.
- Hinnakujundus ei arvesta müügilepinguid.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
