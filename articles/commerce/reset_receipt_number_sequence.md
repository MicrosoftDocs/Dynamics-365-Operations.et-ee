---
title: Kviitungi numbrite lähtestamine
description: See teema kirjeldab, kuidas lähtestada kviitungi numbreid, mida kasutatakse erinevate tegevuste jaoks soovitud kuupäeval (nt finantsaasta või kalendriaasta).
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: e81ff86a8b8a4dca6b14a21d6e982b03a928d29e
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020074"
---
# <a name="reset-receipt-numbers"></a>Kviitungi numbrite lähtestamine 

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Jaemüüjad loovad kviitungi numbreid kaupluses erinevate tegevuste jaoks, nt sularaha- ja vedamiskanded, tagastuskanded, klienditellimused, hinnapakkumised ja maksed. Kuigi jaemüüjad määravad kviitungi vormingud ise, on osades riikides või regioonides määrused, mis seavad nendele kviitungi vormingutele piirangud. Näiteks võivad need määrused piirata märkide arvu kviitungil, nõuda järjestikuseid kviitungi numbreid, piirata mõningaid erimärke või nõuda kviitungi numbrite lähtestamist aasta alguses. Microsoft Dynamics 365 Commerce muudab kviitungite numbrite haldamise protsessi väga paindlikuks, et aidata jaemüüjatel täita seadusest tulenevaid nõudeid. See teema selgitab, kuidas kasutada kviitungi numbrite lähtestamise funktsiooni.

Rakenduses Commerce võivad kviitungi vormingud olla tähtnumbrilised. Saate lisada nendesse nii staatilist sisu kui ka dünaamilist sisu. Staatiline sisu sisaldab tähemärke, numbreid ja erimärke. Dünaamiline sisu sisaldab üht või mitut märki, mis esindavad teavet, nagu kaupluse number, terminali number, kuupäev, kuu, aasta ja numbriseeriad, mis automaatselt suurenevad. Vormingud määratletakse funktsiooniprofiili jaotises **Kviitungi nummerdamine**. Järgmine tabel kirjeldab dünaamilist sisu tähistavaid märke.

| Märgid | Kirjeldus |
|------------|-------------|
| L          | Kaupluse numbri jaoks kasutatakse märki **S**. Näiteks kui kaupluse number on HOUSTON1, kuvatakse vorming **SSS** kviitungil kui „ON1”. Vorming **SSSSS** kuvatakse kviitungil kui „STON1”. |
| T          | Terminali numbri jaoks kasutatakse märki **T**. Näiteks kui terminali number on 00011, kuvatakse vorming **TTTT** kviitungil kui „0001”. |
| C          | Personali ID numbri jaoks kasutatakse märki **C**. Näiteks kui töötaja ID on 000160, kuvatakse vorming **CCCC** kviitungil kui „0160”. |
| ddd        | Märgid **ddd** vastavad päevale aastas, alates 1 kuni 366. Näiteks 15. jaanuaril kuvatakse vorming **ddd** kviitungil kui „015”. |
| MM         | Märke **MM** kasutakse kahekohaliseks kuuks. Näiteks jaanuaris kuvatakse vorming **MM** kviitungil kui „01”. |
| DD         | Märke **DD** kasutakse kahekohaliseks kuupäevaks. Näiteks 15. jaanuaril kuvatakse vorming **DD** kviitungil kui „15”. |
| YY         | Märke **YY** kasutakse kahekohaliseks aastaks. Näiteks mis tahes kuus 2020. aastal kuvatakse vorming **YY** kviitungil kui „20”. |
| \#         | Järjestikuseks nummerdamiseks kasutatakse numbrimärki (**\#**). Näiteks vorming **####** kuvatakse kviitungil kui „0001”, „0002”, „0003” jne. |

Saate lähtestada kviitungi järjestikuse nummerdamise kindlal kuupäeval. Seejärel lähtestab süsteem esimese kande, mis toimub valitud lähtestamise kuupäeval pärast kl 12.00, numbriseeriale 1. Samuti saate määrata, kas lähtestamine toimub ainult üks kord või kas see kordub igal aastal. Kui määratud on iga-aastane kordumine, toimub lähtestamine automaatselt igal aastal, kuni jaemüüja otsustab selle peatada. 

Lähtestamise sisselülitamiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**.
1. Kiirkaardil **Kviitungi nummerdamine** valige suvand **Lähtesta numbri lähtestamise kuupäev**.
1. Rippmenüü dialoogiaknas väljal **Lähtestamise kuupäev** valige tulevane kuupäev, millal lähtestamine peaks aset leidma.
1. Väljal **Kviitungi lähtestamise tüüp** valige suvand **Ainult üks kord** või **Kord aastas**.
1. Valige nupp **OK**.

![Kviitungi lähtestamise kuupäeva valimine](media/Enable_receipt_reset.png "Kviitungi lähtestamise kuupäeva valimine")

Pärast kuupäeva valimist kuvatakse see veerus **Järgmine kviitungi numbri lähtestamise kuupäev**. Lähtestamise kuupäev kohaldub kõigile kviitungi kande tüüpidele. Seega lähtestatakse kviitungi numbriseeria kõigil kviitungi tüüpidel.

Kui lähtestamise kuupäev saabub, lähtestatakse kviitungi number iga tüübi esimese kande jaoks. Lisaks teisaldatakse lähtestamise kuupäev funktsiooniprofiilis veerust **Järgmine kviitungi numbri lähtestamise kuupäev** veergu **Praegune kviitungi numbri lähtestamise kuupäev**. See muudatus näitab, et kui registrit lähtestamise kuupäeval ei kasutata, lähtestatakse kviitungi number järgmine kord, kui registrit *kasutatakse*. Näiteks 3. detsembril 2019 valisite lähtestamise kuupäevaks **1. jaanuar 2020**. 1. jaanuaril, kui registrid teevad oma esimese kande, lähtestatakse kviitungi number. Samas ühte registrit detsembris ja jaanuaris ei kasutata, kuid seejärel hakatakse seda kasutama veebruaris. Sellisel juhul, kuna lähtestamise toiming on määratletud, lähtestatakse selle registri kviitungi number, kui register teeb veebruaris esimese kande.

Tulevaste lähtestamise kuupäevade tühjendamiseks saate kasutada funktsiooni **Tühjenda lähtestamise kuupäev**. Kui aga lähtestamise kuupäev toimus minevikus, ei saa seda tagasi võtta. Seega toimub lähtestamine ikkagi kõikide registrite jaoks, kus lähtestamist veel pole toimunud.

> [!NOTE]
> Olenevalt teie valitud lähtestamise kuupäevast ja kviitungi vormingust, võivad esineda kviitungi numbrite duplikaadid. Kuigi kassasüsteem saab nende olukordadega hakkama, suurendavad need tagastuste töötlemiseks kuluvat aega, kuna müüjad peavad valima kviitungite duplikaatide seast. Kui kviitungite duplikaadid ei olnud plaanitud tagajärg, võivad ilmneda muud andmete korrastamisega seotud komplikatsioonid. Seetõttu soovitame teil kasutada dünaamilisi kuupäeva märke (nt **ddd**, **MM**, **DD** ja **YY**), et pärast lähtestamist aidata vältida kviitungi numbrite duplikaate.
