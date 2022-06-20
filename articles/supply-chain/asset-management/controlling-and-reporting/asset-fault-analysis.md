---
title: Vara vea analüüs
description: See artikkel selgitab varahalduses vara tõrke analüüsi.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d4503c39a643461c75878c6c7096d824642ad1a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869774"
---
# <a name="asset-fault-analysis"></a>Vara vea analüüs

[!include [banner](../../includes/banner.md)]

 

Varade Halduses saate analüüsida vara vea registreerimisi, et saada ülevaade kindla perioodi jooksul registreeritud vigade koguarvust. Vea registreerimisi saab analüüsida erinevatest vaatenurkadest, näiteks keskendudes varadele, vara tüüpidele, töö asukohtadele, vigade sümptomitele või vigade tüübile.

1. Klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vea analüüs**.

2. Dialoogiaknas **Vara vea analüüsi arvutamine** saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et vara vea read oleksid seotud töö asukohtadega. 

    Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik vara vea read töö asukoha kohta ja seetõttu võib rea tunnid kokku liita töö asukohtadest, mis asuvad madalamal tasemel. 
        
    Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, kus kuvatakse kõik vara vea read kõigil töö asukoha tasemetel, millega need on seotud.

3. Kui soovite otsingut piirata, saate valida kindlad varad, vea kuupäevad, vea põhjused ja vea parandusmeetmed **Lisamiskirjed** kiirkaardi valikus.

4. Arvutuse alustamiseks klõpsake **OK**.

5. Klõpsake vahekaardil **Vara vea analüüs** ühte või mitut nuppu **Grupeerimisalus**, et kuvada detailide tase, mida soovite näha. Aktiveeritud nupud on esile tõstetud. Nuppude aktiveerimiseks või inaktiveerimiseks klõpsake neil.

6. Klõpsake **Värskenda arvutusi**, et näidata oma valikuid ekraanil. 

>[!NOTE]
>Iga kord, kui aktiveerite või desaktiveerite nupu **Grupeerimisalus**, ärge unustage klõpsata nuppu **Värskenda arvutusi**. See on nõutav, kuna suur hulk andmeid töödeldakse, kui arvutate vea tõenäosuse ümber.

## <a name="examples"></a>Näited

Vigade registreerimiste analüüsimiseks on mitu võimalust. Selles jaotises kirjeldatakse viit näidet, kuidas erinevad andmevalikud saavad pakkuda rohkem teavet ja üksikasju, analüüsides vara vea registreerimisi.

### <a name="group-by-symptoms"></a>Grupeerimine sümptomite alusel

Alltoodud ekraanipildil on valitud ainult **Sümptomi** nupp.

- Vea registreerimised on tehtud kolme vea sümptomi korral: "Õhuleke", "Läbipõlenud kaitse" ja "Seade ummistunud".  
- Veerus **Tõenäosuse %** on kõik protsendid kokku 100%. Tõenäosus põhineb kõigi **Sümptom** valikute registreerimisel selles tõrke analüüsis.

![Joonis 1.](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Grupeerimine sümptomite ja ajaperioodi alusel

Alloleval ekraanipildil lisatakse **Aasta** ja **Kuu**, et näidata, kuidas saate vaadata vigade registreerimisi valitud perioodi jooksul.

- Vea sümptomid on nüüd näidatud registreerimistena aastas/kuus.  
- Veerus **Tõenäosuse %**, kui lisate kõik protsendid iga kuu kohta, moodustavad nad kokku 100%. Tõenäosus põhineb **Sümptom** valikute registreerimisel selles vea analüüsis. Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea sümptomist, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea sümptomite registreerimiste arvu.

![Joonis 2.](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Grupeerimine mitme sümptomi ja vara alusel

Varade ja varade tüübi kombinatsiooni kasutatakse kolmes allpool olevas ekraanipildis näidatud arvutuste alusena, mis suurenevad detailsuse tasemel.  

Üldiselt, nupud **Rühmita kuupäeva järgi**, **Rühmita vara järgi**, **Rühmita töö asukoha järgi** toimingupaanide gruppides, nagu ka **Viga** nupp (Vea ID), sisaldavad perioode või vara suhted. Nupud **Sümptom**, **Ala**, **Tüüp**, **Põhjus** ja **Parandusmeede** on veahalduses kasutatavad kategooriad, et analüüsida vara vigade registreerimisi ja probleemseid alasi täpselt ära näidata.  

**Grupeerimine sümptomi, vara ja varatüübi alusel**

Alloleval ekraanipildil lisati **Vara** ja **Vara tüüp**, et anda üksikasjalikumat teavet vigade registreerimiste kohta.

- Vea sümptomid on nüüd jaotatud **Vara** / **Vara tüüp** / **Sümptom** kombinatsioonideks.  
- Kui lisate kõik protsendid veerus **Tõenäosuse %** vastavalt **Vara** / **Vara tüüp** / **Sümptom** kombinatsioonidele, moodustavad nad kõik kokku 100%. Tõenäosus põhineb **Sümptom** registreeringutel selles vea analüüsis. Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea sümptomist, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea sümptomite registreerimiste arvu.

![Joonis 3.](media/08-controlling-and-reporting.png)

**Grupeerimine kahe sümptomi, vara ja varatüübi alusel**

Alloleval ekraanipildil lisati **Ala** suvand **Sümptom**, **Vara**, ja **Vara tüüp** suvanditele, et anda üksikasjalikumat teavet vigade registreerimiste kohta.

- Veerus **Tõenäosuse %**, kui lisate varale kõik kombinatsioonide **Vara** / **Vara tüüp** / **Sümptom** protsendid, moodustavad nad kõik kokku 100%. Tõenäosus põhineb **Sümptom** ja **Ala** kombinatsioonis siin veaanalüüsis. Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea alast, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea ala registreerimiste arvu.  

![Joonis 4.](media/09-controlling-and-reporting.png)

**Grupeerimine kolme sümptomi, vara ja varatüübi alusel**

Alltoodud ekraanipildil lisati **Tüüp** ja on näidatud kõige üksikasjalikum arvutus selles näites.
 
- Veerus **Tõenäosuse %**, kui lisate varale kõik kombinatsioonide **Vara** / **Vara tüüp** / **Sümptom** protsendid, moodustavad nad kõik kokku 100%. Tõenäosus põhineb **Sümptom**, **Ala** ja **Tüüp** kombinatsioonis siin veaanalüüsis. Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea tüübist, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea tüübi registreerimiste arvu.

![Joonis 5.](media/10-controlling-and-reporting.png)


>[!NOTE]
>Töökäskudele ja hooldusnõuetele loodud kõigi vigade registreerimiste ülevaate jaoks klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vead**. Lehel **Vara vead** valige vara vea registreerimine ja laiendage **Seotud teabe** paani, et näha teavet seotud töökäsu või hooldusnõude kohta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]