---
title: Graafiku töökoormuse võimsus
description: Selles teemas kirjeldatakse, kuidas seadistada ja planeerida töökoormuse võimsust lao töötajatele või kogu laole.
author: MarkusFogelberg
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 004abe379004d0dc8d0bff526872312bfa7a994b0f7422d1c415927bbecc90ec
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780478"
---
# <a name="schedule-workload-capacity"></a>Töökoormuse võimsuse plaanimine

[!include[banner](../includes/banner.md)]

Saate plaanida töökoormuse võimsuse ladudele ning kavandada praegused ja tulevased töökoormused üksikutes ladudes olevatele töötajatele. Saate kavandada kogu lao töökoormuse või saate sissetulevate ja väljaminevate töökoormuste jaoks töökoormuse eraldi kavandada.

Valitud ladudele töökoormuse väljundi kavandamiseks peavad koondplaneerimise andmed nende ladude kohta saadaval olema. Lisateavet vt teemast [Koondplaanide ülevaade](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Lao töökoormuste plaanimine ja vaatamine

Lao töökoormuse võimsuse plaanimiseks saate luua töökoormuse seadistuse ühele või mitmele laole ja seostada seejärel töökoormuse seadistuse koondplaaniga. Töökoormuse võimsuse seadistamises saate määratleda piirangud sissetulevate ja väljaminevate kannete kaalu või mahu jaoks. Saate luua ka rohkem kui ühe seadistuse igale laole ja seejärel seostada seadistuse üksikute koondplaanidega. Näiteks võite seda lähenemist kasutada hooajaliste muudatuste kohandamiseks tööjõus.

Kui lao töötajad töötavad nii sissetulevate kui ka väljaminevate töökoormuste kannetega, saate konfigureerida lao võimsuse seadistuse, nii et töökoormus kavandatakse kombineeritud vaates.

Ladude töökoormuste plaanimiseks ja vaatamiseks peate läbima järgmised toimingud.

1. Looge töökoormuse võimsuse seadistus ja määratlege töökoormuse võimsuse piirangud ühele või mitmele laole.
2. Seostage töökoormuse võimsuse seadistus koondplaaniga, et luua töökoormuse kavandid ja määrata, kui kaua need kavandid kehtivad.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Töökoormuse võimsuse seadistuse loomine laole

1. Valige **Varude haldamine** \> **Seadistamine** \> **Lao jälgimine** \> **Töökoormuse võimsus**.
2. Valige toimingupaanilt suvand **Uus**, et luua töökoormuse võimsuse seadistus.
3. Kiirkaardil **Laod** valige suvand **Uus** ja sisestage seejärel väärtused reale, et seostada ladu töökoormuse võimsuse seadistusega.
4. Valige märkeruut **Kombineeritud sissetulev ja väljaminev töökoormus**, kui aruanne **Töökoormuse võimsus** peaks kuvama sissetulevate ja väljaminevate kannete kogutöökoormust ühel vaatel.
5. Kiirkaardil **Kandetüübid** valige sissetulevate ja väljaminevate kannete tüübid, millele töökoormuse piirangud kehtivad.

    > [!NOTE]
    > Peate valima vähemalt ühe kande tüübi nii sissetulevale kui ka väljaminevale töökoormusele.

#### <a name="define-limits-for-volume-or-weight"></a>Mahu- või kaalupiirangute määramine

Saate seadistada piirangud mahule või kaalule olenevalt piirangust, mis on lao tööjõu seisukohalt olulised. Määratud piirangud sisalduvad töökoormuse võimsuse kavandis, mida saate vaadata aruandes **Töökoormuse võimsus**.

Kaupade mahu ja kaalu teabe kavandamiseks peavad ühe laokauba standardne maht ja ühe laokauba kaal kõikidele toodetele määratud olema. Vajalikud väljad on saadaval järgmistes väljagruppides lehe **Väljastatud toote üksikasjad** kiirkaardil **Varude haldus**.

- Käsitsemine
- Füüsilised dimensioonid
- Kaaluühikud

Kui seda teavet pole õigesti määratud, saate aruande **Töökoormuse võimsus** loomisel sõnumi. Aruandes saate seejärel süvitsi minna, et tuvastada puuduv teave, mis on vajalik tulevase töökoormuse kavandamiseks.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Töökoormuse võimsuse seadistuse seostamine koondplaaniga

1. Valige **Varude haldamine** \> **Perioodiline** \> **Töökoormuse plaanimine**.
2. Valige väljal **Koondplaan** töökoormuse kavandite jaoks kasutatav koondplaan.
3. Määrake väljal **Koondplaan** päevade arv, mille vältel töökoormuse kavand kehtib.
4. Valige väljal **Koondplaan** töökoormuse seadistus, mis seostatakse koondplaaniga.

### <a name="view-workload-capacity"></a>Töökoormuse võimsuse vaatamine

1. Valige **Varude haldamine** \> **Päringud ja aruanded** \> **Füüsiliste varude aruanded** \> **Töökoormuse võimsus**.
2. Määrake väljal **Veergude arv** aruandes kuvatavate veergude arv.
3. Valige väljas **Tellimuse tüüp** suvand **Plaanitud ja kinnitatud**, **Plaanitud** või **Kinnitatud**, et näidata, mis tüüpi tellimusi aruandes kavandada.
4. Valige väljal **Koondplaan** koormuse tüüp, et määrata, kas töökoormuse võimsus tuleb kavandada mahule või kaalule.
5. Valige väljal **Koondplaan** töökoormuse võimsuse seadistus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]