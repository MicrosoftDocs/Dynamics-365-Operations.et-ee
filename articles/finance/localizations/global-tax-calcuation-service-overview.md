---
title: Maksuarvutuse ülevaade
description: Selles teemas selgitatakse maksuarvestuse võimekuse üldist ulatust ja funktsioone.
author: wangchen
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: caa7e458763b6ba6b2b85ab016a1aa2e53cee89a
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647053"
---
# <a name="tax-calculation-overview"></a>Maksuarvutuse ülevaade

[!include [banner](../includes/banner.md)]

Maksuarvestus on hüperskaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada. Maksumootor on täielikult konfigureeritav. Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga. Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.

Maksuarvutus integreerub Dynamics 365 Finance ja Dynamics 365 Supply Chain Management-iga. Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.

> [!IMPORTANT]
> Kui lubate maksuarvestuse teenuse, võidakse teha mõningaid seotud andmete toiminguid andmekeskuses, mis ei ole andmekeskus, mis haldab teie teenuse andmeid. Vaadake [Reeglid ja tingimused](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) üle enne maksuarvutamise lubamist. Teie privaatsus on meie jaoks oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://go.microsoft.com/fwlink/?LinkId=521839).

Maksu arvutamine on mikroteenustel põhinev maksumootor, mis pakub astmelist skaleeritavust ja aitab täita järgmisi ülesandeid:

- Täiustatud määratlemismehhanismi abil saate automaatselt määrata õige käibemaksugrupi, kauba käibemaksugrupi ja maksukoodid.
- Kui teil on mitu maksuregistreerimise numbrit ühe hankija kohta, saab maksuarvestuse lisandmoodul õige maksuregistreerimise numbri määrata automaatselt.
- Saate toetada üleviimistellimuste maksu määramist, arvutamist, sisestamist ja tasakaalustamist.
- Määratlege konfigureeritavad maksuarvutuse valemid ja tingimused teie konkreetsetele ärinõuetele.
- Jagage maksu määramise ja arvutamise lahendust juriidiliste isikute vahel, et salvestada hoolduse panus ja vältida tõrkeid.
- Kliendi ja hankija maksu registreerimisnumbri määramine.
- Tugiloendi koodi määramine.
- Toetab maksuarvutuse parameetreid maksu jurisdiktsiooni tasandil.

Maksuarvutusteenuse kasutamiseks installige Tax Calculation lisandmoodul oma projektist Microsoft Dynamics Lifecycle Services. Seejärel lõpetage seadistus rakenduses [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) ja lubage maksu arvutamise teenus rakenduses Finance ja Supply Chain Management. Lisateavet leiate teemast [Maksuteenusega alustamine](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Kättesaadavus

Maksu arvutamine on üldiselt saadaval tootmiskeskkondades kõigile klientidele versiooni 10.0.21 alusel.

Uute funktsioonide tarnimist jätkatakse. Kontrollige kindlasti kõige ajasemat dokumentatsiooni, et teada saada toetatud funktsioonide laovarudest ja ulatusest.

Maksuarvestus on juurutatud järgmistes Azure'i geograafilistes asukohtades. Vastavalt klientide vajadustele lisatakse rohkem Azure'i geograafilisi asukohti.

- Aasia ja Vaikse ookeani
- Austraalia
- Kanada
- Euroopa
- Jaapan
- Ühendkuningriik
- Ameerika Ühendriigid

> [!NOTE]
> Maksuarvutus ei toeta Dynamics 365 varasemat versiooni, nt Dynamics AX 2012 või Dynamics 365 valdustes juurutamist.

## <a name="data-flow"></a>Andmevoog

Siin on ülevaade maksude arvutamise andmevoo protsessist. 

1. RCS-s saate vaadata ja importida maksustatava dokumendi mudeli konfiguratsioone ja mudeli vastendamise konfiguratsioone. Kui peate täpsema stsenaariumi konfiguratsioone laiendama, vaata [Andmeväljade lisamine maksukonfiguratsioonides](tax-service-add-data-fields-tax-configurations.md).
2. RCS-sis looge või säilitage maksufunktsioonid. Saate kasutada maksufunktsiooni maksumäärade ja maksu kohaldatavusreeglite säilitamiseks.
3. Pärast maksufunktsiooni häälestuse lõpuleviimist avaldage maksukonfiguratsioonid ja maksufunktsioonid RCS-ist globaalsesse hoidlasse.
4. Rakenduses Finance valige, millist maksufunktsiooni seadistusversiooni konkreetse juriidilise isiku puhul kasutada.
5. Finance ja Supply Chain Management halduses kasutage kandeid nagu tavaliselt. Kui on vaja maksu arvutamist, kogub klient kandest teavet, nt müügitellimust või ostutellimust, ja pakib teabe lastiks. Seejärel saadetakse maksu arvutamiseks taotlus.
6. Maksu arvutamise taotlus on kliendilt saadud ja kalkulatsioon on lõpule viidud. Maksu tulemus tagastatakse seejärel kliendile.
7. Dynamics 365 klient saab käibemaksu tulemuse ja esitab käibemaksu arvutamise tulemuse käibemaksu leheküljel.

## <a name="supported-transactions"></a>Toetatud kanded

Maksu arvutuse saab lubada kannetega. 

Finantsversioonis 10.0.21 toetatakse järgmisi kandeid: 

- Müük

    - Müügipakkumine
    - Müügitellimus
    - Kinnitus
    - Komplekteerimisleht
    - Saateleht
    - Müügiarve
    - Kreeditarve
    - Tagastustellimus
    - Mitmesugused tasude päis
    - Mitmesuguste kulude rida

- Ost

    - Ostutellimus
    - Kinnitus
    - Saabunud kaupade loend
    - Toote sissetulek
    - Ostuarve
    - Mitmesugused tasude päis
    - Mitmesuguste kulude rida
    - Kreeditarve
    - Tagastustellimus
    - Ostutaotlus
    - Ostutaotluse rea lisakulud
    - Pakkumiskutse
    - Pakkumispäise lisakulunõue
    - Pakkumisrea lisakulunõue

- Varud

    - Kandetellimus-- lähetus
    - Kandetellimus-- kättesaamine

Finantsversioonis 10.0.23 toetatakse järgmisi kandeid: 

- Vabas vormis arve

## <a name="supported-countriesregions"></a>Toetatud riigid/regioonid

Maksude arvutamist saab lubada juriidiline isik. 

Versioonis 10.0.21 toetatakse järgmisi juriidilise isiku esmase aadressi riike/piirkondi:

- Austria
- Belgia
- Taani
- Eesti
- Soome
- Prantsusmaa
- Saksamaa
- Ungari
- Island
- Itaalia
- Läti
- Leedu
- Holland
- Norra
- Poola
- Rootsi
- Šveits
- Ühendkuningriik
- USA

Versioonis 10.0.22 toetatakse järgmisi juriidilise isiku esmase aadressi riike/piirkondi:

- Austraalia
- Bahrein
- Kanada
- Egiptus
- Hong Kongi EHP
- Kuveit
- Uus-Meremaa
- Omaan
- Katar
- Saudi Araabia
- Lõuna-Aafrika
- Araabia Ühendemiraadid

Versioonis 10.0.23 toetatakse järgmisi juriidilise isiku esmase aadressi riike/piirkondi:

- Tai
- Jaapan
- Malaisia
- Singapur

## <a name="related-resources"></a>Seotud ressursid

[Maksuteenusega alustamine](./global-get-started-with-tax-calculation-service.md)

[Mitu käibemaksukohustuslase numbrit](./emea-multiple-vat-registration-numbers.md)

[Maksufunktsiooni tugi üleviimistellimuse jaoks](./tasks/tax-feature-support-for-transfer-order.md)

[Kuidas koostada maksuteenuste laiendit](./tax-service-add-data-fields-tax-integration-by-extension.md)
