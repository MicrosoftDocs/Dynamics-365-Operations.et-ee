---
title: Kolmanda osapoole rakenduste manustamine
description: See artikkel selgitab, kuidas manustada kolmanda osapoole rakendusi toote funktsionaalsuse suurendamiseks.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef5ed6c3c99d62010643940f3e2f158963ff0dc2
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123714"
---
# <a name="embed-third-party-apps"></a>Kolmanda osapoole rakenduste manustamine

[!include [banner](../includes/banner.md)]

Paljud kliendid kasutavad oma äritegevuses mitmesuguseid rakendusi. Mõned neist rakendustest on kolmanda osapoole veebirakendused, mis töötavad koos finantside ja toimingute rakendustega. Sujuvama kasutajakogemuse võimaldamiseks saate kasutada täieliku lehekülje rakenduste funktsiooni, et manustada need kolmanda osapoole rakendused otse oma finantsidesse ja toimingute rakendustesse (eeldusel, **et** kolmanda osapoole rakendused lubavad end manustatud olla). Sel viisil pääsevad kasutajad ligi veebisaitidele ja rakendustele, mida nad vajavad ilma, et nad vahetaks vahekaarte või aknaid.

Enne kui saate kolmanda osapoole rakendused tootele manustada, peate funktsioonihalduses lülitama sisse funktsiooni **Täieliku lehekülje rakenduste** funktsioonihalduse. Seejärel saate kasutada üht järgmistest meetoditest, et manustada kolmanda osapoole rakendus või veebisait. Need meetodid on analoogsed meetoditele, mida kasutatakse lõuendi rakenduste kaasamiseks Microsoft Power Apps finantside ja toimingute rakendustesse.

- Manustage rakendus või veebisait olemasoleval lehel uue vahekaardina (liigendtabel, kiirkaart, rakendus või tööruumi jaotis).
- Looge uus täislehe kasutuskogemus töölauarakenduse või veebisaidi jaoks.

## <a name="embed-a-website-on-an-existing-page"></a>Veebisaidi manustamine olemasolevale leheküljele

Kasutage seda protseduuri, kui soovite täiendada süsteemi olemasolevat lehekülge manustatud rakendusega.

1. Avage leht, kus soovite rakenduse manustada.
2. Avage paan **Lisa rakendus**:

    1. Valige suvand **Seaded** ja seejärel **Isikupärastamine**, et avada tööriistariba **Isikupärastamine**.
    2. Valige **Veel \> Lisa rakendus**.

3. Valige piirkond lehel, kuhu soovite rakendust lisada. See regioon peab olema *vahekaardi konteiner* ristkaardi, kiirkaardi, tööruumi või tööruumi sektsiooni jaoks.
4. Valige **veebisait**.
5. Manustatud rakenduse konfigureerimine.

    - **Nimi** – sisestage tekst, mis tuleks kuvada manustatud rakendust sisaldaval vahekaardil. Sageli soovite, et selleks tekstiks oleks rakenduse nimi.
    - **URL** – määrake rakenduse asukoht.

    > [!IMPORTANT]
    > - Turvalisuse tagamiseks peab URL kasutama Hypertext Transfer Protocol Secure'i (HTTPS).
    > - Rakendus või veebisait peab olema konfigureeritud nii, et see lubaks end manustada.

6. Valige **Salvesta**, et lehele rakendus manustada. Rakendus lisatakse grupi viimase vahekaardi või jaotisena.
7. Kinnitage, et rakendust kuvatakse nii, nagu sooviti. Kui rakendust ei renderdata, vaadake selles artiklis [jaotist](#troubleshooting) Tõrkeotsingu.
8. Avage vaatevalija ja valige suvand **Salvesta** (kui rakendus tuleks seostada praeguse vaatega) või **Salvesta nimega** (rakenduse salvestamiseks erineva vaate juurde).

    Kui lehel ei ole vaatevalijat (nt kui lehekülg on dialoogiboks või tööruum), võite selle sammu vahele jätta.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Manusta veebisait armatuurlauda täislehekogemusena

Kasutage seda protseduuri, kui rakendus, mida soovite manustada ei ole seotud olemasoleva lehega või kui soovite rakenduse jaoks ainult tervet lehekülge kogemust finantside ja toimingute rakenduses.

1. Avage armatuurlaud.
2. Valige ja hoidke lehte all (või paremklõpsake) armatuurlaual, valige **Isikupärastamine** ja seejärel valige **Lisa lehekülg**.
3. Klõpsake paani **Lisa leht** valikul **Veebileht**.
4. Manustatud rakenduse konfigureerimine.

    - **Nimi** – sisestage tekst, mis tuleks kuvada armatuurlauda manustatud rakenduse jaoks lisatud paanil. Sageli soovite, et selleks tekstiks oleks rakenduse nimi.
    - **URL** – määrake rakenduse asukoht.

    > [!IMPORTANT]
    > - Turvalisuse tagamiseks peab URL kasutama HTTPS-i.
    > - Rakendus või veebisait peab olema konfigureeritud nii, et see lubaks end manustada.

5. Valige **Salvestamine**, et lisada rakendus armatuurlauale uue paanina.
6. Valige armatuurlaual uus paan ja veenduge, et rakendust kuvatakse nii, nagu oodatud. Kui rakendust renderdatakse, vaadake selles artiklis [hiljem](#troubleshooting) jaotist Tõrkeotsingu.

## <a name="sharing-embedded-apps"></a>Manustatud rakenduste ühiskasutusse andmine

Pärast rakenduse manustatud kasutamist, kasutades ühte eelmistes jaotistes kirjeldatud meetodit, võite soovida vaadet teiste süsteemi kasutajatega jagada. Manustatud rakenduse jagamiseks kasutage ühte järgmistest meetoditest.

- **Avaldage vaade (soovitatav):** kui manustatud rakendus on vaatesse salvestatud, on soovitatav ja eelistatud viis seda jagada, et avaldada vaade kasutajatele, kellel on sihitud juriidilistes isikutes asjakohased turberollid. Sel juhul näevad selle lehe manustatud rakendust ainult soovitud kasutajad. Lisateavet vaate avaldamise kohta vt jaotisest [Vaadete avaldamine](saved-views.md#publishing-views).

    Saate avaldada ka rakenduse, mis on armatuurlaualt täislehe kogemusena manustatud. Valige ja hoidke armatuurlaual (või paremklõpsake) rakendusega seotud paanil, valige **isikupärastamine** ja seejärel valige **Avalda leht**. Kuvatakse selline kogemus, mis sarnaneb *avaldamisvaadete* kogemusega ja te saate valida turvarollid, mida avaldada. Kui **täiustatud juriidilise isiku tugi salvestatud vaadete** funktsiooni jaoks on sisse lülitatud, saate värskenduses 10.0.21 või hiljem avaldada rakenduses soovitud juriidilistele isikutele.

- **Isikupärastamise kopeerimine:** lehtedel, mis ei toeta vaateid (nt dialoogiboksid või tööruumid) või kogu lehe rakendusekogemuse jaoks saate isikupärastamise kopeerida vastavale kasutajale. Lisateavet leiad artiklist [Isikupärastamiste jagamine](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Manustatud rakenduste kuvamine

Manustatud rakenduse vaatamiseks lehel finantside ja toimingute rakendustes avage manustatud rakendusega lehekülg. Pidage meeles, et mõndadel lehtedel on rakendustele võimalik juurde pääseda standardsel toimingupaanil asuva nupu **Power Apps** kaudu. Teise võimalusena võidakse need kuvada otse lehel uue vahekaardi, kiirkaardi või labana või tööruumis uue jaotisena.

## <a name="editing-or-removing-embedded-apps"></a>Manustatud rakenduste redigeerimine või eemaldamine

Kui rakendus on lehele manustatud võib juhtuda, et peate redigeerima selle konfiguratsiooni (nt muutes sektsiooni silti või URL-i). Võimalik, et peate selle leheküljelt eemaldama. Manustatud rakenduse konfiguratsiooni redigeerimiseks või selle täielikult eemaldamiseks kasutage ühte järgmistest protseduuridest.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Olemasolevatele lehtedele manustatud rakendused

1. Avage leht, kuhu rakendus on manustatud.
2. Valige suvand **Seaded** ja seejärel **Isikupärastamine**, et avada tööriistariba **Isikupärastamine**.
3. Valige **valimistööriist** ja seejärel valige manustatud rakendus.
4. Rakenduse redigeerimiseks tehke konfiguratsioonis vajalikud muudatused ja valige käsk **Salvesta**.

    Teise võimalusena rakenduse eemaldamiseks valige **Kustuta**.

5. Salvestage vaade uuesti või avaldage see uuesti. Pange tähele, et kui lahkute lehelt ilma vaadet eraldi salvestamata, ei säilitata ühtki **veebisaidi redigeerimise** paanil tehtud tegevust.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Armatuurlaualt manustatud rakendused

1. Avage armatuurlaud.
2. Valige ja hoidke (või paremklõpsake) manustatud rakendusega seotud paanil, ja seejärel valige **isikupärastamine**.
3. Rakenduse redigeerimiseks valige **Lehe redigeerimine**. Tehke paanil **Veebilehe redigeerimine** vajalikud muudatused rakenduse konfiguratsioonis ning valige seejärel suvand **Salvesta**.

    Teise võimalusena rakenduse eemaldamiseks valige **Eemalda leht**.

## <a name="appendix"></a>Lisa

### <a name="troubleshooting"></a>Tõrkeotsing

Kui veebisaiti ei renderdata õigesti pärast seda, kui see on manustatud finantsi ja toimingu rakendusse või kui saate tõrketeate, mis takistab URL-i ühenduse keelamist, on veebisait tõenäoliselt konfigureeritud nii, et see ei satud iframe'i. Järgige neid samme, et määrata, kas veebisaiti saab manustada.

1. Avage arendaja tööriistad brauseri jaoks, mida kasutate.
2. Vahekaardil **Võrk** valige manustatud saidilt vastus.
3. Otsige vahekaardil **Päised** jaotises **Vastuse päised** **x-raami** valikuid. Kui **x-raami valikud** on vastusepäistes olemas ja nende väärtus on **DENY** või **SAMEORIGIN**, ei saa veebisaiti hetkel manustada. Peate tegema rakenduse omanikuga koostööd, et seda saaks turvaliselt manustada.

### <a name="developer-modeling-a-website-on-a-form"></a>[Arendaja] Veebilehe modelleerimine vormil

Kuigi see artikkel keskendub isikupärastamise kaudu kolmanda osapoole rakenduste või veebisaitide kaasamiseks, Visual Studio saavad arendajad neid vormile manustada, kasutades arenduskogemust. Lihtsalt lisage vormile **WebsiteHostControli** juhtelement. Juhtelemendil saadaolevad metaandmete atribuudid pakuvad samu võimalusi nagu isikupärastamise kogemuski.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

