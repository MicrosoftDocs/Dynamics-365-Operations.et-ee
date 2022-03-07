---
title: Tootedimensioonid
description: 'On olemas viis tootedimensiooni: värv, konfiguratsioon, suurus, stiil ja versioon. Tootedimensioonid saab ühendada dimensioonigruppidesse ja dimensioonigrupid saab määrata tooteetalonidele. Tootevariantide määratlemise määravad tootedimensioonide kombinatsioonid.'
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bdfd9482d30bd65cf84fae032df78e1243e05239
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426031"
---
# <a name="product-dimensions"></a>Tootedimensioonid

[!include [banner](../includes/banner.md)]

On olemas viis tootedimensiooni: värv, konfiguratsioon, suurus, stiil ja versioon. Tootedimensioonid saab ühendada dimensioonigruppidesse ja dimensioonigrupid saab määrata tooteetalonidele. Tootevariantide määratlemise määravad tootedimensioonide kombinatsioonid.

Tootedimensioonid on tootevarianti identifitseerivad omadused. Tootevariantide määratlemiseks saate kasutada tootedimensioonide kombinatsioone. Tootevariandi loomiseks peate määratlema tooteetaloni jaoks vähemalt ühe tootedimensiooni.

## <a name="product-variants"></a>Tootevariandid

Tootevariante nimetatakse ka kaupadeks. Kaup on materiaalne toode, mis ei ole sama, mis teenus. Samuti on võimalik määratleda tooteetalon, mille tüüp on „teenus”. Kasutades tüüpi „teenus”, saate määratleda teenuseid sisaldavaid tootevariante. Näiteks saate määrata tooteetaloni nõustamistööle ning tootevariandid tööle, mida teevad vanem- ja nooremnõustajad.

## <a name="product-dimensions"></a>Tootedimensioonid

Tootevariandi saab luua tootedimensiooni väärtuste alusel.

Suuruse-, värvi- ja stiilidimensioonide jaoks saab tootedimensiooni väärtusi luua järgmistes asukohtades.

- Leht **Suurus** (**Tooteteabe haldus \> Seadistus \> Dimensiooni- ja variandigrupid \> Suurused**)
- Leht **Värv** (**Tooteteabe haldus \> Seadistus \> Dimensiooni- ja variandigrupid \> Värvid**)
- Leht **Stiil** (**Tooteteabe haldus \> Seadistus \> Dimensiooni- ja variandigrupid \> Stiilid**)

Konfiguratsioonidimensiooni jaoks luuakse tootedimensiooni väärtused tavaliselt kas tootekonfiguraatoris või dimensioonipõhises konfiguraatoris. 

Tooteversioonid luuakse tavaliselt kindlate versioonide jaoks siis, kui toode oma elutsükli jooksul areneb. Tooteversioonidest räägitakse selles teemas hiljem üksikasjalikumalt.

Tootedimensioone saab luua ja hallata ka lehel **Tootedimensioonid**, millele pääseb juurde järgmistest asukohtadest.

- Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**. Valige toimingupaanil **Tootedimensioonid**.
- Avage **Tooteteabe haldus \> Tooted \> Kõik tooted ja tooteetalonid**. Valige tooteetalon. Valige toimingupaanil **Tootedimensioonid**.
- Avage **Tooteteabe haldus \> Väljastatud tooted**. Valige tooteetalon. Valige toimingupaani vahekaardi **Toode** grupis **Tooteetalon** suvand **Tootedimensioonid**.

Kaubale loodavate variantide arv on piiratud võimalike tootedimensiooni kombinatsioonide arvuga.

> [!TIP]
> Toote kasutamisel näiteks tellimusereal valite tootedimensioonid selleks, et määrata tootevariant, millega soovite töötada.

## <a name="example"></a>Näide

Ettevõte müüb teksasid. Kaup *Teksad* kasutab värvi- ja suurusedimensioone. Teksasid müüakse kolmes eri värvis ja kuues eri suuruses. Värvid on sinine, must ja pruun. Suurused on XS, S, M, L, XL ja XXL. Kõiki suurusi pole kõigis kolmes värvis saadaval. Kui kõik kombinatsioonid oleksid saadaval, oleks teksasid 18 tüüpi. Selles näites aga on toodetud ainult järgmised üheksa tootevariandi kombinatsiooni.

| Värv | Suurus |
|-------|------|
| Sinine  | XS   |
| Sinine  | L    |
| Sinine  | E    |
| Must | E    |
| Must | L    |
| Must | XL   |
| Pruun | L    |
| Pruun | XL   |
| Pruun | XXL  |

## <a name="the-version-product-dimension"></a>Tootedimensioon „versioon”

Versioon on tootedimensioon, mille eesmärk on aidata teil kogu tarneahelas hallata ja jälgida toote mitut versiooni. Versiooni jälgimine on tootjatele oluline edu saavutamiseks, sest nad tegutsevad maailmas, kus toote elutsüklid kahanevad pidevalt, kvaliteedi- ja töökindlusnõuded on järjest karmimad ning tooteohutusele keskendutakse üha enam.

Standardse tootedimensioonina toimib versioon samamoodi nagu olemasolevad tootedimensioonid (suurus, stiil, värv ja konfiguratsioon). Seetõttu saate seda kasutada lisaks tooteversioonide jälgimisele ka muude eesmärkide jaoks.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Versioonidimensiooni sisselülitamine

#### <a name="before-you-turn-on-the-version-dimension"></a>Enne versioonidimensiooni sisselülitamist

Kui lülitate versioonidimensiooni sisse, võivad mõned funktsioonid rikki minna või lakata ootuspäraselt töötamast, kui olete paigaldanud muid lahendusi, mis kohandavad varude dimensioone. Kui soovite, et versioonidimensioon töötaks korralikult, peate need lahendused värskendama, et nende varude dimensioonid hõlmaks ka versioonidimensiooni.

Kui testite oma lahenduste ühilduvust versioonidimensiooniga, pöörake tähelepanu järgmistele elementidele.

1. **Funktsionaalsus:** on oluline kontrollida, et varude dimensioone hõlmavad kohandused töötaks koos versioonidimensiooniga.
1. **Viited varude dimensioonidele:** otsige viiteid varude dimensioonidele (st kohti, kus dimensioonidele viidatakse sõnaselgelt). Viited üksusele `InventDimId` peaks töötama midagi muutmata, kuid pöörake tähelepanu stiili või värvi hõlmavatele viidetele. Näiteks kontrollige kindlasti järgmisi elemente.

    - API kutsed laiendatud klassides
    - Kõik viited kindlatele varude dimensioonidele laiendamiskoodis (see kood peab samal ajal hakkama saama nii versioonidimensiooni kui ka stiili- värvi- ja suurusedimensioonidega).

1. **Viited aegunud API kutsetele:** versioonidimensiooni juurutamisel püüdis Microsoft teha kasutuks nii vähe API-sid kui võimalik. Need vähesed API-d, mis on nüüd aegunud, kuvavad nüüd konfiguratsioonivõtme **Tootedimensioon – versioon** sisselülitamisel hoiatuse. Enne tootmissüsteemis versioonidimensiooni sisselülitamist tuleb teie laiendatud lahendustes nende API-de kutsed parandada. Siin on versioonipõhised aegunud API-d.

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Kaardid:** kui mõni kaart kasutab varude dimensioone, tuleb värskendada selle kaardiga seotud asjaomaseid seosevastendusi, et need sisaldaks versioonidimensiooni. Laiendatud mudelis või tabelilaiendustes pöörake tähelepanu tabelitele, mille väljad sisaldavad varude dimensioone.
1. **Microsoft Dynamics 365 Commerce'i funktsionaalsus:** pärast sisselülitamist võib versioonidimensiooni leida rakenduses Dynamics 365 Supply Chain Management tervest Commerce'iga seotud koodist. Sellegipoolest ei toetata versioonidimensiooni veel Commerce'i kanali andmebaasis, kassades ega e-kaubanduse rakendustes. Nendes Commerce'i põhistes rakendustes ei toetata olukordi, kus kasutajad müüvad/lähetavad või tagastavad / võtavad vastu varusid versioonidimensiooni põhjal. Varude saadavuse otsingu funktsioonid ei erista Commerce'i rakendustes varusid versioonidimensiooni järgi. Selline käitumine meenutab konfiguratsioonidimensiooni praegust käitumist terves Commerce'is.

#### <a name="turn-on-the-version-dimension"></a>Versioonidimensiooni sisselülitamine

Enne versioonidimensiooni kasutamist peate selle oma süsteemis sisse lülitama. Selleks on vaja administraatoriõigusi.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
1. Lülitage sisse funktsioon nimega *Tootedimensioon „versioon”*. (Lisateavet leiate teemast [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Lülitage oma süsteem [hooldusrežiimi](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Laiendage vahekaardil **Konfiguratsioonivõtmed** suvandit **Kaubandus** ja märkige märkeruut **Tootedimensioon – versioon**.
1. Lülitage [hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) välja.

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Valdkonnad, kus versioonidimensiooni ei toetata

Järgmistes valdkondades ei toetata versioonidimensiooni, kuna selle dimensiooni juurutamine põhjustaks kahjutoovaid muudatusi.

- Kuluobjekti kuuaruanne
- Kuluobjekti aruande vahemälu
- MCR-i müügi statistika kauba põhjal
- Hankija kataloogid
- EcoResProductDimensionGroupEntity

Lisaks ei toeta versioonidimensiooni Commerce'i tellimuste loomise ja töötlemise funktsioonid (nt kassa, kõnekeskuse ja e-kaubanduse tellimused). Pole veel teada, millal Commerce'i tellimusi täiendatakse, et seda toetada.

### <a name="functional-characteristics-of-the-version-dimension"></a>Versioonidimensiooni funktsionaalsed omadused

Versioonidimensioon toimib samamoodi nagu teised tootedimensioonid. Kuid selle eripära tõttu ning kuna see on mõeldud toote mitme versiooni haldamiseks ja jälgimiseks, toimib see veidi teistmoodi. Siin on mõned erinevused ja sarnasused.

- **Versioonigruppi pole.**

    Kuigi suuruse, värvi ja stiili puhul eksisteerib gruppide kontseptsioon (värvigrupp, suurusegrupp ja stiiligrupp), pole olemas versioonigrupi kontseptsiooni. Grupid võimaldavad teil eelmääratleda rakendatavaid väärtuseid, nii et kui määrate näiteks tootele värvigrupi, saab toode kasutada kõiki selle värvigrupi värve. Seda kontseptsiooni ei rakendata versioonidimensiooni puhul, kuna toote loomisel ei ole toote versioonid eelmääratletud. Selle asemel luuakse versioonid toote elutsükli jooksul nii nagu vaja. Kui toote vorm, sobivus ja funktsioon jäävad samaks, siis loote tüüpiliselt uue toote asemel uue versiooni.

- **Tootevariandi soovitused töötavad nii nagu praegu.**

    Tootevariandi soovitused loovad soovitusi kõikide versioonidimensiooni väärtuste põhjal, nii nagu teiste dimensioonide puhul. Versioonidega toodete loomise ja väljaandmise protsess on sama mis teisi dimensioone kasutavate toodete puhul. Versioonidega toote loomisel luuakse esimene versioon (V1) tootedimensioonina ja väljastatakse variandid. Toote muutumisel ja uue versiooni vajaminemise korral lisatakse uus versiooni väärtus (V2) ning väljastatakse vajalikud variandid. Ei eeldata, et kõik versioonid (V1, V2 ja V3) luuakse toote jaoks varem valmis.

> [!IMPORTANT]
> Kui lülitate versioonidimensiooni sisse ja kasutate seda, võivad mõned lahendused, mis viitavad varude dimensioonidele, lõpetada ootuspärase töötamise. Nende probleemide kinnitamiseks ja lahendamiseks võtke mõjutatud lahendustega seoses ühendust oma sõltumatu tarkvaratarnijaga (ISV). Lisateavet leiate teemast [Versioonidimensiooni lubamine](#enable-version-dim).
