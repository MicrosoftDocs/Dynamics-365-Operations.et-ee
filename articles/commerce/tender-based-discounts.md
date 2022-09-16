---
title: Maksevahendil põhinevad allahindlused
description: See artikkel kirjeldab maksevahendipõhiseid allahindluse funktsioone, mis võimaldab jaemüüjatel konfigureerida allahindlusi kindlate maksevahendi tüüpide jaoks rakenduses Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473776"
---
# <a name="tender-based-discount"></a>Maksevahendipõhine allahindlus

[!include [banner](includes/banner.md)]

See artikkel kirjeldab maksevahendipõhiseid allahindluse funktsioone, mis võimaldab jaemüüjatel konfigureerida allahindlusi kindlate maksevahendi tüüpide jaoks rakenduses Microsoft Dynamics 365 Commerce.

Jaemüüjate seas on levinud tava anda välja kaubamärgiga tähistatud erakrediitkaarte. Jaemüüjad saavad kasu seetõttu, et nad saavad pankadelt soodusmäärasid. Lisaks, kuna need krediitkaardid võivad julgustada kliente kauplust sagedamini külastama, aitavad need suurendada jaemüüja käivet. Seetõttu on jaemüüjatel stiimul suurendada oma kaubamärgiga krediitkaartide kasutust klientide seas. Selle eesmärgi saavutamiseks pakuvad nad sageli täiendavaid allahindlusi klientidele, kes kasutavad neid krediitkaarte.

Teise võimalusena võivad jaemüüjad, kes ei paku marginimega krediitkaarte, julgustada kliente maksma, kasutades muid maksevahenditüüpe, nt sularaha, kinkekaarte või püsikliendipunkte. Sel viisil võivad nad aidata vähendada krediitkaardi töötlemistasude kulu. Seetõttu võivad jaemüüjad pakkuda allahindlusi klientidele, kes kasutavad neid alternatiivseid maksevahenditüüpe.

## <a name="tender-based-discount"></a>Maksevahendipõhine allahindlus

Commerce toetab maksevahendil *põhinevat* allahindlust, mis võimaldab jaemüüjatel konfigureerida allahindluse protsendi, mida kandele rakendada, kui kande kogusumma ületab teatud summa ja klient maksab, kasutades eelistatud maksetüüpi. Maksevahendipõhine allahindlus on mitmetasandiline, nii et erinevaid allahindlusprotsente saab seostada erinevate summalävedega. Klient saab otsustada, kas teha osaline makse või täielik makse ja hinnakujunduse mootor määrab sobiva allahindluse summa. Maksevahendipõhine allahindlus antakse alati müügiridade maksueelsele summale.

Maksevahendipõhist allahindlust saab rakendada ainult müügiridadele, kus hinnad pole lukustatud ja see on proportsionaalselt jaotatud kvalifitseeritud ridadele. Kui tellimusele lisatakse uued müügiread, rakendatakse maksevahendipõhist allahindlust makse ajal ainult uutele müügiridadele. Kui kliendi tellimus peale võetakse või tarnitakse, rakendatakse maksevahendipõhist allahindlust ainult deposiidisummale. Pärast tellimuse esitamist ehk täitmise ajal on müügiridade hinnad lukus. Maksevahendipõhist allahindlust ei rakendata saldole, mis tasutakse peale võttes või saadetise ajal autoriseeritud. Maksevahendil põhinevat allahindlust saab rakendada klienditellimuse kogusummale ainult juhul, kui jaemüüja võtab tellimuse esitamisel kogusumma deposiidina.

Maksevahendipõhised allahindlused ei võistle kaubapõhiste allahindlustega (nt lihtsad allahindlused, koguse allahindlused, läve allahindlused, segamise ja sobitamise allahindlused ning käsitsi allahindlused). Maksevahendipõhised allahindlused liittakse alati kaubapõhiste allahindlustega. Seega, isegi kui kaubale rakendatakse välistav allahindlus, saab maksevahendipõhist allahindlust siiski rakendada välistav allahindlusele. Samuti, kui kandele rakendatakse läve allahindlust ja maksevahendil põhinev allahindlus vähendab kogusumma lävest allapoole, rakendatakse kandele endiselt läve allahindlust.

Isegi kui maksevahendipõhised allahindlused vähendavad kande vahesummat, ei mõjutata kandele rakendatud automaatseid kulusid. Näiteks kui tarnekulud arvutatakse summana $5, kuna vahesumma oli suurem kui $100 ja maksevahendipõhine allahindlus vähendab summat, et see oleks väiksem kui $100, jäävad tarnekulud $5 tellimusele.

Maksevahendipõhine allahindlus on praegu piiratud kahe maksetüübiga: krediitkaardid ja sularaha. Kui maksevahendil põhinevad allahindlused on maksetüübi jaoks konfigureeritud, rakendatakse ainult parimat maksevahendil põhinevat allahindlust.

## <a name="pos-user-experience"></a>Kassa kasutamine

Kui maksevahendipõhine allahindlus on seadistatud sularaha jaoks ja kassapidaja valib sularahas maksmise nupu sularahas **kannete** tegemiseks, rakendatakse maksevahendil põhinevat allahindlust kandele automaatselt. Seejärel kuvatakse vähendatud summa saldona. Kuid juhul, kui kassapidaja valib maksekuval nupu **Tagasi**, eemaldatakse allahindlus ja kandekuval näidatakse algsummat. Maksevahendil põhinev allahindlus eemaldatakse, kui tühistada makse rida.

Krediitkaardimaksete puhul saavad jaemüüjad määrata maksevahendipõhise allahindluse ühel või enamal krediitkaarditüübil. Süsteem ei saa siiski kontrollida, millist tüüpi krediitkaarti kasutatakse, kui kaarti pole autoriseeritud. Kui allahindlus rakendatakse pärast autoriseerimist, autoriseeritakse makse suurema summa jaoks, kuid makse hõivamine tehakse väiksema summa jaoks. Selle olukorra vältimiseks, kui klient maksab krediitkaardiga, küsitakse kassapidajalt dialoogiboksi, kus on loetletud mis tahes eelistatud krediitkaardid, mis annavad kliendile täiendava allahindluse. Seejärel saab kassapidaja küsida, kas klient soovib kasutada ühte eelistatud kaartidest, et saada lisaallahindlust. Kui kassapidaja valib eelistatud kaardi, rakendatakse kandele maksevahendil põhinevat allahindlust ja vähendatud summa kuvatakse maksekuval. Autoriseerimine tehakse vähendatud summa jaoks. Kui klient sisestab kaardi, mis erineb kassapidaja valitud kaardist, kuvatakse veateade ja autoriseerimine tühistatakse.

## <a name="call-center-user-experience"></a>Kõnekeskuse kasutamine

Kui kõnekeskuse kasutaja valib kõnekeskuse **tellimuse** ajal suvandi Lõpeta, **kuvatakse kuva Summad**. Alguses ei sisalda selle kuva kogusummad maksevahendil põhinevaid allahindlusi, kuna makseviisi pole veel valitud. Kui kasutaja valib kuval **Lisa makse** makseviisi, mille puhul maksevahendil põhinev allahindlus on konfigureeritud, korrigeeritakse maksesummat automaatselt nii, et see kajastab allahindlusega summat. Nagu klient müügikohas, saab kõnekeskuse klient otsustada, kas maksta täismakse või osamakse. Makstud summa põhjal rakendatakse maksevahendil põhinev allahindlus müügitellimusele.

> [!NOTE]
> Kaarti kõnekeskuse tellimuste puhul ei kinnitata. Näiteks kui kõnekeskuse kasutaja valib krediitkaardiks Visa, kuid klient kasutab Mastercardi, rakendab süsteem ikka allahindlust.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
