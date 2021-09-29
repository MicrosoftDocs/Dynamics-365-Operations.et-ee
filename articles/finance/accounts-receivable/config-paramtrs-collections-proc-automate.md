---
title: Märgukirjaprotsessi automatiseerimise parameetrite konfigureerimine
description: Selles teemas kirjeldatakse parameetreid, mis mõjutavad automatiseeritud kogumise protsesse, ja antakse nende seadistamise juhised, et automatiseeritud protsess kajastaks teie ülesandeid ja ootusi.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3055e10375f1b0be936e3ed0344cdf33dc7bc7e9
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487070"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Märgukirjaprotsessi automatiseerimise parameetrite konfigureerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse parameetreid, mis mõjutavad automatiseeritud kogumise protsesse, ja antakse nende seadistamise juhised, et automatiseeritud protsess kajastaks teie ülesandeid ja ootusi. Lisateabe saamiseks märgukirjaprotsesside automatiseerimise kohta vaata [Protsessi automatiseerimise kogud](collections-process-automate.md).

## <a name="general"></a>Üldine
Sisestage number lahtrisse **Klientide protsent partiiülesande kohta**, et määrata pakettülesannete arv automatiseerimisprotsessi kohta. Seadke **Märgukirjade automaatne sisestamine** väärtusele **Jah**, et märgukirja tegevuse tüüp sisestaks kirja automatiseerimise ajal. Seadistage **Automatiseerimise jaoks tegevuste loomine** väärtusele **Jah**, et luua ja sulgeda tegevused, mis pole tegevusetüübid, et vaadata kõiki kontol automatiseeritud samme. Määrake kogumiste ajaloo salvestamise päevade arv **Päevad kogumiste automatiseerimise ajaloo säilitamiseks**. Kui arve jõuab sissenõuete protsessi viimase sammuni, ei kasutata seda tulevaste protsessi automatiseerimise tegevuse tüüpide loomiseks, kui **Pärast viimase protsessi etapi aktiveerimist jäta arve välja** on seatud väärtusele **Jah**. Järgmine vanim arve määratleb järgmise protsessi automatiseerimise sammu, et tagada märgukirjaprotsessi automatiseerimistoimingute jätkamine. 

## <a name="payment-predictions"></a>Makseprognoosid
Alates versioonist 10.0.21, Finance insights all leiduvad kliendimakseprognoosid prognoosivad, kas arve tasutakse õigeaegselt, hilja või väga hilja. Iga kategooriat saate konfigureerida Finance insights all. Kui arvete maksetähtaeg on prognoositud, on oluline käivitada sissenõuete protsess enne arve tähtaja algust. Neid ennustusi saab kasutada sissenõuete tegevuste loomiseks, kui sissenõuete protsessi automatiseerimised käitatakse. Seadke **Makseprognooside lubamine** väärtusele **Jah** , et kasutada kliendi makseprognoose ja luua sissenõuete tegevusi, mis põhinevad tõenäosusel, et arve tasutakse hiljem. 

Lisateabe jaoks kliendi makseprognooside ja Finance insights kohta vaata [Kliendi makseennustused](payment-insights-overview.md).

Kui kliendi makseprognooside mudel töötab, määrab see protsendi prognoosimakstava arve kohta õigeaegselt, hilja või väga hilja. Seda teavet saate kasutada märgukirjategevuste automaatseks käivitamiseks, kasutades sissenõuete protsessi automatiseerimist juhul, kui oodatakse hilinenud makset. Neid protsente saate vaadata **Makseprognoosid kliendi kohta** alt või **Makseennustused kandelehtede kohta** alt jaotises **Kreedit ja sissenõuded > Sissenõuded**. 

Kui keskmise makse ennustus kliendiarve jaoks on väiksem kui võrdlustesti protsent, siis tegevust ei looda. Kui arve ennustus kliendiarve jaoks on suurem või võrdne võrdlustesti protsendiga, siis luuakse üks tegevus kliendi kohta. **Ennustus: Hilinenud** jaoks sisestage **Võrdlustesti protsent**, millal sissenõuete protsessi automatiseerimine peaks looma sissenõuete tegevused. See on nii hilinenud kui ka väga hilinenud koondväärtus. Valige **Äridokumendi mall**, mida kasutada loodud tegevuse jaoks või looge uus. See tuvastab **Tüübi**, **Eesmärgi** ja **Päevad tegevuse sulgemiseni**. Sisestage **Märkused**, mida tegevuse loomisel kasutatakse vaikimisi kirjeldusena. **Ennustus: Väga hilinenud** jaoks sisestage **Võrdlustesti protsent**, millal sissenõuete protsessi automatiseerimine peaks looma sissenõuete tegevused kliendi jaoks kes ennustatavalt maksab arveid väga hilja. Valige **Äridokumendi mall**, mida kasutada loodud tegevuse jaoks. See tuvastab **Tüübi**, **Eesmärgi** ja **Päevad tegevuse sulgemiseni**. Sisestage **Märkused**, mida tegevuse loomisel kasutatakse vaikimisi kirjeldusena. 

### <a name="example"></a>Näide
Kui hilinenud võrdlustesti protsendiks on seatud 60%. Kui kliendi makseprognoosid esitatakse iga arve jaoks, määrab süsteem protsentuaalse ennustuse õigeaegse, hilinenud või väga hilinenud tasumise kohta. Kui ennustus, et arve tasutakse hilinedes, on 59% või vähem, ei looda automaatse sissenõudeprotsessiga arve jaoks sissenõudetegevust. Kui kliendi makse ennustus arve jaoks on suurem kui 60% või sellega võrdne, luuakse sissenõude tegevus sissenõuete protsessi automatiseerimise ajal. 

> [!NOTE]
> Väga hilinenud ennustust hinnatakse enne hilise ennustuse ilmnemist, kuna väga hiljutised arved sisaldavad eeldatavalt hilinenult makstavaid arveid. Sissenõuete protsess loob ainult ühe tegevuse, kui arve langeb nii hilinenud kui väga hilinenud võrdlustesti. Sel juhul kasutab süsteem väga hilinenud tegevust ja äridokumenti, sest väga hilja on kõrgemad prioriteedid. Kõiki teisi juba loodud tegevusi ei looda teist korda.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
