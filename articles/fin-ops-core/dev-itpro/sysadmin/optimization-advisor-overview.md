---
title: Optimeerimisnõustaja ülevaade
description: See artikkel kirjeldab, kuidas optimeerimise sisu saab kasutada finantside ja toimingute optimaalse konfigureerimise tagamiseks.
author: kamaybac
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: f24e8dfecb04f928994bb5a197d32a7279022512
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281351"
---
# <a name="optimization-advisor-overview"></a>Optimeerimisnõustaja ülevaade

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas optimeerimise sisu saab kasutada finantside ja toimingute optimaalse konfigureerimise tagamiseks.

## <a name="overview"></a>Ülevaade

Mooduli vale konfiguratsioon ja seadistus võivad ebasoodsalt mõjutada rakenduse funktsioonide saadavust, süsteemi jõudlust ja äriprotsesside sujuvat tööd. Äriandmete kvaliteet (nt andmete õigsus, täielikkus ja puhtus) mõjutab ka süsteemi jõudlust ja organisatsiooni otsuste tegemise võimalusi, tootlikkust jne.

Tööruum **Optimeerimise nõustaja** on vahend, mis aitab lauskasutajatel, analüütikutel, funktsionaalsetel konsultantidel ja IT-toe funktsioonidel tuvastada probleeme mooduli konfiguratisoonis ja äriandmetes. Optimeerimise nõustaja soovitab mooduli konfiguratsiooni häid tavasid ja tuvastab aegunud või valed äriandmed.

Optimeerimise nõustaja käitab korrapäraselt hea tava reeglite kogumi. Reeglite vaikekogum on saadaval, kuid kasutajad saavad luua ka nende kohandustele, sõltumatute tarkvaramüüjate (ISVs) lahendustele ja äriandmetele omaseid reegleid. Lisateavet reeglite loomise kohta vt jaotisest [Optimeerimisnõustaja reeglite loomine](./create-rules-optimization-advisor.md).

Kui tuvastatakse reegli rikkumine, luuakse optimeerimisvõimalus, mis ilmub tööruumis **Optimeerimise nõustaja**. Kasutaja saab kasutusele võtta sobiva parandustoimingu otse tööruumis **Optimeerimise nõustaja**.

Võimalused võivad olla ettevõttekohased või ettevõtteülesed, olenevalt seadistuse tüübist ja valideeritavatest andmetest. Ettevõtteüleseid võimalusi saab vaadata kõikides ettevõtetes. Konkreetse ettevõtte võimaluste vaatamiseks peate esmalt valima ettevõtte.

Standardsed turbereeglid kehtivad optimeerimisvõimalustele. Näiteks optimeerimise võimalused, mis on seotud mooduli **Laohaldus** konfiguratsiooniga, on nähtavad ainult kasutajatele, kellel on juurdepääs laohaldusele ja kes saavad selle seadistust muuta.

Kui tegelete optimeerimisvõimalusega, arvutab süsteem võimaluse mõju äriprotsesside käitusaja vähendusena. Kahjuks ei ole see funktsioon saadaval kõikide optimeerimisvõimaluste jaoks.

Lisateavet optimeerimise proovimise kohta vaadake rakenduse [Dynamics 365 Finance video lühikest optimeerimist](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

## <a name="optimization-rules"></a>Optimeerimisreeglid

Optimeerimise nõustaja reeglite täieliku loendi vaatamiseks ja nägemaks, kui tihti reegleid hinnatakse, valige **Süsteemihaldus** &gt; **Perioodilised ülesanded** &gt; **Diagnostika kinnitamise reegli haldamine**. Hinnatakse vaid neid reegleid, mille olek on **Aktiivne**. Hindamise sageduse saab seadistada valikule **Kord päevas**, **Kord nädalas**, **Kord kuus** või **Ajastamata**.

Ajastamata reeglite hindamise käivitamiseks või perioodiliste reeglite hindamiseks väljaspool määratud graafikut valige **Süsteemihaldus** &gt; **Perioodilised ülesanded** &gt; **Diagnostika kinnitamise reegli ajastamine**. Seejärel valige märkeruudus **Diagnostikareeglite kinnitamine** hindamise sagedus. Kõiki reegleid, millel on määratud sagedus, hinnatakse uuesti.

Praeguse optimeerimisreeglite kogumi saab jagada järgmistesse kategooriatesse.

### <a name="module-configuration-and-setup"></a>Mooduli konfigureerimine ja seadistamine

Laohoolduse seadistamine on keeruline protsess. Protsessi lihtsamaks muutmiseks on lisatud mõned reeglid, mis aitavad kinnitada seadistuse õigsust. Näiteks üks reegel valideerib müügitellimuste ja üleviimistellimuste lao tootevariandi fikseeritud asukohtade asukohakorralduste seadistust.

Peale selle kontrollivad mõned reeglid, kas lubatud funktsioone ka tegelikult kasutatakse. Näiteks üks reegel määrab, kas kasutate moodulit **Koondplaneerimine**. Kui reegel määrab, et te ei kasuta moodulit, luuakse optimeerimisvõimalus, mis soovitab teil plaanimisprotsessi välja lülitada.

### <a name="system-configuration"></a>Süsteemi konfiguratsioon

Kui konkreetset funktsiooni, mida juhitakse konfiguratsioonivõtmega, ei kasutata, luuakse optimeerimisvõimalus, mis soovitab teil konfiguratsioonivõtme keelata. Konfiguratsioonivõtme näited on **Tegelik kaal**, **Eelarve plaanimine**, **Projekt** ja **Kinnitatud hankijaloend**.

### <a name="business-data-consistency-and-cleanup"></a>Äriandmete ühtsus ja puhastamine

Kui koondandmed ei ole õiged (näiteks kui teil on mõõtühiku teisendused ühikutele, mida ei ole määratud, või mõõtühiku teisendused nulliga 0 \[null\] jagades), luuakse optimeerimisvõimalus, mis soovitab andmeid parandada. 

Kui teil on liiga palju pakett-töö ajaloo kirjeid, aegunud üksusi, suletud laoseisu kirjeid lao lubatud üksustele jne või kui need kirjed ja üksused on liiga vanad, luuakse optimeerimisvõimalused, mis soovitavad andmeid puhastada. Andmeid puhtana hoides saate aidata parandada süsteemi üldist jõudlust.

### <a name="best-practices"></a>Head tavad

Kui te ei käita mõnda äriprotsessi heade tavade järgi (näiteks käitate varude eelsulgemise enne varude sulgemist või kui kasutate plaanitud partiid alampearaamatu partii ülekandmiseks), teavitavad optimeerimisvõimalused teid heast tavast ja paluvad teil seda järgida.

## <a name="optimization-opportunities"></a>Optimeerimisvõimalused

Optimeerimisreeglite hindamise ajal loodud optimeerimisvõimaluste vaatamiseks avage tööruum **Optimeerimise nõustaja**.

Selles tööruumis saate vaadata rohkem teavet võimaluse kohta, valides suvandi **Lisateave**. Kui soovite, et süsteem tegutseks ja seadistuse parandaks, andmeid puhastaks jne, et te ei peaks vastavaid lehti ise avama, valige suvand **Tee toiming**.

Optimeerimisvõimalustel töövoog puudub. Kui olete valinud suvandi **Tee toiming** või kasutanud navigeerimisteed dialoogikastis **Lisateave**, kaob optimeerimisvõimalus loendist. Kui parandustoiming ei lahenda probleemi täielikult, luuakse võimalus uuesti järgmine kord, kui reeglit hinnatakse.

Kui võimalus ei vasta teie rollile, võite valida suvandi **Peida minu loendist**. Isegi kui selle võimaluse reegel käivitatakse hiljem uuesti, ei näe te võimalust oma loendis.

Konkreetsete reeglite hindamise inaktiveerimiseks valige võimalus, mis reegliga lood, ja seejärel valige suvand **Inaktiveeri analüüs**.

## <a name="additional-resources"></a>Lisaressursid

[Optimeerimisnõustaja reeglite loomine](./create-rules-optimization-advisor.md)

[Optimeerimine rakenduses Dynamics 365 Finance (video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
