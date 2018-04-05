---
title: Microsoft Projecti kliendi integreerimine
description: "Projektigraafiku kavandamine ja haldamine võib olla keeruline, seega vajavad projektijuhid seda ülesannet hõlbustavaid vahendeid. Microsoft Projecti kliendiga integreerimine aitab projekti tööjaotuse struktuuri avada ja hallata."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Microsoft Projecti kliendi integreerimine

[!include[banner](../includes/banner.md)]

Projektigraafiku kavandamine ja haldamine võib olla keeruline, seega vajavad projektijuhid seda ülesannet hõlbustavaid vahendeid. Microsoft Projecti kliendiga integreerimine aitab projekti tööjaotuse struktuuri avada ja hallata. Projektijuht saab muudatusi saata tagasi Finance and Operationsi projekti tööjaotuse struktuuri.

> [!NOTE]
> Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations 2017. aasta juuli värskendust, peate installima KB 4054797 ja 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Projecti kliendi lisandmooduli konfigureerimine
Microsoft Projecti kliendiga integreerimise lubamiseks tuleb kasutaja Microsoft Projecti klientrakendusse installida Microsoft Dynamics 365 lisandmoodul. Selleks tuleb avada **Projektihalduse tööruum**.

•   Klõpsake suvandit **Projecti kliendi lisandmooduli konfigureerimine** tööruumi jaotises **Lingid** > **Seadistamine**.

•   Klõpsake käsku **Ava** ning seejärel selle kuvamisel käsku **Käivita**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Microsoft Projecti kliendis oleva projekti tööjaotuse struktuuri mustandi avamine ja redigeerimine
Kui rakenduse Finance and Operations projektis on juba loodud tööjaotuse struktuur, saab seda avada Microsoft Projecti klientrakenduses, kui tööjaotuse struktuur on mustandi olekus. Lehelt **Projekti** avamiseks klõpsake vahekaardil **Plaan** olevat linki **Microsoft Projectis avamine**. Seda lehte saate avada ka Microsoft Projecti klientrakenduses, vahekaardil **Microsoft Dynamics 365** käsku **Ava**. Valige loendist **Juriidiline isik** ja **Projekt**.

> [!NOTE]
> Kui kasutate brauserina Internet Explorerit, peate faili selle allalaadimise asukohast käsitsi avamiseks klõpsama käsku **Salvesta**. Võite ka faili Microsoft Projecti klientrakenduses avamiseks klõpsata käsku **Salvesta ja ava**. Ärge nimetage faili salvestamisel ümber.

Enne Microsoft Projecti klientrakendust kasutava faili redigeerimist peate selle välja registreerima. Klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Registreeri välja**. See takistab teistel kasutajatel tööjaotuse struktuuri samal ajal rakenduses Finance and Operations redigeerida. Tööjaotuse struktuuri avaldamiseks pärast redigeerimist klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Registreeri sisse**.

Kui projektile on rakenduses Finance and Operations juba lisatud projekti töörühm, täidetakse ressursiloend töörühma liikmetega. Kas projekti töörühma ei ole veel projektile lisatud, saate ressursse valida ja töörühma luua Microsoft Projecti klientrakenduses, klõpsates vahekaardi **Microsoft Dynamics 365** nuppu **Ressursid**. 

Sisseregistreerimise osana sünkroonitakse järgmised andmed tagasi rakendusse Finance and Operations.

•   Ülesande nimi

•   Alguskuupäev

•   Lõpetamiskuupäev

•   Eelkäijad

•   Ressursinimed

•   Kategooria:

•   Ressursikategooria

•   Töötunnid

•   Märkmed

•   Prioriteet

> [!NOTE]
> Microsoft Projecti klientrakendusse veergude lisamisel ei salvestata neid faili ega kuvata faili uuesti avamisel.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Projecti klientrakenduse abil olemasoleva projekti tööjaotuse struktuuri loomine
Microsoft Projecti klientrakenduse abil olemasoleva projekti tööjaotuse struktuuri loomiseks tehke läbi järgmised etapid.


1.  Avage Microsoft Projecti klient.

2.  Klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Ava**.

3.  Valige projekti jaoks **Juriidiline isik**.

4.  Valige **Projekt**.

5.  Klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Registreeri välja**.

6.  Kui olete valmis seda rakenduses Finance and Operations avaldama, klõpsake vahekaardil **Microsoft Dynamics 365** olevat käsku**Registreeri sisse**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Projecti klientrakenduse abil olemasoleva projekti tööjaotuse asendamine
Microsoft Projecti klientrakenduse abil uue tööjaotuse struktuuri loomiseks ja olemasoleva projekti tööjaotuse asendamiseks tehke läbi järgmised etapid.

1.  Avage Microsoft Projecti klient.

2.  Looge Microsoft Projecti kliendil graafik.

3.  Klõpsake vahekaardil **Microsoft Dynamics 365** käske **Salvesta** > **Asenda olemasolev projekt**.

4.  Valige projekti jaoks **Juriidiline isik**.

5.  Valige **Projekt**.

6.  Klõpsake nupul **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Uue projekti loomine Microsoft Projecti klientrakenduses


1.  Avage Microsoft Projecti klient.

2.  Looge Microsoft Projecti kliendil graafik.

3.  Klõpsake vahekaardil **Microsoft Dynamics 365** käske **Salvesta** > **Salvesta uude projekti**.

4.  Valige projekti jaoks **Juriidiline isik**.

5.  Vajaduse korral sisestage **Projekti ID**.

6.  Sisestage **Projekti nimi**.

7.  Valige **Projekti tüüp**, **Projektigrupp** ja **Projektilepingu ID**. Teise võimalusena saate luua uue projektilepingu, klõpsates suvandit **Uus**.

8.  Valige ressurssideks kasutatav **Kalender**.

11. Klõpsake nupul **OK**.

