---
title: Vahekaardimoodul
description: See artikkel katab vahekaardi moodulid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 91c79ca1b70a776352ef99d854397ada34c548e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276969"
---
# <a name="tab-module"></a>Vahekaardimoodul

[!include [banner](includes/banner.md)]

See artikkel katab vahekaardi moodulid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce.

Vahekaardi moodulid on konteinerilaadsed moodulid, mida kasutatakse vahekaartide abil saidi lehel teabe korrastamiseks. Neid saab kasutada igal lehel, kus teave tuleb esitada vahekaartidel.

Igas vahekaardi moodulis saab lisada ühe või enama vahekaardi mooduli. Iga vahekaardi moodul tähistab üht vahekaarti. Igas vahekaardi moodulis saab lisada ühe või enama mooduli. Vahekaardi moodulisse saab lisada igat tüüpi mooduleid.

Järgmisel pildil on näide vahekaardi moodulist saidi lehel. Näites on valitud vahekaart **Lähetamine**.

![Vahekaardi mooduli näide.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Vahekaardi mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Päis | Tekst | See atribuut määratleb vahekaardi mooduli jaoks valikulise teksti pealkirja. |
| Aktiivse vahekaardi indeks | Number | See atribuut määratleb vahekaardi, mis peaks lehe laadimisel olema vaikimisi aktiivne. Kui väärtust ei esitada, siis on vaikimisi aktiivne esimene vahekaart. |

## <a name="tab-item-module-properties"></a>Vahekaardi üksuse mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri | Tekst | See atribuut määratleb vahekaardi üksuse mooduli jaoks pealkirja teksti. |

## <a name="add-a-tab-module-to-a-page"></a>Lehele vahekaardi mooduli lisamine

Lehele vahekaardi mooduli lisamiseks ja atribuutide seadistamiseks toimige järgmiselt.

1. Kasutage Fabrikami turundusmalli (või mis tahes piiranguteta malli) uue lehe loomiseks, mille nimi on **Kaupluse poliitikate leht**.
1. **Valige vaikelehe** põhipesas **kolmikpunkt** (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige vahekaart **ja** seejärel valige **OK**.
1. Valige vahekaardi mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.
1. Sisestage dialoogiboksis **Päis** jaotisesse **Päise tekst** päise tekst (nt **Poliitikad**). Seejärel valige **OK**.
1. **Vahekaardil pesal** valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige vahekaart **üksuse moodul** ja seejärel valige **OK**.
1. Sisestage vahekaardi üksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Tarne**).
1. Vahekaardi kauba **pesal** valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige tekstibloki **moodul** ja seejärel valige **OK**.
1. Lisage tekstiploki mooduli atribuutide paani väljale **Rikastekst** tekstilõik.
1. Lisage pesas **Vahekaart** veel mõned pealkirjaga vahekaardi üksuse moodulid. Lisage igas vahekaardi üksuse moodulis sisuga tekstiploki moodul.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Lehel kuvatakse vahekaardi moodul, mis sisaldab teie lisatud sisuga vahekaardi üksuse mooduleid.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Akordionmoodul](add-accordion.md)

[Tekstiploki moodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
