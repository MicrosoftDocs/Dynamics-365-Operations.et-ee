---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (27. november 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460903"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (27. november 2018)

**Järk 8.1.2064**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.


## <a name="changes"></a>Muutused

### <a name="unable-to-create-a-note-in-case-management"></a>Juhtumihalduses ei saa märget luua

Muudeti probleemi, mis ilmneb juhtumihalduse juhtumilogi märke redigeerimise või lisamise katsel.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Valesti kirjutatud sõna kompensatsiooni tööruumi analüütika vahekaardil 

Kompensatsiooni tööruumi kompensatsiooni analüütika vahekaardil parandati valiku Ethnic Origin (Etniline päritolu) õigekirja.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Tööruumi Töövõtja iseteenindus ei kuvata, kui töötajale pole kasutajat määratud 

Tehti muudatus käivitusel tööruumi **Töövõtja iseteenindus** valides esialgse lehena kasutaja jaoks, kes pole töövõtjale määratud. Selles olukorras kuvatakse vaikearmatuurlaud.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Puhkuste ja puudumiste tõrge: objekti viide ei ole seatud objekti eksemplarile

Pärast puhkuste ja puudumiste kirjete kinnitamist loendis **Mulle määratud tööüksused** on tõrke lahendamiseks tehtud puhkustes ja puudumistes muudatusi.

### <a name="unable-to-recall-an-image-workflow"></a>Pildi töövoogu ei saa tagasi kutsuda

Pärast pildi töövoo tagasikutsumist seatakse töövoo väärtuseks „tühistatud” ja olemasoleva taotluse saab kustutada töövõtja iseteeninduse tööruumis.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Uuesti värvatud töövõtjate või peatöövõtjatele mitmekordne kuvamine pärast lepingu lõpetamist 

Selle uuendusega kuvatakse lepingu lõpetanud ja uuesti värvatud töövõtjad lahkunute loendis ühekordselt. 

## <a name="known-issue"></a>Teadaolev probleem

- **Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid. 
- **Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud. Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud. (See probleem lahendatakse järgmisel platvormivärskendusel.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]