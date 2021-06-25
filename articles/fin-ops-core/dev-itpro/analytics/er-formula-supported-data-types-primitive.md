---
title: Elektroonilise aruandluse valemite toetatud primitiivsed andmetüübid
description: See teema annab teavet primitiivsete andmetüüpide kohta, mida toetatakse elektroonilises aruandluses (ER) valemites.
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d5e6bb5e070ebbcdb7e99b1b70010acd5fca5ac
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224087"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Elektroonilise aruandluse valemite toetatud primitiivsed andmetüübid

[!include [banner](../includes/banner.md)]

See teema annab teavet primitiivsete andmetüüpide kohta, mida toetatakse [elektroonilises aruandluses (ER)](general-electronic-reporting.md) valemites. Primitiivsete andmetüüpide loend on järgmine:

- [kahendmuutuja](#boolean)
- [kuupäev](#date)
- [kuupäev ja kellaaeg](#datetime)
- [loetelu](#enumeration)
- [juhend](#guid)
- [täisarv](#integer)
- [int64](#int64)
- [tegelik](#real)
- [string](#string)

## <a name="boolean"></a><a name="boolean"></a>Loogiline

*Kahendmuutuja* primitiivne andmetüüp sisaldab väärtust, mida hinnatakse *tõeseks* või *vääraks*. Reserveeritud sõnalisi märksõnu **Tõene** ja **Väär** saate kasutada kõikjal, kus *kahendavaldist* oodatakse. Vaikeväärtus on *väär*.

*Kahendväärtuse* sisemine esitus on *täisarv*. *Täisarvu* väärtust 0 (null) hinnatakse *vääraks* ja kõiki muid *täisarvuväärtusi* loetakse *tõeseks*. Kui [valideerite](general-electronic-reporting-formula-designer.md#TestFormula) konfigureeritud avaldise, mis tagastab *kahendmuutuja* [ER-i valemikujundajas](er-advanced-formula-editor.md), testtulemi paanil kuvatakse *0* (null), kui avaldis tagastab väärtuse *väär*. Vastasel juhul kuvatakse testtulemuste paanil *1*.

*Kahendmuutujal* pole kaudseid konversioone. Siiski saate kasutada [TEKST](er-functions-text-text.md) funktsiooni et *kahendmuutuja* *stringiks* teisendada.

- *Väär* väärtus teisendatakse tekstistringiks **Väär**.
- *Tõene* väärtus teisendatakse tekstistringiks **Tõene**.

> [!NOTE]
> See teisendamine ei sõltu esitatud keele ja kultuuri [kontekstist](er-design-multilingual-reports.md).

Võrlus [tehted](er-formula-language.md#Operators) on ainus tehtemärgi tüüp, mida saab kasutada koos *kahend* andmetüübiga. Kahe *kahendväärtuse* võrdlemiseks saab kasutada järgmisi tehtemärke: \<\> ja =.

## <a name="date"></a><a name="date"></a>Kuupäev

Primitiivne *kuupäeva* andmetüüp talletab päeva, kuu ja aasta. Kuupäevad on võimalik saada järgmiste funktsioonide abil:

- [KUUPÄEVAVÄÄRTUS](er-functions-datetime-datevalue.md)
- [NULLKUUPÄEV](er-functions-datetime-nulldate.md)
- [SEANSSTÄNA](er-functions-datetime-sessiontoday.md)
- [TÄNA](er-functions-datetime-today.md)

*Kuupäeva* andmetüüp võib hoida kuupäevi vahemikus 1. jaanuar 1900 kuni 31. detsember 2154. Vaikeväärtus on **tühi** ja sisemine esitus on kuupäev 1. jaanuar 1900.

*Kuupäeval* pole kaudseid konversioone. Siiski saate kasutada järgmisi selgesõnalisi teisendusfunktsioone:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [KUUPÄEVTÄNAAEG](er-functions-datetime-datetodatetime.md)
- [TEKST](er-functions-text-text.md)

[PÄEVALISAMINE](er-functions-datetime-adddays.md) funktsioon võimaldab teil lisada ja lahutada päevi alates kuupäevadest. Sel viisil saate kuupäeva teisaldada kindla arvu päevi tulevikku ja minevikku. [PÄEVAD](er-functions-datetime-days.md) funktsioon võimaldab teil lahutada kuupäevi üksteisest ja arvutada päevade erinevuse. Lisateavet *kuupäeva* väärtuste teisendamise kohta vt [Kuupäeva ja aja kategooria ER-funktsioonide loendist](er-functions-category-datetime.md).

Võrdlus [tehted](er-formula-language.md#Operators) on ainus tehtemärgi tüüp, mida saab kasutada koos *kuupäeva* andmetüübiga. Kahe *kuupäeva* võrdlemiseks saab kasutada järgmisi tehtemärke: \<\>, \<, \<=, =, \> ja \>=.

## <a name="datetime"></a><a name="datetime"></a>Kuupäev ja kellaaeg

*Kuupäeva ja kellaaja* primitiivne andmetüüp ühendab *kuupäeva* tüübi ja väärtuse, mis tähistab keskööst möödunud kellaaega. Kellaaega väljendatakse tundides, minutites, sekundites ja sekundi murdosades. *Kuupäeva ja kellaaja* väärtus sisaldab ka teavet ajavööndi kohta.

*Kuupäev ja kellaaeg* andmetüüp võib hoida kuupäevi ajavahemikus 1. jaanuar 1900 (1900-01-01T00:00:00.0000000+00:00 edasi-tagasi [vormingus](/dotnet/standard/base-types/standard-date-and-time-format-strings)) ja 31. detsembrini 2154 (2154/12/31T11:59:59.9999999+00:00 edasi-tagasi vormingus). *Kuupäeva ja kellaaja* väikseim ajaühik on üks kümnest miljonist sekundist.

> [!NOTE]
> Kui **hh** [spetsifikatsiooni](/dotnet/standard/base-types/standard-date-and-time-format-strings) kasutatakse tundideks, ei saa 12:59:59:9999999 kohal olevaid ajaväärtusi tõlgendada kehtivate aegadena.
>
> Kui **hh** spetsifikatsiooni kasutatakse tundideks, ei saa 23:59:59:9999999 kohal olevaid ajaväärtusi tõlgendada kehtivate aegadena.

Vaikeväärtus on **tühi** ja sisemine esitus on kuupäev 1. jaanuar 1900 (1900-01-01T00:00:00.0000000+00:00 edasi-tagasi vormingus).

Kuupäevad ja kellaajad on võimalik saada järgmiste funktsioonide abil:

- [KUUPÄEVJA KELLAAEGVÄÄRTUS](er-functions-datetime-datetimevalue.md)
- [NULNULLKUUPÄEVJAKELLAAEG](er-functions-datetime-nulldatetime.md)
- [SEANSSNÜÜD](er-functions-datetime-sessionnow.md)
- [NÜÜD](er-functions-datetime-now.md)

*Kuupäeval ja kellaajal* pole kaudseid konversioone. Siiski saate kasutada järgmisi selgesõnalisi teisendusfunktsioone:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEKST](er-functions-text-text.md)

Lisateavet *kuupäeva ja aja* väärtuste teisendamise kohta vt [Kuupäeva ja aja kategooria ER-funktsioonide loendist](er-functions-category-datetime.md).

Võrdlus [tehted](er-formula-language.md#Operators) on ainus tehtemärgi tüüp, mida saab kasutada koos *kuupäeva ja aja* andmetüübiga. Kahe *kuupäeva ja aja* võrdlemiseks saab kasutada järgmisi tehtemärke: \<\>, \<, \<=, =, \> ja \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Loetelu

*Loendamise* primitiivne andmetüüp on literaalide loend. Võite kasutada rakenduse lähtekoodis määratletud loendeid [lähtekood](../dev-ref/xpp-data-primitive.md#enum). Saate tutvustada ka oma loendusi ER [andmemudelis](general-electronic-reporting.md#data-model-and-model-mapping-components) ja ER [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponentides.

Rakenduste *loendamist* saab kasutada mis tahes ER-mudeli vastenduse ja ER-vormingu avaldistes.

Järgmisel joonisel on kujutatud, kuidas saate **CustVendCorrectiveReasonCode** mudeli redigeeritavale ER-andmemudelile lisada.

[![Konfigureeritud loendimudel ER-i andmemudeli kujundajas](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Mudeli *loendamist* saab kasutada mis tahes ER-mudeli vastenduse ja ER-vormingu avaldistes, mis loodi andmemudeli alusel, kus *loend* kasutusele võeti.

Järgmisel joonisel on kujutatud, kuidas saate lisada **Natura pöördmaksustamise alamkategooriate** redigeeritavale ER-vormingule vormingu loendi.

[![Konfigureeritud loendi vorming ER-i vormingu kujundajas](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Vormingu *loendamist* saab kasutada ainult ER-vormingus avaldistes, kus *loend* kasutusele võeti.

Konfigureeritud ER-komponendile kindla loendi toomiseks konstantina või väärtusena, mida kasutaja, kes kasutab käitusajal dialoogiboksis määratletud ER-lahendust, peate kasutama sobivat tüüpi ER-andmeallikaid.

- Rakenduste loenditele pääseb juurde **Dynamics 365 for Operations \ Loendamine** ja **Üldine \ Kasutaja sisendparameetrid** andmeallika abil. Järgmisel joonisel on kujutatud, kuidas saate redigeeritavasse ER-vormingusse lisada **appenumEiJah** ja **uipEiJah** andmeallikad, mis viitavad rakenduse **NoYes** loendile.

    [![Rakenduste loendamise andmeallikate lisamine ER-vormingus kujundajasse](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Andmemudeli loenditele pääseb juurde kasutades **Andmemudel \ Loendamine** ja **Andmemudel \ Kasutaja sisendparameetrid andmeallika abil** andmeallikaid. Järgmisel joonisel on kujutatud, kuidas saate redigeeritavasse ER-vormingusse lisada **CustVendCorrectiveReasonCode** andmeallikad, mis viitavad **CustVendCorrectiveReasonCod** andmemudeli loendile.

    [![Mudeli loendamise andmeallikate lisamine ER-vormingus kujundajasse](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Vormingule pääseb juurde kasutades **Vorming \ Loendamine** ja **Vorming \ Kasutaja sisendparameetrid** andmeallika abil. Järgmisel joonisel on kujutatud, kuidas saate redigeeritavasse ER-vormingusse lisada **NaturaReverseCharge** andmeallikad, mis viitavad **Natura reverse char alamkategooria** vormingu loendile.

    [![Vormingu loendamise andmeallikate lisamine ER-vormingus kujundajasse](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*Loendamisel* pole kaudseid konversioone. Saate siiski kasutada [TEKST](er-functions-text-text.md) teisendusfunktsiooni *loendi* teksti stringiks teisendamiseks. See teisendus ei sõltu keelest. Lisateavet *loendi* väärtuse seostamise kohta sobivate keelekohaste siltidega leiate [LISTOFFIELDS](er-functions-list-listoffields.md) ja [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) funktsioonide kasutusnäidetest.

Võrdlus [tehted](er-formula-language.md#Operators) on ainus tehtemärgi tüüp, mida saab kasutada koos *loendi* andmetüübiga. Kahe *loendi* võrdlemiseks saab kasutada järgmisi tehtemärke: \<\> ja =.

## <a name="guid"></a><a name="guid"></a>Juhend

*Juhendi* primitiivne andmetüüp sisaldab globaalse ainuidentifikaatori (GUID) väärtust. JUHEND on väärtus, mida saab kasutada kõigis arvutites ja võrkudes, kus kordumatu identifikaator on nõutav. On ebatõenäoline, et number dubleeritakse. Kehtiv JUHEND vastab kõigile järgmistele spetsifikatsioonidele:

- Sellel peab olema 32 kuueteistkümnendnumbrit.
- Lisaks peab olema neli kriipsmärki, mis on manustatud järgmistesse asukohtadesse: 8-4-4-4-12.
- Lisaks saab stringi algusesse ja lõppu lisada valikulisi \{\} klambreid. Näiteks nii **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** kui ka **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** on kehtivad JUHENDI stringid.
- Seetõttu peab sõltuvalt sellest, kas klambrid on lisatud, olema kokku 36 või 38 märki.
- Kuueteistkümnendkohana kasutatavad tähed võivad olla suurtähed (A–F), väiketähed (a–f) või segud.

Saate kasutada järgmisi selgesõnalisi teisendusfunktsioone:

- [JUHENDVÄÄRTUS](er-functions-text-guidvalue.md)
- [TEKST](er-functions-text-text.md)

Võrdlus [tehted](er-formula-language.md#Operators) on ainus tehtemärgi tüüp, mida saab kasutada koos *juhendi* andmetüübiga. Kahe *juhend* väärtuse võrdlemiseks saab kasutada järgmisi tehtemärke: \<\> ja =.

## <a name="integer"></a><a name="integer"></a>Täisarv

*Täisarvuline* primitiivne andmetüüp tähistab arvu, millel pole kümnendkohti. Täisarvu kasutatakse kontrollmuutujatena korduvates lausetes või indeksitena kirjeloendites.

*Täisarv* on täisarv, kuna see sisestatakse otse ER [avaldisse](general-electronic-reporting-formula-designer.md#formula-designer-overview) (valemisse), nagu näiteks **12345**. *Täisarv* on 32 bitti lai. Vaikeväärtus on **0** ja sisemine esitus on pikk arv. *Täisarv* teisendatakse automaatselt *reaalarvuks*.

Lisaks saate kasutada järgmisi selgesõnalisi teisendusfunktsioone:

- [INTVÄÄRTUS](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEKST](er-functions-text-text.md)

*Täisarvu* vahemik on \[-2,147,483,647: 2,147,483,647\]. Kõiki selle vahemiku täisarvusid saab kasutada literaalidena.

Kõiki võrdlus- ja matemaatilisi [tehtemärke](er-formula-language.md#Operators) saab kasutada *täisarvulise* andmetüübiga.

## <a name="int64"></a><a name="int64"></a>Int64

*int64* primitiivne andmetüüp tähistab arvu, millel pole kümnendkohti. *Int64* väärtusi kasutatakse kontrollmuutujatena korduvates lausetes või kirjete identifitseerijatena.

*int64* on 64 bitti lai. Vaikeväärtus on **0** ja sisemine esitus on pikk arv. *int64* teisendatakse automaatselt *reaalseks*.

Lisaks saate kasutada järgmisi selgesõnalisi teisendusfunktsioone:

- [INT64VÄÄRTUS](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEKST](er-functions-text-text.md)

Täisarvu *int64* on \[-9,223,372,036,854,775,807: 9,223,372,036,854,775,807\].

Kõiki võrdlus- ja matemaatilisi [tehtemärke](er-formula-language.md#Operators) saab kasutada *int64* andmetüübiga.

## <a name="real"></a><a name="real"></a>Tegelik

*Reaalne* primitiivne andmetüüp võib lisaks täisarvudele hoida kümnendväärtusi. Saate kümnendkoha literaale kasutada kõikjal, kus *reeaalset* eeldatakse. Kümnendkoha literaal on kümnendkoht, kuna see sisestatakse otse koodi nagu näiteks **2.19**.

> [!NOTE]
> ER-avaldistes kasutatakse komakohtade eraldajana alati perioodi (.).

Reaalset saab kasutada kõikides avaldistes ja neid saab kasutada nii võrdlus- kui aritmeetiliste tehtemärkidega. *Reaali* täpsus on 16 olulist numbrit. *Reaalse* vaikeväärtus on **0.0** ja sisemine ehitus on kahendkoodiga digitaalne (BCD) number. BCD-kodeering võimaldab 0,1 kordsete väärtuste täpseid esitusi. *Reaal* muutuja vahemik on -(10)<sup>127</sup> kuni (10)<sup>127</sup>. Selles vahemikus saab kõiki reaale kasutada ER-avaldistes literaalidena.

*Reaalsel* pole kaudseid konversioone. Kuid järgmisi funktsioone saate kasutada selgesõnaliselt *reaalandmete* teisendamiseks teisteks andmetüüpideks ja teistet andmetüüpidest *reaaliks*:

- [INTVÄÄRTUS](er-functions-conversion-intvalue.md)
- [INT64VÄÄRTUS](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEKST](er-functions-text-text.md)
- [VÄÄRTUS](er-functions-conversion-value.md)

Kõiki võrdlus- ja matemaatilisi [tehtemärke](er-formula-language.md#Operators) saab kasutada *reaalse* andmetüübiga.

## <a name="string"></a><a name="string"></a>String

*Stringi* primitiivne andmetüüp esindab märkide jada, mida kasutatakse tekstide, kontonumbrite, aadresside ja telefoninumbritena.

*Stringi* literaalid on märgid, mis on lisatud jutumärkidesse (""). *Stringi* literaale saab kasutada *stringi* eeldatud väärtuste korral ER avaldistes. Stringe saate kasutada loogilistes avaldistes, näiteks võrdlustes. Saate ühendada ka *stringi* väärtused kasutades **\&** tehtemärki või [CONCATENATE](er-functions-text-concatenate.md) funktsiooni.

> [!NOTE]
> Kui ühendate kaks *stringi* väärtust ja soovite, et tulem *string* ulatub üle ühe rea, kasutage väärtuste vahel reapiiri eraldajat. TEKSTIväljundi puhul võib see eraldaja olla märk, mis luuakse [CHAR](er-functions-text-char.md)(10) või CHAR(13) avaldisega. HTML-i puhul võib see olla **\<br\>** silt.

*Stringi* vaikeväärtus on tühi tekstistring, millel ei ole märke ning sisemine esitus on märkideta loend.

Stringide puhul automaatseid teisendusi ei ole. Siiski saate kasutada järgmisi selgesõnalisi teisendusfunktsioone:

- [CHAR](er-functions-text-char.md)
- [VORMING](er-functions-text-format.md)
- [VASAK](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [ASENDA](er-functions-text-replace.md)
- [PAREM](er-functions-text-right.md)
- [TEKST](er-functions-text-text.md)
- [TÕLGI](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [ÜLEMINE](er-functions-text-upper.md)

Lisateavet *stringi* väärtuste teisendamise kohta vt [tekstikategooria ER-funktsioonide loendist](er-functions-category-text.md).

*Stringi* märkide arv võib olla määramata.

Kõiki võrdlus [tehtemärke](er-formula-language.md#Operators) saab kasutada *stringi* andmetüübiga.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse valemi keel](er-formula-language.md)
- [Toetatud liitandmetüübid](er-formula-supported-data-types-composite.md)
