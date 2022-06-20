---
title: Asünkroonne kliendi loomise režiim
description: See artikkel kirjeldab asünkroonset kliendi loomise režiimi moodulis Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 4ca63fe06a804035e976a3432454078c1cca0020
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880136"
---
# <a name="asynchronous-customer-creation-mode"></a>Asünkroonne kliendi loomise režiim

[!include [banner](includes/banner.md)]

See artikkel kirjeldab asünkroonset kliendi loomise režiimi moodulis Microsoft Dynamics 365 Commerce

Äris on kliendi loomiseks kaks režiimi: sünkroonne (või sünkroonitud) ja asünkroonne (või async). Vaikimisi luuakse kliendid sünkroonselt. See tähendab, et need luuakse Commerce Headquarters`is reaalajas. Sünkroonitud kliendi loomise režiim on kohe tellitav, kuna uued kliendid on kanalites kohe otsitavad. Ent sellel on ka puudusi. Kuna see loob [Commerce Data Exchange: Real-time Service'i](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) kutsed Commerce Headquarters`isse, võib see mõjutada jõudlust, kui tehakse mitu samaaegset kliendi loomise kutset.

Kui **Loo klient asünkroonses režiimis** suvand on häälestatud **jah** funktsiooniprofiilis (**jaemüügi ja ärikanali \> kanali häälestus \> võrgupoe häälestuse \> funktsiooniprofiilid**), reaalajas teenuse kõnesid ei kasutata kliendikirjete loomiseks kanali andmebaasis. Async Customeri loomise režiim ei mõjuta Commerce Headquartersi jõudlust. Ajutine globaalselt kordumatu IDENTIFIKAATOR (GUID) määratakse igale uuele async Customeri kirjele ja seda kasutatakse kliendi konto ID-na. Seda GUID-i ei kuvata kassakasutajatele. Selle asemel näevad need kasutajad **Ootel sünkroonimist** kliendikonto ID-na.

> [!IMPORTANT]
> Kui müügikoht ei tööta, loob süsteem automaatselt kliendid asünkroonselt, isegi kui async Customeri loomise režiim on keelatud. Seepärast peavad Commerce headquartersi **administraatorid hoolimata sünkroonimise ja async Customeri loomise valikust looma ja plaanima P-töö jaoks korduva pakett-töö**, **sünkroonida kliendid ja äripartnerid async** Mode tööst (**varasema nimega Sünkrooni kliendid ja äripartnerid Async** Mode'ist) **ja 1010** töö, nii et kõik async kliendid teisendatakse klientide sünkroonimiseks Commerce Headquartersis.

## <a name="async-customer-limitations"></a>Asünkroonse kliendi piirangud

Async Customeri funktsioonil on praegu järgmised piirangud:

- Asünkroonse kliendi kirjeid ei saa redigeerida, kui klient ei ole loodud Commerce Headquarters`is ja uus kliendi konto ID on kanalisse tagasi sünkroonitud.
- Kliendikaarte ei saa async Klientidele väljastada enne, kui uus kliendi konto ID on kanalisse sünkroonitud.

## <a name="async-customer-enhancements"></a>Async Customeri täiustused

Rakenduse Commerce version 10.0.24 **väljalaskest alates saate funktsioonihalduse tööruumis lubada täiustatud async Kliendi** **loomise** funktsiooni. See funktsioon sildeerib asynci ja sünkroonimise kliendi loomisrežiime kassas ja e-kaubanduses järgmistel viisidel:

- Seotusi saab seostada async Klientidega.
- Async Klientide pealkirjad saab lisada.
- Async Klientide teisesed meiliaadressid ja telefoninumbrid saab hõivata.

Äriversiooni 10.0.22 **·** **vabastamisel saate lubada kliendi aadresside asünkroonse loomise funktsiooni Funktsioonihalduse tööruumis**. See funktsioon võimaldab vastloodud kliendiaadresside asünkroonset salvestamist nii klientide sünkroonimise kui ka async Klientide puhul.

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
