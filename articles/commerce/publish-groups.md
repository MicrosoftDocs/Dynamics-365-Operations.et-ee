---
title: Avaldamisrühmadega töötamine
description: Selles teemas kirjeldatakse avaldamisrühmade funktsiooni teenuses Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0a4f19af0cdf9c72add0ec18be84e36c807af9ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969872"
---
# <a name="work-with-publish-groups"></a>Avaldamisrühmadega töötamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse avaldamisrühmade funktsiooni teenuses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

E-kaubanduse veebisaite uuendatakse pidevalt uue sisuga kogu aasta jooksul. Uuendused avaldatakse sageli partiidena kiirete e-kaubanduse sündmuste ajal, nagu pühad, hooajalised turunduskampaaniad või kampaania käivitamine. Need uuendused nõuavad sageli, et veebisaitide sisu rümad (näiteks lehed, pildid, fragmendid ja mallid) oleksid ettevalmistatud, kontrollitud ja avaldatud samaaegselt ühe tegevusega.

Üksuste koos avaldamiseks üksuste loogilistesse kogumitesse rühmitamise võimalus, kus igal kogumil on oma elutsükkel, pakub saidi autoritele palju eeliseid. Commerce’is on need loogilised kogumid tuntud kui avaldamisrühmad. Nad võimaldavad saidi autoritel jälgida uuenduste kogumeid oma konfigureeritavate, testitavate ja avaldatavate üksustena.

Autorid saavad kuvada ettevalmistatud avaldamisrühma uuenduste eelvaate ilma reaalajas saiti ega teisi iseseisvaid avaldamisrühmi mõjutamata. Autorid saavad seejärel ajastada avaldamistoimingu, et avaldada üheaegselt kõik avaldamisrühma üksused reaalajas saidil. Avaldamiseks mõeldud uuenduste rühmitamine, eelvaate kuvamine ja ajastamine on oluline paljudele suurettevõtte tasemel ettevõtetele, mis saavad märkimisväärse iga-aastase tulu ettevõttepõhiste saidi uuenduste vahe-eesmärkide ajal.

Aeglane või kehtetuks muutunud sisu avaldamised, mis ei kulge sujuvalt, võivad tuua ettevõttele kaasa kulutusi. Avaldamisrühmad aitavad tagada, et käivitamised on korraldatud, kontrollitud ja õigeaegselt avaldatud. Kas need on suured või väikesed, avaldamisrühmad pakuvad väärtuslikku tööriistakogumit, mis aitab autoritel korraldada ja lihtsustada jooksvaid saidi uuendamise ülesandeid.

## <a name="when-to-use-publish-groups"></a>Millal avaldamisrühmasid kasutada?

Saate kasutada avaldamisrühmasid, kui peate valmistama ette ja avaldama mitu dokumenti koos. Näiteks kui teie veebisait uuendab sisu igal hooajal, saate luua avaldamisrühmad nende hooajaliste turundusliigutuste jaoks. Teie avaldamisrühm „Sügise hooajalise uuendus” avaldamine võib sisaldada uusi hooajalisi pilte, hooajaliste turundussõnumitega fragmente, hooajaliste toodete kollektsioone sisaldavaid lehti ja teisi hooajalisi veebisaidi värskendusi.

Avaldamisrühmade eeliseks on, et saate paralleelselt valmistada ette mitu uuendust. Näiteks varsti pärast uuendust avaldamisrühmale „Sügise hooajaline uuendus” võib peagi järgneda konkreetse püha nädalavahetuse uuendus. Sel juhul saate avaldamisrühma „Sügise hooajaline uuendus” sisu valmistada ette samal ajal, kui valmistate ette järgnevat avaldamisrühma „Sügispuhkuse uuendus” Iga avaldamisrühm sisaldab oma ainulaadset lehtede, piltide, fragmentide, mallide jne komplekti. Saate valmistada ette, kuvada eelvaade ja kinnitada need kaks avaldamisrühma sõltumatult, kuid samal aja jooksul. Seejärel saab ajastada iga avaldamisrühma avaldamine teie saidil konkreetsetel kuupäevadel ja kellaaegadel.

## <a name="turn-on-the-publish-groups-feature"></a>Avaldamisrühmade funktsiooni sisselülitamine

Avaldamisrühmade funktsioon on valikuline ja see tuleb saidi jaoks sisse lülitada.

Commerce’i autorluse tööriistades oma saidi avaldamisrühmade funktsiooni sisselülitamiseks toimige järgmiselt.

1. Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.
1. Jaotises **Saidi sätted** valige suvand **Funktsioonid**.
1. Seadke valik **Avaldamisrühmad** väärtusele **Sees**.

## <a name="create-a-publish-group"></a>Avaldamisrühma loomine

Commerce’i autorluse tööriistades ma saidi jaoks avaldamisrühma loomiseks toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanilt suvand **Avaldamisrühmad**.
1. Valige ülemisel käsuribal suvand **Uus**.
1. Dialoogiboksi **Avaldamisrühma loomine** jaotises **Avaldamisrühma nimi** sisestage kirjeldav nimi. Seejärel valige **OK**.

## <a name="set-the-publish-group-authoring-context"></a>Avaldamisrühma autorluse konteksti seadmine

Commerce’is on vaikimisi autorluse kontekst reaalajas saidi kontekst. Reaalajas saidi autorluse kontekst on vaikevaade, kus saate vaadata ja teha muudatusi otse oma veebisaidil, ilma avaldamisrühma kasutamata. See näitab teie saidi avaldatud versiooni värskeimaid otseseid uuendusi. Kui konteksti juhtelemendil vasakpoolse navigeerimispaani jaotises **Avaldamiserühmad** kuvatakse saidi nimi **Reaalajas sait**, töötate reaalajas saidi autorluse kontekstis. **Reaalajas sait** on konteksti juhtelemendi vaikenimi. Vastasel juhul kuvab konteksti juhtelement avaldamisrühma nime.

Avaldamisrühmas töötamiseks peate lülituma selleks avaldamisrühma autorluse konteksti. Avaldamisrühma konteksti määramiseks järgige ühte järgmistest sammudest.

- Vasakpoolsel navigeerimispaanil valige konteksti juhtelement otse suvandist **Avaldamisrühmad** ja valige seejärel kuvatavas valikute loendis avaldamisrühma nimi. Konteksti juhtelement nimetatakse ümber ja see kuvab avaldamisrühma nime.
- Valige vasakpoolsel navigeerimispaanil suvand **Avaldamisrühmad** ja seejärel jaotises **Avaldamisrühmad** valige avaldamisrühma nimi. Konteksti juhtelement nimetatakse ümber ja see kuvab avaldamisrühma nime.

Pärast avaldamisrühma autorluse konteksti määramist töötate selles avaldamisrühma kontekstis, kui kuvate eelvaate ja redigeerite saidi sisu.

Vaikimisi reaalajas saidi autorluse konteksti naasmiseks valige konteksti juhtelement ja valige seejärel **Reaalajas sait**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Avaldamisrühma lehtede ja teiste üksuste lisamine

Pärast avaldamisrühma autorluse konteksti valimist ja konteksti juhtelement vasakpoolsel navigatsioonipaanil kuvab selle nime, saate luua sisu samamoodi, nagu vaikimisi reaalajas saidi kontekstis. Saate lisada ka olemasolevaid lehti või teisi üksusi teistelt avaldamisrühmadest või reaalajas saidi kontekstist.

Olemasolevate lehtede avaldamisrühma kopeerimiseks toimige järgmiselt.

1. Valige autorluse kontekst, kust kopeerida, ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Lehed**.
1. Valige leht avaldamisrühma lisamiseks.
1. Valige käsuribal käsk **Kopeeri avaldamisrühma**.
1. Valige dialoogiboksis **Avaldamisrühma valimine** avaldamisrühm, millele leht lisada, ja seejärel valige **OK**.

Saate kasutada samu põhisamme, et luua kohandatud tootelehti, URL-e, malle, paigutusi, fragmente ja meediumiteegi ressursse, või lisada seda tüübi avaldamisrühmadesse olemasolevaid üksuseid.

## <a name="validate-a-publish-group"></a>Avaldamisrühma valideerimine

Kindlustamaks, et kõik sõltuvused avaldamisrühma sisus oleksid täidetud ja et kõik valideerimised oleksid läbitud, saate käitada valideerimise, et tuvastada mis tahes probleemid, mis tuleb enne avaldamistoimingu ajastamist lahendada.

Avaldamisrühma valideerimiseks enne selle ajastamist tehke järgmist.

1. Valige vasakpoolsel navigeerimispaanilt suvand **Avaldamisrühmad**.
1. Valige valideerimiseks avaldamisrühm.
1. Valige ülemisel käsuribal suvand **Valideeri**.

Valideerimine käitatakse avaldamisrühma kogu sisul. Kõik probleemid, mis takistavad edukat avaldamistoimingut, näidatakse üleval paremal kuvatavas teavitusaknas.

> [!NOTE]
> Valideerimine käitatakse alati automaatselt, kui avaldamisrühm ajastatakse. Samas on nupp **Kinnita** käsuribal kasulik, kuna see aitab tuvastada probleemid, mille peate enne avaldamisrühma avaldamise ajastamise proovimist lahendama.

## <a name="schedule-a-publish-group-to-go-live"></a>Avaldamisrühma avaldamise ajastamine

Oma saidil avaldamisrühma avaldamise ajastamiseks tehke järgmist.

1. Valige vasakpoolsel navigeerimispaanilt suvand **Avaldamisrühmad**.
1. Valige jaotises **Avaldamisrühmad** ajastamiseks avaldamisrühm.
1. Valige ülemisel käsuribal suvand **Graafiku redigeerimine**. Ilmub dialoogiboks **Graafiku redigeerimine**.
1. Valige kuupäev ja kellaaeg, millal avaldamisrühm peaks avaldatama, ja valige seejärel **OK**.

Avaldamisrühma graafikust eemaldamiseks järgige samu etappe, kuid valige käsk **Eemalda avaldamisrühm ajakavast** dialoogiboksis **Ajakava redigeerimine**.

> [!NOTE]
> Väga suurtel avaldamiserühmadel võib kuluda üks kuni kaks minutit, et need planeeritud aja kättejõudmisel avaldataks. Arvestage, et avaldamistoiming ei ole hetkeline ja väiksemad avaldamisrühmad avaldatakse kiiremini.

## <a name="publish-groups-faq"></a>Avaldamisrühmade KKK

**Mitu üksust võib avaldamisrühmas olla?**

Praegu on piir 2000 üksust avaldamisrühma kohta. Arvestage, et väga suurtel avaldamiserühmadel võib kuluda kuni mitu minutit, et need planeeritud aja kättejõudmisel avaldataks.

**Kas avaldamisrühmad on tarkvaraarenduse terminoloogias nagu koodi nn harud?**

Jah ja ei. Avaldamisrühmi võib vaadelda kui teie saidi haralisi versioone. Sel viisil käituvad need nagu harud. Samas üksikute üksuste tasandil liitumise konseptsioon puudub. Viimati avaldatud üksus lihtsalt kirjutab üle varem eksisteerinu ja kõige viimane avaldamistoiming alati alistab eelmised avaldamistoimingud.

**Kas ma saan planeerida kahe avaldamisrühma avaldamise samal ajal?**

Ei. Jõudluse ja konflikti tõttu sunnib süsteem teid jätma kahe avaldamisrühma vahele vähemalt viis minutit aega.

**Kas ma saan kasutada avaldamisrühmi, et ajasada omnikanali arveldusüksuseid, nagu allahindlused ja toote uuendused?**

Praegu toetab avaldamisrühmade funktsioon ainult veebisaidi sisu. Kuid Microsoft on teadlik, et kontorikaupade stsenaariumitega integreerimine võib olla väärtuslik omnikanali kampaania käivitamiste koordineerimiseks ja automatiseerimiseks.

## <a name="additional-resources"></a>Lisaressursid

[Sisu lisamise viisid](add-manage-content.md)

[Lehemudeli sõnastik](page-elements-overview.md)

[Dokumendi olekud ja töötsükkel](document-states-overview.md)

[Kanaliülese ühiskasutuse lubamine ja kasutamine](cross-channel-sharing.md)

[Moodulitega töötamine](work-with-modules.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Saidil navigeerimise kohandamine](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]