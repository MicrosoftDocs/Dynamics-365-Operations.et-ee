---
title: Dynamics 365 Commerce e-äri lokaliseerimise juhend
description: See teema kirjeldab, kuidas lokaliseerida Microsoft Dynamics 365 Commerce e-äri saiti lisakeeltesse ja konfigureerida saiti mitme kanali toetamiseks.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661502"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce e-äri lokaliseerimise juhend

[!include [banner](includes/banner.md)]

See teema kirjeldab Microsoft Dynamics 365 Commerce, kuidas lokaliseerida e-äri saiti lisakeeltesse ja konfigureerida sait toetama mitut kanalit, ning käsitleb ka protsessiga seotud mõisteid ja terminoloogiat.

E-kaubanduse Dynamics 365 Commerce võimalused on loodud selleks, et võimaldada veebikogemusi, mida saab kohandada kindlate riikide ja keelte järgi, kuid võimaldades samal ajal mallide, lehekülgede, sisu ja meedia maksimaalset taaskasutust. Saate luua ka põhisaidi ja seejärel laiendada uutele turustele, lisades aja jooksul toe täiendavatele riikidele ja keeltele.

## <a name="definitions"></a>Definitsioonid

**Lokaadi ID**: lokaadiks (nimetatakse ka lokaadiks) määratletakse riigi või regiooniga seostatud keel. Näiteks lokaadi identifikaator "fr-ca" on seotud Kanada prantsuse identifikaatoriga.

**Põhikeel**: keel, mis töötate oma saidi sisu välja enne lokaliseerimise eksportimist.

**Kanal, võrgupood**: kanal (tuntud ka kui võrgupood) määratleb makseviisid, hinnagrupid, tootehierarhiad, sortimendid ja tooted võrgu e-äri kaupluses.

## <a name="concepts"></a>Mõisted

### <a name="url-driven-experience"></a>URL-iga juhitav kogemus

Dynamics 365 Commerce e-ärisaidid annavad klientide jaoks kordumatuid turustatud ja lokaliseeritud kogemust kanalite ja lokaadi identifikaatorite kaudu. Kanalid määratlevad turu jaoks kordumatud tooted, kategooriad, valuutad ja makseviisid ning lokaadi ID-d määravad klientide nähava sisu keele. E-pood kasutab URL-e turustatud ja lokaliseeritud kogemuste eristamiseks. Nende kordumatute kanali ja lokaadikogemuste saidi URL-id määratletakse **\>** saidi jaoks saidisätete kanalite lehel saidikonstruktoris.Dynamics 365 Commerce

Saidikonstruktoris on URL domeeni ja tee kombinatsioon, mis määratleb sisenemiskoha kanali ja lokaadi kordumatu kombinatsiooni jaoks. Järgmises näites on fiktiivne e-pood Fabrikam Inc. määratleb kanali ja lokaadi neli kordumatut kombinatsiooni ning vastendab iga kombinatsiooni kordumatu URL-iga, mis teenib klientidele sisu.

| Domeen                     |  Tee      | Kanal       |   Lokaat     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Laiendatud Fabrikami e-pood | et  |
| `https://fabrikam.com` | /es    | Laiendatud Fabrikami e-pood | es     |
| `https://fabrikam.ca`  | /      | Contoso e-pood    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso e-pood    | en-ca  |

#### <a name="domain"></a>Domeen

Domeenid luuakse siis, kui seadistate oma e-äri saidi Microsoft Dynamics elutsükli teenustes (LCS). Kui teie e-äri keskkond on ette ettevalmistamine, saate lisada rohkem domeene, avades teenustaotluse. Lisateavet selle kohta, kuidas seadistada oma e-äri saidi domeene, vt domeene [jaotisest Domeenid Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Tee

- Tee on nimeline string, mis koos domeeniga on vastendatud kanali ja lokaadi kordumatu kombinatsiooniga. Eelmises näites on teena kasutatav string vastavuses lokaadi ID-ga, mille jaoks tee on vastendatud. Siiski saate kasutada erinevat lähenemist.
- Kanali ja lokaadi kombinatsiooni saab vastendada domeeniga ja tühja teega ("/"). Eelnevas näites saavad külastavad kliendid `https://fabrikam.ca/` tooteid ja sortimente Kanada turu jaoks Kanada prantsuse keeles.
- Ärisaidi koostaja takistab domeeni ja tee topeltkombinatsioonide loomist. Kuid te saate vastendada kanali ja lokaadi duplikaatkombinatsioone domeeni ja tee erineva kombinatsiooniga.

#### <a name="channel"></a>Kanal

- Kanalid (tuntud ka kui e-poed) määratlevad makseviisid, hinnagrupid, tootehierarhiad, sortimendid ja tooted e-kaubanduses.
- Kanalid on määratletud, konfigureeritud ja peakontoris avaldatud Dynamics 365 Commerce.
- Saidikonstruktur saab tuvastada e-poode, mis on konfigureeritud Commerce Headquartersis ja on saadaval vastendamiseks saidiga.

Lisateavet kanalite kohta vt kanalite [ülevaatest](channels-overview.md). Lisateavet võrgukanali häälestamise kohta vt häälestage [võrgukanal](channel-setup-online.md).

#### <a name="locale"></a>Lokaat

- Lokaadiks on tegelik identifikaator, mida kasutatakse XML-i lokalisatsiooni vahetuse failivormingu (XLIFF) failide lokaliseerimiseks väljastamisel. Locales määratakse ja avaldatakse igas kanalis Commerce Headquartersis. Lisateavet keelte ja kanalite konfigureerimise kohta saidikonstruktoris vt järgmisest jaotisest.
- Sama lokaadi saab vastendada mitme kanaliga. Sel viisil saab ühtseid keeli pakkuda mitmes turus.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Konfigureerige oma e-äri saidi keeli ja kanaleid

Karbist sõltumata on kõik e-äri saidid konfigureeritud kasutama ühte võrgukanalit ja ühte keelt, sõltumata sellest, Dynamics 365 Commerce kas alustate Fabrikami demosaidiga või loote nullist uue saidi.

Selles konfiguratsioonis arendavad kliendid ja partnerid tavaliselt välja kõik varad, mida kasutatakse kõigis riikides ja keeltes. Need varad hõlmavad malle, lehti, killusteid, sisu ja meediat. Kogu saidi sisu töötatakse välja oma saidi jaoks valitud esimeses keeles või kui kasutate Fabrikami demosaidi, töötatakse saidi sisu välja inglise keeles.

![Boksist väljas Dynamics 365 Commerce e-kaubanduse sait](media/loc-guide-1.png)

> [!NOTE]
> Saate Fabrikami demosaidi konfigureerida lisakeeleks, nii et sisu arendust saab selles keeles teha. Lisateavet selle kohta, kuidas saidile ja kanalile uut keelt lisada, [vaadake jaotisest Konfigureeri](#configure-an-additional-language-for-your-site) saidi jaoks lisakeel hiljem selles teemas.

Kuid e-kaubanduse saitide sisu haldussüsteem (CMS) Dynamics 365 Commerce ja lehekülje mudel on mõeldud laienduse võimaldamiseks uutesse turgudesse ja lokaadile. Seega saate üksiku e-kaubanduse saidi kaudu hallata põhivarasid võrgupoes, mis hõlmab mitut turust ja keelt.

![Dynamics 365 Commerce e-kaubanduse sait, mis hõlmab mitut turu ja keelt](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Konfigureerige oma saidile lisakeel

E-kaubanduse saidi jaoks uue keele konfigureerimisel on kolm sammu.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>1. etapp: lisage keel oma kanalile (võrgupoes) Commerce headquartersis

1. Minge Commerce Headquartersi kanalisse, millele soovite uut keelt lisada. Rakenduse Commerce headquarterss konfigureeritud kanalite loendi leidmiseks minge jaemüügi ja ärikanalite **võrgupoodidesse \>\>**.
1. Avage oma saidiga vastendatud võrgupood, valides selle jaemüügikanali **ID** väärtuse. Saate kontrollida oma saidiga vastendatud võrgupoodi, **avades** kanalite saidi sätte lehe Commerce'i saidi koostajas ja vaadates võrgupoe nime kanalite **veerus**. 
1. Valige kiirkaardil **Keeled** käsk **Lisa**. **Valige väljal** Keel uue keele lokaadikood. Seejärel valige nupp **Salvesta**.
1. Minge jaemüügi ja rakenduse Commerce **Retail ja Commerce IT jaotusgraafikusse \>\> ja käitage töö** 1070 kanali konfiguratsioon **.** Kui töö on töö lõpetanud, saate liikuda sammu 2 ja lisada keele oma saidi kanalile saidiloojas.

![E-poe keelte kiirkaart Commerce Headquartersis](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>2. etapp: keele lisamine saidikonstruktori kanalile

Keele lisamiseks saidikonstruktori kanalile järgige neid samme.

1. Ärisaidi koostajas avage sait ja seejärel avage kanalite **lehekülg** saidi sätetes.
1. Valige kanali nimi, millele soovite keelt lisada.
1. Valige parempoolsel paanil **suvand Lisa lokaadiks**.
1. Valige dialoogiboksi **Lokaadi lisamine** jaotises Lokaadi lisamine keele lokaadiks, **mille** eelnevalt Commerce headquartersi kanalisse lisasite.
1. Valige domeen ja tee, mida kliendid taotlevad teie saidi vaatamiseks selles kanalis ja keeles.
1. Kui soovite, et keel oleks saidikonstruktori lehtede ja tükilehtede vaatamiseks, loomiseks ja värskendamiseks vaikekeel, **märkige** ruut Kasuta vaikimisi autorikanali keelena. 
    > [!NOTE]
    > Säte mõjutab ainult saidikonstruktorit. See ei mõjuta avaldatud saidi kogemust teie klientide puhul.
1. Valige nupp **OK**.
1. Valige suvand **Salvesta ja avalda**.

#### <a name="step-3-localize-your-site-content"></a>3. etapp: saidi sisu lokaliseerimine

Kui naasete **Commerce'i** saidi koostaja lehtede vaatesse, on uus keel saadaval kanali ja lokaadi valija ülemisel paremal. Nüüd saate luua oma põhikeeles lokaliseeritud lehekülgede versioone.

Lehtede ja killukondade sisu lokaliseerimise protsess on teema teemas teemas ["Lokaliseeri e-kaubanduse saidi](#localize-e-commerce-site-content) sisu jaotis".

### <a name="configure-a-new-channel-for-your-site"></a>Uue kanali konfigureerimine oma saidile

Dynamics 365 Commerce e-commerce'i saitidel võivad olla kogemused, mis on määratud erinevates võrgukanalites, mis on konfigureeritud Commerce Headquartersis. Sait kasutab mitut kanalit, et näidata klientidele makseviiside, hinnagruppide, tootehierarhiate, sortimentide ja toodete komplekti kordumatut konfiguratsiooni. Kanalit kasutatakse tavaliselt nende dimensioonide konfigureerimiseks nii, et need vastaksid iga riigiga seotud kogemuse vajadustele ja eelistustele. See lähenemine on siiski kliendi tehtud äriotsus. See pole nõue.

Kanali (e-poe) seadistamisega seotud eeltingimused ja ülesanded on selle dokumendi ulatusest väljaspool. Lisateavet võrgukanali seadistamise kohta rakendusse Commerce Headquarters vaadake kanali häälestamise [põhiseadistusest](channels-overview.md#channel-setup-basics). Lisateavet võrgukanalitele omaste sammude ja nõuete kohta vt [võrgukanali häälestamist](channel-setup-online.md).

Saidikonstruktoris kanali lisamiseks järgige neid samme.

1. Minge Ärisaidi koostajas saidi sätete **kanalitesse \>**. 
1. Valige **suvand Lisa kanal**.
1. **Kanali lisamiseks valige** dialoogiboksi Lisa kanal **jaotisest** Kanal. 
    > [!NOTE]
    > Saate lisada vaid kanaleid, mida pole veel teie saidile lisatud.
1. Valige kanali vaikeasu koht. Kui lisate kanalile uusi keeli, saate muuta vaikekeelt ühele neist.
1. Määratlege domeen ja tee, mis moodustab URL-i, mis teenib selle kanali ja keele kombinatsiooni sisu ja kogemused.
1. Valige nupp **OK**.
1. Valige suvand **Salvesta ja avalda**.

## <a name="localize-e-commerce-site-content"></a>e-ärisaidi sisu lokaliseerimine

### <a name="xliff-basics"></a>XLIFF-põhised

XLIFF on tööstusstandardne failivorming lokaliseeritava sisu edastamiseks sisuhalduse tööriistade vahel. Ärisaidi koostaja kasutab XLIFF-failivormingut lehe, killu ja pildi metaandmete sisu eksportimiseks, et seda saaks lokaliseerida ja uuesti importida.

Microsoft Dynamics Kliendid töötavad tavaliselt koos kolmandate osapoolte lokaliseeritud [hankijategaTranslated.com](https://translated.com/welcome) et tõlkida oma XLIFF-failid ksi, mida nad vajavad.

### <a name="localize-assets-in-site-builder"></a>Varade lokaliseerimine saidikonstruktoris

Järgmisi e-äri saidi varasid saab saidikonstruktoris lokaliseerida:

- Lehed
- Fragmendid
- Meedia varad
- Moodulid

Kanali ja keele kontekstis luuakse kõik uued lehed, killud ja meediumivarad, mis on praegu kanalis ja lokaadil valitud. See keel on tavaliselt teie "põhikeel", eeldusel, et te pole konfigureerinud täiendavaid keeli või kanaleid. Saitidel, kus on konfigureeritud mitu kanalit ja keelt, on **põhikeel** määratud kanali ja lokaadiga, mille olete määranud vaikimisi saidi kanalite lehel.

Lehekülgede, killude ja meediavarade sisu lokaliseerimise sammud on sarnased. Erandeid ja erinevusi näidatakse järgnevates jaotistes. Kuid mooduli sisu lokaliseerimise sammud erinevad. Lisateavet vt selle teema jaotisest [Lokaliseeri](#localize-modules) moodulid.

#### <a name="step-1-export-an-xliff-file"></a>1. etapp: XLIFF-faili eksportimine

XLIFF-faili eksportimiseks leheküljele, killusta või pildina saidikonstruktoris, järgige neid samme.

1. Avage vara, mille põhikeele sisu soovite eksportida, nii et seda saab lokaliseerida.
1. Käsuribal valige lokaliseerimise ekspordi **\> XLIFF**.
    > [!NOTE]
    > Lokaliseerimisvalik **on** nähtav ainult siis, kui vara on olekus **Redigeeri**.

XLIFF-fail nimega **\<assetname\>.xlf** laaditakse alla teie brauseri allalaadimiskausta. See XLIFF-fail on omane varale, mida lokaliseerite. XLIFF-fail eksporditakse iga vara puhul, mida soovite lokaliseerida.

#### <a name="step-2-localize-the-xliff-file"></a>2. etapp: XLIFF-faili lokaliseerimine

Enamasti töötate koos lokaliseeritud hankijaga oma XLIFF-failide tõlkimiseks. Kuid kui lokaliseerite varad ettevõttesiseselt või kui soovite lihtsalt lokaliseerimisprotsessi testida, peate XLIFF-faili tegema järgmised muudatused:

- Lisage elemendile /xliff/file sihtkeele atribuut ja seadke väärtus lokaliseeritud keele lokaadile ID-le. 
    > [!NOTE]
    > See lokaadi identifikaator peab saidi sätetes kanalite lehe lokaadi **identifikaatoriga** kattuma.
- Lisage igale //allika elemendile sihtelemendi õed, kus tekstiväärtus on selle lähteelemendi sisu lokaliseeritud versioon.

Teavet XLIFF-faile juhiva skeemi kohta vt [XLIFF 1.2 täpsustust](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Vara lokaliseerimiseks mitmesse keelde peate iga keele jaoks looma lokaliseeritud XLIFF-faili.

#### <a name="step-3-import-the-localized-xliff-file"></a>3. etapp: lokaliseeritud XLIFF-faili importimine

Vara XLIFF-faili importimiseks järgige neid samme.

1. Commerce'i saidi koostajas avage vara, mille jaoks soovite importida XLIFF-faili.
1. Valige parempoolses kanalis ja lokaadil kanal ja keel, mille jaoks soovite lokaliseeritud sisu importida.
1. Käsuribal valige lokaliseerimise impordi **\> XLIFF**. Seejärel sirvige ja valige lokaliseeritud XLIFF-fail valitud vara ja keele jaoks.

Pärast XLIFF-faili edukat importimist on loodud lehekülje "variant", tükk või vara. Sellest punktist alates mõjutavad kõik lokaliseeritud variandile tehtud muudatused ainult seda varianti. Need ei mõjuta põhivara, millelt variant tuletati. Samamoodi ei mõjuta põhivara muudatused selle vara varianti. 

Kuid lehekülgede puhul saate variante muuta, muutes malli või paigutust, millega need lehed on seotud. Tüki muutmine mõjutab ka kõiki sellest variandist sõltuvaid lehekülgi.

### <a name="images"></a>Pildid

Pilte saab renderdada lehel või mooduli variandis ainult siis, kui nende piltidega seostatud sisu metaandmed on lokaliseeritud. Praegu on järgmised meedia vara metaandmed lokaliseeritavad:

- Asetekst
- Kirjeldus
- Pealkiri

Praegu ei saa te lokaliseerida digitaalvara kahendväärtust, nt pilti või videot. Tootemeeskond Dynamics 365 Commerce töötab praegu selle võimalusega.

### <a name="localize-modules"></a>Moodulite lokaliseerimine

Stringe, mida renderdatakse osana moodulist (nt "Eelmine" ja "Edasi" carousel moodulis) lokaliseeritakse eraldi mooduli sisust. Juhiseid vt mooduli [lokaliseerimine](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Lehe mudeli sõnastik](page-elements-overview.md)

[Kanaliülene ühiskasutus](cross-channel-sharing.md)

[Mooduli lokaliseerimine](e-commerce-extensibility/localize-module.md)

[Mooduli definitsioonifail](e-commerce-extensibility/module-definition-file.md)

[Commerce'i laiendiressursside ja sildifailide lokaliseerimine](dev-itpro/extension-resource-localization.md)

[Globaliseeri moodulid CultureInfoFormatter klassi abil](e-commerce-extensibility/globalize-modules.md)

[Rakenduse sätted: kujundused](e-commerce-extensibility/app-settings.md#themes-section)
