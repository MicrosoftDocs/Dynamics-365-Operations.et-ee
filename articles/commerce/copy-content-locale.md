---
title: Sisu kopeerimine teise lokaadi
description: See artikkel kirjeldab, kuidas kopeerida olemasolevat sisu saidi teise lokaadile saidi koostajas Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: bcfa3c7cb2ea8018422803d85df6b6761b8d1145
ms.sourcegitcommit: d719d0a549aecac231fad0abb42250eab9dd0ded
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2022
ms.locfileid: "9126466"
---
# <a name="copy-content-to-another-locale"></a>Sisu kopeerimine teise lokaadi

[!include[banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas kopeerida olemasolevat sisu saidi teise lokaadile saidi koostajas Microsoft Dynamics 365 Commerce.

Commerce'i saidi koostajas sisu loomisel on see alati seostatud lokaadi identifikaatoriga, nt "en-us". Saate kopeerida üksikuid lehekülgi ja varasid sama e-äri saidi eri lokaadile, lülitudes sisuüksuse redigeerimise ajal lokaadile ja luues seejärel kaubale uue variandi. Mõnel juhul, nt kui käivitate oma kaupluses täiesti uue lokaadi, on mõtet kopeerida kõik olemasoleva lokaadi sisuüksused uude lokaadi. Kui uuel lokaadil on olemasoleva lokaadiga sama põhikeel, saate kasutada lähte lokaadina olemasolevat lokaadi koopiatoimingu jaoks. (Näiteks nii "en-us" kui ka "en-au" lokaliseerimised kasutavad nii inglise keelt.) Sel viisil aitab vähendada panust, mis on vajalik sisu lokaliseerimiseks uues lokaadis.

Järgmised protseduurid selgitavad, kuidas lisada olemasolevale kanalile uus lokaadi, kopeerida kõik sisuüksused olemasolevast lokaadist uude lokaadi ja jälgida lokaadi koopiatoimingu olekut.

## <a name="add-a-new-locale"></a>Uue lokaadi lisamine

Commerce'i saidi koostajasse uue lokaadi lisamiseks järgige neid samme.

1. Minge saidikonstruktori saidile.
1. Valige vasakul navigeerimispaanil saidisätted **ja** seejärel **kanalid**.
1. Kanali **all** valige kanal, et lisada uus lokaadile.
1. Paremal kuvatavas kanali dialoogiboksis valige lisa **lokaadiks**.
1. **Valige dialoogiboksi Lokaadi** lisamine toetamisväljal **lokaadiks**.
1. Veenduge, et **domeeni** väärtus on õige.
1. Sisestage **väljale** Tee kordumatu URL-tee (**nt en-us** või **english-us**).
1. Valige nupp **OK**.
1. Sulgege kanali dialoogiboks.
1. Kinnitage **jaotises** Kanal, et uus lokaadiks on loetletud õige kanali kõrval.
1. Valige käsk **Salvesta ja avalda**.

> [!NOTE]
> Enne uue lokaadi konfigureerimist saidikonstruktoris tuleb see lisada commerce headquartersi seostatud võrgupoe kanalile.

## <a name="copy-all-content-items-to-a-new-locale"></a>Kopeeri kõik sisuüksused uude lokaadi

Kõikide sisuüksuste kopeerimiseks commerce'i saidi koostaja uude lokaadi, järgige neid samme.

1. Minge saidikonstruktori saidile.
1. Valige vasakul navigeerimispaanil saidisätted **ja** seejärel **kanalid**.
1. Käsuribal valige käsk Loo lokaadi **koopia**.
1. Paremal lähtesaidi **all kuvatavas** dialoogiboksis Lokaadi koopia loomine veenduge, **et** valitud on õige sait.
1. **Valige lähtekanali** väljal lähtekanal.
1. **Valige sihtkanali** väljal sama lähtekanal.
1. Valige lähte **lokaadil** allika lokaadiks.
1. **Siht lokaadil** valige uus lokaadiks.
1. Valige **kopeerimis lokaadiks**. Teatis kinnitab, et lokaadi koopia toiming on käivitatud.

> [!NOTE]
> Sisu saate kopeerida ka eri kanalite vahel.

## <a name="monitor-the-status-of-the-locale-copy"></a>Lokaadi koopia oleku s monitorimine

Lokaadi koopiatoimingu oleku jälgimiseks järgige neid samme.

1. Minge saidikonstruktori saidile.
1. Valige vasakul navigeerimispaanil saidi **sätted ja** seejärel töö **.**
1. Valige **jaotises Praegused** tööd jälgimist vajav töö. Töö üksikasjad kuvatakse paremal kuvatavas dialoogiboksis.
