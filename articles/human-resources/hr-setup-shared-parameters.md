---
title: Ühisparameetrite konfigureerimine
description: Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72742c38c3ff25d665bd1a3d0ea54f167dc0693c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430045"
---
# <a name="configure-shared-parameters"></a>Ühisparameetrite konfigureerimine

Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.

Mõnd tüüpi kirjeid, nt ametikohakirjeid, ühiskasutatakse kõikides ettevõtetes. Nende kirjete puhul peate seadistama ühiskasutatavad parameetrid. Kasutate näiteks lehte **Inimressursside ühiskasutusega parameetrid**, et seadistada inimressursside parameetrid juriidilistele isikutele. 

Lehel **Inimressursside ühiskasutusega parameetrid** on parameetrid rühmitatud piirkondadeks nende funktsiooni põhjal. 

### <a name="previously-released-functionality"></a>Varem välja antud funktsioonid
Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode. Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada. Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**. Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake valikuid **Personalijuhtimine** &gt; **Linkide vahekaart** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**. Saate sisestada lihtsa koodi ja kirjelduse. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Rakenduse Dynamics 365 Human Resources kasutamisel
Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode. Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada. Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**. Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake suvandeid **Inimressursid** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**. Saate sisestada lihtsa koodi ja kirjelduse. 

Vahekaardil **Numbriseeriad** saate valida numbriseeriad, mida kasutatakse järgmiste kirjete puhul: Personalinumber, Ametikoht, Kasutajanõude ID, I-9 dokument, Kandidaat, Arutelu, Soodustuse ID ja Personalitoiming (kui see kirje tüüp on lubatud). Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad**. Selle lehe leidmiseks kasutage lehe otsimise funktsiooni. 

Osutage vahekaardil **Ametikohad**, kas määramisele on saadaval vaikimisi uusi ametikohti.

-   **Alati** – ametikohtade loomisel saate töötajaid uutele ametikohtadele määrata. Ametikohtade loomisel seatakse valiku **Määramiseks saadaval** kuupäev ja kellaaeg lehe **Ametikoht** vahekaardil **Üldine** automaatselt loomise kuupäevale ja kellaajale.
-   **Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata. Selle suvandi valimisel peata avama lehe **Ametikoht** iga uue ametikoha jaoks kohe, kui see muutub kättesaadavaks, ja sisestama siis vahekaardile **Üldine** suvandi **Määramiseks saadaval**kuupäeva, et lubada töötaja määramine.
