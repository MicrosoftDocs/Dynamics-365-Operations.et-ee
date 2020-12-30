---
title: Vara kooslused
description: Selles teemas kirjeldatakse mooduli Asse Management vara kooslusi (BOM).
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42646ae865cd530203c997fd10c8ccd59e7fa2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426395"
---
# <a name="asset-boms"></a>Vara kooslused

[!include [banner](../../includes/banner.md)]

 

Selles teemas kirjeldatakse mooduli Asse Management vara kooslusi (BOM). Lehel **Vara kooslus** kuvatakse kõigi nende kaupade (varuosad ja muud kaubad) loend, mida vara kogu eluea jooksul kasutatakse. Uue vara loomisel peaksite kaaluma vara koosluse seadistamist seadistusprotseduuri osana. Sel viisil saate jälgida vara kaubaajalugu loomiskuupäevast alates.

Kui olete hooldustöö lõpule viinud ja kauba tarbimine on töökäsul registreeritud, saate jälgida varuosade ja muude põhivarana kasutatavate kaupade tarbimist. See funktsioon võimaldab teil hoida kõigi oma varade puhul täielikku kauba tarbimise kirjet. Näiteks saate seda kirjet kasutada, et jälgida, kas konkreetne varuosa on sageli asendatud või jälgida varuosi või muid kaupu, mida praegu varas kasutatakse.

> [!NOTE]
> Töökäsul võib kauba tarbimine hõlmata nii varuosi kui ka muid lisakaupu, nagu määrdeained, poldid ja tihendid.

Põhivara kooslust saab automaatselt uuendada, tuginedes mooduli Asset Management seadistusele. Kui töökäsu töötsükli olek on loodud valmis või lõpule viidud töökäskude käsitsemiseks ja kui selle töökäsu töötsükli oleku suvandi **Uuenda vara kooslust** väärtuseks on määratud **Jah** lehel **Töökäsu töötsükli olekud**, siis kõik töökäsul kasutatud kaubad uuendatakse automaatselt lehel **Vara kooslus**, kui töökäsk on uuendatud sellesse töökäsu olekusse. 


Samuti saate vara koosluse käsitsi uuendada, luues uue kaubarea lehel **Vara kooslus.**

Lehel **Vara kooslus** saate jälgida varade varuosade ajalugu pärast kauba tarbimise registreerimist töökäsul. Selle funktsiooni kasutamiseks peate valima kaubagrupid, mida tuleks kasutada varuosade registreerimiseks lehel **Varuosade kaubagrupid.**

Vara koosluse funktsiooni kasutamiseks peate esmalt seadistama nõutavad varuosade kaubagrupid. Kui soovite, et vara kooslus töökäsu lõpuleviimise korral automaatselt uuendatakse, saate seadistada töökäsu töötsükli oleku, et seda uuendust käsitseda. 


## <a name="set-up-spare-parts-item-groups"></a>Varuosade kaubagruppide seadistamine

Varuosade ajaloo seadistus põhineb kaubagruppidel, mis on loodud moodulis **Varude ja laohaldus**. Moodulis Asset Management saate seadistada kaubagrupid nii, et saate jälgida valitud kaubagruppide kaupade varuosade ajalugu.

1. Valige **Varahaldus** \> **Seadistus** \> **Vara** \> **Varuosade kaubagrupid**.
2. Kaubagrupi seadistamiseks valige **Uus**.
3. Valige grupp väljal **Kaubagrupp**. Grupi nimi sisestatakse automaatselt väli **Nimi**.

## <a name="view-and-update-asset-boms"></a>Vara koosluste vaatamine ja uuendamine

Pärast kauba tarbimise sisestamist töökäsule saate vaadata registreeritud kauba tarbimist lehel **Vara kooslus**.

1. Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Aktiivsed varad**. Valige loendist vara ja seejärel valige **Vara kooslus.**

    > [!NOTE]
    > Kõigi varade kõigi kauba tarbimise registreerimiste vaatamiseks valige **Varahaldus** \>**Päringud**\>**Varad**\>**Vara kooslus**.

2. Valige **Uuenda vara kooslust**. Värskendusele saate vastavalt vajadusele lisada varasid, varatüüpe ja ressursse, valides suvandi **Vali**. Uuendamise alustamiseks valige **OK**. Samuti saate funktsiooni Uuenda seadistada pakett-tööna.
3. Kui soovite näha rohkem kaupadega seotud teavet, saate lisada laodimensioone. Valige **Varud** \> **Dimensioonide kuvamine** ja seejärel märkige nende dimensioonide ruudud, mida soovite vaadata. Et hoida seda seadistust kõigi varade puhul lehel **Vara kooslus**, seadke suvandi **Salvesta seadistus** väärtuseks **Jah.**
4. Et saada ülevaadet sellest, kus Asset Managementis valitud real olevat kaupa kasutatakse, valige varade, töötüübi vaikesätete, varuosade ja töökäskude puhul väärtus **Kauba kasutuskoht**. 
5. Kui soovite näha ainult aktiivseid kaubaridu, valige **Kuva** \>**Praegune**. Kõigi kaubaridade kuvamiseks, sh read, mille aegumiskuupäev on praegusest kuupäevast varasem, valige **Kuva** \>**Kõik.**

> [!NOTE]
> Kui olete töökäsu täitnud, kui mõned seotud varaga seotud kaubad või varuosad on aegunud või asendatud muude kaupade või varuosadega, soovitame teil vastavalt uuendada ka põhivara kooslust.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Uue kaubarea loomine vara koosluses

Varade kaubaridu saate käsitsi luua.

1. Valige lehel **Vara kooslus** suvand **Uus**.
2. Valige väljal **Vara** väärtus põhivara, millele soovite kaubarea lisada.
3. Sisestage väljale **Rea number** rea seerianumber.
4. Sisestage väljale **Kehtiv** kauba alguskuupäev.
5. Kui kaup aegub, sisestage väljale **Aegumine** lõppkuupäev.
6. Valige kaup väljalt **Kaubakood**. Nimi sisestatakse automaatselt väljale **Toote nimetus**.
7. Sisestage kasutatav kogus väljale **Kogus**. Välja  **Ühik** uuendatakse automaatselt.
