---
title: Ühisparameetrite konfigureerimine
description: Käesolev teema kirjeldab inimressursside parameetrite seadistamist juriidiliste isikute lõikes.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 039d8e2100824921d568c013fe3e113e1b091979
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729095"
---
# <a name="configure-shared-parameters"></a>Ühisparameetrite konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Peate seadistama ühised parameetrid kirjetele, mida jagatakse ettevõtete vahel, nt **Positsiooni** kirjed. Käesolev teema kirjeldab inimressursside parameetrite seadistamist juriidiliste isikute lõikes.

Teatud tüüpi kirjed, nt Positsiooni **·** kirjed, on mitme ettevõtte ühiskasutuses. Nende kirjete puhul peate seadistama ühiskasutatavad parameetrid. Näiteks inimressursside jagatud **parameetrite lehte kasutatakse inimressursside parameetrite** häälestamiseks juriidiliste isikute lõikes. 

Lehel **Inimressursside ühiskasutusega parameetrid** on parameetrid rühmitatud piirkondadeks nende funktsiooni põhjal. 

### <a name="settings"></a>Sätted
Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode. Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada. Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**. Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks minge personalihalduse linkide **·** &gt; **·** &gt; **häälestuse** &gt; **ID-tüüpi.** Saate sisestada lihtsa koodi ja kirjelduse. 

Numbriseeriate vahekaardil saate valida numbriseeriad, mida kasutatakse järgmiste kirjete **·** jaoks: personalinumber, positsioon, kasutajanõude **·** **·** **·** **ID, I-9** dokument, **·** kandidaat, **·** arutelu, **hüvitise ID** **·** ja personalitegevus (kui see kirjetüüp on lubatud). Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad**. Selle lehe leidmiseks kasutage lehe otsimise funktsiooni. 

Osutage vahekaardil **Ametikohad**, kas määramisele on saadaval vaikimisi uusi ametikohti.

- **Alati** – ametikohtade loomisel saate töötajaid uutele ametikohtadele määrata. Ametikohtade loomisel seatakse valiku **Määramiseks saadaval** kuupäev ja kellaaeg lehe **Ametikoht** vahekaardil **Üldine** automaatselt loomise kuupäevale ja kellaajale.
- **Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata. Kui valite selle suvandi, peate avama lehekülje **Ametikoht** iga uue ametikoha jaoks, kui see muutub kättesaadavaks. Seejärel sisestage **Üldine** vahekaardil **määramise jaoks** töötaja määramise lubamiseks kuupäeva.

Vahekaardil **Täpsem juurdepääs** saate piirata juurdepääsu teabele või linkidele:

- **Juurdepääsu piiramine töötaja teabele – valige see funktsioon, kui kasutajatel peaks olema võimalik vaadata töötaja teavet ainult nende juriidiliste isikute puhul, kellele neil on juurdepääs, ja töötajate puhul, kelle töö on nendes** juriidilistes isikutes.

    Kui see funktsioon on valitud, järgige neid samme, et seadistada sobivad õigused igale kasutajale, kelle vaade peab olema piiratud:

    1. Valige **kasutaja** lehel kasutaja.
    1. Valige kasutajale roll. Suvand **Organisatsioonide määramine** muutub kättesaadavaks.
    1. Valige **Organisatsioonide määramine**.
    1. Valige uuel leheküljel suvand **Anna juurdepääs konkreetsetele organisatsioonidel** ja seejärel valige organisatsioonid, mille juurdekasutajal peab juurdepääs olema.
    1. Korrake samme 2 kuni 4 iga täiendava rolliga, mis kasutajal on, k.a süsteemi kasutaja roll.

    > [!NOTE]
    > Ettevõtted, kus kasutajal juurdepääs on, peavad ühtima kõigi kasutaja rollidega.

- **Luba ettevõtetevahelise hüvitise vaade** – hüvitus töötajatele määratakse tööle juriidilise isiku kohta. Mõnikord võib töötaja olla tööle võetud korraga mitmesse juriidilisse isikusse. Kui see funktsioon on valitud, kuvatakse hüvitus igale juriidilisele isikule Töötaja iseteeninduses ja juhataja iseteeninduses ilma, et peate **·** **·** juriidilised isikud muutma. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
