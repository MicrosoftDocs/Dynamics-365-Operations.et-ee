---
title: Asünkroonne kliendi loomise režiim
description: See artikkel kirjeldab asünkroonset kliendi loomise režiimi moodulis Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 1ac1bc842d5d12ece8951ffed18157e6f9b50d14
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228719"
---
# <a name="asynchronous-customer-creation-mode"></a>Asünkroonne kliendi loomise režiim

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel kirjeldab asünkroonset kliendi loomise režiimi moodulis Microsoft Dynamics 365 Commerce

Äris on kliendi loomiseks kaks režiimi: sünkroonne (või sünkroonitud) ja asünkroonne (või async). Vaikimisi luuakse kliendid sünkroonselt. See tähendab, et need luuakse Commerce Headquartersis reaalajas. Sünkroonitud kliendi loomise režiim on kohe tellitav, kuna uued kliendid on kanalites kohe otsitavad. Ent sellel on ka puudusi. Kuna see loob [Commerce Data Exchange: Real-time Service'i](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) kutsed Commerce Headquarters`isse, võib see mõjutada jõudlust, kui tehakse mitu samaaegset kliendi loomise kutset.

Kui **Loo klient asünkroonses režiimis** suvand on häälestatud **jah** funktsiooniprofiilis (**jaemüügi ja ärikanali \> kanali häälestus \> võrgupoe häälestuse \> funktsiooniprofiilid**), reaalajas teenuse kõnesid ei kasutata kliendikirjete loomiseks kanali andmebaasis. Async Customeri loomise režiim ei mõjuta Commerce Headquartersi jõudlust. Ajutine globaalselt kordumatu IDENTIFIKAATOR (GUID) määratakse igale uuele async Customeri kirjele ja seda kasutatakse kliendi konto ID-na. Seda GUID-i ei kuvata kassakasutajatele. Selle asemel näevad need kasutajad **Ootel sünkroonimist** kliendikonto ID-na.

> [!IMPORTANT]
> Kui müügikoht ei tööta, loob süsteem automaatselt kliendid asünkroonselt, isegi kui async Customeri loomise režiim on keelatud. Seega, olenemata valikust sünkroonimise ja async Customeri loomise vahel, peavad Commerce Headquartersi **administraatorid P-töö jaoks looma ja plaanima korduva pakett-töö**, **sünkroonida kliente ja äripartnereid async Mode** **tööst ja 1010** tööga, nii et kõik async Customersid teisendatakse klientide sünkroonimiseks Commerce Headquartersis.

## <a name="async-customer-limitations"></a>Asünkroonse kliendi piirangud

Async Customeri funktsioonil on praegu järgmine piirang:

- Kliendikaarte ei saa async Klientidele väljastada enne, kui uus kliendi konto ID on kanalisse sünkroonitud.

## <a name="async-customer-enhancements"></a>Async Customeri täiustused

Selleks, et aidata organisatsioonidel klientide haldamiseks kasutada async Customeri loomise režiimi ja aidata reaalajas sidet Commerce Headquartersiga vähendada, on läbi pööratud järgmised täiustused, et tuua sõelumist sünkroonimisrežiimide ja asynci režiimide vahel kanalites. 

| Funktsiooni täiustus | Äriversioon | Funktsiooni üksikasjad |
|---|---|---|
| Jõudluse parendused klienditeabe toomisel kanali andmebaasist | 10.0.20 ja uuem | Jõudluse parandamiseks tükeldatakse kliendiüksus väiksemateks üksusteks. Siis toob süsteem kanali andmebaasist ainult vajaliku teabe. |
| Võimalus luua väljaregistreerimise ajal aadressi asünkroonselt | 10.0.22 ja uuem | <p>Funktsiooni lüliti: **kliendi aadresside asünkroonse loomise lubamine**</p><p>Funktsiooni üksikasjad:</p><ul><li>Aadresside lisamise võimalus ilma reaalajas teenusekutseid commerce headquartersisse tegemata</li><li>Võime kordumatult tuvastada aadresse kanali andmebaasis, ilma kirje ID-d (**RecId** väärtus)</li><li>Aadressi loomise jälitamise ajatemplid</li><li>Aadresside sünkroonimine Commerce Headquartersis</li></ul><p>See funktsioon mõjutab nii sünkroonitud kliente kui ka asynci kliente. Aadresside asünkroonseks redigeerimiseks lisaks nende asünkroonselt **loomisele peate lubama klientide redigeerimise asünkroonses režiimis**.</p> |
| Luba kliendi sünkroonse ja asünkroonse loomise paarsus | 10.0.24 ja uuem | <p>Funktsioonilüliti: **täiustatud async Customeri loomise lubamine**</p><p>Funktsiooni üksikasjad: võimalus koguda täiendavat teavet, nt tiitel, vaikekliendi alluvused ja teisene kontaktteave (telefoninumber ja meiliaadress), kui loote kliente asünkroonselt</p> |
| Kasutajasõbralikud tõrketeated | 10.0.28 ja uuem | Need täiustused aitavad parandada kasutajasõbralikuid tõrketeateid, kui kasutaja ei saa sünkroonimise ajal teavet kohe redigeerida. Lubage need täiustused, **kasutades Commerce’i saidikonstruktori saidisätete laiendustes teatud** **\>** kasutajaliidese elemente, et neid ei saa muuta. |
| Klienditeabe asünkroonse redigeerimise võimalus | 10.0.29 ja uuem | <p>Funktsioonilüliti: **klientide redigeerimise lubamine asünkroonses režiimis**</p><p>Funktsiooni üksikasjad: oskus redigeerida kliendi andmeid asünkroonselt</p><p>Asünkroonselt klienditeabe redigeerimisega [seotud tavaprobleemidele vastuste saamiseks vt Asünkroonse kliendi loomise režiimi KKK-d](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Funktsiooni lülituse hierarhia

Funktsioonilülitite hierarhia **tõttu** peate enne klientide asünkroonses režiimis redigeerimise lubamist lubama järgmised funktsioonid: 

- **Klienditellimuste ja kliendikannete** jõudluse parendused – see funktsioon on pärast versiooni Commerce 10.0.28 väljalaset kohustuslik. 
- **Luba täiustatud async Customeri loomine**
- **Kliendiaadresside asünkroonse loomise lubamine**

Ühistele tõrkeotsingu küsimustele vastuste saamiseks vt [asünkroonse kliendi loomise režiimi KKK-d](async-customer-mode-faq.md). 

**Pärast eelnevalt nimetatud funktsioonide lubamist peate plaanima korduva pakett-töö P-töö** jaoks, **klientide ja äripartnerite sünkroonimine async Mode** **Tööst ja 1010** töö, nii et kõik asynci kliendid teisendatakse klientide sünkroonimiseks Commerce Headquartersis.

### <a name="customer-creation-in-pos-offline-mode"></a>Kliendi loomine ühenduseta režiimis

Nagu varem mainitud, loob süsteem iga kord, kui müügikoht võrgust väljas, automaatselt asünkroonselt kliente, isegi kui async Customeri loomise režiim on keelatud. Seetõttu peavad Commerce Headquartersi **administraatorid looma ja planeerima P-töö jaoks korduva pakett-töö**, **sünkroonima kliendid ja äripartnerid async Mode** **Tööst ja 1010** tööga, nii et kõik asynci kliendid teisendatakse klientide sünkroonimiseks Commerce Headquartersis.

> [!NOTE]
> Kui suvand **Kliendi ühisandmete tabelite filtreerimise** on seatud **jah** väärtusele **Commerce Channeli skeemi** lehel (**Jaemüük ja ärikanal \> Headquarters`i häälestus \> Jaemüügi häälestus \> Kanali andmebaasigrupp**), ei looda kliendikirjeid kassa võrguühenduseta režiimis. Lisateavet leiate artiklist [Andmeüksused](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Lisaressursid

[Kaupluste kliendihaldus](customer-mgmt-stores.md)

[Asünkroonsete klientide teisendamine sünkroonseteks klientideks](convert-async-to-sync.md)

[Kliendi atribuudid](dev-itpro/customer-attributes.md)

[Võrguühenduseta andmete välistamine](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
