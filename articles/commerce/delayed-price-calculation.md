---
title: Viivituse täpne hinna ja allahindluse arvutamine täiustatud jõudlusele
description: See teema kirjeldab hilinenud hinnakalkulatsiooni võimalust, mis on saadaval Microsoft Dynamics 365 Commerce kassas (POS) ja kõnekeskuses.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8c4264c3a4c71e6aab0e1ef8d7d8cfffad065a46
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488359"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Viivituse täpne hinna ja allahindluse arvutamine täiustatud jõudlusele

[!include [banner](includes/banner.md)]

See teema kirjeldab hilinenud hinnakalkulatsiooni võimalust, mis on saadaval Microsoft Dynamics 365 Commerce kassas (POS) ja kõnekeskuses.

Dynamics 365 Commerce toetab mitmerealise allahindluste loomist, mis rakendatakse mitme müügitellimuse või müügipakkumise müügirea kombineerimisel. Need allahindlused hõlmavad segamist ja sobitamist, läve ja koguse allahindlusi.

Iga kord, kui tellimusele lisatakse uus rida, hindab Commerce'i hinnakujunduse mootor kogu ostukorvi, et määrata, kas neid multiallahindlusi saab rakendada. Selle ümberarvutamise tõttu võib uute ridade lisamine müügitellimuse kasvul mõjutada jõudlust.

Ettevõtetevahelistel (B2B) ja mõndadel ettevõttelt tarbijale (B2C) ettevõtetel on sageli suured tellimuste suurused. Seetõttu võib olla aeganõudev oodata, kuni hinnakujundusmootor pärast iga kauba ostukorvi lisamist uuesti arvutatakse. Lisaks pole suurte tellimuste puhul tavaliselt väga oluline näidata täpset hinda ja allahindlust iga kord, kui kaup ostukorvi lisatakse. On olulisem, et kasutajad saaksid kaupu kiiresti lisada. Täpne hinna ja allahindluse arvutamise edasilükkamine seni, kuni kasutaja seda või tellimust taotleb, võib oluliselt parandada jõudlust. See võib ka vähendada tellimuse lõpetamiseks vaja minevat aega.

Täpne hinna ja allahindluse arvutamise edasilükkamine on kassas juba pikalt olnud. Äriversiooni 10.0.22 vabastamisel on see saadaval ka kõnekeskuse jaoks.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Viivitusega hinna ja allahindluse arvutamise lubamine kassa puhul

Viivitusega hinna ja allahindluse arvutamise lubamiseks kassa puhul, järgige neid samme.

1. Avage Commerce'i peakontoris funktsionaalsusprofiil, mis on seotud füüsilise poega.
1. Lubage kiirkaardil **Summa** **Mitme kauba allahindluse käsitsi arvutamine** konfiguratsioon.
1. Avage ekraani paigutuse kujundaja kassaaparaatide jaoks, kus viivitusega arvutus peaks olema lubatud.
1. Lisage nupp **Kogusumma arvutamine** toimingu jaoks soovitud nupupaneeli.
1. Käivitage tööd **1070** ja **1090**.

Nüüd, Kui kaubad lisatakse kandesse, siis multiallahindlusi ei arvutata, välja arvatud juhul, kui kassapidaja valib nupu **Arvuta summa**. Kui kande jaoks on valitud **Arvuta kogusumma**, arvutatakse selle kohta alati multiallahindlused. Kassapidaja ei pea nuppu uuesti valima, isegi kui ostukorvi lisatakse täiendavaid kaupu. Süsteem ei luba kassapidajal makset hõivata enne, kui **Arvuta kogusumma** on valitud.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Viivitusega hinna ja allahindluse arvutamise lubamine kõnekeskuse puhul

Viivitusega hinna ja allahindluse arvutamise lubamiseks kõnekeskuse puhul, järgige neid samme.

1. Avage Commerce'i peakontoris jaotis **Tööruumid \> Funktsioonide haldamine**.
1. Lubage **Soovimatu hinnakalkulatsioon äritellimuse jaoks** funktsioon. See funktsioon on viivitusega hinna ja allahindluse arvutamise võimaluse eeltingimus.

    > [!NOTE]
    > Uute juurutuste puhul on **Äritellimuse soovimatu hinna arvutamise ennetamine** funktsioon vaikimisi lubatud.

1. Minge **Commerce'i parameetritesse \> Hinnad ja allahindlused**.
1. Jaotises **Mitmesugused** lubage **Mitmerealiste hindade ja allahindluste käsitsi arvutamine** konfiguratsioon.

Kui kõnekeskuses luuakse või redigeeritakse müügitellimust või müügipakkumist, siis täpse hinna ja allahindluse arvutamine selle jaoks lükatakse edasi. Hinnakujunduse mootor võtab arvesse ainult müügirida, mis on lisatud või redigeeritud, ja ignoreerib kõiki teisi müügiridu. Kauba netosumma hõlmab hinnakalkulatsiooni ja lihtsaid allahindlusi (allahindluse protsent või üksiku kauba summa maha). Segamise ja sobitamise, läve ja koguse allahindlusi siiski ei rakendata. Kõnekeskuse kasutajad, kes soovivad vaadata täpset hinda, sh kõiki allahindlusi, saavad valida ühe kolmest nupust: **Arvuta uuesti**, **Kogusummad** või **Lõpeta**.

> [!NOTE]
> Kõnekeskuse tellimuste puhul näitab süsteem hoiatusteadet, mis tuletab kasutajale meelde, et täpse hinna ja allahindluse arvutamiseks tuleb valida nupp **Arvuta uuesti**, **Summad** või **Lõpetatud**. Tellimustel, mille on nupp **Lõpetatud** saadaval, puudub kõnekeskuse kasutajal võimalus täpse hinna ja allahindluse arvutuse vahele jätta, kuna tellimuse hõivamiseks tuleb valida **Vii lõpule**. Tellimuste puhul, mille puhul nupp **Lõpetatud** pole saadaval, puudub toiming, mis näitaks tellimuse hõivamise lõpuleviimist. Seetõttu vastutab kõnekeskuse kasutaja selle eest, et enne tellimuse hõivamise lõpule viimist valite väljad **Arvuta uuesti** või **Summad**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
