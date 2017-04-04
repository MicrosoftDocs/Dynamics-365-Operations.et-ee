---
title: "Küsimustiku laialisaatmine ja täitmine"
description: "See teema selgitab, kuidas levivad küsimustikud, kujundada, nii, et nad on isik või grupp inimesi, kes täidab neid."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Küsimustiku laialisaatmine ja täitmine

See teema selgitab, kuidas levivad küsimustikud, kujundada, nii, et nad on isik või grupp inimesi, kes täidab neid. 

Küsimustiku laialisaatmiseks on mitu võimalust.

-   Saate märkida küsimustiku aktiivseks. Küsimustik on siis saadaval kõigile töötajatele, kui küsimusegrupile pole määratud piiratud juurdepääsu.
-   Saate määrata õigused küsimustike grupile. Küsimustik on siis saadaval valitud grupi liikmetele.
-   Saate luua plaanitud vastamissessioone. Küsimustik on siis saadaval ainult kindlale isikule.
-   Saate luua graafiku. Küsimustik võib siis olla saadaval mitmele inimesele.

## <a name="marking-a-questionnaire-as-active"></a>Küsimustiku aktiivseks märkimine
Seadmisega ning **aktiivne** välja **Jah** kohta on **küsimustikud** leht, teete küsimustik saadaval kõigi töötajate lõpuleviimiseks. Vastanutest saab küsimustikku mitu korda. See funktsioon on kasulik, kui soovite koguda kogu aasta vältel pidevat tagasisidet. Näiteks võite koostada küsimustiku, mille kaudu töötajad saavad anda kohviku lõunateenuse kohta tagasisidet.

## <a name="questionnaire-groups"></a>Küsimustikugrupid
Saate seadistada küsimustikugrupid ja lisada sinna siis vastavad, kellele küsimustik tuleks saata. 

Saate luua küsimustikugruppe järgmistelt lehtedelt.

-   **Küsimustikugrupid **– valitud küsimustikku saavad täita ainult küsimustikugrupis olevad inimesed. Näiteks on teie sihtrühm töövõtjad, seega koostate neile vastajatele mõeldud küsimustikugrupi.
-   **Küsimustikugrupi liikmed** – saate lisada küsimustikugruppidesse inimesi.

Et määrata küsimustiku grupi küsimustikule, on **küsimustikud** klõpsake valikul **kasutajaõiguste**. Pärast seda, kui küsimustik on salvestatud aktiivseks, küsimustiku rühma liikmed saab täita küsimustiku. See funktsioon on kasulik, kui soovite testida küsimustik on grupile enne seda vδlja suuremasse rühma või kui soovite küsimustiku väga kindlale sihtrühmale suunatud.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Plaanitud vastamisseansid küsimustiku kohta
Plaanitud vastamisseansid on küsimustikud, mille olete kavandanud ja millele vastajad valinud. 

**Märkus.** Enne plaanitud vastamisseansside seadistamist tuleb kavandada küsimustik. 

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

Kasutage lehte **Viitetüübid** küsimustiku viitetüüpide seadistamiseks. Iga viitetüübi vastab tabeli Microsoft Dynamics 365 toiminguteks. Küsimustikugraafikute loomisel saate määrata eraldi tabelikirjeid või kirjete vahemikku, millega küsimustik seostatakse. 

Näiteks kui valite tabeli Kursused, saate määrata, millise konkreetse kursuse jaoks küsimustik on mõeldud. Kui seadistate viite kursuse tabelile, muutuvad mõned väljad ja nupud väljal **Kursused** kättesaadavaks.

### <a name="questionnaire-schedules"></a>Küsimustiku graafikud

Saate luua viitetüübi põhinev kasutajate rühma mitu planeeritud vastamisseansside küsimustiku sõiduplaanid. Luua ajakava ning **küsimustiku sõiduplaanide** lehel. Valige planeerimistüübi kategoriseerida ajakava ja valida võib kasutada päringu süsteemi spetsiifilistele viitetüübi. Näiteks kui seate kursused tabeli viitetüüpi, valige konkreetse kursuse ning **viide** välja. 

Klõpsake valikut **Seadistuse üksikasjad** küsimustiku ja muude kriteeriumide valimiseks. Näiteks määrata juhendaja nimega kriteeriumina, kui küsimustik on juhendaja hinnangut. Kui olete lõpetanud setup andmete sisestamine, loob süsteem planeeritud vastamisseansside kasutajatele, kes on kaasatud päring. 

Klõpsake valikut **Plaanitud vastusesessioonid** graafiku vastusesessioonide vaatamiseks. Seejärel saate luua käsitsi täiendavaid plaanitud vastamisseansse või vastusteta plaanitud vastuseseansse kustutada. 

Klõpsake **funktsioonid**&gt;**alustada** võimaldamiseks küsimustik kasutajatele seotud planeeritud vastamisseansse. Klõpsake valikut **Vastused** küsimustiku täidetud vastuste vaatamiseks. Soovi korral saate kopeerida küsimustiku graafiku sätteid, plaanitud vastamisseansse ja vastuseid uue küsimustiku graafikusse.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Vastajate teavitamine neile saadaolevatest küsimustikest
Kui küsimustiku laiali saadate, peate vastajatele teatama, et küsimustikud on neile kättesaadavad. 

**Märkus:** vastanutest peavad olema kasutajatele Microsoft Dynamics 365 operatsioonide küsimustiku täitmist.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Vastajate teavitamine plaanitud vastamissessioonist

Kui kasutate plaanitud vastamisseanssi, peate teavitama inimest otse (nt telefoni või meili teel).

### <a name="notifying-respondents-about-a-scheduling"></a>Vastajate teavitamine plaanimisest

Lehel **Küsimustikugraafikud** saate ette valmistada ja saata meilid kõigile vastajatele, kellele küsimustik on määratud. Sisestage meili tekst vahekaardile **Meil töötaja iseteeninduse jaoks**. Pärast ajakava, klõpsake **funktsioonid**&gt;**saata e-posti** luua ja saata e-posti vastanutest. Vastanutest saate siis veebisaidile sisse logida ja küsimustikku. 

**Märkus.** Enne, kui saate meilifunktsiooni kasutada, peab teie IT-administraator sisestama meilisätted lehele **Meiliparameetrid**.

## <a name="ending-a-scheduled-questionnaire"></a>Plaanitud küsimustiku lõpetamine
Plaanitud küsimustiku saate lõpetada pärast seda, kui kõik vastajad on neile määratud vastuseseansid sooritanud. Pärast plaanitud küsimustiku lõpetamist ei saa selle sätteid uude graafikusse kopeerida. 

**Märkus.** Kui vähemalt üks vastaja pole küsimustikku täitnud, kuid soovite siiski plaanimise lõpetada, peate esmalt kustutama need vastajad loendist lehel **Plaanitud vastamissessioon**. Seejärel saate graafiku lõpetada.

## <a name="completing-questionnaires"></a>Küsimustike täitmine
Pärast küsimustiku kavandamist ja laiali saatmist saavad valitud vastajad selle täita. Saate täita küsimustikud, mis on saadaval kahes kohas:

-   Navigeerimispaanil klõpsake **küsimustikud**&gt;**hajuta**&gt;**küsimustiku täitmist,**.
-   Klõpsake töötaja iseteeninduses valikut **Täidetavad küsimustikud**.

Küsimustikud saab teha kättesaadavaks kindlatele kasutajatele või kasutajagruppidele või kõigile kasutajatele võrgus.

<a name="see-also"></a>Vt ka
--------

[Küsimustike kavandamine](design-questionnaires.md)

[Küsimustike kasutamine](questionnaires.md)

[Küsimustike tulemuste vaatamiseks ja](evaluate-questionnaire-results.md)


