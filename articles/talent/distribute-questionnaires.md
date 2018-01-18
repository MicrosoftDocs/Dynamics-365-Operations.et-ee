---
title: "Küsimustiku laialisaatmine ja täitmine"
description: "See teema selgitab, kuidas saata laiali enda kavandatud küsimustikke, nii et need oleksid kättesaadavad inimesele või inimeste grupile, kes neid täidavad."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 97003c6e90db1fe1335deff65efe6b5ef07ae24b
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a>Küsimustiku laialisaatmine ja täitmine

[!include[banner](includes/banner.md)]


See teema selgitab, kuidas saata laiali enda kavandatud küsimustikke, nii et need oleksid kättesaadavad inimesele või inimeste grupile, kes neid täidavad. 

Küsimustiku laialisaatmiseks on mitu võimalust.

-   Saate märkida küsimustiku aktiivseks. Küsimustik on siis saadaval kõigile töötajatele, kui küsimusegrupile pole määratud piiratud juurdepääsu.
-   Saate määrata õigused küsimustike grupile. Küsimustik on siis saadaval valitud grupi liikmetele.
-   Saate luua plaanitud vastamissessioone. Küsimustik on siis saadaval ainult kindlale isikule.
-   Saate luua graafiku. Küsimustik võib siis olla saadaval mitmele inimesele.

## <a name="marking-a-questionnaire-as-active"></a>Küsimustiku aktiivseks märkimine
Määrates lehel **Küsimustikud** välja **Aktiivne** sätteks **Jah**, teete küsimustiku kõigile töövõtjatele täitmiseks kättesaadavaks. Vastajad võivad täita küsimustikku mitu korda. See funktsioon on abiks, kui soovite koguda terve aasta jooksul pidevat tagasisidet. Näiteks võite koostada küsimustiku, mille kaudu töötajad saavad anda kohviku lõunateenuse kohta tagasisidet.

## <a name="questionnaire-groups"></a>Küsimustikugrupid
Saate seadistada küsimustikugrupid ja lisada sinna siis vastavad, kellele küsimustik tuleks saata. 

Saate luua küsimustikugruppe järgmistelt lehtedelt.

-   **Küsimustikugrupid**– valitud küsimustikku saavad täita ainult küsimustikugrupis olevad inimesed. Näiteks on teie sihtrühm töövõtjad, seega koostate neile vastajatele mõeldud küsimustikugrupi.
-   **Küsimustikugrupi liikmed** – saate lisada küsimustikugruppidesse inimesi.

Küsimustikule küsimustikugrupi määramiseks klõpsake lehel **Küsimustikud** valikut **Kasutajaõigused**. Pärast küsimustiku aktiivsena salvestamist saavad küsimustikugrupi liikmed küsimustiku täita. See funktsioon on abiks, kui soovite testida küsimustikku valitud inimeste grupil, enne kui edastate selle suuremale grupile, või kui soovite suunata küsimustiku väga konkreetsele sihtrühmale.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Plaanitud vastamisseansid küsimustiku kohta
Plaanitud vastamisseansid on küsimustikud, mille olete kavandanud ja millele vastajad valinud. 

> **Märkus.** Enne plaanitud vastamisseansside seadistamist tuleb kavandada küsimustik. 

Lehel **Plaanitud vastamisseanss** saate luua üksiku töötaja jaoks plaanitud vastamisseansi. Lehe loendis kuvatakse kõik kavandatud küsimustikud. 

Plaanitud vastuseseansse kasutatakse ka lehel **Küsimustikugraafikud**, kus saate küsimustikke plaanida mitme inimese jaoks.

-   Töötajad
-   Kursusel osalejad
-   organisatsiooniühikud

Iga inimene saab vastata küsimustikule ainult üks kord.

## <a name="scheduling-a-questionnaire"></a>Küsimustiku plaanimine
Soovi korral saate plaanida küsimustiku mitme vastaja jaoks.

### <a name="planning-types"></a>Planeerimise tüübid

Plaanimise tüübid on vajalikud, kui soovite plaanida vastusesessioonid mitmele vastajale. Plaanimise tüüpe kasutatakse küsimustiku graafikute klassifitseerimiseks. Näiteks võite plaanida küsimustikke järgmistel eesmärkidel.

-   Hindamine
-   Uuring
-   Testimine

Küsimustiku graafiku plaanimise tüüpe saab määrata lehel **Küsimustikugraafikud**.

### <a name="reference-types-for-questionnaire"></a>Küsimustiku viitetüübid

Võite kasutada viitetüüpe vastajate kriteeriumide sisestamiseks, mida saab küsimustiku plaanimisel valida. 

Kasutage lehte **Viitetüübid** küsimustiku viitetüüpide seadistamiseks. Iga viitetüüp vastab Microsoft Dynamics 365 for Finance and Operationsi tabelile. Küsimustikugraafikute loomisel saate määrata eraldi tabelikirjeid või kirjete vahemikku, millega küsimustik seostatakse. 

Näiteks kui valite tabeli Kursused, saate määrata, millise konkreetse kursuse jaoks küsimustik on mõeldud. Kui seadistate viite kursuse tabelile, muutuvad mõned väljad ja nupud väljal **Kursused** kättesaadavaks.

### <a name="questionnaire-schedules"></a>Küsimustiku graafikud

Võite kasutada küsimustikugraafikuid mitme plaanitud vastusesessiooni loomiseks kasutajagrupile viitetüübi põhjal. Looge graafik lehel **Küsimustikugraafikud**. Valige graafiku kategoriseerimiseks plaanimise tüüp ja valige ka viitetüüp, mida tuleb konkreetsete kasutajate puhul süsteemi päringute edastamisel kasutada. Näiteks kui määrate viitetüübiks kursuse tabeli, saate valida konkreetse kursuse väljal **Viide**. 

Klõpsake valikut **Seadistuse üksikasjad** küsimustiku ja muude kriteeriumide valimiseks. Näiteks saate määrata kriteeriumiks juhendaja nime, kui küsimustik on juhendaja hindamiseks. Pärast seadistuse üksikasjade sisestamist loob süsteem päringusse lisatud vastajatele plaanitud vastusesessioonid. 

Klõpsake valikut **Plaanitud vastusesessioonid** graafiku vastusesessioonide vaatamiseks. Seejärel saate luua käsitsi täiendavaid plaanitud vastamisseansse või vastusteta plaanitud vastuseseansse kustutada. 

Klõpsake valikuid **Funktsioonid** &gt; **Käivita**, et teha küsimustik seotud plaanitud vastuseseanssides kasutajatele kättesaadavaks. Klõpsake valikut **Vastused** küsimustiku täidetud vastuste vaatamiseks. Soovi korral saate kopeerida küsimustiku graafiku sätteid, plaanitud vastamisseansse ja vastuseid uue küsimustiku graafikusse.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Vastajate teavitamine neile saadaolevatest küsimustikest
Kui küsimustiku laiali saadate, peate vastajatele teatama, et küsimustikud on neile kättesaadavad. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Vastajate teavitamine plaanitud vastamissessioonist

Kui kasutate plaanitud vastamisseanssi, peate teavitama inimest otse (nt telefoni või meili teel).

### <a name="notifying-respondents-about-a-scheduling"></a>Vastajate teavitamine plaanimisest

Lehel **Küsimustikugraafikud** saate ette valmistada ja saata meilid kõigile vastajatele, kellele küsimustik on määratud. Sisestage meili tekst vahekaardile **Meil töötaja iseteeninduse jaoks**. Pärast graafiku käivitamist klõpsake valikuid **Funktsioonid** &gt; **Saada meilisõnum** meilisõnumi koostamiseks ja vastajatele saatmiseks. Vastajad saavad siis veebisaidile sisse logida ja küsimustiku täita. 

> **Märkus.** Enne, kui saate meilifunktsiooni kasutada, peab teie IT-administraator sisestama meilisätted lehele **Meiliparameetrid**.

## <a name="ending-a-scheduled-questionnaire"></a>Plaanitud küsimustiku lõpetamine
Plaanitud küsimustiku saate lõpetada pärast seda, kui kõik vastajad on neile määratud vastuseseansid sooritanud. Pärast plaanitud küsimustiku lõpetamist ei saa selle sätteid uude graafikusse kopeerida. 

> **Märkus.** Kui vähemalt üks vastaja pole küsimustikku täitnud, kuid soovite siiski plaanimise lõpetada, peate esmalt kustutama need vastajad loendist lehel **Plaanitud vastamissessioon**. Seejärel saate graafiku lõpetada.

## <a name="completing-questionnaires"></a>Küsimustike täitmine
Pärast küsimustiku kavandamist ja laiali saatmist saavad valitud vastajad selle täita. Saate täita küsimustikud, mis on saadaval kahes kohas:

-   Klõpsake navigeerimispaanil valikuid **Küsimustikud** &gt; **Laialisaatmine** &gt; **Küsimustiku täitmine**.
-   Klõpsake töötaja iseteeninduses valikut **Täidetavad küsimustikud**.

Küsimustikud saab teha kättesaadavaks kindlatele kasutajatele või kasutajagruppidele või kõigile kasutajatele võrgus.

<a name="see-also"></a>Vt ka
--------

[Küsimustike kavandamine](design-questionnaires.md)

[Küsimustike kasutamine](questionnaires.md)

[Küsimustike tulemuste vaatamine ja hindamine](evaluate-questionnaire-results.md)



