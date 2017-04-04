---
title: "Pearaamatu töölehe töötlemine"
description: "Käesolevas artiklis kirjeldatakse võimalusi Microsoft Dynamics 365, mis aitavad teha peažurnaali töötlemist lihtsamaks ja see aitab tagada, et õiged andmed on hõivatud ja sisekontrolli turvalisus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Pearaamatu töölehe töötlemine

Selles artiklis kirjeldatakse Microsoft Dynamics AX-i võimalusi, mis lihtsustavad üldise töölehe töötlemist ja mis aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud.  

Töölehe nimed

Üks tähtsamaid valdkondi seadistamiseks on nimed. See on mõistlik määratleda konkreetse töölehe nimesid soliidselt, nagu kontsernisisene, viitvõlgade seadistamise ja vigade parandamiseks. Saab vastavalt iga töölehe nimi, et muuta andmete sisestamisel soliidselt, lihtne ja turvaline. 

Lehel **Töölehe nimed** saate seadistada järgmisi elemente.

-   **Töövoo kinnitamine** – sisekontrolli tõhustamiseks määratlege töölehe töövood, mis loovad ülevaatus- ja kinnitamisetappide materiaalsuspiirangud kriteeriumide, nagu deebeti kogusummade alusel. Saate seadistada Peažurnaalide töövood on ** pearaamatu töövood ** lehekülg.
-   **Vaikeväärtused** – valige vastaskontode, valuuta ja finantsdimensioonide vaikeväärtused.
-   **Töölehe juhtimine** – saate seadistada ettevõtte ja kontotüübi piiranguid ja ka segmendi väärtusi. 

**Näited**

Töölehe nime võib kasutada ainult korrigeerimiseks. Sellisel juhul saate määrata, et kõigis ettevõtetes kehtib ainult konto tüüp **Pearaamat**. [![Töölehe juhtelemendi tüübid](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Töölehe nime saab kasutada ainult kindla segmendi või põhikontode vahemiku puhul. [![Töölehe juhtelemendi segmendi](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Päevaraamatutes on saadaval suvand **Automaatne tühistamine**. Näiteks viitvõlgade korrigeerimise puhul, kui tegelikku dokumenti pole veel töödeldud, nagu on näidatud järgmisel joonisel.
[![Tagurdamine peažurnaali](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Exceli lisandmoodul päevikukande pakub automaatika ja lihtsustab andmete sisestamisel. Tegevus **Ridade avamine Excelis **on saadaval lehtedel **Päevaraamat** ja **Töölehe kanne**. 

Lehel **Perioodilised töölehed** saate töölehe töötlemise automatiseerimiseks seadistada korduvad töölehed. 

Kande malle saate kasutada igal ajal. Kohta ning **Peažurnaalide** lehel on **salvestada** ja **valige kande malli** meetmeid võib leida ning **töölehe kanne** lehekülg alla **funktsioonid** kande ridade.

## <a name="related-setup"></a>Seotud seadistus
Järgmine seadistus ei ole omane päevaraamatutele, kuid aitab tagada, et andmesisestus oleks õige ja lihtne.

### <a name="main-account"></a>Põhikonto

Põhikonto seadistus pakub päevaraamatu töötlemiseks mitmeid järgmisi suvandeid.

-   **DC/CR-i nõue** – kasutage seda suvandit, kui põhikonto on piiratud deebet- või kreeditkannetele. Seadistus kinnitatakse töölehe kontrollimisel või sisestamisel.
-   **Vaikevastaskonto**
-   **Peatatud** – põhikonto peatamine andmesisestuseks kõigis ettevõtetes või kindla ettevõtte/juriidiliste isikute puhul.
-   **Ära luba käsitsi sisestamist** – takistab kasutajatel töölehtede konto väärtuse käsitsi sisestamise.
-   **Vaikevaluuta/valuuta kinnitamine**
-   **Juriidilise isiku alistamine** – see seadistus on omane määratud ettevõttele/juriidilisele isikule.
    -   **Vaikimisi käibemaks/käibemaksu kinnitamine**
    -   **Vaikedimensioon** – **Pole fikseeritud** või **Fikseeritud väärtus**. **Fikseeritud väärtus** aitab tagada, et kõigi selle põhikonto sisestuste puhul kasutatakse alati dimensiooniväärtust, mis on seadistatud kui **Fikseeritud**.
-   **Sisestuse kontrollimine**
    -   **Kasutaja kinnitamine** – see suvand kontrollib, millised kasutajad võivad põhikontole sisestada.
    -   **Sisestamistüübi kinnitamine** – see suvand kontrollib, millised sisestamistüübid on lubatud põhikonto puhul.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Arvestusstruktuurid ja täpsemate reeglite struktuurid

Arvestusstruktuurid ja täpsemate reeglite struktuurid on äärmiselt olulised, tagamaks andmete nõudmine finantsaruandluseks ja jõudluse jälgimise rakendamine päevaraamatu töötlemisel ja mis tahes dokumentide puhul. Arvestusstruktuurid ja täpsemate reeglite struktuurid võimaldavad teil andmete sisestamise kogemust kohandada. Saate lubada andmesisestuse ainult igas olukorras asjakohaste finantsdimensioonide puhul ja rakendada alati kohustuslike ja õigete andmete hõivamise nõuet.

Lisateabe saamiseks vaadake [planeerimine: kontoplaani](plan-chart-of-accounts.md). 


