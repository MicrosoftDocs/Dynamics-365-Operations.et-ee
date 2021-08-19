---
title: Finantsaruandluse KKK
description: Selles teemas antakse vastused mõnedele korduma kippuvatele küsimustele finantsaruandluse kohta.
author: jiwo
ms.date: 07/07/2021
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
ms.openlocfilehash: dd493e855e45362c1681dc9cdfbbcb71f7627d64624cd093eadab32fd966c174
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733607"
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

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Kuidas mõjutab ajaloolise kursi teisendamise valik aruande tulemuslikkust?

Ajaloolist kurssi kasutatakse tavaliselt jaotamata kasumi, kinnisvara, seadmete ja omakapitali kontode puhul. Ajalooline kurss võib olla vastavalt Finantsarvestuse standardite nõukogu (FASB) suunistele või heale raamatupidamistavale (GAAP) nõutav. Lisateavet vt teemast [Finantsaruande valuutavõimalused](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Mitut tüüpi valuutakursse on olemas?

Neid on kolme tüüpi.

- **Praegune kurss** – seda tüüpi kasutatakse tavaliselt bilansikontodel. Seda nimetatakse tavaliselt *hetkekursiks* ja see võib olla kuu viimase päeva või mõne muu eelnevalt määratud kuupäeva kurss.
- **Keskmine kurss** – seda tüüpi kasutatakse tavaliselt kasumiaruande (kasumi/kahjumi) kontodel. Saate keskmise kursi määrata nii, et see oleks lihtne keskmine või kaalutud keskmine.
- **Ajalooline kurss** – seda tüüpi kasutatakse tavaliselt jaotamata kasumi, kinnisvara, seadmete ja omakapitali kontode puhul. Need kontod võivad olla FASB või GAAP suuniste kohaselt nõutavad.

## <a name="how-does-historical-currency-translation-work"></a>Kuidas ajalooline valuutateisendus toimib?

Kursid kehtivad kandekuupäeva kohta. Seetõttu teisendatakse iga kanne eraldi, lähtudes lähimast vahetuskursist.

Ajaloolise valuutateisenduse puhul võidakse üksikute kande üksikasjade asemel kasutada eelnevalt arvutatud perioodisaldosid. Selline käitumine erineb praeguse kursiga teisendamise käitumisest.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Kuidas mõjutab ajalooline valuutateisendus jõudlust?

Aruannetes esitatud andmete värskendamisel võib ilmneda viivitus, kuna summad tuleb kande üksikasjade kontrollimise teel ümber arvutada. See viivitus käivitatakse iga kord, kui kursse värskendatakse või sisestatakse rohkem kandeid. Kui ajalooliseks teisendamiseks seadistatakse paar korda päevas tuhandeid kontosid, võib aruande andmete värskendamine viibida kuni tund aega. Teisest küljest, kui konkreetsete kontode arv on väiksem, võib aruande andmete värskenduste töötlemisaeg lüheneda minutitele või lühemaks.

Samamoodi, kui aruanded genereeritakse ajaloolist tüüpi kontode valuutateisenduse abil, tehakse täiendavaid kandepõhiseid arvutusi. Olenevalt kontode arvust võib aruande genereerimise aeg olla enam kui kaks korda pikem.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
