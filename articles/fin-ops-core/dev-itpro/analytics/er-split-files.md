---
title: Loodud XML-failide tükeldamine failimahu ja sisukoguse alusel
description: See teema annab teavet loodud failide tükeldamise kohta failimahu ja sisuüksuste koguse alusel.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3735bcb06eff966fc364a891b38d44e34e845e35f59314822d13eba40d51d5f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769968"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Loodud XML-failide tükeldamine failimahu ja sisukoguse alusel

[!include[banner](../includes/banner.md)]

Saate kujundada elektroonilise aruandluse vormingud looma väljaminevaid dokumente XML-vormingus. Mõnikord saab neid dokumente aktseptida ainult siis, kui need vastavad teatud kriteeriumidele, nagu maksimaalne failimaht või mõningate XML-sõlmede maksimaalne arv. Saate kujundada elektroonilise aruandluse vormingud looma elektroonilisi dokumente, mis täidavad nende dokumentide saajate määratud nõudeid.

- Vorminguelemendi FILE puhul saate määratleda failimahu piirangu elektroonilise aruandluse avaldisena. Kui elektroonilise aruandluse aruande loomisel ületatakse määratud piirang, lõpetab elektrooniline aruandlus praeguse faili loomise ja liigub edasi järgmise faili loomise juurde.
- Vormingu XML ELEMENT puhul saate määratleda elementide arvu piirangu elektroonilise aruandluse avaldisena. Kui elektroonilise aruandluse aruande käitamisel ületab XML-sõlmede arv loodud failis selle määratud piirangu, lõpetab elektrooniline aruandlus praeguse faili loomise ja liigub edasi järgmise faili loomise juurde.
- Mis tahes vorminguelemendi XML SEQUENCE puhul saate määratleda tütarelementide arvu piirangu elektroonilise aruandluse avaldisena. Kui elektroonilise aruandluse aruande käitamisel ületab vorminguelemendi pesastatud XML-sõlmede arv loodud failis selle määratud piirangu, lõpetab elektrooniline aruandlus praeguse faili loomise ja liigub edasi järgmise faili loomise juurde.
- Saate märkida mis tahes vorminguelemendi XML ELEMENT mittemurtavaks. Sel moel saate hoida XML-sõlmede pesastatud üksused, mis on loodud vorminguelemendi all, ühes loodud failis.

Peale vorminguelementide XML ELEMENT ja XML SEQUENCE kasutamise XML-sõlmede lisamiseks loodud faili saate kasutada vorminguelementi RAW XML. Vorminguelemendi RAW XML abil lisatud sõlmi ei võeta siiski arvesse sõlmede arvu arvutamisel, et hinnata elementide arvu piiranguid.

Kui olete konfigureerinud failisihtkohad vorminguelemendile FILE, mis on konfigureeritud loodud väljundi tükeldamiseks alati, kui konkreetne piirang ületatakse, saadetakse iga loodud väljundi tükk konfigureeritud faili sihtkohta eraldi failina. Väljundi tükeldamisel loodud failidele kordumatu nime andmiseks peate konfigureerima vorminguelemendile FILE elektroonilise aruandluse avaldise. Kui kaasate elektroonilise aruandluse andmeallika tüübiga NUMBER SEQUENCE, suureneb numbriseeria iga tükeldatud väljundi tüki puhul.

Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhist **Elektrooniline aruandlus: XML-failide tükeldamine failimahu või sisuüksuste koguse põhjal**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** ja mille saab alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684). See tegevusejuhis viib teid läbi elektroonilise aruandluse vormingu konfigureerimise protsessi loodud failide tükeldamiseks failimahu ja sisuüksuste koguse piirangute põhjal. Tegevusejuhise lõpuleviimiseks peate alla laadima järgmised failid.

- [Elektroonilise aruandluse mudeli konfiguratsioon – XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [Elektroonilise aruandluse vormingu konfiguratsioon – XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Lisaressursid
[Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)

[Valemikoostaja elektroonilises aruandluses (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
