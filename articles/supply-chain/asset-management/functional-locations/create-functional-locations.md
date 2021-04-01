---
title: Töö asukohtade loomine
description: Selles teemas selgitatakse, kuidas varahalduses töö asukohta luua.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1875ddd5c57639830a70aeebf7ef41114044f839
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253659"
---
# <a name="create-functional-locations"></a>Töö asukohtade loomine

[!include [banner](../../includes/banner.md)]

 

Selles teemas selgitatakse, kuidas varahalduses töö asukohta luua.

Kui loote töö asukoha struktuuri, võtke arvesse, et kui olete töö asukoha korra loonud, siis te ei saa seda enam algsest asukohast teisaldada. See tähendab, et peaksite hoolikalt kaaluma oma tööde asukohtade struktuuri, enne kui hakkate neid varahalduses looma. Kui töö asukoht ei sobi, saate selle kustutada eeldusel, et seda poel veel kasutusele võetud.

Töö asukohtadega töötamiseks alustage kahe töö asukoha „kategooria” loomisega.

- Looge *üks* töö vaikeasukoht, millel poel alamasukohti. Seda töö asukohta kasutatakse uute varade loomisel ainult varade standardasukohana.  
- Looge oma ettevõttes hooldustööde haldamiseks vajalikud töö asukoha struktuurid.

## <a name="create-a-default-functional-location"></a>Uue töö vaikeasukoha loomine

Kui kasutate töö asukohti, alustage uue vara loomisel ühe vaikeasukoha loomisega. See töö asukoht on see, mille teete valikus **Varahaldus** > **Seadistus** > **Varahalduse parameetrid** > **Vara** link > väli **Töö vaikeasukoht**. Töö vaikeasukohta saab kasutada uute varade loomisel ja kui te pole veel seadistanud nende varade jaoks töö asukoha struktuuri.

1. Valige **Varahaldus** > **Ühine** > **Töö asukohad** > **Kõik töö asukohad**.  
2. Tehke funktsioonis **Kõik töö asukohad** valik **Uus**.
3. Sisestage ID väljale **Töö asukoht**, näiteks „0000” või „vaikimisi”, et näidata, et see on spetsiaalne töö asukoht.
4. Sisestage töö vaikeasukoha nimetus väljale **Nimi**.
5. *Ärge* valige väljal **Emaüksus** ülataseme üksust – jätke see väli tühjaks.
6. Valige väljal **Töö asukoha tüüp** töö asukoha tüüp, mida kasutatakse töö vaikeasukoha jaoks. Lisateavet töö asukohtade tüüpide seadistamise kohta lugege teemast [Töö asukoha tüübid](../setup-for-functional-locations/functional-location-types.md).
7. Valige nupp **OK**. Sellesse töö asukohta ei tohi lisada täiendavaid andmeid, kuna seda kasutatakse ainult uute varade ajutise asukohana seni, kuni olete oma ettevõtte kasutuses olevate töö asukohtade jaoks vara installinud.

## <a name="create-functional-locations"></a>Töö asukohtade loomine

Järgnev protseduur kirjeldab, kuidas luua teie ettevõtte hoolduse haldamiseks vajalikke töö asukohti.

1. Valige **Varahaldus** > **Ühine** > **Töö asukohad** > **Kõik töö asukohad**. Töö asukoha saate luua tabelivaates või üksikasjade vaates.
2. Valige nupp **Uus**.
3. Sisestage ID väljale **Töö asukoht**.
4. Sisestage töö asukoha nimetus väljale **Nimi**.
5. Kui töö asukoht on struktuuri alamasukoht, valige ülataseme asukoht väljal **Ülataseme üksus**.
6. Valige tüüp väljal **Töö asukoha tüüp**.
7. Valige nupp **OK**.
8. Lisateabe lisamiseks valige töö asukoht ja klõpsake nuppu **Redigeeri**.

>[!NOTE]
>Olenevalt teie töö asukoha töötsükli oleku seadistusest peate võib-olla looma kõik töö asukoha alamasukohad ja seejärel muutma enne varade installimise alustamist töö asukoha töötsükli olekut. Lisateavet leiate vara installimise kohta lugege teemast [Varade installimine töö asukohtades](../functional-locations/install-objects-on-functional-locations.md). Lisateabe saamiseks töö asukoha töötsüklite oleku kohta lugege teemast [Töö asukoha töötsükli olekud](../setup-for-functional-locations/functional-location-stages.md).

Üksikasjade vaates näete kiirkaarti, kus saate lisada ja redigeerida töö asukohta käsitlevat teavet.

## <a name="general-information"></a>Üldteave

Selles jaotises antakse ülevaade ülataseme ja alataseme teabest töö asukoha struktuuris. Jaotises **Üksikasjad** näete varade atribuutide, hoolduskavade ja töö asukohaga seotud varade arvu. Jaotises **Varud** saate valida tegevuskoha ja lao, millega töö asukoht on seotud. Tegevuskoht ja ladu kasutatakse seoses töökäsu kaubaeelarvetega. Kaubaeelarve loomisel kasutatakse vara töö asukohast automaatselt tegevuskoha- ja laoteavet. Jaotises **Töötsükli olek** kuvatakse teave töö asukoha töötsükli oleku kohta.

## <a name="installed-assets"></a>Paigaldatud varad

Lisateavet vara installimise kohta lugege teemast [Varade installimine töö asukohtades](../functional-locations/install-objects-on-functional-locations.md). Selle kiirkaardi nupu **Vaade** abil saate kuvada kiirkaardil rohkem välju. Välju **kehtiv alates** ja **Alamvara** saab kuvada tabelis.

## <a name="asset-attribute-requirements"></a>Vara atribuudi nõuded

Sellel kiirkaardil saate töö asukohta installitud varade jaoks lisada kindlaid atribuudinõudeid. Need nõuded on ainult teavitamise eesmärgil. Need ei takista teil installida varasid teiste atribuutide nõuetega. Valige **Lisa rida** ja valige atribuudi tüüp. Seejärel sisestage vastav **Väärtus**, valige lävi väljal **Lävekriteeriumid** ja salvestage kirje.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Hoolduskavad ja hoolduskorrad

Siin saate töö asukohtadele lisada hoolduskavu ja hoolduskordi (sh alguskuupäeva). Töö asukohta installitud varadel võivad olla seadistatud muud hoolduskavad. Kõiki hoolduskavu ja hoolduskordi saab kasutada töö asukoha varade ja praegu installitud varade kalendrikannete plaanimiseks.

>[!NOTE]
>Kui uuendate varatüüpe, vara kaubamärke ja vara mudelid hoolduskavade üksikasjade vaate **Kõik töö asukohad** > kiirkaardil **Hoolduskavad** pärast hoolduskavade plaanimist, kustutatakse selle töö asukohaga seotud olemasolevad hooldusgraafiku kirjed automaatselt. Selleks, et luua uusi graafikukirjeid, mis vastavad uuendatud hooldusgraafiku installiga töö asukohas, peate selle töö asukoha jaoks käivitama uue hoolduskava graafiku. 

## <a name="address"></a>Kontaktaadress

Sisestage töö asukoha aadress kiirkaardil **Aadress**. Töö asukohtade aadressid päritakse, mis tähendab, et kui alamasukohale pole aadressi määratud, kasutatakse ülataseme üksuse asukoha aadressi.

## <a name="workers"></a>Töötajad

Sellel kiirkaardil saate lisada töö asukohaga seotud töötajaid ja valida töötaja jaoks esmase töö asukoha. 

## <a name="attributes"></a>Atribuudid

Sellel kiirkardil saate määrata töö asukoha väärtused. Neid atribuute saab kasutada töö asukohale vastavate atribuutide või omaduste kirjeldamiseks, näiteks struktuurilised omadused, ehituse tüüp, piirkonna kirjeldused või asukoht maa peal või maa all.

Valige **Lisa rida** ja valige atribuudi tüüp. Järgmisena sisestage atribuudi tüübiga seotud **Väärtus** ja salvestage kirje.

## <a name="financial-dimensions"></a>Finantsdimensioonid

Saate valida töö asukoha finantsdimensiooni. [Töö asukoha tüüpe](../setup-for-functional-locations/functional-location-types.md) saab seadistada nii, et see võimaldaks finantsdimensioonide automaatset uuendamist töö asukohast. See tähendab, et finantsdimensioonile installitud varad saavad automaatselt töö asukoha finantsdimensioonid. See on kasulik, kui soovite erinevaid kulukeskusi olenevalt asukohtadest.

Kui ülataseme töö asukohas uuendatakse andmeid üksuste **Sait**, **Ladu**, **Aadress** ja **Finantsdimensioonid** kohta, saab töö alamasukohti vastavalt uuendada, kui teete selle valiku uuendamise ajal. Avaneb dialoogiaken, mis pakub teile uuendamissuvandeid.

## <a name="copy-a-functional-location-structure"></a>Töö asukoha struktuuri kopeerimine

Kui teie ettevõttel on mitu sarnaste asukohastruktuuridega töö asukohta, saate kasutada mooduli Asset Management kopeerimisfunktsiooni, et luua kiiresti mitu sarnase asukoha hierarhiat. Kui kopeerite kindla töö asukoha või kogu struktuuri, on uuel asukohal või struktuuril kopeerituga sama nimi. Pärast kopeerimist, saate hõlpsalt muuta uue töö asukoha nime või muid sätteid eeldusel, et uue töö asukoha jaoks valitud töö asukoha töötsükli olek seda võimaldab.

1. Valige funktsioonis **Kõik töö asukohad** töö asukoht, mida soovite kopeerida. Näiteks saate valida ülataseme asukoha (ülataseme üksus), kui soovite kopeerida kogu töö asukoha struktuuri, sealhulgas alamasukohad.
2. Valige nupp **Kopeeri töö asukoha struktuur**. Loendilehel valitud asukoht kuvatakse väljal **Kopeeri väljalt**.
3. Sisestage uue asukoha nimi väljale **Uus töö asukoht**.
4. Väljale **Ülataseme üksus, kuhu kopeerida** peate sisestama ainult ülataseme üksuse ID, kui loodav asukoht saab olemasoleva töö asukoha struktuuri osaks.
5. Klõpsake valikut **OK**. Uus töö asukoha struktuur kuvatakse aknas **Kõik töö asukohad**.

>[!NOTE]
>Kui kopeerite töö asukoha struktuuri, määratakse uues struktuuris töö asukoha töötsükli olekuks „esimene etapp”, mille olete töö asukohtade jaoks loonud. Kas saate töö asukohta ümber nimetada või kustutada, kasutades nuppe **Nimeta ümber** ja **Kustuta** väljal **Kõik töö asukohad**, oleneb töö asukoha praegusest töötsükli olekust.

## <a name="delete-a-functional-location"></a>Töö asukoha kustutamine

Töö asukohta koos alamasukohtadega saab kustutada, kui ühtegi kustutavasse töö asukohta pole installitud varasid ja kui praegune töö asukoha töötsükli olek võimaldab seda.

1. Valige funktsioonis **Kõik töö asukohad** töö asukoht, mida soovite kustutada.
2. Vajadusel uuendage töö asukohta töö asukoha töötsükli olekusse, mis võimaldab töö asukohta kustutada.
3. Valige **Kustuta**.

>[!NOTE]
>Kui te ei saa töö asukohta kustutada, saate selle asemel kustutamiseks seadistada töö asukoha töötsükli oleku. Näiteks saate seadistada etapi "Mahakantud" või "Kustutatud", mis ei tohiks olla aktiivne etapp vormil **Töö asukoha töötsükli olekud**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]