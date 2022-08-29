---
title: Kaubahindade võrdluse talletuse aruanne
description: Saage teada, kuidas luua kaubahindade võrdluse talletuse aruannet ja seejärel tulemusi sirvida ja/või eksportida.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c6373679299b68413d75236ca8cc18ceba03e091
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334981"
---
# <a name="compare-item-prices-storage-report"></a>Kaubahindade võrdluse talletuse aruanne

[!include [banner](../includes/banner.md)]

See artikkel **selgitab**, kuidas käivitada kauba hindade võrdluse salvestusaruannet ja muuta väljundi digitaalselt kättesaadavaks, Dynamics 365 Supply Chain Management kas kasutajapõhise lehena või eksporditud dokumendina mitmes vormingus.

Aruande brauseris vaatamisel reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele. Saate sortida tulemusi, filtreerida neid, minna andmetesse süvitsi ja muud.

Aruande tulemused talletatakse andmeüksuses **Kaubahindade võrdlus**, mis võimaldab teil tulemusi filtreerida ja eksportida vormingus, nagu CSV või Microsoft Excel.

Aruanne **Kaubahindade võrdluse talletus** on kasulik juhtudel, kui väljund sisaldab palju ridu. Näiteks sisaldab väljund palju ridu, kui teil on enam kui 40 000 üksusel kuluversioonis ootel kauba hind.

## <a name="turn-the-compare-item-prices-storage-feature-on-or-off"></a>Kaupade hindade salvestamise funktsiooni sisse- või väljalülitamine

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumis valikut Võrdle kauba hinna talletusfunktsiooni.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="generate-a-compare-item-prices-storage-report"></a>Kaubahindade võrdluse talletuse aruande loomine

Aruande **Kaubahindade võrdluse talletus** loomiseks ja salvestamiseks tehke järgmist.

1. Avage **Kuluhaldus > Päringud ja aruanded > Eelmääratud kulude aruanded > Kaubahindade võrdluse talletus**.

1. Valige suvand **Uus**, et avada paan **Kaubahindade võrdlus**. Määrake järgmised valikud, et määratleda, milliseid hindu teie aruandes võrreldakse.

    - Kiirkaardil **Parameetrid** andke aruandele kordumatu **nimi** ja kasutage väljasid jaotistes **Võrreldavad ootel hinnad** ja **Võrdluses kasutatavad hinnad**, et määratleda, milliseid hindu ja kuupäevi võrrelda.
    - Seadistage kiirkardil **Kaasatavad kirjed** filtrid ja piirangud, et määratleda, millised andmed aruandesse kaasata.
    - Seadistage kiirkaardil **Käivita taustal** aruannete loomise viis, aeg ja sagedus.
    > [!NOTE]
    > See aruanne käivitatakse alati pakett-töö osana.

1. Valige **OK**, et rakendada oma sätted ja sulgeda paan.

1. Kui pakett-töö on lõpetatud, loetletakse see lehel **Kaubahindade võrdluse talletus**. Aruande nägemiseks võib olla vajalik lehe värskendamine.

## <a name="explore-the-compare-item-prices-storage-report"></a>Kaubahindade võrdluse talletuse aruandega tutvumine

Pärast aruande loomist saate igal ajal seda vaadata ja sellega tutvuda järgmisel viisil.

1. Avage **Kuluhaldus > Päringud ja aruanded > Eelmääratud kulude aruanded > Kaubahindade võrdluse talletus**.

1. Valige loendist aruanne.

1. Tehke üht järgmistest valikutest.

    - Aruande tulemustest ülevaate saamiseks valige suvand **Ülevaade**.
    - Aruande üksikajalikuma kuva saamiseks valige suvand **Kuva üksikasjad**

1. Pärast valitud vaate avamist saate teha järgmist.

    - Valige peaaegu mis tahes veerupäis, et sortida või filtreerida tabelit selle veeru väärtuste järgi, nagu enamike standardete vormidega Supply Chain Managementis. Pange tähele, et te ei saa sortida ega filtreerida veergu **Netomuutuse hinna %**, kuna see on arvutatud väli.
    - Valige suvand **Dimensiooni kuvamine**, et avada paan, kus saate valida, milline dimensiooni veerg vormile kaasata. Määrake suvand **Salvesta seadistus** olekule **Jah**, kui soovite need seadistused salvestada, et need oleksid alles järgmine kord, kui aruande avate. Valige **OK**, et rakendada oma sätted ja sulgeda.
    - Valige vormil mis tahes rida ja seejärel valige **Kuva üksikasjad**, et näha valitud üksuse kohta rohkem teavet. Saate siin andmetesse süvitsi minna.
    - Valige vormil mis tahes rida ja seejärel valige **Kuva võrdlusdiagramm**, et näha oma tulemuste interaktiivset graafilist esitust, nagu need teie valitud üksusega seonduvad. Saate neid tulemusi uurida, valides diagrammil ja diagrammi legendis erinevaid graafilisi elemente.
    - Valige vormil mis tahes rida ja seejärel valige **Kuva arvutuse üksikasjad**, et näha valitud üksusega seotud arvutuste kohta rohkem teavet. Saate siin andmetesse süvitsi minna.

## <a name="export-the-compare-item-prices-storage-report"></a>Kaubahindade võrdluse talletuse aruande eksportimine

Iga loodud aruanne talletatakse andmeüksuses **Kaubahindade võrdlus**. Saate kasutada Supply Chain Managementi standardseid andmekogumise funktsioone, et eksportida selle üksuse andmed mis tahes toetatud vormingusse, sh CSV või Microsoft Excel.

Järgnev on näide selle kohta, kuidas aruannet **Kaubahindade võrdluse talletus** eksportida.

1. Avage **Süsteemihaldus > Tööruumid > Andmehaldus**.

1. Valige nupp **Ekspordi** jaotises **Andmehaldus**.

1. Avaneb leht **Eksport**, mida kasutate eksportimistöö seadistamiseks. Alustage sellega, et annate oma tööle **grupi nime**.

1. Jaotises **Valitud olemid** valige suvand **Lisa olem**, et avada dialoogiaken, kus saate määrata järgmised valikud.

    - **Olemi nimi** – valige **Kaubahindade võrdlus**.
    - **Sihtüksuse vorming** – valige vorming, mille soovite eksportida.

1. Valige käsk **Lisa**, et lisada uus rida, ja seejärel klõpsake nuppu **Sulge**, et sulgeda dialoogiboks.

1. Tavaliselt ekspordite ühe aruande korraga. Selle tegemiseks seadistage **Filter** rea jaoks, mille äsja paanile **Päring** lisasite. See võimaldab teil määratleda, milliseid aruandeid üksusest **Kaubahindade võrdlus** soovite oma eksporti kaasata. Ühe aruande eksportimiseks seadke järgmised filtri valikud.

    - Vahekaardil **vahemik** valige käsk **Lisa**, et lisada uus rida.
    - Määrake suvad **Tabel** valikule **Kaubahindade võrdlus**.
    - Määrake suvad **Tuletatud tabel** valikule **Kaubahindade võrdlus**.
    - Määrake suvand **Väli** väljale, mille alusel soovite filtreerida. Tavaliselt kasutate suvandit **Täimise nimi** või **Täitmise kellaaeg**.
    - Seadke suvand **kriteeriumid** valitud välja väärtusele, mida soovite otsida (kas aruande nimi või aruande loomise kellaaeg).
    - Vajadusel lisage tabelisse **Vahemik** veel ridu, kuni olete otsitava aruande üheselt identifitseerinud.

1. Valige **OK**, et salvestada oma sätted ja sulgeda.

1. Oma ekspordi seadistuse salvestamiseks valige **Salvesta**.

1. Avage vahekaart **Eksportimise suvandid** ja valige suvand **Ekspordi kohe**, et luua eksportimise fail.

1. Avaneb leht **Käivitamise kokkuvõtte** kokkuvõte, kus saate vaadata oma ekspordi töö olekut ja eksporditud üksuste loendit. Valige üksus **Kaubahindade võrdlus**, mis on loetletud alal **Üksuse töötlemise olek**, ja seejärel valige suvand **Laadi fail alla**, et laadida alla sellest olemist eksporditud andmed.

Lisateavet andmete eksportimiseks andmehalduse kasutamise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]