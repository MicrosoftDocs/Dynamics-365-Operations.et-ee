---
title: Failide importimine XML-vormingus koos valikuliste atribuutidega
description: Selles teemas kirjeldatakse ER-vormingute kujundamist, mis määravad XML-atribuute sissetulevate elektrooniliste dokumentide sõelumiseks XML-vormingus.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849991"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Failide importimine XML-vormingus koos valikuliste atribuutidega

Saate kujundada elektroonilise aruandluse (ER) vormingud sõeluma sissetulevaid dokumente XML-vormingus. XML-elementide teatud atribuute saab loodud ER-vormingus määratleda valikuliselt. See võimaldab teil selliste XML-atribuutidega ja ilma nendeta sissetulevaid faile õigesti käsistseda. Seejärel saate neist failidest pärit sisu kasutada rakenduse andmete värskendamiseks.

Selle funktsiooni kohta lisateabe saamiseks läbige etapid teemas [RCS failide importimine XML-vormingus valikuliste atribuutidega](tasks/import-files-xml-format-optional-attributes.md), mis on osa 7.5.4.3 omandada/arendada IT-teenuse/-lahenduse komponentide hankimise/arendamise (10677) äriprotsessist. Saate selle tegevuse juhise ja seotud näitefailid alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684).


| Sisu kirjeldus       | Fail                                                         |
|---------------------------|--------------------------------------------------------------|
| Näidisfail XML-vormingus | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Ülesande juhis                | RCS failide importimine XML-vormingus koos valikuliste atribuutidega.axtr |


Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kujundada elektroonilise aruandluse (ER) vormingu konfiguratsiooni failide importimiseks XML-vormingus koos valikuliste atribuutidega. Etappide lõpuleviimiseks, peate esmalt läbima protseduuri [Konfiguratsiooni pakkuja loomine ning aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) etapid. Enne alustamist laadige alla ja salvestage lokaalselt fail IncomingDocumentToLearnHowToHandleOptionalAttributes.xml Microsofti allalaadimiskeskusest (https://go.microsoft.com/fwlink/?linkid=874684).

1. Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**.
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsiooni pakkujat, peate esmalt läbima etapid teemas [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Klõpsake valikut **Aruandluse konfiguratsioonid**.

## <a name="create-a-new-data-model-configuration"></a>Uue andmemudeli konfiguratsiooni loomine
1. Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.
2. Sisestage väljale **Nimi** „Mudel XML-faili importimiseks”.
3. Klõpsake **Loo konfiguratsioon**.
4. Klõpsake valikut **Kujundaja**.
5. Rippdialoogi avamiseks klõpsake valikut **Uus**.
6. Sisestage väljale **Nimi** "Juur".
7. Klõpsake käsku **Lisa**.
8. Rippdialoogi avamiseks klõpsake valikut **Uus**.
9. Sisestage väljale **Nimi** "Loend".
10. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
11. Klõpsake käsku **Lisa**.
12. Rippdialoogi avamiseks klõpsake valikut **Uus**.
13. Sisestage väljale **Nimi** "Kood".
14. Valige väljalt **Üksuse tüüp** suvand **String**.
15. Klõpsake käsku **Lisa**.
16. Klõpsake valikut **Salvesta**.
17. Sulgege leht.
18. Klõpsake valikut **Muuda olekut**.
19. Klõpsake valikut **Vii lõpule**.
20. Klõpsake valikut **OK**.

## <a name="create-a-format-for-data-import"></a>Vormingu loomine andmete impordiks
1. Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.
2. Sisestage väljale **Uus** valik "Vorming põhineb andmemudelil Mudel XML-faili importimiseks".
3. Sisestage väljale **Nimi** „Vorming XML-faili importimiseks”. 
4. Valige väljal **Toetab andmeimporti** valik **Jah**.
5. Klõpsake **Loo konfiguratsioon**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Vormingu kujundamine XML-vormingus sissetuleva faili sõelumiseks
1. Klõpsake valikut **Kujundaja**.
2. Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.
3. Valige puul suvand **XML\Element**.
4. Sisestage väljale **Nimi** "Juur".
5. Klõpsake valikut **OK**.
6. Klõpsake valikut **Lisa** rippdialoogi avamiseks.
7. Valige puul suvand **XML\Element**.
8. Sisestage väljale **Nimi** "Dokument".
9. Valige väljal **Mitmekordsus** suvand **One many**.
10. Klõpsake valikut **OK**.
11. Tehke puul valik **root\document**.
12. Klõpsake valikut **Lisa** rippdialoogi avamiseks.
13. Valige puul suvand **XML\Atribuut**.
14. Sisestage väljale **Nimi** "ID".
15. Klõpsake valikut **OK**.
16. Klõpsake valikut **Salvesta**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Vormingu vastenduse kujundamine sõelutud teabe andmemudelile salvestamiseks
1.  Klõpsake valikut **Vormingu vastendamine mudeliga**.
2.  Klõpsake valikut **Uus**.
3.  Sisestage või valige väärtus väljal **Määratlused**.
4.  Sisestage väljale **Nimi** "Vastendamine".
5.  Klõpsake valikut **Salvesta**.
6.  Klõpsake valikut **Kujundaja**.
7.  Laiendage puul valikut **format**.
8.  Laiendage puul valikut **formatoot: XML Element(root)**.
9.  Valige puul **formatoot: XML Element(root)\document: XML Element 1..* (dokument)**.
10. Klõpsake valikult **Seo**.
11. Laiendage puul valikut **formatoot: XML Element(root)\document: XML Element 1..* (dokument)**.
12. Valige puul **formatoot: XML Element(root)\document: XML Element 1..* (dokument)\id**.
13. Laiendage puul valikut **List = format.root.document**.
14. Valige puul **List = format.root.document\Code**.
15. Klõpsake valikult **Seo**.
16. Klõpsake valikut **Salvesta**.
17. Sulgege leht.

## <a name="run-format-mapping"></a>Vormingu vastendamise käivitamine
1. Klõpsake nuppu **Käivita**.
2. Klõpsake nuppu **Sirvi** ja valige fail **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klõpsake valikut **OK**.

> [!NOTE]
> Valitud faili ei ole imporditud, kuna vormingu kujundus eeldab atribuudi "ID" olemasolu "dokumendi" elemendi jaoks, kuid imporditud fail ei sisalda sellist atribuuti.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Vormingu struktuuri muutmine, et käsitseda XML-atribuuti valikulisena
1. Sulgege leht.
2. Laiendage puul valikut **root\document**.
3. Tehke puul valik **root\document\id**.
4. Valige väljal **Tühjenda puuduva atribuudi string** suvand **Jah**.
5. Klõpsake valikut **Salvesta**.

## <a name="run-format-mapping-to-test-changes"></a>Muudatuste katsetamiseks vormingu vastenduse käivitamine
1. Klõpsake valikut **Vormingu vastendamine mudeliga**.
2. Klõpsake nuppu **Käivita**.
3. Klõpsake nuppu **Sirvi** ja valige fail **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klõpsake valikut **OK**.
5. Vaadake genereeritud fail üle. Pange tähele, et sama fail on imporditud, kuna vormingu kujundus arvestab nüüd "dokumendi" elemendi "ID" atribuuti valikulisena.
