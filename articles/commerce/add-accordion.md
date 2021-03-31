---
title: Akordionmoodul
description: See teema hõlmab akordionmooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a08441f5dffa9c2c65b304d0265dd107a838a685
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206603"
---
# <a name="accordion-module"></a>Akordionmoodul

[!include [banner](includes/banner.md)]

See teema hõlmab akordionmooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Akordionmoodulid on konteinerilaadsed moodulid, mis pakuvad leheküljel teabe või moodulite korrastamiseks võimalust, mis sarnaneb ahendatava sahtliga. Akordionmoodulit saab kasutada igal leheküljel.

Igasse akordionmoodulisse saab lisada ühe või enama akordioniüksuse mooduli. Iga akordioniüksuse moodul tähistab ahendatavat sahtlit. Igasse akordioniüksuse moodulisse saab lisada ühe või enama mooduli. Akordioniüksuse moodulisse saab lisada igat tüüpi mooduleid.

Järgmisel pildil on näide akordionmoodulist, mida kasutatakse kaupluse korduma kippuvate küsimuste (KKK) lehe teabe korrastamiseks.

![Akordionmooduli näide](./media/ecommerce-accordion.PNG)

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
1. Valige **Vaikelehe** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Akordion** ja klõpsake seejärel **OK**.
1. Valige akordionmooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.
1. Sisestage dialoogiboksis **Pealkiri** jaotises **Pealkirja tekst** tekst **Korduma kippuvad küsimused**. Seejärel valige **OK**.
1. Valige akordionmooduli atribuutide paanil märkeruut **Kuva laiendamine** ja seejärel valige väljal **Suhtlemisstiil** suvand **Sõltumatu**.
1. Valige pesas **Akordion** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Akordioniüksus** ja klõpsake seejärel **OK**.
1. Sisestage akordioniüksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Kuidas toimib tagastamine?**).
1. Valige pesas **Akordioniüksus** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.
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