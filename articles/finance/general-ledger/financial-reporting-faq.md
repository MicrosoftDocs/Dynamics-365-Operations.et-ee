---
title: Finantsaruandluse KKK
description: Selles teemas antakse vastused mõnedele korduma kippuvatele küsimustele finantsaruandluse kohta.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266629"
---
# <a name="financial-reporting-faq"></a>Finantsaruandluse KKK

Selles teemas antakse vastused korduma kippuvatele küsimustele finantsaruandluse kohta.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Kuidas piirata puuturbe abil juurdepääsu aruandele?

Järgmises näites kirjeldatakse aruandele juurdepääsu piiramist puuturbe abil.

Demoettevõttel USMF on **bilansiaruanne**, millele ei pea kõik finantsaruandluse kasutajad juurde pääsema. Turvapuu abil saate piirata juurdepääsu ühele aruandele nii, et sellele oleks juurdepääs ainult teatud kasutajatel.

1. Logige rakendusse Financial Reporter Report Designer sisse.
2. Uue puu definitsiooni loomiseks valige **Fail \> Uus \> Puu definitsioon**.
3. Topeltpuudutage (või topeltklõpsake) veerus **Üksuse turve** rida **Kokkuvõte**.
4. Valige **Kasutajad ja grupid**.
5. Valige kasutajad või grupid, kellele soovite anda juurdepääsu sellele aruandele.
6. Valige käsk **Salvesta**.
7. Lisage aruande definitsioonis uus puudefinitsioon.
8. Valige puudefinitsioonis **Säte**. Seejärel valige jaotises **Aruandlusüksuse valik** **Kaasa kõik üksused**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Kuidas tuvastada, millised kontod minu saldodele ei vasta?

Kui teil on aruanne, millel pole kattuvaid saldosid, kasutage iga konto ja hälbe tuvastamiseks järgmisi protseduure.

### <a name="in-financial-reporter-report-designer"></a>Asukohas Financial Reporter Report Designer

1. Looge uus readefinitsioon.
2. Valige **Redigeeri \> Lisa read dimensioonidest**.
3. Valige **MainAccount**.
4. Valige nupp **OK**.
5. Salvestage readefinitsioon.
6. Looge uus veerudefinitsioon.
7. Looge uus aruande definitsioon.
8. Valige **Sätted** ja tühjendage selle suvandi ruut.
9. Looge aruanne. 
10. Eksportige aruanne Microsoft Excelisse.

### <a name="in-dynamics-365-finance"></a>Asukohas Dynamics 365 Finance

1. Avage **Pearaamat \> Päringud ja aruanded \> Proovibilanss**.
2. Seadistage järgmised väljad.

    - **Alguskuupäev** – sisestage finantsaasta alguskuupäev.
    - **Lõppkuupäev** – sisestage kuupäev, mille kohta aruande loote.
    - **Finantsdimensioon** – seadke selle välja väärtuseks **Põhikonto kogum**.

3. Valige **Arvuta**.
4. Eksportige aruanne Excelisse.

Nüüd saate kopeerida andmeid Financial Reporteri Exceli aruandest **proovibilansi** aruandesse, et võrrelda veerge **Sulgemissaldo**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Aruande kujundamisel Report Designeris või finantsaruande genereerimisel kuvati järgmine teate: „Toimingut ei saanud andmepakkuja raamistikus ilmnenud probleemi tõttu lõpule viia.” Mida peaksin tegema?

Teade näitab, et probleem tekkis siis, kui süsteem püüdis tuua finantsmetaandmeid andmevakast finantsaruandluse kasutamise ajal. Selle probleemi lahendamiseks on kaks võimalust.

- Vaadake üle andmete integreerimisolek, tehes Report Designeris valikud **Tööriistad \>integreerimisolek**. Kui integreerimine on pooleli, oodake, kuni see on lõpule viidud. Seejärel proovige uuesti toimingut, mida tegite teate ilmnemisel.
- Probleemi tuvastamiseks ja lahendamiseks pöörduge toe poole. Süsteemis võivad olla vastuolulised andmed. Tugitehnikud aitavad teil seda probleemi serveris tuvastada ja leida kindlad andmed, mis võivad vajada värskendamist.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
