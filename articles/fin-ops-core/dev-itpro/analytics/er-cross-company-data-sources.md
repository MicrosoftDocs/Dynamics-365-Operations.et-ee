---
title: Ettevõtteülesed andmeallikad elektroonilises aruandluses (ER)
description: See artikkel selgitab, kuidas kasutada ettevõteteülesi andmeallikaid elektroonilises aruandluses (ER).
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
ms.openlocfilehash: ec96533dd2da933d5275adadedc9a92a33e47a38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277722"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Ettevõtteülesed andmeallikad elektroonilises aruandluses (ER)

[!include[banner](../includes/banner.md)]

Saate kujundada elektroonilise aruandluse vormingud looma väljaminevaid dokumente erinevates vormingutes. Dokumendi loomisel pöördub elektroonilise aruandluse vorming andmeallikate poole, mis on vastavas elektroonilise aruandluse mudelivastenduses konfigureeritud. Kirje toomiseks rakendusetabelitele juurdepääsu konfigureerimiseks saate kasutada elektroonilisi andmeallikaid tüübiga **Tabelikirjed**. Kui soovitud tabel on ühiskasutatav tabel (st tabel, kuhu andmeid salvestatakse ilma ettevõtte identifikaatorita), tagastab see andmeallikas kõik kirjed. Kui soovitud tabel on ettevõttest sõltuv tabel (st tabel, kuhu andmeid salvestatakse ettevõtte kaupa), tagastab see andmeallikas ainult praeguse ettevõtte (st ettevõtte, mille all elektroonilise aruandluse vormingut käitatakse) kohta salvestatud kirjed.

Iga andmeallika, mille tüüp on mudelivastenduses **Tabelikirjed**, saab nüüd märkida ettevõtteüleseks andmeallikaks. Seega saate kasutada rakendusetabelites ettevõtteülestele andmetele juurdepääsuks andmeallikaid tüübiga **Tabelikirjed**.

Kui te ei märgi andmeallikat ettevõtteüleseks, juhtub järgmine.

- Andmeallikas, mis viitab mis tahes ühiskasutatavale tabelile, v.a CompanyInfo, tagastab kõik kirjed mis on viidatud tabelis olemas. 
- Andmeallikas, mis viitab tabelile CompanyInfo, isegi kui CompanyInfo on ühiskasutatav tabel, tagastab kirjed, mis sisaldab määratletud ulatuse ettevõtte identifikaatorit.
- Iga ettevõttest sõltuva tabeli puhul tagastab andmeallikas viidatud tabeli kirjed, mis sisaldavad määratletud ulatuse ettevõtte identifikaatorit.

Kui süsteemipäringu dialoogiboksis on suvand **Päringu küsimine** sisse lülitatud kõigi ettevõtteülesteks märgitud andmeallikate puhul sisse lülitatud, saate käsitsi valida ühe või mitu ettevõtet, mida vahekaardile **Ettevõtete vahemik** kaasata.

> [!IMPORTANT]
> Nagu teiste filtrite puhul, säilitatakse ettevõttefilter päringute puhul viimati kasutatud väärtusena, kui käitate elektroonilise aruandluse vormingut. Filtrit ei muudeta automaatselt, kui muudate andmeallika ettevõtteülest väärtust. Teise andmeallika puhul teistsuguse ettevõtteülese väärtuse kasutamiseks kustutage vastav kasutajakohane valik.

Iga ettevõtteüleseks märgitud andmeallika puhul saate soovitud kirjed valida, kasutades elektroonilise aruandluse avaldistes funktsioone **FILTER** ja **WHERE**. Välja **dataAreaID** saab kasutada ka ettevõtte identifikaatorina. Praegu on väli **dataAreaID** piiratud funktsiooni **FILTER** kasutamisel järgmist tüüpi tingimustega.

- Toetatakse ainult tingimusi, millel on üks välja **dataAreaID** võrdlus.
- Lubatud on ainult võrdlused, mille avaldised ei sõltu kirjeloendi üksustest.

Seetõttu on kehtiv järgmine avaldis.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Vaikimisi hõlmab ulatus kõiki praeguse rakenduse ettevõtteid. Seda saab siiski piirata. Ettevõtteülestele andmetele juurdepääsu ulatuse piiramiseks ühe elektroonilise aruandluse vormingu puhul määrake vormingule kindel organisatsioonihierarhia. Kui elektroonilise aruandluse vormingu jaoks on hierarhia määratletud, tagastatakse ainult määratud hierarhias olevate juriidiliste isikute kirjed, isegi kui vorming pöördub ettevõtteüleste andmeallikate poole. Kui elektroonilise aruandluse vormingu aoks on määratletud viide hierarhiale, mida pole enam olemas, rakendatakse vaikeulatust ja vorming pöördub ettevõtteüleste andmeallikate poole. Sellisel juhul tagastatakse rakenduse kõigi ettevõtete kirjed.

Pange tähele, et kui ühele elektroonilise aruandluse vormingule määratud organisatsioonihierarhia puhul on suvand **Kasuta mustandit** sisse lülitatud, kasutatakse ettevõtteüleste andmeallikate ulatuse tuvastamiseks selle hierarhia mustandversioonist pärit juriidilisi isikuid. Kui mustandversiooni pole olemas, kasutatakse selleks selle organisatsioonihierarhia viimati avaldatud versioonist pärit juriidilisi isikuid.

Pange tähele, et kui ühele elektroonilise aruandluse vormingule määratud organisatsioonihierarhia puhul on suvand **Kasuta mustandit** välja lülitatud, kasutatakse ettevõtteüleste andmeallikate ulatuse tuvastamiseks selle organisatsioonihierarhia viimati avaldatud versioonist pärit juriidilisi isikuid. Organisatsioonihierarhiate kuupäevalist jõustumist praegu veel elektroonilise aruandluse raamistikus ei toetata.

Hierarhia saab määrata vormingule konkreetsel lehel, millele pääseb juurde elektroonilise aruandluse tööruumist või kasutades menüüvalikuid **Organisatsiooni haldus \> Elektrooniline aruandlus \> Juriidilise isiku filter vormingute jaoks**. Lehele pääsemiseks peab kasutajale olema antud õigus **Juriidilise isiku filtrite haldamine vormingute jaoks** (ERMaintainFormatMappingLegalEntityFilters). Hierarhial põhinevate juriidiliste isikute ulatuse piirang vormingu puhul rakendatakse lisaks piirangule, mida kasutaja saab süsteemipäringu dialoogiboksis käsitsi määrata. Nende piirangute ühisosa kasutatakse vormingu käitamisel.

Lisateabe saamiseks selle funktsioon kohta vaadake tegevusejuhist **Elektrooniline aruandlus: ettevõttest sõltuvate tabelite kirjetele juurdepääs ettevõtteüleses režiimis**, mis on osa äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) ja mille saab alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684). Ülesandejuhis viib teid läbi elektroonilise aruandluse mudelivastenduse ja elektroonilise aruandluse vormingu konfigureerimise protsessi ettevõtteüleses režiimis rakenduse tabelitele juurdepääsuks.

Tegevusejuhise lõpuleviimiseks laadige alla järgmised failid.

- [Elektroonilise aruandluse mudeli konfiguratsioon – CrossCompanyDataAccessModel.xml](https://download.microsoft.com/download/4/2/5/4258f891-7054-4821-aedd-3721ba25fdd5/CrossCompanyDataAccessModel.xml)
- [Elektroonilise aruandluse vormingu konfiguratsioon – CrossCompanyDataAccessFormat.xml](https://download.microsoft.com/download/3/2/1/321deb75-3ba9-4323-99bf-207a52c60b5c/CrossCompanyDataAccessFormat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
