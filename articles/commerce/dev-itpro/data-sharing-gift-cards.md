---
title: Kinkekaartide kontsernisisene andmete jagamine
description: See artikkel kirjeldab, kuidas konfigureerida Microsoft Dynamics 365 Commerce Kasutama Dynamics 365 Finance’i andmete ühiskasutuse funktsioone andmealades kinkekaardi andmete sünkroonimiseks.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: bc0df6c4aac72907e8523069e3f1ae100780dc3c
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473927"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Kinkekaartide kontsernisisene andmete jagamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida nii Microsoft Dynamics 365 Commerce, et see kasutab Dynamics 365 Finance andmete ühiskasutuse funktsioone kinkekaardi andmete sünkroonimiseks. Seejärel saab andmekirjete ühiskasutuse funktsiooni kasutada andmete jagamiseks ettevõtete vahel kahe andmeala vahel. Nii saab ärisisene kingitabel jagada andmeid kahe ettevõtteüksuse vahel. Lisateavet Dynamics 365 Finance’i ettevõtetevahelise andme ühiskasutuse kohta vt ettevõtetevahelisest [andmete ühiskasutusest](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Ettevõte | Dynamics 365 Finance keskkonnas juriidiline isik |
| Kinkekaart | Sisemine Dynamics 365 Commerce kinkekaardi toode. |

## <a name="prerequisites"></a>Eeltingimused

Kasutajad peavad konfigureerima oma keskkonna ettevõtetevaheliseks andmete jagamiseks, nagu on kirjeldatud [ettevõtetevahelises andmete ühiskasutuses](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

**Tabeli RetailGiftCardTable** välja **DataSharingType väärtuseks** **peab** kinkekaardi tabeli topeltkirjete ühiskasutuse lubamiseks olema seatud Duplicate (DRS). Lisateavet vt arendajate [jaoks ettevõtetevahelisest andmete ühiskasutusest](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Konfigureerige kinkekaartide jaoks ettevõteteülene andmete ühiskasutus.

Kinkekaartide jaoks ettevõtetevahelise andmete ühiskasutuse konfigureerimiseks järgige neid samme.

1. Minge commerce headquartersi süsteemihalduse häälestuse **konfigureerimiseks \>\> ettevõtetevahelise andme ühiskasutusena**.
1. Tegevuspaanil valige uus **,** et lisada andmete ühiskasutuse kirje.
1. Sisestage **väljale** Nimi andmete ühiskasutuse kirje nimi (nt **Kinkekaardid**).
1. Valige jaotisest **Tabelid ja väljad, mida** soovite jagada, suvand **Lisa**.
1. Sisestage **dialoogiboksi Jaga** uut tabelit väljale **Tabeli** **nimi väärtus RETAILGIFTCARDTABLE** (jaemüügi kinkekaartide tabel). Väli **Tabeli silt** tuleks automaatselt seada kinkekaardi **tabeliks**.
1. Veenduge, et **kõikide valitud on märkeruudud** **Salvesta** andmed ettevõtte kohta, **On kordumatu** indeks ja Pole veel ühiskasutuses. Nende märkeruutee valimine käivitab andmete ühiskasutuse funktsiooniga seotud kontrollid.
1. Valige käsk **Lisa tabel**. Kinkekaardi **tabeli (RetailGiftCardTable) kirje** peaks nüüd ühiskasutuseks ilmuma tabelites **ja väljades**. Valige kae sümbol (^), et vaadata kõiki tabeli välju, mis seostatakse automaatselt ühiskasutuseks tabeliga.
1. Jaotises Ettevõtted **, mis jagavad neis tabelites** kirjeid, valige **suvand Lisa**, et lisada ettevõte, millega andmeid jagada.
1. Valige ripploendist **rida** Ettevõte.
1. **Sisestage väljale** Nimi ettevõtte nimi.
1. Ettevõtteridade lisamiseks korrake samme 8 kuni 10.
1. Kui olete lõpetanud ettevõtteridade lisamise, valige tegevuspaanil suvand **Luba**.
1. Saate hoiatusteate, mis sisaldab järgmist: "Soovitatav on teha see toiming ainult mittet tööaegades. Kõik samaaegsed kandetoimingud nurjuvad poliitika tabelite puhul. Kas soovite jätkata?" Valige **Jah,** et nõustuda.
1. Saate hoiatusteate, mis ütleb: "Kas soovite nüüd kopeerida kõik olemasolevad andmed kõigi ühisettevõtete vahel?" Valige **Jah,** et nõustuda.

Pärast mõlema teatega nõustumist hakkavad tabelid kopeerima andmeid üle konfigureeritud ettevõtete. Saldod, mis ilmnevad ühe ettevõtte kinkekaardi vastu, on siis teisele ettevõttele nähtavad.

## <a name="additional-resources"></a>Lisaressursid

[Maksete KKK](payments-retail.md)

[Maksmismoodul](../add-checkout-module.md)

[Maksemoodul](../payment-module.md)
