---
title: Laokannete tootefiltrite konfigureerimine
description: Selles teemas kirjeldatakse, kuidas konfigureerida tootefiltreid ja filtrikoode laokaupade kategoriseerimiseks laos. Filtrite abil saate ka määratleda, millised kliendid saavad kindlat kaupa tellida ja milliseid kaupu saab kindlalt hankijalt osta.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 021ce940a4ea6d59719d1c6bc79532832cc2f3ff
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567675"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Laokannete tootefiltrite konfigureerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida tootefiltreid ja filtrikoode laokaupade kategoriseerimiseks laos. Filtrite abil saate ka määratleda, millised kliendid saavad kindlat kaupa tellida ja milliseid kaupu saab kindlalt hankijalt osta.

Peale selle saate seadistada ja kasutada tootefiltreid, et laokaupu laos automaatselt korraldada ning ühendada filtreeritud kaubad filtrigruppidesse. Filtreid saab kasutada kaupade käsitsemis-, ostmis- ja müügiprotsesside puhul kategooriatesse panemiseks. Võite soovida rühmitada kaubaartiklid kokku või eraldada need üksteisest, kui nende käsitsemise viis põhine kaalul või käsitsemise piirangutel. Samuti saate määrata, millistelt klientidelt või hankijatelt saab kaupa osta või kellele müüa.

## <a name="prerequisites"></a>Eeltingimused

Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

| Eeltingimus | Juhised |
|---|---|
| Enne toodete lehel **Väljastatud toote üksikasjad** peate lülitama toote laoala dimensiooni grupi lao töötlemise sisse. | Avage **Tooteteabe haldus \> Seadistus \> Dimensiooni- ja variandigrupid \> Laoala dimensiooni grupid** ja valige või looge laoala dimensiooni grupp, kus suvand **Kasuta laohaldusprotsesside valikut** on määratud valikule *Jah*. |
| Kui kasutate kliendi filtreid ja/või hankija filtreid, peate lubama nende kasutamise laohalduse parameetrites. | Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**. Seadke vahekaardil **Tootefiltrid** suvandi **Luba kliendi filtrid** ja/või **Luba hankija filtrid** väärtuseks *Jah*. |

## <a name="set-up-product-filters"></a>Tootefiltrite häälestamine

Tootefiltrid pakuvad kuni 10 **filtri pealkirja** omadust, mis on loetelu (enum) väärtused. Need loeteluväärtustes on valimiseks saadaval tootefiltri loomisel. Loeteluväärtused *Kood 1* kuni *Kood 10* on süsteemi poolt määratletud ja tähistavad kauba spetsiifilist omadused või atribuuti. Näiteks *Kood 1* võib tähistada kaupu, mille klassifikatsioon on ohtlik materjal. *Kood 2* võib tähistada kaupu, mida ainult hankijad saavad osta. Tootefiltrid määratlevad siis konkreetse **filtri koodi** väärtuse, mis on seostatud väärtusega **Filtri pealkiri**.

1. Avage **Laohaldus \> Seadistamine \> Tootefiltrid \> Tootefiltrid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku tootefilter.
1. Valige väärtus väljal **Tootefilter**.
1. Sisestage väärtus väljale **Filtri kood**.

    ![Tootefiltri häälestamine.](media/Product_Filters10.png "Tootefiltri häälestamine")

1. Sisestage väljale **Kirjeldus** koodi nimi. Näiteks *Kood 2* võib tähistada hankijaid. Seejärel saate luua kindla hankija või hankijate grupi jaoks tootefiltri. Lisateabe saamiseks vaadake teemas allpool toodud jaotist [Hankija filtri koodide häälestamine](#vendor-product-filters).

    ![Tootefiltrite kogum.](media/Product_Filters.png "Tootefiltrite kogum")

## <a name="set-up-product-filter-groups"></a>Tootefiltri rühmade seadistamine

Saate filtri koodide rühmitamiseks kasutada filtrigruppe. See võimalus on abiks, kui asukohakorralduse päringus kasutatakse gruppi ja soovite otsida koodiseeria asemel gruppi. Iga filtrigrupp on seotud kaubagrupiga.

> [!IMPORTANT]
> Mitte kõik tootefiltri grupid pole saadaval filtri koodide jaoks, mis on suuremad kui *Kood 4* (st *Kood 5* kuni *Kood 10*). Näiteks väljastatud toodete puhul, kuigi lisatakse kõik tootefiltri koodid, filtri koodide rühmitamist ei uuendata. Seda käitumist võidakse hilisemates väljaannetes uuendada.

Filtrigruppide seadistamiseks tehke järgmist.

1. Avage **Laohaldus \> Seadistamine \> Tootefiltrid \> Tootefiltrite grupid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljadele **Grupp 1** ja **Grupp 2** kaupade kategooriatesse paigutamiseks kasutatavad nimed.
1. Valige uue rea lisamiseks kiirkaardil **Üksikasjad** suvand **Uus**.
1. Sisestage väljadele **Alguskuupäev/-kellaaeg** ja **Lõpukuupäev/-kellaaeg** filtrigrupi algus- ja lõpukuupäev.
1. Valige väljal **Kaubagrupp** kaubagrupp, mille puhul tootefilter peaks rakenduma.
1. Valige väljadel **Kood 1** kuni **Kood 10** vastavalt vajadusele gruppi kaasatavad filtri koodid.

    ![Kaubagrupp.](media/ProdFilterGroup.png "Kaubagrupp")

> [!NOTE]
> Kui saate lehe sulgemisel tõrketeate, võib koodi seadistus puududa. Lehel **Kaupade grupid** saate muuta koodid kaubagrupi jaoks kohustuslikuks, valides märkeruudud **Määra kaubagrupile filtri kood 1**, **Määra kaubagrupile filtri kood 2** jne.

## <a name="set-up-filter-codes-on-item-groups"></a>Kaubagruppide jaoks filtri koodide häälestamine

Kaubagrupile filtri koodide seadistamisega saate luua koodid, mis on nõutavad toodete jaoks, mis on sellesse kaubagruppi lisatud.

Kaubagruppidele filtrikoodide seadistamiseks toimige järgmiselt.

1. Avage **Varude haldus \> Seadistus \> Varud \> Kaubagrupid**.
1. Kaubagrupi loomiseks valige toimingupaanilt suvand **Uus**.
1. Sisestage nimi väljale **Kaubagrupp**.
1. Väljale **Nimi** sisestage kirjeldus.
1. Märkige kiirkaardil **Ladu** jaotises **Filter on nõutav** ühe või mitme filtri koodi ruudud, mis peavad olema määratud toodete jaoks, mis on kaubagrupiga seotud.

    Väljastatud toote värskendamiseks avage selle leht **Väljastatud toote üksikasjad** ja valige seejärel tegevuspaanil suvand **Redigeeri**. Koodidega seostatud filtrid muutuvad seejärel kiirkaardil **Ladu** kättesaadavaks.

    ![Kaubagrupid.](media/ItemGroup10.png "Kaubagrupid")

1. Märkige jaotises **Kaubagrupi filter** märkeruudud filtritele, mis peavad ühtima filtrigrupiga, et see oleks kauba vaikimisi filtrigrupp.

    Näiteks kui märgitud on märkeruudud **Kasutaja filtri kood 1** ja **Kasutaja filtri kood 2**, peavad nii filtri kood 1 kui ka filtri kood 2 vastama kaubagrupi filtri grupi seadistusele, enne kui filtri grupi saab valida. Uue kauba loomisel on valitud filtrigrupp vaikimisi filtrigrupp väljadel **Grupp 1** ja **Grupp 2** kiirkaardil **Ladu** lehel **Väljastatud toote üksikasjad**.

> [!IMPORTANT]
> Tootefiltri koodid on lubatud ainult kaupade puhul, mis kasutavad täpsemat laohaldust.

## <a name="specify-filter-codes-for-released-products"></a>Väljastatud toodete filtri koodide määramine

Väljastatud toodetele filtri koodide määramiseks tehke järgmist. Näiteks saate kasutada filtri koode, et grupeerida konkreetsete tarnijate ostetavad ohtlikke tooteid.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Toote loomiseks valige toimingupaanilt suvand **Uus**.
1. Sisestage dialoogiboksis **Uus väljastatud toode** andmed, mis on vajalikud uue toote aluse loomiseks, ja seejärel valige **OK**.

    Tootefiltri koodid pole lubatud, kui tootega seotud kaubagrupp ei ole filtri koodide jaoks konfigureeritud.

    Lisateavet vt teemast [Uue toote loomine](../pim/tasks/create-new-product.md).

1. Valige vastavalt vajadusele kiirkaardil **Ladu** jaotises **Tootefiltri koodid** väljade **Kood 1** kuni **Kood 10** filtri koodid, et määratleda tootefiltri koodid.

## <a name="set-up-generally-available-items"></a>Üldiselt kättesaadavate üksuste häälestamine

Saate teha kindlad laokaubad kättesaadavaks ainult klientidele, ainult hankijatele või mõlemale.

> [!NOTE]
> Kliendi ja hankija filtrid ei rakendu ühegi üldiselt saadaolevana seadistatud kauba puhul.

Üldiselt saadaolevate kaupade seadistamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistamine \> Tootefiltrid \> Üldiselt saadaolevad tooted**.
1. Kirje loomiseks valige toimingupaanilt suvand **Uus**.
1. Väljal **Klient või Hankija** valige suvand *Klient*, *Hankija* või *Kõik*, et kaubad oleks kliendile, hankijale või mõlemale saadaval.
1. Sisestage väljale **Alguskuupäev/-kellaaeg** kauba kättesaadavaks muutumise kuupäev ja kellaaeg.
1. Valige kaubagrupp väljal **Kaubagrupp**.
1. Valige väljadel **Kood 1** kuni **Kood 10** filtri koodid üldiselt saadaolevate kaupade piiramiseks.

    Kaubagrupi valimisel saate määrata selle kaubagrupi üldiselt kättesaadavaks. Nendel väljadel filtrikoodide valimisega piirate saadaolevaid kaupu.

## <a name="set-up-customer-product-filters"></a>Kliendi tootefiltrite häälestamine

Saate kasutada seda valikulist protseduuri, et määrata kaubad, mis peaksid olema kliendile saadaval lisaks kaupadele, mis on muudetud kättesaadavaks filtri häälestamise kaudu lehel **Üldiselt kättesaadavad kaubad**. Ühele kliendile saab seadistada mitu filtrit.

Kliendi filtrikoodide seadistamiseks toimige järgmiselt.

1. Avage jaotis **Müük ja turundus \> Kliendid \> Kõik kliendid**.
1. Valige klient.
1. Valige toimingupaani vahekaardil **Klient** grupis **Häälesta** suvand **Toote filtrid**.
1. Valige toimingupaani lehel **Tootefiltri koodid** suvand **Uus**.
1. Sisestage väljadele **Alguskuupäev/-kellaaeg** ja **Lõpukuupäev/-kellaaeg** valitud kaubagrupi algus- ja lõpukuupäev.
1. Valige kaubagrupp väljal **Kaubagrupp**.
1. Väljadel **Kood 1** kuni **Kood 10** valige filtri koodid, mida kasutada kriteeriumidena valitud kaubagrupis klientidele saadavaolevate kaupade piiramiseks. Valik tuleb teha iga kaubagrupi jaoks seadistatud filtri koodi puhul.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Hankija tootefiltrite häälestamine

Saate kasutada seda valikulist protseduuri, et määrata kaubad, mis peaksid olema hankijale saadaval lisaks kaupadele, mis on muudetud kättesaadavaks filtri häälestamise kaudu lehel **Üldiselt kättesaadavad kaubad**. Saate ühe hankija jaoks häälestada mitu filtrit.

Hankija filtrikoodide seadistamiseks toimige järgmiselt.

1. Avage **Hanked \> Hankijad \> Kõik hankijad**.
1. Valige hankija.
1. Valige toimingupaani vahekaardil **Klient** grupis **Häälesta** suvand **Toote filtrid**.
1. Valige toimingupaani lehel **Filtri koodid** suvand **Uus**.
1. Sisestage väljadele **Alguskuupäev/-kellaaeg** ja **Lõpukuupäev/-kellaaeg** valitud kaubagrupi algus- ja lõpukuupäev.
1. Valige kaubagrupp väljal **Kaubagrupp**.
1. Väljadel **Kood 1** kuni **Kood 10** valige filtri koodid, mida kasutada kriteeriumidena valitud kaubagrupis hankijatele saadavaolevate kaupade piiramiseks. Valik tuleb teha iga kaubagrupi jaoks seadistatud filtri koodi puhul.

> [!NOTE]
> Hankija toodetele filtrite häälestus kehtib väljastatud toodetele, kus laohaldusprotsessid on seostatud laoala dimensioonigrupi puhul lubatud. Filtri koode kasutatakse selleks, et määrata, kas süsteem võimaldab kasutajatel ostutellimuse ridade loomisel osta antud kaupa antud hankijalt. Rakenduses Microsoft Dynamics 365 Supply Chain Management on hankija kinnituse käsitlemiseks kaks meetodit. Kui on olemas üks või mitu väljastatud toodet, kus välja **Kinnitatud hankija kontrollmeetod** väärtuseks on seatud *Ainult hoiatus* või *Pole lubatud*, saab nende kaupade puhul lubada mõlemad hankija kinnitamise meetodid. Selline olukord võib põhjustada probleeme, kui kasutajad loovad ostutellimuse ridu.

## <a name="see-also"></a>Vt ka

[Lisateavet vt ajaveebipostitusest WMS – Laofiltri koodid](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]