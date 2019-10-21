---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (7. veebruar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4005a8745e46a23fe16b94cab7b7aeb20f84035
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009758"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (7. veebruar 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="interview-scheduling-enhancements"></a>Vestluse plaanimise täiustused
Täielikule vestluse plaanimise kogemusele on tehtud täiustusi. Nüüd saate näha sisemise kandidaadi saadavust kalendris ja kasutada sisemise kandidaadi kalendrit graafikusoovitusteks. Lisateavet vt teemast [Vestluse plaanimine ja tagasiside](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Töö sisestamine LinkedIni – ettevõtte mittevastavuse probleem on parandatud
Parandati probleem, mille tõttu kuvati Attractist LinkedIni sisestatud tööd vale ettevõtte nime all. Lisateabe saamiseks vt [Tööde loomine, kinnitamine ja sisestamine Attractis](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Karjäärisaidi URL kuvatakse administraatori sätetes
Karjäärisaidi avalehe URL kuvatakse nüüd lehe **Administraatori sätted** jaotises **Karjäärisaidi haldus**.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

**Järk 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Töödel on toetatud mitu hüvitustaset
See muudatus võimaldab töös määratleda rohkem kui ühe hüvitustaseme, mis lubab töövõtja põhipalga vahemikud, mis võivad sama töö kasutamisel olla eri plaanides erinevad. 

Näide:    
*Töö* – kontohalduri *seostatud hüvitustasemed:* B1 ja B2 – igal tasemel on väärtuste määratletud vahemik. B1 = min 50 000, keskm 60 000, max 75 000 ja B2 = min 65 000, keskm 74 000, max 85 000. Määratud sobivusreeglite alusel töövõtjatele põhipalga loomisel saab nüüd iga fikseeritud plaan osutada samale tööle ja töösisestele erinevatele tasemetele. See võimaldab määratleda plaane erinevates piirkondades/ettevõtetes ning osutada samale tööle, kuid erinevatele vahemikele, ilma et töid oleks erinevuste arvesse võtmiseks vaja dubleerida.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Töövõtja põhipalga üksusesse lisati hüvitustaseme väli 
Selle värskendusega täiendati töövõtja põhipalga üksust väljaga **Hüvitustase**. See täiendus lihtsustab töövõtja põhipalga plaanide värskendamist. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Tööpere värskendamine uute ametikohtade värskendamisel ja loomisel
Ametikoha töö muutmisel on nüüd valitud töös vaikesätteks **Tööpere**.

### <a name="performance-improvements-when-rendering-workspaces"></a>Jõudluse parendamised tööruumide renderdamisel.
Tööruumide analüütika vahekaardid laaditakse nüüd ainult nende lehtede kasutamisel. Lehe algsel renderdamisel kuvatakse lehe vasakus ülanurgas indikaator.
