---
title: (RCS) Failide importimine XML-vormingus koos valikuliste atribuutidega
description: Selles teemas kirjeldatakse, kuidas saab kasutaja kujundada elektroonilise aruandluse vormingu konfiguratsiooni failide importimiseks XML-vormingus koos valikuliste atribuutidega.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9447c827a02acb616bbfdcb2c7305e8bdd013c9811e28bb25256db056d85d6a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720708"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Failide importimine XML-vormingus koos valikuliste atribuutidega

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kujundada elektroonilise aruandluse (ER) vormingu konfiguratsiooni failide importimiseks XML-vormingus koos valikuliste atribuutidega. Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid. Enne alustamist laadige alla ja salvestage lokaalselt fail IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684).

1.    Avage **Kõik tööruumid** > **Elektrooniline aruandlus**.
2.    Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.
3.    Klõpsake valikut **Aruandluse konfiguratsioonid**.

## <a name="create-a-new-data-model-configuration"></a>Uue andmemudeli konfiguratsiooni loomine
1.    Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.
2.    Sisestage väljale **Nimi** „Mudel XML-faili importimiseks”.
3.    Klõpsake **Loo konfiguratsioon**.
4.    Klõpsake valikut **Kujundaja**.
5.    Rippdialoogi avamiseks klõpsake valikut **Uus**.
6.    Sisestage väljale **Nimi** "Juur".
7.    Klõpsake käsku **Lisa**.
8.    Rippdialoogi avamiseks klõpsake valikut **Uus**.
9.    Sisestage väljale **Nimi** "Loend".
10.    Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
11.    Klõpsake käsku **Lisa**.
12.    Rippdialoogi avamiseks klõpsake valikut **Uus**.
13.    Sisestage väljale **Nimi** "Kood".
14.    Valige väljalt **Üksuse tüüp** suvand **String**.
15.    Klõpsake käsku **Lisa**.
16.    Klõpsake valikut **Salvesta**.
17.    Sulgege leht.
18.    Klõpsake valikut **Muuda olekut**.
19.    Klõpsake valikut **Vii lõpule**.
20.    Klõpsake valikut **OK**.

## <a name="create-a-format-for-data-import"></a>Vormingu loomine andmete impordiks
1.    Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.
2.    Sisestage väljale **Uus** valik "Vorming põhineb andmemudelil Mudel XML-faili importimiseks".
3.    Sisestage välja **Nimi** „Vorming XML-faili importimiseks”.
4.    Valige väljal **Toetab andmeimporti** valik **Jah**.
5.    Klõpsake **Loo konfiguratsioon**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Vormingu kujundamine XML-vormingus sissetuleva faili sõelumiseks
1.    Klõpsake valikut **Kujundaja**.
2.    Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.
3.    Valige puul suvand **XML\Element**.
4.    Sisestage väljale **Nimi** "Juur".
5.    Klõpsake valikut **OK**.
6.    Klõpsake valikut **Lisa** rippdialoogi avamiseks.
7.    Valige puul suvand **XML\Element**.
8.    Sisestage väljale **Nimi** "Dokument".
9.    Valige väljal **Mitmekordsus** suvand **One many**.
10.    Klõpsake valikut **OK**.
11.    Tehke puul valik **root\document**.
12.    Klõpsake valikut **Lisa** rippdialoogi avamiseks.
13.    Valige puul suvand **XML\Atribuut**.
14.    Sisestage väljale **Nimi** tüübi ID.
15.    Klõpsake valikut **OK**.
16.    Klõpsake valikut **Salvesta**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Vormingu vastenduse kujundamine sõelutud teabe andmemudelile salvestamiseks
1. Klõpsake valikut **Vormingu vastendamine mudeliga**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljal **Määratlused**.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage väljale **Nimi** "Vastendamine".
6. Klõpsake valikut **Salvesta**.
7. Klõpsake valikut **Kujundaja**.
8. Laiendage puul valikut **format**.
9. Laiendage puul valikut **formatoot: XML Element(root)**.
10.    Valige puul **formatoot: XML Element(root)\document: XML Element 1..* (dokument)**.
11.    Klõpsake valikult **Seo**.
12.    Laiendage puul valikut **formatoot: XML Element(root)\document: XML Element 1..* (dokument)**.
13.    Valige puul **formatoot: XML Element(root)\document: XML Element 1..* (dokument)\id**.
14.    Laiendage puul valikut **List = format.root.document**.
15.    Valige puul **List = format.root.document\Code**.
16.    Klõpsake valikult **Seo**.
17.    Klõpsake valikut **Salvesta**.
18.    Sulgege leht.
 
## <a name="run-format-mapping"></a>Vormingu vastendamine käivitamine
1. Klõpsake nuppu **Käivita**.
2. Klõpsake nuppu **Sirvi** ja valige suvand **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klõpsake valikut **OK**.

> [!NOTE]
> Valitud faili ei ole imporditud, kuna vormingu kujundus eeldab atribuudi „ID” olemasolu „dokumendi” elemendi jaoks, kuid imporditud fail ei sisalda sellist atribuuti.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Vormingu struktuuri muutmine, et käsitseda XML-atribuuti valikulisena
1. Sulgege leht.
2. Laiendage puul valikut **root\document**.
3. Tehke puul valik **root\document\id**.
4. Valige suvand **Jah** väljas **Tühjenda puuduva atribuudi string**.
5. Klõpsake valikut **Salvesta**.
 
## <a name="run-format-mapping-to-test-changes"></a>Muudatuste katsetamiseks vormingu vastenduse käivitamine
1. Klõpsake valikut **Vormingu vastendamine mudeliga**.
2. Klõpsake nuppu **Käivita**.
3. Klõpsake nuppu **Sirvi** ja valige fail **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klõpsake valikut **OK**.
5. Vaadake genereeritud fail üle. 

> [!NOTE]
> Sama fail on imporditud, kuna vormingu kujundus võtab nüüd dokumendi elemendi ID atribuuti arvesse valikulisena.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]