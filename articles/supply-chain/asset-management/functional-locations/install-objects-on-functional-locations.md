---
title: Varade installimine töö asukohtades
description: Selles teemas kirjeldatakse, kuidas varasid moodulis Asset Management installida.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44e7d3f366ab79b54f021d01c69779ed04859be8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253634"
---
# <a name="install-assets-on-functional-locations"></a>Varade installimine töö asukohtades

[!include [banner](../../includes/banner.md)]

 

Pärast töö asukoha struktuuride loomist on järgmiseks sammuks varade installimine vastavatele töö asukohtadele. Selles teemas kirjeldatakse, kuidas varasid mooduli Asset Managementi nendesse töö asukohtadesse installida. Lisateabe saamiseks varade loomise kohta lugege teemat [Varade sissejuhatus](../objects/introduction-to-objects.md).

Kui olete loonud varade struktuuri, peab kogu vara struktuur olema installitud töö asukohta. Seetõttu saab töö asukohas valida ainult emavarasid (ülataseme varad, mille puudub emavara). Töö asukohta installitakse ka kõik seotud tütarvarad (alamvarad). Kui installite varad töö asukohta, võidakse töö asukohas olevad finantsdimensioonid neile automaatselt üle kanda olenevalt töö asukohas valitud töö asukoha tüübi seadistusest. Lisateavet töö asukohtade tüüpide seadistamise kohta lugege teemast [Töö asukoha tüübid](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Töö asukoha tüübile, mida töö asukoha jaoks kasutatakse, saate seadistada varatüübid. Sel juhul, kui installite vara töö asukohta, kuvatakse ainult emavarad, millel on sama varatüüp varade loendis, mida saab installida töö asukohta.

Pärast varade töö asukohta installimist saate vastavalt vajadusele asendada emavara või vara struktuuri. Nagu varade installimisel, valite asendamiseks emavara. Samuti asendatakse kõik seotud tütarvarad. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Vara struktuuri installimine töö asukohta

1. Valige **Varahaldus** \> **Ühine** \> **Töö asukohad** \> **Kõik töö asukohad** või **Aktiivsed töö asukohad**.
2. Valige vara installimiseks töö asukoht.
3. Valige **Installi vara**.

    Jaotises **atribuudid** kuvatakse vara atribuudinõuete loend, mis on seadistatud töö asukoha tüübis, mis on töö asukoha jaoks valitud. Atribuutidel on ainult informatiivne eesmärk. Süsteem ei valideeri atribuute atribuuteidega, mis on seadistatud installitava varaga. Seda valideerimist peate tegema pärast vara valimist väljal **Vara**.

4. Valige installitav emavara väljal **Vara**. Kõik seotud tütarvarad kaasatakse installi automaatselt.

    Varaloendis paremal olev jaotis **Vara atribuudid** näitab valitud varaga seotud varade atribuute.

5. Valige väljal **Kehtiv** kuupäev ja kellaaeg, millest alates vara installimine kehtib. Pärast seda kuupäeva ja kellaaega on vara ja sellega seotud alamvarade kulud seotud töö asukohaga.

    > [!NOTE]
    > Jaotises **Atribuudid** kuvatakse varas seadistatud vara atribuudid. Näiteks atribuudinõue **Kaal** on lisatud nõudena nii varas kui ka töö asukohas. Kui vara ja töö asukoha atribuudinõuded on samad, sisestatakse väljale **Väärtus** vara atribuudinõuete väärtused. Seetõttu saate kinnitada vara väärtused atribuudinõuetele, mis on seadistatud töö asukohas. Töö asukohas seadistatud atribuudinõuded on tähistatud märkega.

6. Valige nupp **OK**.

    > [!NOTE]
    > Vara installimise muutmiseks selle installimisel uude töö asukohta järgige selle protseduuri juhiseid 1 kuni 6. Kui installite vara uude töö asukohta, desinstallitakse vara automaatselt eelmisest töö asukohast. Aktiivseid hooldustaotlusi või töökäske, mis loodi varale enne selle installimist uude töö asukohta, **ei** kanta automaatselt üle uude töö asukohta. Kui vara jaoks on neid hooldustaotlusi ja töökäske vaja, peate need käsitsi uuesti looma pärast vara installimist uude asukohta.

7. Kõigi töö asukohta installitud varade (sh alamvarade) loendi vaatamiseks valige lehel **Kõik töö asukohad** töö asukoht ja seejärel valige väärtus **Varad**.
8. Töö asukohta installitud varaga seotud aktiivsete hooldustaotluste, aktiivsete töökäskude või vigade registreerimiste loendi kuvamiseks valige lehel **Kõik töö asukohad** töö asukoht ja seejärel Valige **Taotlused**, **Töökäsud** või **Vead**.

> [!NOTE]
> Kui varaga seotud andmeid muudetakse, värskendatakse seda automaatselt töö asukohas, kuhu vara on installitud. See automaatvärskendus puudutab muudatusi hooldustaotlustes, töökäskudes, varade vigade registreerimistes, hooldusekatkestuste registreerimistes ja varamõõdikute registreerimistes.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Ühe vara automaatne loomine töö asukohas

Saate seadistada töö asukohtade etappe ja töö asukoha tüüpe, et käsitseda *ühe* vara automaatset loomist töö asukohas. Vara saab sama ID ja nime nagu töö asukoht. See funktsioon võib olla kasulik, kui tegelete hooldusega suurel, staatilisel varal (nt ehitis).

Enne vara automaatset loomist töö asukohas peavad saadaval olema järgmised seadistusandmed.

- Vara automaatse loomise käitlemiseks saate luua töö asukoha tüübi. Väljal **Vara tüüp** valige vara tüüp. Lisateabe saamiseks lugege teemat [Töö asukoha tüübid](../setup-for-functional-locations/functional-location-types.md).
- Vara automaatse loomise käitlemiseks saate luua töö asukoha töötsükli oleku. Määrake suvand **Loo vara** valikule **Jah**. Lisateabe saamiseks lugege teemat [Töö asukoha töötsükli olekud](../setup-for-functional-locations/functional-location-stages.md).

Kui seadistusandmed on saadaval, olete valmis vara looma.

1. Veenduge lehel **Kõik töö asukohad**, et töö asukoht, kuhu soovite vara automaatselt luua, kasutab töö asukoha tüüpi, mille olete sel eesmärgil loonud.
2. Valige loendist töö asukoht.
3. Valige **Värskenda töö asukohta olekut** ja seejärel valige selleks otstarbeks loodud töötsükli olek. Üks vara installitakse nüüd automaatselt töö asukohta. Varal on töö asukohaga sama nimi.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]