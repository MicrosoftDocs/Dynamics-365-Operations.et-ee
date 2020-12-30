---
title: Kasutajaõiguste seadistamine Attractis
description: Teema sisaldab teavet rolliturbe kohta rakenduses Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: efac512cfa07bb2183f06b8be45f74bef9af0767
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460912"
---
# <a name="set-user-permissions-in-attract"></a>Kasutajaõiguste seadistamine Attractis

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract kasutab rollipõhist turvet. Teisisõnu ei anta juurdepääsu üksikkasutajatele vaid kasutajatele määratud turberollidele. Kasutajal, kellele on määratud turberoll, on ligipääs selle rolliga seotud määratud privileegidele.

Attractis on viis põhilist kasutaja rolli.

- Administraator
- Personalijuht
- Värbaja
- Vestluse läbiviija
- Kirjutuskaitstud

Administraatori roll on ainus, millel on luba teiste kasutajate lisamiseks ja nende õiguste muutmiseks.

- **Lisa** – valige halduskeskusest **Kasutajaõiguste** vahekaardil **Määra rollid**, otsige lisatav kasutaja ja määrake sellele kasutajale õigused.
- **Redigeeri** – otsige kasutajat või leide kasutaja loendist ja valige seejärel **Redigeerimine**, et muuta tema õiguseid.
- **Kustuta** – kasutaja õiguste kustutamisel ei eemalda te kasutajat süsteemist. Kuid tee piirate kasutaja ligipääsu ja privileege Attractis. Näiteks on Hilda määratud personalijuhi rolli ja ta on lisatud personalijuhi tööle. Kui Hilda eemaldatakes hiljem personalijuhi rollist, jääb ta töö personalijuhiks ja tal on ikka ligipääs tööle. Kuid ta ei saa luua teisi töid.

Järgmistes jaotistes esitatakse iga rolli üksikasjalik kirjeldus. Allolevad tabelid annavad rohkem üksikasjalikku teavet.

> [!NOTE]
> Mõned funktsioonid on saadaval ainult tervikliku värbamise lisandmooduliga Attractile.

## <a name="administrator"></a>Administraator

Kasutajad, kellele määratakse Administraatori roll, pääsevad ligi ja saavad muuta kõiki Attracti andmeid. Administraatorid saavad luua, lugeda, värskendada ja kustutada andmeid. Neil on ka juurdepääs Halduskeskusele, kus nad saavad konfigureerida Attracti rakendust ja seadistada kasutajateavet. Soovitame administraatori rolli määrata vähemalt ühe inimese. Vaikimisi seatakse Microsoft Power Appsis keskkonna administraator Attracti administraatoriks. Kui te registreerute Attracti prooviversiooni jaoks, määratakse administraatori roll automaatselt teile. Praegu peab administraatori rolliga kasutajal tööde loomiseks olema ka värbaja või personalijuhi roll.

## <a name="hiring-manager"></a>Personalijuht

Kasutajad, kes on määratud personalijuhi rolli saavad luua töid ja värskenada varem loodud töid. Personalijuhid saavad tööga ja selle tööga seotud rakendustega teha piiratud hulga toiminguid. Ainult kasutajad, kellele on määratud personalijuhi roll, saab personalijuhina värbamistöörühma lisada.

## <a name="recruiter-role"></a>Värbaja roll

Kasutajatel, kellel on värbaja roll, on täielik lugemise, loomise, värskendamise ja kustutamise õigus enda loodud töödele. Neil on ka täielik loomise, lugemise, värskendamine ja kustutamise õigus nende loodud töödega seotud rakendustele. Ainult kasutajad, kellele on määratud värbaja roll, saab värbajana värbamistöörühma lisada.

## <a name="interviewer"></a>Intervjueerija

Iga kasutaja, kellel on organisatsioonis Microsoft Azure Active Directory (Azure AD) konto, saab lisada värbamistöörühma intervjueerijana. Intervjueerija rolli määratud kasutajad saavad vaadata töö üksikasju ja kandidaadi andmeid nende tööde kohta, mille pärast nad värbamistöörühmas on. Intervjueerijad saavad tööde kohta teha ka värbamissoovitusi ja pakkuda kandidaatide kohta tagasisidet. Kuid nad ei saa värskendada töö üksikasju või kandidaadi andmeid.

## <a name="read-only"></a>Kirjutuskaitstud

Kasutajatele, kellele on määratud kirjutuskaitstu roll, on kogu Attract keskkonna teabele kirjutuskaitstud ligipääs. Kuid nad ei saa andmeid luua ega redigeerida.

## <a name="find-out-which-roles-you-have"></a>Määratud rollide vaatamine

1.  Klõpsake rakenduse Attract paremas ülanurgas küsimärki (**?**).

2.  Klõpsake valikut **Teave**.

    Avanevas aknas näete, millised rollid on teile rakenduses Attract määratud.

    ![Oma Attracti litsentsi tüübi vaatamine](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Delegeeritud rollid

Iga töö jaoks, mille pärast nad värbamistöörühmas on, saavad värbajad ja personalijuhid määrata endale ühe või mitu delegaati. Kuid nad ei saa määrata delegaate teistele värbamistöörühma inimestele.

Delegaatidel on samad õigused nagu inimesel, kes nad määras. Näiteks kui personalijuht määrab endale töö jaoks delegaadi, on delegaadil selle töö kohta samad õigused nagu personalijuhil. Delegaadid ei saa teisi delegaate värbamistöörühmast eemaldada. Nad ei saa eemaldada ka inimesi, kes määrasid nad enda delegaadiks.

## <a name="job-details-and-actions"></a>Töö üksikasjad ja tegevused

Kasutajad, kellel on värbaja või personalijuhi roll, saavad luua töid. Järgmised õigused kehtivad töö üksikasjadele ja töödega tehtavatele tegevustele.

| Andmed või tegevus    | Värbaja | Personalijuht | Vestluse läbiviija |
|-------------------|-----------|----------------|-------------|
| Töö üksikasjad       | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Kirjutuskaitstud |
| Värbamistöörühm       | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Kirjutuskaitstud |
| Töö sisestamine       | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Kirjutuskaitstud | Kirjutuskaitstud |
| Töötlemine           | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Kirjutuskaitstud |
| Kandidaatide lisamine    | Kandidaatide lisamine tööde jaoks, mille pärast kasutaja värbamistöörühmas on | Kandidaatide lisamine tööde jaoks, mille pärast kasutaja värbamistöörühmas on | Pole lubatud |
| Potentsiaalselt sobivate kandidaatide lisamine     | Potentsiaalselt sobivate kandidaatide lisamine tööde jaoks, mille pärast kasutaja värbamistöörühmas on | Konfiguratsiooni suvand [potentsiaalselt sobiva kandidaadi tegevuse seadistamine](./activities-attract.md#prospect-activity) kontrollib, kas vestluse läbiviijad saavad potentsiaalseid kandidaate lisada ja vaadata. | Pole lubatud |
| Töö aktiveerimine      | Nende tööde aktiveerimine, mille pärast kasutaja värbamistöörühmas on | Nende tööde aktiveerimine, mille pärast kasutaja värbamistöörühmas on | Pole lubatud |
| Sule töö         | Nende tööde sulgemine, mille pärast kasutaja värbamistöörühmas on | Pole lubatud | Pole lubatud |
| Kustuta töö        | Nende tööde kustutamine, mille pärast kasutaja värbamistöörühmas on | Ainult siis, kui tööle ei ole lisatud ühtegi kandidaati | Pole lubatud |
| Kandidaatide kustutamine | Kandidaatide kustutamine, kui kasutaja on värbamistöörühmas | Pole lubatud | Pole lubatud |

## <a name="application-details-and-actions"></a>Avalduse üksikasjad ja tegevused

Järgmised õigused kehtivad kandidaatide tööspetsiifilistele andmetele ja avalduste osas tehtavatele tegevustele.

| Andmed või tegevus          | Värbaja | Personalijuht | Vestluse läbiviija |
|-------------------------|-----------|----------------|-------------|
| Avalduse dokumendid   | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Kirjutuskaitstud |
| Avalduse märkmed       | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Luua, lugeda, värskendada ja kustutada töösid, mille pärast kasutaja värbamistöörühmas on | Kirjutuskaitstud|
| Avalduse tegevuse    | Vaadake, kas kasutaja on värbamistöörühmas | Vaadake, kas kasutaja on värbamistöörühmas | Kirjutuskaitstud |
| Avalduse tagasiside    | Lisage ja vaadake kogu tagasisidet, kui kasutaja on värbamistöörühmas | Lisage ja vaadake kogu tagasisidet, kui kasutaja on värbamistöörühmas | Saab lisada tagasiside\*\* |
| Avalduse tagasilükkamine      | Võidake lükata, kas kasutaja on värbamistöörühmas | Pole lubatud | Pole lubatud |
| Etapi võrra edasi           | Võidake lükata, kas kasutaja on värbamistöörühmas | Võidake edasi liikuda, kas kasutaja on värbamistöörühmas | Pole lubatud |
| Pakkumise haldamise käivitamine | Saab alustada pakkumise haldamist | Pakkumise tegevusel on konfiguratsioonivalik. | Pole lubatud |


\*\* Konfiguratsioonivalik väljal [tagasiside tegevuse seadistamine](./activities-attract.md) kontrollib, kas küsitlejad näevad teineteise tagasisidet.


## <a name="process-templates"></a>Töötlusmallid

Järgmised õigused kehtivad värbamisprotsessi mallidele. Töörühma liikmete võimet luua ja redigeerida malle konfigureeritakse **Mallihalduses** halduskeskuses. Kui mallihaldus on sisse lülitatud, saavad värbajad ja personalijuhid luua ja redigeerida oma protsessimalle. Kui mallihaldus on välja lülitatud, saavad protsessimalle luua ja redigeerida ainult administraatorid. Järgnev tabel eeldab, et mallihaldus on välja lülitatud.

| Andmed              | Värbaja                                           | Personalijuht                                      | Vestluse läbiviija |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Töötlusmallid | Täielikud õigused kasutaja loodud mallidele | Täielikud õigused kasutaja loodud mallidele | Juurdepääs puudub   |

## <a name="email-and-email-templates"></a>E-post ja e-posti mallid

Järgmised õigused kehtivad e-posti mallidele ja e-postiga tehtavatele tegevustele. E-posti malle saab luua ja redigeerida ainult administraator.

| Andmed või tegevus     | Värbaja          | Personalijuht     | Vestluse läbiviija |
|--------------------|--------------------|--------------------|-------------|
| E-kirjade mallid    | Kirjutuskaitstud ligipääs   | Kirjutuskaitstud ligipääs   | Juurdepääs puudub   |
| Saada meilisõnum         | Saatke tegevuse kohta  | Saatke tegevuse kohta  | Juurdepääs puudub   |
| E-posti sisu redigeerimine | E-posti sisu redigeerimine | E-posti sisu redigeerimine | Juurdepääs puudub   |

## <a name="talent-pools"></a>Talendikaustad

Talendikaustadele kehtivad järgmised õigused. Talendikaustad on nähtavad ainult neid loonud inimesele, va juhul kui see inimene otsustab neid jagada. Kandidaadi otsingut saab kasutada kandidaatide otsinguks, keda ei ole veel nimetatud kausta lisatud.

| Andmed või tegevus   | Värbaja                                       | Personalijuht                                  | Vestluse läbiviija |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Nimetatud kaust       | Täielikud õigused kasutaja loodud kaustadele | Täielikud õigused kasutaja loodud kaustadele | Juurdepääs puudub   |
| Ühiskasutuse kaust       | Ainult kasutaja loodud kaustad                | Ainult kasutaja loodud kaustad                | Juurdepääs puudub   |
| Kandidaadi otsing | Täielikud otsinguvõimalused                        | Täielikud otsinguvõimalused                        | Juurdepääs puudub   |

## <a name="candidates"></a>Kandidaadid

Kandidaadid on inimesed, kes on lisatud talendikausta, kuid ei ole tööga seostatud.

| Andmed                        | Värbaja                        | Personalijuht                   | Vestluse läbiviija |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profiil – kandidaadi andmed | Looge, lugege, värskendage ja kustutage | Looge, lugege, värskendage ja kustutage | Juurdepääs puudub   |
| Dokumendid                   | Looge, lugege, värskendage ja kustutage | Looge, lugege, värskendage ja kustutage | Juurdepääs puudub   |
