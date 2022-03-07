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
ms.openlocfilehash: 57eda6a833df6ff8e91c006bbc5096554eff6c503a8b7ba2bd0b13e2f8e98f56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766142"
---
# <a name="generate-variants-for-engineering-products"></a>Tehnikatoodete variantide loomine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua tehnikatoodete variante.

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
1. Sulgege leht ja valige **Väljastatud tootevariandid**. Pange tähele, et kuvatakse esmakordselt loodud variant (valge V-1).
1. Valige **Variantide soovitused**.
1. Süsteem soovitab loodud värviväärtustega variante (näiteks valge V-1, kollane V-1 ja roheline V-1).
1. Valige soovitatud variandid ja valige **OK**, et vabastada variandid tehnikaettevõttele. Pange tähele, et kehtivad järgmised tingimused. 
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
