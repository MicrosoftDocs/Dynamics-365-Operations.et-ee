---
title: Piltide üleslaadimine
description: See artikkel kirjeldab, kuidas saidikonstruktori pilte Microsoft Dynamics 365 Commerce üles laadida.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283375"
---
# <a name="upload-images"></a>Piltide üleslaadimine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas saidikonstruktori pilte Microsoft Dynamics 365 Commerce üles laadida.

Kaubanduse saidiehitaja meediumiteek võimaldab teil üles laadida pilte, kas üksikult või kaustades hulgakaupa. Te peaksite alati üles laadima kõrgeima lahutuse ja kvaliteediga pildiversiooni, sest pildi suuruse muutmise komponent optimeerib pildi automaatselt erinevate vaateportide ja nende katkestuspunktide järgi.

### <a name="image-information-specified-during-upload"></a>Üleslaadimise ajal määratav pilditeave

Pildi üleslaadimisel saab määrata järgmise teabe.

- **Pealkiri, Alt tekst, Kirjeldus, Märksõnad**: pildi või piltide metaandmed. Pealkiri ja alt-tekst on nõutavad väärtused.
- **Vali kategooria**:
    - **Puudub**: kasutatakse e-Kaubanduse jutustuse pildi või piltide jaoks.
    - **Toode, Kategooria, Klient, Töötaja, Kataloog**: kasutatakse Dynamics 365 Commerce omnikanali pildi või piltide jaoks.
- **Avalda varad pärast üleslaadimist**: kui see ruut on märgitud, avaldatakse pilt või pildid kohe pärast üleslaadimist.

> [!NOTE]
> - Pildivarad, mille kategooria on määratud, sildistatakse automaatselt selle kategooriaga märksõnana, mis aitab otsida kindla kategooria varasid.
> - Toote üksikasjade leheküljed loovad dünaamiliselt **asetekst**, kasutades toote nime, **nii** et tootepildi asetekst muutmine ei mõjuta renderdatud pilti.

### <a name="naming-conventions-for-omni-channel-images"></a>Omnikanali piltide nimetustavad 

Kui olete konfigureerinud Meediumiteegi omnikanali pildi taustaks, saate kasutada kujutise kategooriaid, et näidata, millisesse kategooriasse üleslaaditud pilt kuulub. On olemas ka nimetava, mida tuleb järgida tagamaks, et pildid võetakse õigesti vastu teiste kanalite kaudu, nt kassas (POS).

Vaikimisi nimetava sõltub kategooriast:
- Kataloogipildid peavad olema nimega "**/Catalogs/\{LanguageId\}/\{CatalogName\}. jpg**"
- Kategooriapildid tuleb nimetada "**/Categories/\{CategoryName\}. png**"
- Kliendipildid peavad olema nimega "**/Customers/\{CustomerNumber\}. jpg**"
- Töötajapildid peavad olema nimega "**/Workers/\{WorkerNumber\}. jpg**"
- Tootepildid tuleb nimetada "**/Toode/\{TooteNumber\}\_000_001. png**"
    - 001 on pildijärjestus ja see võib olla 001, 002, 003, 004 või 005
- Tootevariandi pildid tuleb nimetada "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"
    - Näiteks: 93039 \^ &nbsp;\^ 2 \^ Black \^\_000_001.png
- Tootevariandi kujutised, millel on konfiguratsioonimõõtmed, peaksid kandma nime "**/Tooted/\{TooteNumber\} \^ \{Konfiguratsioon\}\_000_001.png**"
    - Näiteks: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Tootevariandi piltide puhul, kui dimensiooni väärtus on tühi, peab failinimes mõõtude vahel olema kaks tühikut.

Ülaltoodud näited kasutavad vaikekonfiguratsiooni. Eraldaja märk ja dimensioonid on konfigureeritavad ning täpne nime andmine võib juurutuste vahel erineda. Üks täpse nimetamistava tuvastamise viis on kasutada brauseri arendajakonsooli tootevariandi pilditaotluste üle vaatamiseks, muutes tootedimensioone kaupluse toote üksikasjade lehel (PDP).

## <a name="upload-an-image"></a>Laadi pilt üles

Pildi üleslaadimiseks saidiehitajasse toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.
1. Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.
1. Fail Exploreri aknas navigeerige ja valige üleslaadimiseks üks või mitu pildifaili ja seejärel valige **Ava**.
1. Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.
1. Sisestage valikuline kirjeldus ja märksõnad ning valige soovi korral kategooria. 
1. Piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.
1. Valige nupp **OK**.

## <a name="upload-a-folder-of-images"></a>Pildikausta üleslaadimine

Pildikausta üleslaadimiseks saidiehitajasse toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.
1. Valige tegumiriba käsk **Laadi üles \> Laadi üles kaust**.
1. Fail Exploreri aknas navigeerige ja valige üleslaadimiseks kaust ja seejärel valige **Ava**.
1. Dialoogiaknas **Meediumiüksuse üleslaadimine** sisestage valikulised märksõnad ja valige soovi korral kategooria. 
1. Kausta piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.
1. Valige nupp **OK**.

## <a name="additional-resources"></a>Lisaressursid

[Digitaalse varahalduse ülevaade](dam-overview.md)

[Video üleslaadimine](dam-upload-video.md)

[Failide üleslaadimine](dam-upload-files.md)

[Piltide kärpimine](dam-crop-images.md)

[Pildi keskpunktide kohandamine](dam-custom-focal-point.md)

[Staatiliste failide üleslaadimine ja kasutamine](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
