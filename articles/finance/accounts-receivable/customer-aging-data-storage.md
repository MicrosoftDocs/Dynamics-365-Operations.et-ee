---
title: Kliendi ajalise jaotuse andmete salvestusruum
description: See artikkel kirjeldab välise salvestuse kasutamist kliendi ajalistusandmete puhul. Saate käivitada kliendi ajalis andmete talletuse protsessi, et muuta väljund kättesaadavaks eksportimiseks välissüsteemi.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7a66485cc9a538f5c3999009b6dbe295d7a5b9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894138"
---
# <a name="customer-aging-data-storage"></a>Kliendi ajalise jaotuse andmete salvestusruum

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab välise salvestuse kasutamist kliendi ajalistusandmete puhul. Microsoft Dynamics 365 Finances saate käivitada kliendi **ajalistuse andmete** talletuse protsessi, et teha väljund välissüsteemi eksportimiseks kättesaadavaks. Protsessi käivitamisel on samad aegumisaruande valikud, mis on süsteemis saadaval, saadaval välissüsteemidele. Üksikasjad kaasatakse alati eksporditud andmetesse.

See võib olla abiks, kui kliendi ajalisustusandmed on välissüsteemi jaoks ladustamiseks kättesaadavad juhul, kui väljund sisaldab palju kliente ja/või palju kandeid. Kui olemasolev kliendi **aegumisaruanne** aegub, kuna printimiseks on liiga palju andmeid, pakub see funktsioon samade andmete saamiseks alternatiivset viisi.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Kliendi aegumisandmete talletamisfunktsiooni lubamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis lubama. Administraatorid saavad funktsioonihalduse sätteid kasutada, et kontrollida funktsiooni olekut ja lubada seda, kui seda on vaja. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** kreedit ja sissenõuete kogumine
- **Funktsiooni nimi:** kliendi aegumisandmete talletus

## <a name="run-the-customer-aging-data-storage-process"></a>Kliendi aegumisandmete talletusprotsessi käitamine

1. Minge konto kreediti **ja sissenõuete päringute \> ja aruannete kliendi ajaloendusandmete \>\> talletusse**.
2. Valige suvand **Uus**.
3. **Sisestage** väljale Nimi protsessi nimi.
4. Seadke ülejäänud parameetrid vastavalt vajadusele.

    > [!NOTE]
    > Kande üksikasjad kaasatakse alati ja töötlemine toimub alati pakett-tööna.

5. Valige nupp **OK**.
6. Värskendage **kliendi aegumisandmete talletuslehte**, et **·** **vaadata partii nime ja partii käitusaja** väärtusi, mis kuvatakse koos töötlemise **oleku väärtusega.** Kui pakett-töö on lõpetatud, **on välja Töötlemine** olekuks **·** **seatud Lõpetatud ja aegumisridade arvu** väli on seatud. Kui pakett-töö on korduv, on **välja Töötlemine väärtuseks** seatud **Ootel**.
7. **Pakett-töö** jaoks lisatud filtrite **ülevaatamiseks** valige aegumisridade arvu välja kõrval nupp Filtreeri.

Kliendi **aegumisandmete talletamisleht** ei sisalda tulemusi. Kliendi aegumisandmete **talletusandmete üksus** võimaldab teil eksportida väljundi mis tahes vormingusse, mida andmehaldus toetab.

> [!NOTE]
> Enne eksportimist lisage filter, et piirata eksporditud tulemused kõige värskema aegumisega. Lisage näiteks järgmised kriteeriumid kõige viimase partii käituse tagastamiseks:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchName())
>
> Teise võimalusena lisage järgmised kriteeriumid, et tagastada praeguse kasutaja viimatine partii käitamine:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchNameForCurrentUser())
