---
title: Pearaamatu töölehe töötlemine
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi võimalusi, mis lihtsustavad üldise töölehe töötlemist ja aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7efd250428f7675b96674dd02e3aeccefe653fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839227"
---
# <a name="general-journal-processing"></a>Pearaamatu töölehe töötlemine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi võimalusi, mis lihtsustavad üldise töölehe töötlemist ja aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud.  

## <a name="journal-names"></a>Töölehe nimed

Üks tähtsaim seadistatav ala on töölehe nimed. Soovitatav on määratleda konkreetsed töölehe nimed igaks eesmärgiks, nt kontsernisiseseks, viitvõlgade korrigeerimiseks ja vigade parandamiseks. Saate kohandada iga töölehe nime iga eesmärgi puhul andmete sisestamise lihtsaks ja turvaliseks muutmiseks. 

Lehel **Töölehe nimed** saate seadistada järgmisi elemente.

-   **Töövoo kinnitamine** – sisekontrolli tõhustamiseks määratlege töölehe töövood, mis loovad ülevaatus- ja kinnitamisetappide materiaalsuspiirangud kriteeriumide, nagu deebeti kogusummade alusel. Saate pearaamatute töövoogusid seadistada lehel **Pearaamatu töövood**.
-   **Vaikeväärtused** – valige vastaskontode, valuuta ja finantsdimensioonide vaikeväärtused.
-   **Töölehe juhtimine** – saate seadistada ettevõtte ja kontotüübi piiranguid ja ka segmendi väärtusi. 

**Näited**

Töölehe nime võib kasutada ainult korrigeerimiseks. Sellisel juhul saate määrata, et kõigis ettevõtetes kehtib ainult konto tüüp **Pearaamat**. 

[![Töölehe juhtimise kontotüübid](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Töölehe nime saab kasutada ainult kindla segmendi või põhikontode vahemiku puhul. 

[![Töölehe juhtimise segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Päevaraamatutes on saadaval suvand **Automaatne tühistamine**. Näiteks viitvõlgade korrigeerimise puhul, kui tegelikku dokumenti pole veel töödeldud, nagu on näidatud järgmisel joonisel.
[![Pearaamatu ennistamine](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Exceli lisandmoodul pakub töölehe sisestuse puhul automatiseerimise täiendavat taset ja lihtsustab andmesisestust. Tegevus **Ridade avamine Excelis** on saadaval lehtedel **Päevaraamat** ja **Töölehe kanne**. 

Lehel **Perioodilised töölehed** saate töölehe töötlemise automatiseerimiseks seadistada korduvad töölehed. 

Saate kande malle kasutada igal ajal. Lehel **Päevaraamatud** on tegevused **Salvesta** ja **Vali kande mall** lehe **Töölehe kanne** kande ridade **Funktsioonid** all.

## <a name="related-setup"></a>Seotud seadistus
Järgmine seadistus ei ole omane pearaamatutele, kuid aitab tagada, et andmesisestus oleks õige ja lihtne.

### <a name="main-account"></a>Põhikonto

Põhikonto seadistus pakub päevaraamatu töötlemiseks mitmeid järgmisi suvandeid.

-   **DC/CR-i nõue** – kasutage seda suvandit, kui põhikonto on piiratud deebet- või kreeditkannetele. Seadistus kinnitatakse töölehe kontrollimisel või sisestamisel.

-   **Vaikevastaskonto**
-   **Peatatud** – põhikonto peatamine andmesisestuseks kõigis ettevõtetes või kindla ettevõtte / juriidilise isiku puhul.
-   **Ära luba käsitsi sisestamist** – takistab kasutajatel töölehtede konto väärtuse käsitsi sisestamise.
-   **Vaikevaluuta/valuuta kinnitamine**
-   **Juriidilise isiku alistamine** – see seadistus on omane määratud ettevõttele/juriidilisele isikule.
    -   **Vaikimisi käibemaks/käibemaksu kinnitamine**
    -   **Vaikedimensioon** – **Pole fikseeritud** või **Fikseeritud väärtus**. **Fikseeritud väärtus** aitab tagada, et kõigi selle põhikonto sisestuste puhul kasutatakse alati dimensiooniväärtust, mis on seadistatud kui **Fikseeritud**.
-   **Sisestuse kontrollimine**
    -   **Kasutaja kinnitamine** – see suvand kontrollib, millised kasutajad võivad põhikontole sisestada.
    -   **Sisestamistüübi kinnitamine** – see suvand kontrollib, millised sisestamistüübid on lubatud põhikonto puhul.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Arvestusstruktuurid ja täpsemate reeglite struktuurid

Arvestusstruktuurid ja täpsemate reeglite struktuurid on äärmiselt olulised tagamaks, et finantsaruandluseks ja jõudluse jälgimiseks vajalikud andmed hõivatakse pearaamatu töötlemisel ja mis tahes dokumentatsioonis. Arvestusstruktuurid ja täpsemate reeglite struktuurid võimaldavad teil andmete sisestamise kogemust kohandada. Saate lubada andmesisestuse ainult igas olukorras asjakohaste finantsdimensioonide puhul ning rakendada alati kohustuslike ja õigete andmete hõivamise nõuet.

Lisateavet vt järgmistest teemadest:
- [Plaanimine: kontoplaan](plan-chart-of-accounts.md). 
- [Täpsemate reeglite loomine töölehtede jaoks](tasks/create-advanced-rules-journals.md)
- [Töölehe sisestuse loomine malli abil](tasks/create-journal-entry-template.md)
- [Töölehtede loomine ja kinnitamine](tasks/create-validate-journals.md)
- [Perioodiliste töölehtede sisestamine](tasks/post-periodic-journals.md)
- [Pearaamatu eraldamistöölehe töötlemine](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Simuleeri sisestamist
Suvandi **Sisestamise simuleerimine** leiate enamiku töölehtede puhul menüüst **Kinnitamine**. Töölehe kinnitamisel funktsiooniga **Kinnitamine** kontrollib süsteemi töölehte konkreetsete tõrketingimuste suhtes. Funktsiooni **Sisestamise simuleerimine** kasutamisel käitab süsteem samu protsesse mida sisestamise ajal, kuid töölehte tegelikult sisestamata. Seejärel saate üle vaadata kuvatud sisestamisteated, paranda leitud tõrked ja seejärel klõpsata töölehe sisestamiseks menüüd **Sisestamine**. 

**Sisestamise simuleerimine** pole saadaval pakktöötluse puhul. Siiski on saadaval kood sisestamise simuleerimiseks pakktöötluses ja arendajatel on võimalik koodi laiendada selle funktsionaalsuse lisamiseks.  
