---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (5. märts 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2019
ms.locfileid: "782845"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (5. märts 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="extending-option-sets-in-attract"></a>Suvandikomplektide laiendamine Attractis

Attractis on mitu välja, mis on teenuse Common Data Service (CDS) suvandikomplektid. Suvandikomplektide laiendamiseks on kasutusele võetud uusi võimalusi, alustades väljadega **Tagasilükkamise põhjus**, **Töösuhte tüüp** ja **Staaži tüüp**.

> [!IMPORTANT]
> Funktsioon Töö sisestamine LinkedIni nõuab lehel **Töö üksikasjad** väljade **Töösuhte tüüp** ja **Staaži tüüp** kasutamist. LinkedIn toetab nende väljade vaikeväärtuseid ja need kuvatakse pärast töö sisestamist. Kui sisestate töid LinkedIni ja muudate nende väljade olemasolevaid suvandikomplekti väärtusi, töö siiski sisestatakse, kuid LinkedIn ei kuva väljade **Töösuhte tüüp** ja **Staaži tüüp** kohandatud väärtusi.

## <a name="changes-in-onboarding"></a>Muutused kasutuselevõtus

### <a name="private-preview-for-onboard-teams"></a>Kasutuselevõtu meeskondade privaatne eelvaade
Nüüd saate malle kogu oma ettevõtte ulatuses hõlpsasti ühiskasutusse anda ja nendega koostööd teha. Lisateabe saamiseks vt jaotist [Kasutuselevõtu meeskondade abil parimate tavade ühiskasutusse andmine kogu ettevõtte ulatuses](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Täitjate kohatäidete privaatne eelvaade
Saate oma malle rikastada, kui määrate tegevusi isikute asemel rollidele. Seejärel määratakse rollid juhendi loomisel isikutele. Lisateabe saamiseks vt jaotist [Juhendi haldamise rollitegevuste määramise abil sujuvamaks muutmine](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Core HR-i muudatused
**Järk 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Konfigureerige töövoog automaatselt kinnitama või jälgima töövoogu, kui inimressursside või rea haldur esitab või värskendab puhkusetaotlusi
Lisatud on uued töövoo tingimused, mis võimaldavad puhkusetaotluste automaatset kinnitamist juhul, kui need esitab töövõtja haldur või personalihaldur. Üks võimalus töövoo automaatse kinnitamise saavutamiseks on lubada töövoo kinnitamisel automaatne tegevus.

Lisatud tingimused sisaldavad järgmist.

- Edastaja – kasutatakse selle kasutaja, kes taotluse töövoogu esitas, süsteemikasutaja ID hindamiseks.
- Kelle nimel edastatud – kasutatakse hindamaks, kas puhkusetaotlus esitati taotlusega seostatud töötaja nimel.
- Inimressursside edastatud – kasutatakse hindamaks, kas taotluse töövoogu esitanud süsteemikasutaja omab inimressursside rolli.
- Halduri edastatud – kasutatakse hindamaks, kas puhkusetaotluse töövoogu esitanud kasutaja on taotlusega seotud töötaja reahierarhia haldur.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Töövõtja põhipalga lubamine tulevaste ametikoha määrangute jaoks
Tavaliselt liituvad töövõtjad ettevõttega tulevikus oleva alguskuupäevaga. See muudatus võimaldab määrata põhipalka tulevaste ametikoha määramistega töövõtjatele.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Ametikoha palgaarvestuse väljad on ametikoha redigeerimisel tühjad
Selle muudatuse tõttu määratakse olemasolevate ametikohtade muudatuste taotlemisel palgaarvestuse väljade vaikeväärtusteks praegused väärtused.

### <a name="other-miscellaneous-bug-fixes"></a>Muud mitmesugused veaparandused
See versioon sisaldab ka muid väikesi veaparandusi.

### <a name="upgrade-to-cds-for-apps"></a>Täiendamine teenusele CDS for Apps
Teenusele CDS for Apps täiendamise tähtajad lähenevad kiirelt. Logige sisse PowerAppsi halduskeskusesse, et määrata, kas teie andmebaas vajab täiendamist. Lisateavet tähtaegade ja täiendamiseks nõutavate etappide kohta vt jaotisest [Täiendamine teenusele Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Peagi tulekul

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Täpsem hüvitusturve (fikseeritud ja muutuv)
Paljudes ettevõtetes pääsevad hüvitise ja eeliste haldurid juurde ainult teatud hüvituskirjetele, nagu juhtkonna või piirkonnapõhiste töövõtjate kirjed. Selle muudatusega saate ettevõttesiseselt hüvitusplaane hallata ja säilitada erinevate töövõtjate populatsioonide jaoks. Fikseeritud ja muutuvatele plaanidele saab määrata turberolle, mis määravad plaanide juurdepääsu ja plaanidega seotud töövõtja andmed, näiteks palga või lisakulumikirjed. Nende töövõtjate hüvitisi saavad töödelda ainult rollid, millele on antud juurdepääs.

###  <a name="platform-update-24"></a>Platvormivärskendus update 24
Lisateavet platvormivärskenduse 24 kohta vt jaotisest [Mis on rakenduse Finance and Operations platvormivärskenduses 24 uut või mida on muudetud (märts 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
