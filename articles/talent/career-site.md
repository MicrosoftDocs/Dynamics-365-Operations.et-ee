---
title: Rakenduse Attract karjäärisaidi funktsionaalsus
description: See teema annab ülevaate kandidaatidele suunatud karjäärisaidi funktsionaalsusest rakenduses Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/13/2019
ms.locfileid: "389958"
---
# <a name="career-site-functionality-in-attract"></a>Rakenduse Attract karjäärisaidi funktsionaalsus

[!include[banner](../includes/banner.md)]

See teema annab ülevaate kandidaatidele suunatud karjäärisaidi funktsionaalsusest rakenduses Dynamics 365 for Talent: Attract. Samuti selgitatakse, kuidas seda funktsionaalsust seadistada.

Attract annab rentniku igale keskkonnale ühe karjäärisaidi. Näiteks kui organisatsioonil on arenduskeskkond ja katsekeskkond, eraldatakse üks karjäärisait arenduskeskkonnale ja teine karjäärisait katsekeskkonnale. Iga karjäärisait on täiesti isoleeritud ja oma autentimismehhanismiga. Ühiseid töid ja kandidaatide profiile karjäärisaitidel pole.

Vaikimisi on karjäärisaidid avalikud. Kandidaadid saavad seetõttu vaadata kõiki väliseks märgitud töökohti ilma sisse logimata. Kõigi muude toimingute jaoks aga peavad kandidaadid sisse logima.

## <a name="career-site-management"></a>Karjäärisaidi haldus

Alljärgnevate üksuste väärtuste määramiseks logige administraatorina rakendusse Attract sisse, valige menüüst **Sätted** (hammasratta kujutis) suvand **Halduskeskus** ja seejärel valige vahekaart **Ettevõtte andmed**.

-   **Organisatsiooni nimi** – organisatsiooni nimi kuvatakse karjäärisaidi ülaosas oleval navigeerimisribal. Organisatsiooni nime valimise korral avaneb kandidaatidele leht, kus on toodud kõik vabad töökohad.

-   **Organisatsiooni logo** – karjäärisaidi ülemises vasakus servas kuvatakse organisatsiooni logo kujutist. Logo kujutise valimise korral avaneb kandidaatidele leht, kus on toodud kõik vabad töökohad.

    >   [!NOTE] 
    >   Karjäärisaidil kuvatava logo kujutise fikseeritud kõrgus on 20 pikslit (px). Halduskeskuse kaudu lisatud pildi suurus muudetakse sobivaks. Olenevalt kujutisest võib laius seetõttu muutuda.
 
Alljärgnevate üksuste väärtuste määramiseks logige administraatorina rakendusse Attract sisse, valige menüüst **Sätted** suvand **Halduskeskus** ja seejärel valige vahekaart **Karjäärisaidi haldus**.

-   **Otsingumootori optimeerimine** – kui see on lubatud, on kõik rakenduse Attract karjäärisaidile sisestatud avalikud töökohad leitavad otsingumootoritega, nagu Bing ja Google.

    >   [!NOTE] 
    >   Selle sätte sisselülitamise ja otsingutulemite ilmumise vahel võib olla viivitus, mis oleneb kasutatavast otsingumootorist.
         
## <a name="career-site-urls"></a>Karjäärisaidi URL-id

Alljärgnev loend sisaldab tavaliselt kasutatavaid karjäärisaitide URL-e ja teavet, kuidas neile juurde pääsed.

-   **Karjäärisaidi avalehe URL** – karjäärisaidi avalehe URL-i vaatamiseks logige rakendusse Attract sisse administraatorina, valige menüüst **Sätted** suvand **Halduskeskus** ja seejärel valige vahekaart **Karjäärisaidi haldus**.

-   **Üksiku töökuulutuse kandideerimise URL** – kui [sisestate välise töökoha](Creating-jobs-Attract.md#postings) esmakordselt, võite rakendusest Attract kopeerida lingi **Kandideeri**. Selle lingi URL on järgmises vormingus: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Üksiku töökuulutuse URL** – töökuulutusee URL on kandideerimise URL-i alamstring. See sisaldab kõike kuni töökoha numbrini. Seetõttu on eelneva kandideerimise URL-i töökuulutuse URL [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Autentimisvõimalused

Kandidaatidel on rakenduse Attract karjäärisaidile sisselogimiseks järgmised võimalused:

-   isiklik konto:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   töö- või koolikonto:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD-ga sisselogimine on mõeldud ainult sisekandidaatidele. Seetõttu toimib see ainult sisekandidaatidega, kes kasutavad oma ettevõtte Azure AD identimisteavet. Näiteks kandidaat, kes on hetkel ettevõtte Contoso Ltd töötaja, soovib kandideerida sellega mitteseotud ettevõtte Alpine Ski House töökohale. Sellisel juhul sisselogimine ei õnnestu, kui töövõtja üritab kasutada ettevõtte Contoso Ltd Azure AD identimisteavet.

## <a name="create-and-maintain-a-profile"></a>Profiili loomine ja haldamine

Pärast karjäärisaidile sisselogimist saavad kandidaadid lehe ülaosas olevalt navigeerimisribalt oma profiili loomiseks ja haldamiseks kasutada valikut **Minu profiil**.
Profiil sisaldab isikuandmeid, andmeid töökogemuse kohta, haridusandmeid, dokumente, linke ja andmeid oskuste kohta. Pärast profiili loomist saab seda kasutada kandidaadile huvi pakkuvatele töökohtadele kandideerimiseks. Samuti aitavad profiilid rakendusel Attract kandidaatidele õigeid töökohti soovitada.

>   [!NOTE]
>   Kui kandidaat kasutab ühe ülevalpool nimetatud autentimisteenuse pakkuja abil sisselogimiseks meili ID-d, määratakse see meili ID vaikimisi profiiliga seotud kontaktmeili ID-ks. Viimast saab aga igal ajal muuta ja see on esimesest täiesti sõltumatu. Attract kasutab kogu meilisuhtluse jaoks alati kontaktmeili ID sidumist teie profiiliga.

## <a name="find-the-right-job"></a>Õige töökoha leidmine

Töökohtade loendi lehel saavad kandidaadid otsingusõnu sisestades otsida kindlat töökohta. Otsingufunktsioon otsib otsingusõnu ametinimetustest ja töökirjeldustest ning kuvab asjakohased töökohad tulemitena. Kandidaadid saavad tulemusi igal ajal töökoha asukoha või tööfunktsiooni alusel filtreerida.

Samuti saavad kandidaadid karjäärisaidil vaadata soovitatud töökohti. Kandidaatidele soovitatavad töökohad põhinevad kandidaadi varasematel kandideerimistel, profiilil ja elulookirjeldustel.

>   [!NOTE] 
>   Soovitatavad töökohad kuvatakse ainult siis, kui karjäärisaidile on sisestatud vähemalt 10 töökohta ja kandidaat on täitnud oma profiili lõpuni.

## <a name="apply-for-jobs"></a>Töökohtadele kandideerimine

Kui kandidaat leiab õige töökoha, saab ta kandideerida lehe **Töö üksikasjad** nupu **Kandideeri** abil. Sellel hetkel saavad kandidaadid luua kas uue profiili või vaadata üle oma olemasoleva profiili andmed.
Samuti saavad kandidaadid vajaduse korral üles laadida elulookirjelduse ja seejärel esitada avalduse töökohale kandideerimiseks.

## <a name="check-application-status"></a>Avalduse oleku kontrollimine

Pärast ühele või mitmele töökohale kandideerimist saavad kandidaadid oma avatud ja suletud avaldusi vaadata lehe ülaosas oleva navigeerimisriba valiku **Avaldused** kaudu. Kui kandidaadid avavad ühe oma avaldustest, näevad nad hetkeseisu ja mistahes ootel olevat tegevust, mille nad peavad teostama. Näiteks, kui kandidaat peab välja pakkuma võimalikud kuupäevad silmast silma vestluseks, kuvatakse lehel võimaliku valikud.

## <a name="internal-jobs"></a>Organisatsioonisisesed töökohad

Hetkel ei kuvata karjäärisaidil organisatsioonisiseseks märgitud ja rakenduse Attract karjäärisaidile sisestatud töökohti. Need on juurdepääsetavad ainult otsese URL-i **Kandideeri** kaudu, mida saab kopeerida rakendusest Attract.
