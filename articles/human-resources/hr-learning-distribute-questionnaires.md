---
title: Küsimustike jaotamine ja kavandamine
description: See artikkel selgitab, kuidas saata laiali enda kavandatud küsimustikke, nii et need oleksid kättesaadavad inimesele või inimeste grupile, kes neid täidavad.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91b2c94c74fd51765a2545424504149fff1f4bfd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908857"
---
# <a name="distribute-and-schedule-questionnaires"></a>Küsimustike jaotamine ja kavandamine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab, kuidas saata laiali enda kavandatud küsimustikke, nii et need oleksid kättesaadavad inimesele või inimeste grupile, kes neid täidavad. 

Küsimustiku laialisaatmiseks on mitu võimalust.

-   Saate märkida küsimustiku **aktiivseks**. Küsimustik on siis saadaval kõigile töötajatele, kui küsimusegrupile pole määratud piiratud juurdepääsu.
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

> [!NOTE]
> Enne plaanitud vastamisseansside seadistamist peate koostama küsimustiku. 

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

Kasutage lehte **Viitetüübid** küsimustiku viitetüüpide seadistamiseks. Iga viitetüüp vastab tabelile Microsoft Dynamics 365 Finantsid. Küsimustikugraafikute loomisel saate määrata eraldi tabelikirjeid või kirjete vahemikku, millega küsimustik seostatakse. 

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

Lehel **Küsimustikugraafikud** saate ette valmistada ja saata meilid kõigile vastajatele, kellele küsimustik on määratud. Sisestage e-kirja tekst vahekaardile **Töötaja iseteenindus**. Pärast graafiku käivitamist klõpsake suvandil **Funktsioonid** &gt; **saada meilisõnum**, et luua ja saata meil vastajatele. Vastajad saavad siis veebisaidile sisse logida ja küsimustiku täita. 

> [!NOTE]
> Enne meilifunktsiooni kasutamist peab IT-administraator sisestama meiliparameetrite **lehele meilisätted**.

## <a name="ending-a-scheduled-questionnaire"></a>Plaanitud küsimustiku lõpetamine

Plaanitud küsimustiku saate lõpetada pärast seda, kui kõik vastajad on neile määratud vastuseseansid sooritanud. Pärast plaanitud küsimustiku lõpetamist ei saa selle sätteid uude graafikusse kopeerida. 

> [!NOTE]
>   Kui üks või mitu vastajat pole küsimustikku täitnud, kuid soovite siiski ajakava lõpetada, peate esmalt need vastajad loendist lehel **Plaanitud vastamisseanss** kustutama. Seejärel saate graafiku lõpetada.

## <a name="completing-questionnaires"></a>Küsimustike täitmine

Pärast küsimustiku kavandamist ja laiali saatmist saavad valitud vastajad selle täita. Saate täita küsimustikud, mis on saadaval kahes kohas:

-   Klõpsake navigeerimispaanil valikuid **Küsimustikud** &gt; **Laialisaatmine** &gt; **Küsimustiku täitmine**.
-   Klõpsake töötaja iseteeninduses valikut **Täidetavad küsimustikud**.

Küsimustikud saab teha kättesaadavaks kindlatele kasutajatele või kasutajagruppidele või kõigile kasutajatele võrgus.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
