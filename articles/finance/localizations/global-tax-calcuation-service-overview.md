---
title: Maksuarvutuse ülevaade
description: See artikkel selgitab maksuarvutuse võimaluse üldist ulatust ja funktsioone.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689880"
---
# <a name="tax-calculation-overview"></a>Maksuarvutuse ülevaade

[!include [banner](../includes/banner.md)]

Maksuarvestus on hüperskaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada. Maksumootor on täielikult konfigureeritav. Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga. Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.

Maksuarvutus integreerub Dynamics 365 Finantside ja .finantsiga Dynamics 365 Supply Chain Management. Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.

> [!IMPORTANT]
> Kui lubate maksuarvestuse teenuse, võidakse teha mõningaid seotud andmete toiminguid andmekeskuses, mis ei ole andmekeskus, mis haldab teie teenuse andmeid. Vaadake [Reeglid ja tingimused](https://go.microsoft.com/fwlink/?linkid=2156043) üle enne maksuarvutamise lubamist. Teie privaatsus on meie jaoks oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://go.microsoft.com/fwlink/?LinkId=521839).

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

- Aasia ja Vaikse ookeani regioon
- Austraalia
- Brasiilia
- Kanada
- Euroopa
- Prantsusmaa
- India
- Jaapan
- Lõuna-Aafrika Vabariik
- Šveits
- Araabia Ühendemiraadid
- Ühendkuningriik
- Ameerika Ühendriigid

> [!NOTE]
> Maksuarvutus ei toeta Dynamics 365 varasemat versiooni, nt Dynamics AX 2012 või Dynamics 365 valdustes juurutamist.

## <a name="versions"></a>Versioonid
Soovitame teil importida ja seadistada oma maksuarvestuse konfiguratsioon versiooniga, mis vastab teie finantside või tarneahela halduse versioonile.

| Finants- või tarneahela halduse versioon | Maksu konfiguratsiooni versioon               |
| --------------- | --------------------------------------- |
| 10.0.31         | Maksu arvutamise konfiguratsioon 40.56.240 |
| 10.0.30         | Maksu arvutamise konfiguratsioon 40.55.239 |
| 10.0.29         | Maksu arvutamise konfiguratsioon 40.55.236 |
| 10.0.28         | Maksu arvutamise konfiguratsioon 40.54.234 |
| 10.0.27         | Maksu arvutamise konfiguratsioon 40.54.234 |


## <a name="data-flow"></a>Andmevoog

Siin on maksuarvestuse andmevoo protsessi liigendus. 

1. RCS-s saate vaadata ja importida maksustatava dokumendi mudeli konfiguratsioone ja mudeli vastendamise konfiguratsioone. Kui peate täpsema stsenaariumi konfiguratsioone laiendama, vaata [Andmeväljade lisamine maksukonfiguratsioonides](tax-service-add-data-fields-tax-configurations.md).
2. RCS-sis looge või säilitage maksufunktsioonid. Saate kasutada maksufunktsiooni maksumäärade ja maksu kohaldatavusreeglite säilitamiseks.
3. Pärast maksufunktsiooni häälestuse lõpuleviimist avaldage maksukonfiguratsioonid ja maksufunktsioonid RCS-ist globaalsesse hoidlasse.
4. Rakenduses Finance valige, millist maksufunktsiooni seadistusversiooni konkreetse juriidilise isiku puhul kasutada.
5. Finance ja Supply Chain Management halduses kasutage kandeid nagu tavaliselt. Kui on vaja maksu arvutamist, kogub klient kandest teavet, nt müügitellimust või ostutellimust, ja pakib teabe lastiks. Seejärel saadetakse maksu arvutamiseks taotlus.
6. Maksu arvutamise taotlus on kliendilt saadud ja kalkulatsioon on lõpule viidud. Maksu tulemus tagastatakse seejärel kliendile.
7. Dynamics 365 klient saab käibemaksu tulemuse ja esitab käibemaksu arvutamise tulemuse käibemaksu leheküljel.

## <a name="supported-transactions"></a>Toetatud kanded

Maksu arvutuse saab lubada kannetega. 

Järgmises tabelis loetletakse vastavas versioonis toetatud kanded.

| Versioon | Kanded |
|---------|--------------|
| 10.0.29 | Perioodilised töölehed |
| 10.0.28 | Hankija maksetööleht<br> Kliendimaksete tööleht | 
| 10.0.26 | Päevaraamatud<br> Hankijaarvete tööleht |
| 10.0.23 | Vabas vormis arve |
| 10.0.21| Müük<br><ul><li>Müügipakkumine</li><li>Müügitellimus</li><li>Kinnitus</li><li>Komplekteerimisleht</li><li>Saateleht</li><li>Müügiarve</li><li>Kreeditarve</li><li>Tagastustellimus</li><li>Mitmesugused tasude päis</li><li>Mitmesuguste kulude rida</li></ul>Ost<br><ul><li>Ostutellimus</li><li>Kinnitus</li><li>Saabunud kaupade loend</li><li>Toote sissetulek</li><li>Ostuarve</li><li>Mitmesugused tasude päis</li><li>Mitmesuguste kulude rida</li><li>Kreeditarve</li><li>Tagastustellimus</li><li>Ostutaotlus</li><li>Ostutaotluse rea lisakulud</li><li>Pakkumiskutse</li><li>Pakkumispäise lisakulunõue</li><li>Pakkumisrea lisakulunõue</li></ul>Varud<ul><li>Kandetellimus-- lähetus</li><li>Kandetellimus-- kättesaamine</li></ul>|

## <a name="supported-countriesregions"></a>Toetatud riigid/regioonid

Maksu arvutamise saab käivitada toetatud lokaliseerimisfunktsiooniga. Järgmine tabel loendab riigid/regioonid juriidilise isiku esmase aadressi jaoks.

| Versioon | Riik/regioon |
|---------|----------------|
| 10.0.26 | -Hiina <br>-Tšehhi Vabariik<br>-Hispaania |
| 10.0.24 | Mehhiko |
| 10.0.23 | -Tai <br>-Jaapan <br>-Malaisia <br>-Singapur |
| 10.0.22 | -Austraalia<br>-Bahrein <br>-Kanada<br>-Egiptus <br>– Hong Kongi EHI <br>-Kuveit <br>-Uus-Meremaa <br>-Omaan <br>-Katar <br>– Saudi Araabia <br>-Lõuna-Aafrika <br>-Ühendemiraadid |
| 10.0.21 | -Austria <br>-Belgia <br>-Taani <br>-Eesti <br>-Soome <br>-Prantsusmaa <br>-Saksamaa <br>-Ungari <br>-Island <br>-Iirimaa <br>-Itaalia <br>-Läti <br>-Leedu <br>-Holland <br>-Norra <br>-Poola <br>-Rootsi <br>-Šveits <br>-Ühendkuningriik <br>-Ameerika Ühendriigid |

Mis tahes Riigi/regiooni puhul, mida Microsoft ei lokaliseeri, saab maksuarvutust lubada ja käitada teiste globaalsete funktsioonidega.

## <a name="related-resources"></a>Seotud ressursid

[Maksuteenusega alustamine](./global-get-started-with-tax-calculation-service.md)

[Mitu käibemaksukohustuslase numbrit](./emea-multiple-vat-registration-numbers.md)

[Maksufunktsiooni tugi üleviimistellimuse jaoks](./tasks/tax-feature-support-for-transfer-order.md)

[Kuidas koostada maksuteenuste laiendit](./tax-service-add-data-fields-tax-integration-by-extension.md)
