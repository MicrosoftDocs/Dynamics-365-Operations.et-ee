---
title: Ühisparameetrite konfigureerimine
description: Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aff01bee8cadcf852ae32fd60447c68e2174a2a
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2021
ms.locfileid: "6332991"
---
# <a name="configure-shared-parameters"></a>Ühisparameetrite konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.

Mõnd tüüpi kirjeid, nt ametikohakirjeid, ühiskasutatakse kõikides ettevõtetes. Nende kirjete puhul peate seadistama ühiskasutatavad parameetrid. Kasutate näiteks lehte **Inimressursside ühiskasutusega parameetrid**, et seadistada inimressursside parameetrid juriidilistele isikutele. 

Lehel **Inimressursside ühiskasutusega parameetrid** on parameetrid rühmitatud piirkondadeks nende funktsiooni põhjal. 

### <a name="settings"></a>Sätted
Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode. Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada. Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**. Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake valikuid **Personalijuhtimine** &gt; **Linkide vahekaart** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**. Saate sisestada lihtsa koodi ja kirjelduse. 

Vahekaardil **Numbriseeriad** saate valida numbriseeriad, mida kasutatakse järgmiste kirjete puhul: Personalinumber, Ametikoht, Kasutajanõude ID, I-9 dokument, Kandidaat, Arutelu, Soodustuse ID ja Personalitoiming (kui see kirje tüüp on lubatud). Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad**. Selle lehe leidmiseks kasutage lehe otsimise funktsiooni. 

Osutage vahekaardil **Ametikohad**, kas määramisele on saadaval vaikimisi uusi ametikohti.

- **Alati** – ametikohtade loomisel saate töötajaid uutele ametikohtadele määrata. Ametikohtade loomisel seatakse valiku **Määramiseks saadaval** kuupäev ja kellaaeg lehe **Ametikoht** vahekaardil **Üldine** automaatselt loomise kuupäevale ja kellaajale.
- **Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata. Kui valite selle suvandi, peate avama lehekülje **Ametikoht** iga uue ametikoha jaoks, kui see muutub kättesaadavaks. Seejärel sisestage **Üldine** vahekaardil **määramise jaoks** töötaja määramise lubamiseks kuupäeva.

Vahekaardil **Täpsem juurdepääs** saate piirata juurdepääsu teabele või linkidele:

- **Juurdepääsu piiramine töötaja teabele** - lülitage see funktsioon sisse, kui kasutajatel peaks olema võimalik vaadata töötaja teavet ainult nende juriidiliste isikute puhul, kellele neil on juurdepääs, ja töötajate puhul, kellel on nendes juriidilistes isikutes töö.

    Kui see funktsioon on sisse lülitatud, järgige neid samme, et seadistada sobivad õigused igale kasutajale, kelle vaade peab olema piiratud:

    1. Valige **kasutaja** lehel kasutaja.
    1. Valige kasutajale roll. Suvand **Organisatsioonide määramine** muutub kättesaadavaks.
    1. Valige **Organisatsioonide määramine**.
    1. Valige uuel leheküljel suvand **Anna juurdepääs konkreetsetele organisatsioonidel** ja seejärel valige organisatsioonid, mille juurdekasutajal peab juurdepääs olema.
    1. Korrake samme 2 kuni 4 muude rollide puhul, mis kasutajal on, k.a süsteemi kasutaja roll.

    > [!NOTE]
    > Ettevõtted, kus kasutajal juurdepääs on, peavad ühtima kõigi kasutaja rollidega.

- **Luba ettevõtetevahelise hüvitise vaade** – hüvitus töötajatele määratakse tööle juriidilise isiku kohta. Mõnikord võib töötaja olla tööle võetud korraga mitmesse juriidilisse isikusse. Kui see funktsioon on sisse lülitatud, kuvatakse igale juriidilisele isikule hüvitus töötajate iseteeninduses ja haldurite iseteeninduses ilma, et peate juriidilisi isikuid muutma. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
