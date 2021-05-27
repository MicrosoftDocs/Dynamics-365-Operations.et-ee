---
title: Üksuse kvaliteedigrupid
description: Selles teemas kirjeldatakse, kuidas kauba kvaliteedigruppe kasutada ja luua toodete loogiliseks rühmitamiseks, et neid saaks kvaliteettellimuste automaatseks genereerimiseks määrata kvaliteediseostele.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022248"
---
# <a name="item-quality-groups"></a>Üksuse kvaliteedigrupid

[!include [banner](../includes/banner.md)]

Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid. Selles teemas kirjeldatakse, kuidas kauba kvaliteedigruppe kasutada ja luua toodete loogiliseks rühmitamiseks, et neid saaks kvaliteettellimuste automaatseks genereerimiseks määrata kvaliteediseostele.

Kvaliteedigrupile määratud kauba või kaubale määratud kvaliteedigruppide seadistamiseks, muutmiseks ja vaatamiseks minge **Varude haldus \> Seaded \> Kvaliteedigrupid**. Pärast katsenõuete määratlemist lehel **Katsegrupid** saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks. Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele. Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte **Kvaliteediseosed**.

## <a name="example-of-an-item-quality-group"></a>Kauba kvaliteedigrupi näide

Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale. Seega määratleb ettevõte kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid. Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded. Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi.

Sama tootmisettevõte toodab ka ühesuguste tootmisalaste testimisnõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete testide tegemiseks. Ettevõte määratleb kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.

## <a name="create-a-quality-group"></a>Kvaliteedigrupi loomine

Kvaliteedigrupi loomiseks tehke järgmist.

1. Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Kvaliteedigrupid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Kvaliteedigrupp** – Sisestage kvaliteedigrupi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage kvaliteedigrupi detailne kirjeldus.

1. Sulgege leht.

## <a name="manually-add-items-to-a-quality-group"></a>Käsitsi kaupade lisamine kvaliteedigruppi

Kaupade käsitsi lisamiseks kvaliteedigruppi järgige neid samme.

1. Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Kvaliteedigrupid**.
1. Valige kvaliteedigrupp, millele soovite kaupu lisada.
1. Toimingupaanil valige käsk **Kaubad**.
1. Ruudustiku rea lisamiseks valige **Kaubad kvaliteedigrupis** lehekülje tegevuspaanil suvand **Uus**. Seejärel seadistage uue rea jaoks välja **Kaubakood** väärtuseks kaubakood, mille soovite lisada.
1. Korrake eelmist etappi iga lisakauba puhul, mille lisama peate.
1. Sulgege lehed.

## <a name="add-multiple-items-to-a-quality-group"></a>Mitme kauba lisamine kvaliteedigruppi

Mitme kauba lisamiseks kvaliteedigruppi järgige neid samme.

1. Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Kvaliteedigrupid**.
1. Looge või valige kvaliteedigrupp, millele soovite kaupu lisada.
1. Toimingupaanil valige käsk **Lisa kaubad**.
1. Sisestage dialoogiboksis **Päring** lisatavate kaupade filtrikriteeriumid. Näiteks võite filtreerida kõiki kaupu konkreetses kaubagrupis.
1. Valige nupp **OK**.
1. Dialoogiboksis **Lisa kaupu** kuvatakse ruudustikus kõik päringuga sobivad kaubad. Tulemuste ülevaatamine.

    Kui muudatused on nõutavad, valige suvand **Vali**, et naasta dialoogiboksi **Päring** ja korrigeerida oma päringut.

1. Kui tulemused sisaldavad kõiki kaupu, mida soovite lisada, valige **OK**.
1. Sulgege leht.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Kauba käsitsi seostamine kvaliteedigrupiga

Kaupade käsitsi kvaliteedigrupiga seostamiseks järgige neid samme.

1. Avage **Varude haldus \> Seades \> Kvaliteedikontroll \> Kauba kvaliteedigrupid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Kaubakood** – Valige lisamiseks kaubakood.
    - **Kvaliteedigrupp** – Valige kaubale määratav kvaliteedigrupp.

1. Korrake eelmist sammu iga lisakauba ja kvaliteedigrupi kombinatsiooni puhul, mida tuleb lisada.
1. Sulgege lehed.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Kvaliteedigrupi käsitsi lisamine lehelt Väljastatud tooted

**Väljastatud tooted** lehelt käsitsi kvaliteedigrupi lisamiseks, järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toode, millele soovite kvaliteedigrupi määrata.
1. Toimingipaani **Varude haldus** vahekaardi **Kvaliteet** grupis, valige **kauba kvaliteedigrupid**.
1. Ruudustiku rea lisamiseks valige **Kaubad kvaliteedigrupis** lehekülje tegevuspaanil suvand **Uus**. Seejärel määrake uue rea jaoks väli **Kvaliteedigrupp** kvaliteedigrupile, mille soovite tootele määrata.
1. Korrake eelmist sammu iga täiendava kvaliteedigrupi puhul, mida soovite tootele määrata.
1. Sulgege lehed.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise testvahendid](quality-test-instruments.md)
- [Kvaliteedijuhtimise testid](quality-tests.md)
- [Kvaliteedijuhtimise testgrupid](quality-test-groups.md)
- [Kvaliteedijuhtimise testi muutujad](quality-test-variables.md)
- [Kvaliteediseosed](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
