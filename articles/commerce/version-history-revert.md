---
title: Versiooni ajaloo kuvamine lehtede ja killute tagasipööramiseks
description: See artikkel kirjeldab, kuidas vaadata lehekülje või killu versiooni ajalugu ja taastada saidilooja vanema Microsoft Dynamics 365 Commerce versiooni.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183335"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Versiooni ajaloo kuvamine lehtede ja killute tagasipööramiseks

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel kirjeldab, kuidas vaadata lehekülje või killu versiooni ajalugu ja taastada saidilooja vanema Microsoft Dynamics 365 Commerce versiooni.

Commerce'i saidi koostaja võimaldab teil vaadata lehekülje või killu versiooni ajalugu ja vajadusel taastada dokumendi konkreetse varasema versiooni. Kui dokument on avatud, **saate** käsuribal valida käsuribal kuva ajaloo, et avada versiooniajaloo dialoogiboks, **kus vahekaardil Versioon** loetletakse **kõigi** versioonide ajalugu ja salvestatakse lehekülje või killu tegevused. Seejärel saate valida loendist dokumendi eelmise versiooni, selle eelvaates kuvada ja taastada selle praeguse versioonina. Dialoogiboksi **vahekaardil** Tegevus on loetletud dokumendi täielik tegevuste ajalugu, k.a kõik sündmuste salvestamine, avaldamine ja avaldamata.

> [!NOTE]
> Dokumendi uus versioon luuakse iga kord, kui saidi autor teeb muudatusi ja valib **siis dokumendi jaoks redigeerimise** lõpetatud. 

Lehe või killu versiooni ajaloo vaatamiseks ja eelmise versiooni tagasipöördumiseks järgige neid samme.

1. Saidikonstruktoris avage leht või tükk, mille versiooniajalugu soovite vaadata.
1. Käsuribal valige näita **ajalugu**.

    ![Ajaloo nupu kuvamine.](./media/version-history-1.png)

1. **Dialoogiakna Versiooniajalugu** vahekaardil **Versioon** valige dokumendi eelmine versioon. Parempoolsel atribuutide paanil kuvatakse valitud versiooni pisipildi eelvaade ja teave selle muutmise kohta ja millal.

    ![Versiooniajaloo loendi vaade.](./media/version-history-2.png)

1. Dokumendi valitud versiooni täielikult renderdatud eelvaate kuvamiseks valige suvand **Eelvaade**. Eelvaate sulgemiseks ja versiooniajaloo dialoogiboksi **naasmiseks** valige väljumise **eelvaade**.
1. Dokumendi varasema versiooni taastamiseks valige see vahekaardi Versioon **loendist** ja seejärel valige käsk **Taasta**. Kuvatakse **versiooni \<version number\>** taastamise teateaken ja teil palutakse kinnitada taastamistegevus. 

    ![Taasta nupp ja kinnitusteadete kast.](./media/version-history-3.png)

1. Taastamistegevustega jätkamiseks valige käsk **Taasta**. Saidikonstruktorit värskendatakse ja kuvatakse lehe taastatud versioon või tükk.
1. Taastatud versiooni avaldamiseks valige suvand **Lõpeta redigeerimine ja** valige käsk **Avalda**.
