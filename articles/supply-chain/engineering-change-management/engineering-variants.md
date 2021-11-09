---
title: Tehnikatoodete variantide loomine
description: See teema kirjeldab, kuidas luua tehnikatoodete variante
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e24bceac9457212ecaafda876d19ba62df049371
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/27/2021
ms.locfileid: "7471832"
---
# <a name="generate-variants-for-engineering-products"></a>Tehnikatoodete variantide loomine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua tehnikatoodete variante.

## <a name="turn-on-variant-generation-for-engineering-products"></a>Lülitage inseneritoodete jaoks sisse variantide genereerimine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Insenerimuudatuse haldus*
- **Funktsiooni nimi:** *Variantide genereerimine inseneritoodete jaoks*

> [!IMPORTANT]
> Funktsiooni *Variantide loomine tehnikatoodete* jaoks on teie süsteemis nähtav alles pärast seda, kui lubate *tehnika muutmise halduse* konfiguratsioonivõtme. Lisateavet vt teemast [Tehniliste muudatuste haldamise ülevaade](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Looge üks või mitu tehnikatoote uut varianti

Saate luua ühe või mitu uut tootevarianti ilma olemasolevast tootest teavet kopeerimata. See on kasulik, kui peate looma korraga mitu tootevariandit.

Järgmine toiming annab näite, kuidas luua mitmeid variante, mis sisaldavad värvidimensiooni.

1. Avage leht **Väljastatud tooted** (näiteks minge **Tehnika muudatuse haldus \> Üldjuhtimine \> Väljastatud tooted**).
1. Valige toimingupaani vahekaardi **Toode** grupis **Uus** suvand **Tehniline toode**.
1. Avaneb **Uus toode** dialoog. Valige sobiv **Tehnika kategooria**.
1. Kui teie valitud tehikakategooria sisaldab variandi mõõtmeid, saate neile nüüd väärtused määrata. Kui kategoorial on näiteks dimensiooni **Värv**, saate seada selle *siniseks*.
1. Tehke muud vajalikud sätted. Toote loomiseks valige **OK**.
1. Luuakse toode ja V-1 tootevariant ning uus toode avaneb nüüd.
1. Vajadusel lisage variandile materjalide arve (BOM) ja marsruut.
1. Valige toimingupaani vahekaardi **Toode** grupis **Tooteetalon** suvand **Tootedimensioonid**.
1. Avaneb leht **Toote dimensioonid**. See lehekülg sisaldab vahekaarti iga saadaoleva dimensiooni kohta. Igal vahekaardil lisage rida iga väärtuse kohta, mida iga asjakohane dimensioon toetab. (Selle näite puhul võite lisada ridu vahekaardile **Värv** väärtustele *Valge*, *Kollane* ja *Roheline*).
1. Sulgege leht ja valige **Väljastatud tootevariandid**. Pange tähele, et kuvatakse esimene loodud variant (sinine V-1).
1. Toimingupaanil vahekaardil **Tootevariant** valige suvand **Variandisoovitused**.
1. Dialoogiboksis **Variandisoovitused** järgige üht järgmistest sammudest:

    - Dialoogiakna ülaosas on iga saadaoleva dimensiooni jaoks sektsioon. Iga dimensiooni puhul märkige ruut iga väärtuse kohta, mille jaoks soovite variandisoovituse luua, ja valige **Soovitamine** tööriistaribal. Jaotisesse **Soovitatud variandid** lisatakse vastavad soovitused.
    - Tehke tööriistaribal valik **Soovita kõiki** et luua variandisoovitusi kõigile saadaval dimensiooniväärtuste kombinatsioonidele. Jaotisesse **Soovitatud variandid** lisatakse vastavad soovitused.

1. Märkige jaotises **Soovitatud variandid** ruut iga variandi puhul, mida soovite luua. Siis valige **Loo**, et luua ja vabastada valitud variandid tehnikaettevõttele. Kehtivad järgnevad tingimused:

    - Ühelgi loodud variandil pole kooslust ega protsessi.
    - Nende variantide atribuudid on vaikimisi tehnikakategooriast ja neid ei kopeerita eelmisest variandist.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Variandi loomine teise tootevariandi koopiana

Saate tootevariandi luua teise tootevariandi põhjal. Kooslus ja protsess kopeeritakse lähtetoote variandist uude varianti. See võib olla kasulik eraldi tootmistoodete puhul, kui võib olla abiks koosluse loomine algkoosluse põhjal ja varasemast variandist tehtud muudatustest. Jälitatavuse säilitamiseks kopeeriti süsteemikirjed uue koopia loomiseks.

Järgnev protseduur annab näite, kuidas luua uus värvimõõdet sisaldav variant, luues olemasoleva variandi koopia

1. Avage leht **Väljastatud tooted** (näiteks minge **Tehnika muudatuse haldus \> Üldjuhtimine \> Väljastatud tooted**).
1. Valige toimingupaani vahekaardi **Toode** grupis **Uus** suvand **Tehniline toode**.
1. Avaneb **Uus toode** dialoog. Valige sobiv **Tehnika kategooria**.
1. Kui teie valitud tehikakategooria sisaldab variandi mõõtmeid, saate neile nüüd väärtused määrata. Kui kategoorial on näiteks dimensiooni **Värv**, saate seada selle *siniseks*.)
1. Tehke muud vajalikud sätted. Toote loomiseks valige **OK**.
1. Luuakse toode ja V-1 tootevariant ning uus toode avaneb nüüd.
1. Vajadusel lisage variandile materjalide arve (BOM) ja marsruut.
1. Vajadusel lisage tootevariandile atribuute.
1. Lisage sinine V-1 tootevariant tehniliste muudatuste tellimusele.
1. Määrake **Mõju** väärtuseks *Uus variant*.
1. Saate valida uue värviväärtuse (nt *Valge*). Pange tähele, et kehtivad järgmised tingimused. 
    - Uuel variandil on BOM ja marsruut, mis on eelmisest variandist kopeeritud.
    - Uuel variandil on eelmisest variandist kopeeritud atribuudid.
1. Kinnitage muudatuse tellimus.
1. Töödelge muudatuse tellimus. Pärast tellimuse töötlemist luuakse uus V-1 variant ja antakse see välja tehnikafirmale.
