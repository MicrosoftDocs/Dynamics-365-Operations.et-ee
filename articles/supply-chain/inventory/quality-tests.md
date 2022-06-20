---
title: Kvaliteedijuhtimise testid
description: See artikkel kirjeldab, kuidas luua katseid, mida Saab Microsofti kvaliteettellimuste puhul kasutada Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac67ee97a4890c646daefa6b09feae25c4f15d0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857601"
---
# <a name="quality-management-tests"></a>Kvaliteedijuhtimise testid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas luua katseid, mida Saab Microsofti kvaliteettellimuste puhul kasutada Dynamics 365 Supply Chain Management.

Kasutate lehte **Testid**, et määratleda ja vaadata üksikuid teste, mis määravad, kas teie tooted vastavad kvaliteedinõuetele. Saate määrata katsegrupile vähemalt ühe eraldi katse. Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused. Kvantitatiivsete testide puhul kasutatakse mõõtmise väärtusi. Kvalitatiivsete testide puhul kasutatakse testi muutujaid.

- Kvantitatiivse testi jaoks on välja **Tüüp** väärtuseks määratud *Murd* või *Täisarv*. Mõõtühik on samuti täpsustatud. Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.
- Kvalitatiivsete katsete puhul väli **Tüüp** on seatud valikule *Suvand*. Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta. Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.

Testile saate soovi korral määrata testimisinstrumendi. Kvaliteeditellimustega testide loomiseks ja kasutamiseks ei pea testimisinstrumente vaja olema. Lisateavet vt [Kvaliteedijuhtimise testvahendid](quality-test-instruments.md).

Samuti võite soovi korral määrata testi jaoks ühiku, et näidata mõõtühikut, milles test tulemused on salvestatud. Näiteks võib temperatuuri test sisaldada kas Fahrenheiti või Celsiuse kraadi ühikut.

## <a name="example-of-a-test"></a>Testi näide

Tootmisettevõte teeb ostetud materjalile kaks testi: kvantitatiivne materjali kvaliteedi test ja pakendikahjustuste kvalitatiivne test. Ettevõte määrab lisateabe kvalitatiivse testi kohta, et määratleda testi muutuja (kahjustatud pakend) ja selle tulemused. Ettevõte kasutab lehte **Katsegrupid**, et määrata katsegrupile kaks katset ning määrata katsepõhine teave. testgrupp määratakse kvaliteettellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.

## <a name="create-a-test"></a>Katse loomine

Testi loomiseks tehke järgmist.

1. Avage **Varud \> Seaded \> Kvaliteedijuhtimine \> Testid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Test** – Sisestage testi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage testi detailne kirjeldus.
    - **Tüüp** – Valige testi tulemuste tüüp. Kvantitatiivsete katsete puhul valige *Murd* või *Täisarv*. Kvalitatiivsete testide jaoks valige *Suvand*.
    - **Testvahend** – Valige [testvahend](quality-test-instruments.md), mida peaks testil kasutama.
    - **Ühik** – kui valisite *Tüüp* väljal *Murd* või **Täisarv** (st kui test on kvantitatiivne test), valige mõõtühik, milles testitulemused tuleks salvestada.

1. Sulgege leht.

> [!NOTE]
> Pärast testi salvestamist ei saa te enam ruudustikul välja **Tüüp** redigeerida. Kui peate testi jaoks salvestatavat testitulemuste tüüpi muutma, valige **Muuda kvaliteettesti tüüpi** tegevuspaanil. Dialoogiaknas **Muuda kvaliteettesti tüüpi**, seadke välja **Uus tüüp** väärtuseks soovitud tüüp ja seejärel valige dialoogiakna sulgemiseks **OK**.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise testvahendid](quality-test-instruments.md)
- [Kvaliteedijuhtimise testgrupid](quality-test-groups.md)
- [Kvaliteedijuhtimise testi muutujad](quality-test-variables.md)
- [Kvaliteediseosed](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
