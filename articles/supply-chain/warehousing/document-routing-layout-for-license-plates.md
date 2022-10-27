---
title: Dokumendi protsessisildi paigutused
description: See artikkel kirjeldab, kuidas kasutada vormindamise meetodeid siltidele väärtuste printimiseks.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708640"
---
# <a name="document-routing-label-layout"></a>Dokumendi protsessisildi paigutus

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas luua litsentsiplaadi, konteineri ja voo siltide paigutusi. See annab ka juhised, kuidas kasutada paigutuste loomiseks kasutatavat TheMibra Programming Language (ZPL) programmi.

Dokumendi protsessi sildi paigutused määravad viisi, kuidas sildid välja asuvad ja andmed, mis neile prinditakse. Saate konfigureerida printimise käivitamispunktid mobiilsideseadme menüü üksuste ja töömallide häälestamisel.

Selle artikli teave kehtib kõikide dokumendi protsessi siltide paigutuste kohta, [kaasa](tasks/license-plate-label-printing.md) arvatud litsentsiplaadi siltide, [konteineri siltide](print-container-labels.md) ja voo siltide [paigutused](configure-wave-label-printing.md).

Saate printida väga keerukaid silte, eeldusel, et printimisseade suudab tuvastada sellele saadetud teksti. Näiteks vöötkoodiga ZPL-i paigutus võib sarnaneda järgmise näitega.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Sildi printimise protsessi käigus asendatakse selle näite tekst `$LicensePlateId$` andmeväärtusega. Mitmed laialdaselt kättesaadavad siltide tegemise tööriistad aitavad teil vormindada sildi paigutuse teksti. Paljud neist tööriistadest toetavad vormingut `$FieldName$`. Lisaks kasutab Microsoft Dynamics 365 Supply Chain Management erivormingu loogikat dokumendi marsruudi valiku paigutuse välja vastenduse osana.

Prinditavate väärtuste nägemiseks avage jaotis **Laohaldus \> Päringud ja aruanded \> Identifitseerimisnumbri sildid**.

## <a name="turn-on-this-feature-for-your-system"></a>Selle funktsiooni sisselülitamine teie süsteemi jaoks

Kui teie süsteem ei kaasa juba selles artiklis kirjeldatud funktsioone, [minge](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsioonihalduse ja lülitage *sisse täiustatud litsentsiplaadi sildipaigutuste* funktsioon. (Tarneahela halduse versiooni 10.0.21 puhul lülitatakse see funktsioon vaikimisi sisse. Tarneahela haldus 10.0.25 kohaselt on see funktsioon kohustuslik ja seda ei saa välja lülitada.)

## <a name="custom-number-formats"></a>Kohandatud numbrivormingud

Saate kohandada numbriväljade väärtuste vormingut, mis prinditakse järgmis vorminguga koodide abil.

```dos
$FieldName:FormatString$
```

Siin on selle vormingu kohta selgitus.

- `FieldName` on andmevälja nimi (nt **Kogus**).
- `FormatString` määratleb, kuidas andmeid peab printima.

Järgmistes näidetes kirjeldatakse, kuidas saate kohandada välja töö kogus (**Kogus**).

- Kui soovite alati nelja numbrit kuvada (kasutades nulle kohatäitena), kasutage `$Qty:0000$`. Näiteks kui kogus on 10, kuvatakse sildil „0010”.
- Kui soovite alati kahte komakohta kuvada, kasutage `$Qty:0.00$`. Näiteks kui kogus on 10, kuvatakse sildil „10,00”.

Saadaolevate numbrivormingu stringide täieliku loendi leiate teemast [Kohandatud numbrivormingu stringid](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Kohandatud stringi vormingud

Stringi esimesi tähemärke saate eemaldada järgneva välja ja vormingu koodi abil.

```dos
$FieldName:#..$
```

Tähemärk `#` tähistab siin vahelejäetavate tähemärkide arvu. Näiteks konteineri seeriaviisilise lähetamise kood (SSCC) identifitseerimisnumbri printimiseks, mis ei sisalda kahte esimest märki, kasutage `$LicensePlateId:2..$`. Sel juhul prinditakse identifitseerimisnumber 0011111111111222221 kujul „11111111111222221”.

## <a name="custom-datetime-formats"></a>Kohandatud kuupäeva/kellaaja vormingud

Järgmises näites kirjeldatakse, kuidas saate juhtida kuupäevade printimiseks kasutatavat vormingut.

```dos
$PrintedDate:dd-MM-yyyy$
```

Selles näites prinditakse kuupäev 30. aprill 2020 kujul „30-04-2020”.

Saadaolevate kuupäeva/kellaaja vormingute täieliku loendi leiate teemast [Kohandatud kuupäeva ja kellaaja vormingu stringid](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Üksikute ridade printimine mitmerealistest andmetest

Kui andmeväli sisaldab mitut rida (st ridu, mis on eraldatud rea jaotustega), saate printida üksiku rea järgmise vormingu abil.

```dos
$FieldName[#]$
```

Tähemärk `#` tähistab siin rea numbrit, mida soovite printida. (Kasutage numbrit 1 esimesel real.)

Näiteks kui teie süsteemil on väli `AdditionalAddress`, mis talletab mitmerealise aadressi järgnevalt.

Contoso Inc.  
Tänava nimi 123  
Mingi linn, mingi riik

Saate printida selle aadressi ühe rea kaupa järgmiste koodide abil.

| Kood | Prinditav tekst |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | Tänava nimi 123 |
| `$AdditionalAddress[3]$` | Mingi linn, mingi riik |

## <a name="print-and-format-from-a-display-method"></a>Printimine ja vorming kuvamisviisilt

Saate printida kuvamisviisi abil, kasutades järgmist vormingut.

```dos
$DisplayMethod()$
```

Seda vormingut saate kombineerida teiste selles artiklis varem kirjeldatud tüüpide abil. Näiteks kui on teil kuvamisviis nimega `DisplayListOfItemsNumbers()` ja soovite printida selle viisi esimese kaubakoodi. Sel juhul saate kasutada järgmist koodi.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Lisateave siltide printimise kohta

Lisateavet siltide häälestamise ja printimise kohta vt järgmistest artiklitest:

- [Litsentsiplaadi sildi printimine](tasks/license-plate-label-printing.md)
- [Prindi konteineri sildid](print-container-labels.md)
- [Voosildi printimine](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
