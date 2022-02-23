---
title: Maksevahendil põhinevad allahindlused
description: See teema annab ülevaate funktsioonidest, mille abil jaemüüjad konfigureerivad allahindlusi kindlate maksevahenditüüpide jaoks.
author: bebeale
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 9f6747ff9d68c29612346254928e869d6d34d433
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962931"
---
# <a name="tender-based-discounts"></a>Maksevahendil põhinevad allahindlused

[!include [banner](includes/banner.md)]


Jaemüüjate seas on levinud tava anda välja kaubamärgiga tähistatud erakrediitkaarte. Jaemüüjad saavad kasu seetõttu, et nad saavad pankadelt soodusmäärasid. Lisaks, kuna need krediitkaardid võivad julgustada kliente kauplust sagedamini külastama, aitavad need suurendada jaemüüja käivet. Seetõttu on jaemüüjatel stiimul suurendada oma kaubamärgiga krediitkaartide kasutust klientide seas. Selle eesmärgi saavutamiseks pakuvad nad sageli täiendavaid allahindlusi klientidele, kes kasutavad neid krediitkaarte.

Teise võimalusena võivad jaemüüjad, kes ei paku marginimega krediitkaarte, julgustada kliente maksma, kasutades muid maksevahenditüüpe, nt sularaha, kinkekaarte või püsikliendipunkte. Sel viisil võivad nad aidata vähendada krediitkaardi töötlemistasude kulu. Seetõttu võivad jaemüüjad pakkuda allahindlusi klientidele, kes kasutavad neid alternatiivseid maksevahenditüüpe.

Rakenduses Microsoft Dynamics 365 Commerce saavad jaemüüjad konfigureerida allahindlusprotsendi, mida rakendatakse kvalifitseeruvatele ridadele, kui klient maksab eelistatud maksevahenditüübi abil. Klient saab otsustada, kas teha osaline makse või täielik makse, ja rakendus Commerce määrab sobiva allahindluse summa. Arvestage, et allahindlus antakse alati kvalifitseeruvate kaupade maksueelse summa kohta.

Maksevahendil põhinevad allahindlused ei konkureeri kaubal põhinevate allahindlustega, nt perioodiliste või käsitsi tehtavate allahindlustega. Need lisatakse alati kaubal põhinevatele allahindlustele. Seega, isegi kui kaubale rakendatakse eksklusiivset perioodilist allahindlust, rakendatakse maksevahendil põhinevat allahindlust siiski eksklusiivsele perioodilisele allahindlusele lisaks. Samuti, kui kandele rakendatakse läve allahindlust ja maksevahendil põhinev allahindlus vähendab kogusumma lävest allapoole, rakendatakse kandele endiselt läve allahindlust.

Kuigi maksevahendil põhinevad allahindlused vähendavad kande vahesummat, ei mõjuta see kandele rakendatud automaatseid tasusid. Näiteks kui tarne tasu arvutatakse 5 €, kuna vahesumma oli suurem kui 100 €, ja maksevahendil põhinev allahindlus vähendab summat nii, et see on väiksem kui 100 €, on tellimuse tarnetasud endiselt 5 €.


> [!NOTE]
> Maksevahendil põhinevad allahindlused jaotatakse proportsionaalselt kvalifitseeruvate müügiridade peale ja need vähendavad üksikute ridade maksueelset summat. Kui maksevahendi tüübi (nt sularaha) jaoks on konfigureeritud mitu maksevahendil põhinevat allahindlust, rakendatakse ainult parimat maksevahendil põhinevat allahindlust.

Maksevahendil põhinevaid allahindlusi saab rakendada ainult nende müügiridade puhul, mille hinnad ei ole lukus. Kui tellimusele lisatakse uued müügiread, rakendatakse maksevahendil põhinevat allahindlust uutele müügiridadele ainult makse ajal. Klienditellimuse esitamisel komplekteerimiseks või saadetise saatmiseks rakendatakse maksevahendil põhinevat allahindlust ainult deposiitsummale. Pärast tellimuse esitamist ehk täitmise ajal on müügiridade hinnad lukus. Seetõttu ei rakendata ühtegi maksevahendil põhinevat allahindlust ühelegi saldole, mis tasutakse vastuvõtul või autoriseeritakse saadetise saatmisel. Maksevahendil põhinevat allahindlust saab rakendada klienditellimuse kogusummale ainult juhul, kui jaemüüja võtab tellimuse esitamisel kogusumma deposiidina.

> [!IMPORTANT]
> Rakenduses Commerce on maksevahendil põhinevad allahindlused praegu piiratud kahe maksetüübiga: krediitkaardid ja sularaha.

## <a name="pos-user-experience"></a>Kassa kasutamine

Kui maksevahendil põhinev allahindlus on seadistatud sularaha jaoks ja kassas olev kassiir valib tasulise sularahas tasumise toiminguga vastendatud nupu, rakendatakse maksevahendil põhinevat allahindlust kandele automaatselt. Seejärel kuvatakse vähendatud summa saldona. Kuid juhul, kui kassapidaja valib maksekuval nupu **Tagasi**, eemaldatakse allahindlus ja kandekuval näidatakse algsummat. Maksevahendil põhinev allahindlus eemaldatakse, kui tühistada makse rida.

Kaardimaksete puhul saavad jaemüüjad seadistada maksevahendil põhineva allahindluse ühele või enamale krediitkaarditüübile. Süsteem ei saa siiski kontrollida, millist tüüpi krediitkaarti kasutatakse, kui kaarti pole autoriseeritud. Kui allahindlus rakendatakse pärast autoriseerimist, autoriseeritakse makse suurema summa jaoks, kuid makse hõivamine tehakse väiksema summa jaoks.

Selle olukorra vältimiseks näeb kassapidaja kliendi kaardimakse korral dialoogiboksi, kus on loetletud krediitkaardid, mis võimaldavad kliendil rohkem säästa. Seejärel saab kassapidaja küsida, kas klient soovib kasutada ühte eelistatud kaartidest, et saada lisaallahindlust. Kui kassapidaja kasutab eelistatud kaarti, rakendatakse kandele maksevahendil põhinevat allahindlust ja maksekuval näidatakse vähendatud summat. Autoriseerimine tehakse vähendatud summa jaoks. Kui klient sisestab kaardi, mis erineb kassapidaja valitud kaardist, kuvatakse veateade ja autoriseerimine tühistatakse.


## <a name="call-center-user-experience"></a>Kõnekeskuse kasutamine

Kui kasutaja teeb kõnekeskuse tellimuse jooksul valiku **Vii lõpule**, kuvatakse **Kogusummad**. Alguses ei sisalda selle kuva kogusummad maksevahendil põhinevaid allahindlusi, kuna makseviisi pole veel valitud. Kui kasutaja valib kuval **Lisa makse** makseviisi, mille puhul maksevahendil põhinev allahindlus on konfigureeritud, korrigeeritakse maksesummat automaatselt nii, et see kajastab allahindlusega summat. Nagu kassas olev klientki, saab kõnekeskuse klient otsustada, kas tasuda täielik makse või osaline makse. Makstud summa põhjal rakendatakse maksevahendil põhinev allahindlus müügitellimusele.

> [!NOTE]
> Kaarti kõnekeskuse tellimuste puhul ei kinnitata. Näiteks kui kõnekeskuse kasutaja valib krediitkaardiks Visa, kuid klient kasutab Mastercardi, rakendab süsteem ikka allahindlust.

## <a name="exclude-items-from-discounts"></a>Kaupade välistamine allahindlustest

Jaemüüjad jätavad tihti mõned tooted, nagu uued kaubad või nõutud kaubad, allahindlustest välja. Siiski võivad nad soovida rakendada maksevahendil põhinevaid allahindlusi. Näiteks saab jaemüüja rakenduse Commerce konfigureerida nii, et see ei luba kaubal põhinevaid allahindlusi ega käsitsi tehtavaid allahindlusi. Samas juhul, kui klient maksab eelistatud maksevahendi abil, rakendab Commerce siiski maksevahendil põhineva allahindluse. Rakenduse Commerce sellisel viisil seadistamiseks peavad jaemüüjad avama **Tooteteabe haldus > Tooted > Väljastatud tooted**, valima kauba ja seejärel kiirkaardil **Kaubandus** määrama suvandid **Kõigi allahindluste ennetamine** ja **Maksevahendil põhinevate allahindluste ennetamine** valikule **Ei** ning suvandid **Allahindluste ennetamine** ja **Käsitsi määratud allahindluste ennetamine** valikule **Jah**.

> [!NOTE]
> Kui konfiguratsioon **Kõigi allahindluste ennetamine** on seatud valikule **Jah**, ei rakendata tootele ühtki allahindlust. Ei rakendata isegi maksevahendil põhinevaid allahindlusi.
