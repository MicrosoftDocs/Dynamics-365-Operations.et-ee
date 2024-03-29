---
title: Akordionmoodul
description: See artikkel käsitleb igioonmooduliid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: ec895476770f297825d6c88d0b0a5fef43a5c6ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279152"
---
# <a name="accordion-module"></a>Akordionmoodul

[!include [banner](includes/banner.md)]

See artikkel käsitleb igioonmooduliid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce

Akordionmoodulid on konteinerilaadsed moodulid, mis pakuvad leheküljel teabe või moodulite korrastamiseks võimalust, mis sarnaneb ahendatava sahtliga. Akordionmoodulit saab kasutada igal leheküljel.

Igasse akordionmoodulisse saab lisada ühe või enama akordioniüksuse mooduli. Iga akordioniüksuse moodul tähistab ahendatavat sahtlit. Igasse akordioniüksuse moodulisse saab lisada ühe või enama mooduli. Akordioniüksuse moodulisse saab lisada igat tüüpi mooduleid.

Järgmisel pildil on näide akordionmoodulist, mida kasutatakse kaupluse korduma kippuvate küsimuste (KKK) lehe teabe korrastamiseks.

![Akordionmooduli näide.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Akordionmooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri | Tekst | See atribuut määratleb akordionmooduli jaoks valikulise teksti pealkirja. |
| Laienda kõik | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, on laiendamis-/ahendamisfunktsioon sisse lülitatud, nii et kõiki akordionmoodulis olevaid üksuseid saab laiendada ja ahendada. |
| Suhtlemisstiil | **Sõltumatu** või **Laienda ainult üht üksust** | See atribuut määratleb akordioniüksuste jaoks suhtlemisstiili. Kui väärtuseks on seatud **Sõltumatu**, saab iga akordioniüksust laiendada või ahendada sõltumatult. Kui väärtuseks on seatud **Laienda ainult üht üksust**, saab korraga laiendada ainult üht üksust. Üksuste laiendamisel ahendatakse enne laiendatud üksused. |

## <a name="accordion-item-module-properties"></a>Akordioniüksuse mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pealkiri | Tekst | See atribuut määratleb akordioniüksuse mooduli jaoks pealkirja teksti. Pealkirja piirkonnale klõpsates saavad kasutajad jaotist laiendada või ahendada. |
| Laienda vaikimisi | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, laiendatakse akordioniüksus vaikimisi siis, kui leht on laaditud. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>KKK lehele akordionmooduli lisamine

KKK lehele akordionmooduli lisamiseks ja selle atribuutide seadistamiseks saidiehitajas toimige järgmiselt.

1. Avage **Lehed** ja kasutage Fabrikami turundusmalli (või mis tahes piiranguteta malli) uue lehe loomiseks, mille nimi on **Kaupluse KKK**.
1. **Valige vaikelehe** põhipesas **kolmikpunkt** (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige moodulis **Tiion** ja seejärel valige **OK**.
1. Valige akordionmooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.
1. Sisestage dialoogiboksis **Pealkiri** jaotises **Pealkirja tekst** tekst **Korduma kippuvad küsimused**. Seejärel valige **OK**.
1. Valige akordionmooduli atribuutide paanil märkeruut **Kuva laiendamine** ja seejärel valige väljal **Suhtlemisstiil** suvand **Sõltumatu**.
1. Valikus **Lisa pesas** valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige kauba **lisakauba moodul** Ja seejärel valige **OK**.
1. Sisestage akordioniüksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Kuidas toimib tagastamine?**).
1. Ionion **kauba pesas** valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige tekstibloki **moodul** ja seejärel valige **OK**.
1. Sisestage tekstiploki mooduli atribuutide paanil tekstilõik (nt **Tagastamiseks tuleb võtta ühendust kõnekeskusega. Tagastamiseks helistage numbrile 1-800-FABRIKAM. Toodetel on 30-päevane tagastuspoliitika. Tagastamist tuleb alustada selle ajavahemiku jooksul.**).
1. Lisage pesas **Akordion** veel mõni akordioniüksuse moodul. Lisage igas akordioniüksuse moodulis sisuga tekstiploki moodul.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Lehel kuvatakse akordionmoodul, milles on teie lisatud sisu.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Vahekaardimoodul](add-tab.md)

[Tekstiploki moodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
