---
title: B2C rentniku seadistus Kaubanduses
description: Selles teemas kirjeldatakse kuidas seadistada Azure Active Directory (Azure AD) ettevõtja ja tarbija vahelisi (B2C) rentnikke kasutaja saidi autentimiseks rakenduses Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 086128091b23ce6ab46dd2dfc0803af38de6bac7
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714308"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C rentniku seadistus Kaubanduses

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse kuidas seadistada Azure Active Directory (Azure AD) ettevõtja ja tarbija vahelisi (B2C) rentnikke kasutaja saidi autentimiseks rakenduses Dynamics 365 Commerce.

Dynamics 365 Commerce kasutab Azure AD B2C'd kasutaja mandaadi ja autentimise voogude toetamiseks. Kasutaja saab nende voogude kaudu registreeruda, sisse logida ja lähtestada parooli. Azure AD B2C talletab kasutaja tundliku autentimisteabe, nt kasutajanime ja parooli. B2C rentniku kasutajakirje salvestab kas kohaliku B2C kontokirje või B2C sotsiaalse identiteedi pakkuja kirje. Need B2C kirjed lingitakse Commerce'i keskkonna kliendikirjetega.

> [!WARNING] 
> Azure AD B2C kustutab vana (pärand) kasutajavood 1. augustiks 2021. Seetõttu peaksite plaanima oma kasutajavood migreerida uude soovitatud versiooni. Uus versioon pakub funktsioonide pariteeti ja uusi funktsioone. Commerce version 10.0.15 või uuema versiooni mooduliteeki tuleb kasutada soovitatud B2C kasutajavoogudega. Lisateabe saamiseks vt [Azure Active Directory B2C kasutajavoog](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce'i hindamiskeskkonnad on eellaaditud Azure AD B2C rentnikuga demo eesmärgil. Oma Azure AD B2C rentniku laadimine alltoodud juhiste alusel ei ole hindamiskeskkondade jaoks vajalik.

> [!TIP]
> Saate oma saidi kasutajaid täiendavalt kaitsta ja suurendada oma Azure AD B2C rentnike turvalisust Azure AD identiteedikaitse ja tingimusliku juurdepääsu abil. Azure AD B2C Premium P1 ja Premium P2 rentnikele pakutavate võimaluste ülevaatamiseks vt [Azure AD B2C identiteedikaitse ja tingimuslik juurdepääs](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Dynamics keskkonna eeltingimused

Enne alustamist veenduge, et teie Dynamics 365 Commerce keskkond ja e-äri kanal konfigureeritakse õigesti, täites järgmised eeltingimused.

- Seadke kassatoimingute **AllowAnonymousAccess** väärtuseks "1" Commerce headquarters`is:
    1. Minge **kassatoimingutesse**.
    1. Tehke paremklõps ruudustikul ja siis klõpsake **Isikupärasta**.
    1. Valige **Lisa väli**.
    1. Valige saadaoleva veeru loendist veerg **AllowAnonymousAccess** et see lisada.
    1. Tehke valik **Värskenda**.
    1. Toimingu **612** "Kliendi lisamine" jaoks muutke **AllowAnonymousAccessiks** "1".
    1. Käitage **1090 (Registrid)** töö.
- Häälestage numbriseeria kliendikonto atribuut **Käsitsi** väärtusele **Ei** Commerce headquarters`is:
    1. Valige suvandid **Jaemüük ja Kaubandus \> Peakontori seadistamine \> Parameetrid \> Nõuete parameetrid**.
    1. Valige **numbriseeria**.
    1. Topeltklõpsake **kliendikonto** real **numbriseeria koodi** väärtust.
    1. Numbriseeria **Üldises** kiirkaardis määrake olekuks **Käsitsi** väärtuseks **Ei**.

Pärast teie keskkonna Dynamics 365 Commerce juurutamist on soovitatav [lähtestada ka algandmed](enable-configure-retail-functionality.md) keskkonnas.

## <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure'i portaalis.

See jaotis hõlmab B2C rentniku loomist Azure AD või seostamist ärisaidil kasutamiseks. Lisateavet vt teemast B2C [rentniku Azure Active Directory loomine](/azure/active-directory-b2c/tutorial-create-tenant).

1. Logige sisse [Azure’i portaali](https://portal.azure.com/).
1. Valige Azure'i portaali menüüst käsk **Loo ressurss**. Veenduge, et kasutate tellimust ja kataloogi, mis on seotud teie Commerce'i keskkonnaga.

    ![Ressursi loomine Azure'i portaalis.](./media/B2CImage_1.png)

1. Avage **Identiteedi \> Azure Active Directory B2C**.
1. Kui olete lehel **Uue B2C üürniku loomine või olemasoleva rentnikuga linkimine**, kasutage ühte valikutest, mis sobib kõige paremini teie ettevõtte vajadustega.

    - **Loo uus Azure AD B2C rentnik**: kasutage seda suvandit uue Azure AD B2C rentniku loomiseks.
        1. Valige käsk **Loo uus Azure AD B2C rentnik**.
        1. Sisestage organisatsiooni nimi jaotises **Organisatsiooni nimi**.
        1. Sisestage algne domeeninimi jaotises **Algne domeeninimi**.
        1. Valige riik ja piirkond jaotises **Riik või piirkond**.
        1. Rentniku loomiseks valige **Loo**.

     ![Uue Azure AD rentniku loomine.](./media/B2CImage_2.png)

     - **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**: kasutage seda suvandit, kui teil on Azure AD B2C rentnik, mida soovite linkida.
        1. Valige **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**.
        1. Jaotises **Azure AD B2C rentnik** valige sobiv B2C rentnik. Kui valikukastis kuvatakse teade „Ei leitud ühtegi sobilikku B2C rentnikku”, pole teil kehtivat sobilikku B2C rentnikku ja teil on vaja luua uus.
        1. Tehke jaotises **Ressursigrupp** valik **Loo uus**. Sisestage ressursirühmale **Nimi**, mis sisaldab rentnikku ja valige **Ressursigrupi asukoht** ning seejärel **Loo**.

    ![Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega.](./media/B2CImage_3.png)

1. Kui uus Azure AD B2C kaust on loodud (see võib võtta mõne hetke), kuvatakse armatuurlaual link uuele kaustale. See link juhatab teid lehele „Tere tulemast Azure Active Directory B2C-sse”.

    ![Link uude kausta Azure AD](./media/B2CImage_4.png)

> [!NOTE]
> Kui teie Azure'i kontol on mitu tellimust või olete seadistanud B2C rentniku aktiivsele tellimusele linkimata, suunab ribareklaam **Tõrkeotsing** rentnikku tellimusega linkima. Valige tõrkeotsingu teade ja järgige tellimuse probleemi lahendamiseks juhiseid.

Järgmine pilt on Azure AD B2C ribareklaami **Tõrkeotsing** näide.

![Kuvatav hoiatus Kataloogist puudub aktiivne tellimus.](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>B2C rakenduse loomine

Kui B2C rentnik on loodud, tuleb teie uues Azure AD B2C rentnikus luua B2C rakendus Commerce'i toimingutega suhtlemiseks.

B2C rakenduse loomiseks toimige järgmiselt.

1. Avage Azure’i portaalis suvand **Rakenduse registreerimised** ja valige **Uus registreerimine**.
1. Sisestage selle Azure AD B2C-rakenduse jaoks nimi väljas **Nimi**.
1. **Toetatud kontotüüpide** all valige **kontod mis tahes identiteedipakkujas või organisatsioonikaustas (kasutajavoogudega kasutajate autentimiseks)**.
1. **Ümbersuunamise URI** puhul sisestage oma sihtotstarbeline vastuse URL-id tüübina **Veeb**. Lisateavet vastuse URL-ide ja nende vormindamise kohta leiate allpool jaotisest [Vastuse URL-id](#reply-urls). Kasutaja autendimisel ümbersuunamiste lubamiseks B2C-st tagasisuunas peate sisestama ümbersuunamise URI/vastuse URL-i Azure AD. Vastuse URL-i saab lisada registreerimisprotsessi ajal või hiljem lisada, **valides B2C** rakenduse ülevaate jaotisest Ülevaade **lingi Lisa ümbersuunamise URI** **link**.
1. **Õiguste** puhul valige suvand **Hüvitise administraatori nõustumine openID-offline_access õigustega**.
1. Valige suvand **Registreeri**.
1. Valige vastloodud rakendus ja liikuge autentimise **menüüsse**. 
1. Vastuse URL-i **·** **·** **sisestamisel valige valiku Vaikimisi hüvitise ja rahavoo all nii juurdepääsu lubade kui ka ID-lubade** suvandid nende lubamiseks rakenduses ja seejärel valige **salvesta.** Kui registreerimise ajal ei sisestatud vastuse URL-i, saab **selle** lisada ka sellele lehele, valides suvandi Lisa platvorm, valides veebi ja **sisestades** seejärel rakenduse ümbersuunamise URI. Siis **on vaikimisi hüvitise ja rahavoo** jaotis saadaval **, et valida nii juurdepääsulubasid kui** **ka ID-pääsu suvandeid**.
1. Minge Azure'i portaali menüüsse **Ülevaade** ja kopeerige **Rakenduse (kliendi) ID**. Pange see ID hilisemate seadistusetappide jaoks üles (mida hiljem viidatakse kui **Kliendi GUID**).

Täiendavat viidet rakenduse registreerimiste kohta Azure AD B2C-s vt [Uue rakenduse registreerimiste kogemust Azure Active Directory B2C-ga](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Vastuse URL-id

Vastuse URL-id on olulised, kuna need tagavad tagastusdomeenide lubatud üksuste loendi, kui teie sait küsib Azure AD B2C kasutaja autentimist. See lubab autenditud kasutajal pöörduda tagasi domeeni, kuhu ta sisse logib (teie saidi domeen). 

Akna **Azure AD B2C - Rakendused \> Uus rakendus** kastis **Vastuse URL** tuleb lisada eraldi read nii saidi domeenile kui ka (kui teie keskkond on ette valmistatud) Commerce'i loodud URL-ile. Need URL-id peavad alati kasutama kehtivat URL-vormingut ja need peavad olema ainult alus-URL-id (neile ei järgne kaldkriipse ega teid). Seejärel tuleb lisada string ``/_msdyn365/authresp`` alus-URL-idele, nagu järgnevates näidetes illustreeritud.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domeen peab vastama täielikult e-kaubanduse domeenile. Kui teil on mitu domeeni, peate selle URL-i lisama igale domeenile.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Kasutajavoo poliitikate loomine

Kasutajavood on poliitikad, mida Azure AD B2C kasutab turvalise sisselogimise, registreerimise, profiili muutmise ja unustatud parooli kasutajakogemuste tagamiseks. Dynamics 365 Commerce kasutab neid voogusid et poliitikaga seonduvate toimingute tegemiseks Azure AD B2C rentnikuga suhtlemisel. Kui kasutaja suhtleb nende poliitikatega, suunatakse ta nende toimingute sooritamiseks Azure AD B2C rentnikku.

Azure AD B2C pakub kolme peamist kasutajavoo tüüpi.
- Registreerimine ja sisselogimine
- Profiili redigeerimine
- Parooli lähtestamine

Võite kasutada vaikimisi antud kasutajavoogusid Azure AD, mis kuvavad B2C majutatud Azure AD lehe. Saate ka luua HTML-lehe, et juhtida nende kasutajavoo kogemuste välimust ja olemust. 

Kasutajapoliitika lehtede kohandamiseks Dynamics 365 Commerce'is ehitatud lehtedega vaadake teemat [Kohandatud lehtede häälestamine kasutaja sisselogimisteks](custom-pages-user-logins.md). Lisateavet leiate teemast [Azure Active Directory B2C kasutuskogemuse liidese kohandamine](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Looge registreerumise ja sisselogimise kasutajavoo poliitika.

Registreerumise ja kasutajavoo poliitikasse sisselogimiseks järgige neid samme.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Valige poliitika **Registreerimine ja sisselogimine** ja seejärel **Soovitatud** versioon.
1. Sisestage poliitika nimi väljale **Nimi**. See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).
1. Jaotise **Identiteedi pakkujad** jaotises Kohalikud **kontod** valige e-kirjaga **registreerimine**. Meili autentimist kasutatakse Rakenduse Commerce kõige tavalisemates stsenaariumides. Kui kasutate ka isiku identiteedipakkuja autentimist, saab neid ka praegu valida.
1. Valige sobiv ettevõtte valik jaotises **Mitmikautentimine**. 
1. Jaotises **Kasutaja atribuudid ja nõuded** valige suvandid atribuutide kogumiseks või nõuete tagastamiseks vastavalt vajadusele. Valige **käsk Kuva rohkem ...** atribuutide ja nõuete suvandite täieliku loendi saamiseks. Commerce nõuab järgmisi vaikesätteid.

    | **Atribuudi kogumine** | **Nõude tagastamine** |
    | ---------------------- | ----------------- |
    | Meiliaadress          | Meiliaadressid   |
    | Eesnimi             | Eesnimi        |
    |                        | Identiteedipakkuja |
    | Perekonnanimi                | Perekonnanimi           |
    |                        | Kasutaja objekti ID  |

1. Valige **Loo**.

Järgmine pilt on näide B2C-ga Azure AD registreerumise ja kasutajavoo sisse logimise kohta.

![Registreerimise ja sisselogimise poliitika sätted.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profiili loomine kasutajavoo poliitika redigeerimisel

Profiili redigeerimise kasutajavoo poliitika loomiseks toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Valige **Profiili redigeerimine** ja seejärel valige **soovitatav** versioon.
1. Jaotises **Nimi** sisestage profiil kasutajavoogu redigeerides. See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).
1. Jaotise **Identiteedi pakkujad** jaotises Kohalikud **kontod** valige Meiliaadress **SignIn**.
1. Jaotises **Kasutaja atribuudid** märkige järgmised ruudud.
    
    | **Atribuudi kogumine** | **Nõude tagastamine** |
    | ---------------------- | ----------------- |
    |                        | Meiliaadressid   |
    | Eesnimi             | Eesnimi        |
    |                        | Identiteedipakkuja |
    | Perekonnanimi                | Perekonnanimi           |
    |                        | Kasutaja objekti ID  |
    
1. Valige **Loo**.

Järgmine pilt on Azure AD B2C profiili redigeerimise kasutajavoo näide.

![Azure AD Näide B2C-profiili redigeerimise kasutajavoost](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Parooli lähtestamise kasutajavoo poliitika loomine

Parooli lähtestamiseks kasutajavoo poliitikas toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Valige **Parooli lähestamine** ja seejärel valige **soovitatav** versioon.
1. Jaotises **Nimi** sisestage parooli lähtestamise kasutajavoo nimi.
1. Jaotises **Identiteedipakkujad** valige suvand **Parooli lähtestamine meiliaadressi kasutades**.
1. Valige **Loo**.
1. Jaotises **Rakenduse nõuded** märkige järgmised ruudud.
    - **Meiliaadressid**
    - **Eesnimi**
    - **Perekonnanimi**
    - **Kasutaja objekti ID**
1. Valige **Loo**.

Järgmisel pildil näidatakse, kuhu seada **Lähtesta parool meiliaadressi abil** Azure AD B2C parooli lähtestamise kasutajavoos.

![„Lähtesta parool meiliaadressi abil” sätestamine parooli lähtestamise poliitikas](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a>Sotsiaalstete identiteedipakkujate lisamine (valikuline)

Sotsiaalsed identiteedipakkujad lubavad kasutajatel autentimiseks sotsiaalmeedia kontosid kasutada. Sotsiaalse identiteedipakkuja autentimise lisamine on Dynamics 365 Commerce'i rakenduses valikuline. 

Kui sotsiaalse identiteedipakkuja autentimist ei lisata, on Azure AD B2C vaikeprofiilid teie kasutajate põhilised profiilid. Kasutajad valivad oma kasutajanime (eelistatud meiliaadressi) ja määravad parooli. Azure AD B2C autendib kasutajaid otse. 

Kui on sotsiaalse identiteedipakkuja autentimine lisatakse ja kasutaja valib ühe pakutava sotsiaalse identiteedipakkuja, luuakse ikkagi üksus Azure AD B2C rentniku jaoks. Azure AD B2C autendib seejärel kasutaja mandaadi sotsiaalse identiteedipakkuja juures.

> [!NOTE]
> Identiteedipakkujaga sisselogimine loob kirje B2C rentnikku, kuidkohalikest kontodest erinevas vormingus, kuna see nõuab autentimiseks välise sotsiaalse identiteedipakkuja viidet. Kasutaja saab kasutada sama meiliaadressi kõigis sotsiaalsetes identiteedipakkujates, mis tähendab, et autentimiseks kasutatav meili kasutajanimi ei pruugi olla rentniku jaoks kordumatu. Azure AD B2C nõuab kasutajatelt on kordumatu meiliaadress kasutamist kohalikel B2C kontodel.

Enne autentimiseks sotsiaalse identiteedipakkuja lisamist, peate pöörduma identiteedipakkuja portaali poole ja häälestama identiteedipakkuja rakenduse Azure AD B2C dokumentatsioonis kirjeldatud juhiste järgi. Allpool on esitatud linkide loend dokumentidele juurde pääsemiseks.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Üksik rentnik)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsofti konto](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Sotsiaalse identiteedipakkuja lisamine ja seadistamine

Sotsiaalse identiteedipakkuja lisamiseks ja seadistamiseks toimige järgmiselt.  

1. Azure'i portaalis liikuge jaotisesse **Identiteedipakkujad**.
1. Valige **Lisa**. Kuvatakse aken **Identiteedipakkuja lisamine**.
1. Sisestage **jaotises** Nimi kasutajatele kuvatav nimi.
1. Valige jaotises **Identiteedipakkuja tüüp** loendist identiteedipakkuja.
1. Valige nupp **OK**.
1. Valige **Selle identiteedipakkuja häälestamine** aknale **Sotsiaalse identiteedipakkuja häälestamine** juurde pääsemiseks.
1. Jaotises **Kliendi ID** sisestage kliendi ID, mille saite identiteedipakkuja rakenduse häälestamisel.
1. Jaotises **Kliendi saladus** sisestage kliendi saladus, mille saite identiteedipakkuja rakenduse häälestamisel.
1. Lisage kasutajavoog sisselogimise/registreerumise poliitikatele.
1. Avage jaotis **Azure AD B2C – kasutajavood (poliitikad) \> {teie sisselogimise registreerumise poliitika} \> Identiteedipakkujad**.
1. Kasutajavoo poliitika seostamiseks sisselogimise/registreerumise poliitikaga valige iga identiteedipakkuja, mille olete oma kontole seadistanud. Nende testimiseks valige käsk **Kasutajavoo käitamine** igale identiteedipakkujale. Uus vahekaart kuvab sisselogimisakna, kus kuvatakse uus identiteedipakkuja valikuväli.

Järgmisel pildil kuvatakse näited akende **Identiteedipakkuja lisamine** ja **Sotsiaalse identiteedipakkuja häälestamine** kohta Azure AD B2C-s.

![Sotsiaalse identiteedipakkuja lisamine rakendusse.](./media/B2CImage_14.png)

Järgmisel pildil kuvatakse näide, kuidas valida identiteedipakkujaid Azure AD B2C lehel **Identiteedipakkujad**.

![Valige kõik enda poliitika jaoks lubatavad sotsiaalse identiteedi pakkujad.](./media/B2CImage_16.png)

Järgmisel pildil kuvatakse näide vaikimisi sisselogimisaken, millel on sotsiaalse identiteedipakkuja sisselogimisnupp.

> [!NOTE]
> Kui kasutate oma kasutajavoogude jaoks teenuses Commerce sisseehitatud kohandatud lehti, tuleb sotsiaalse identiteedi pakkujate nupud lisada Commerce'i mooduli teegi laiendamisfunktsioonide abil. Lisaks, kui seadistate avaldusi kindla isiku identiteedi pakkujaga, võib mõnel juhul URL või konfiguratsioonistring olla tõstutundlik. Lisateabe saamiseks vaadake oma isiku identiteedi pakkuja ühendusjuhiseid.
 
![Näide vaikimisi sisselogimisaknast sotsiaalse identiteedipakkuja sisselogimisnupuga.](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce'i peakontori värskendamine uue Azure AD B2C teabega

Kui eelpool loetletud Azure AD B2C ettevalmistavad etapid on lõpule viidud, peab Azure AD B2C rakendus olema registreeritud teie Dynamics 365 Commerce'i keskkonnas.

Peakontori väsrkendamiseks uue Azure AD B2C teabega toimige järgmiselt.

1. Avage Commerce'i jaotis **Commerce'i jagatud parameetrid** ja valige vasakpoolsest menüüst **Identiteedipakkujad**.
1. Jaotises **Identiteedipakkujad** toimige järgmiselt.
    1. Sisestage **väljale Väljastaja** identiteedipakkuja väljastaja string. Oma väljastajastringi otsimiseks vt allolevat [peakontori häälestamise väljastaja stringi](#obtain-issuer-string-for-headquarters-setup).
    1. Sisestageoma väljaandja kirje nimi väljale **Nimi**.
    1. Väljale **Tüüp** sisestage **Azure AD B2C (id_token)**.
1. Jaotises **Sõltuvad osapooled**, kui eelpool mainitud B2C identiteedipakkuja üksus on valitud, tehke järgmist.
    1. Sisestage oma B2C rakenduse ID väljale **ClientID**. Leiate selle oma B2C rakenduse atribuutide lehe väljalt **Rakenduse ID**.
    1. Väljale **Tüüp** sisestage **Avalik**.
    1. Väljale **Kasutajatüüp** sisestage **Klient**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Sisestage Commerce'i otsingulahtrisse **Jaotusegraafik**
1. Lehe **Jaotusegraafik** vasakpoolses navigeerimismenüüs valige töö **1110 globaalne konfiguratsioon**.
1. Valige toimingupaanil käsk **Käivita kohe**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Hangi halduse häälestuse jaoks väljastaja string

Oma identiteedipakkuja väljastaja stringi hankimiseks järgige neid samme.

1. Liikuge Azure'i portaali Azure AD B2C lehel oma kasutajavoosse **Sisselogimine ja registreerimine**.
1. Valige **Lehe paigutused** vasakul navigeerimismenüüs, valige **Paigutuse nimi** suvand **Ühtne sisselogimine või registreerimine** lehel ja seejärel valige **Käivita kasutajavoog**.
1. Veenduge, et teie rakendus on seatud Azure AD ülal loodud kavandatud B2C-rakendusele ja valige seejärel kasutajavoo link, **mis kuvatakse pakett-töö Käivita kasutajavoo** päises ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Ärge valige **Käivita kasutajavoog**.) Uus vahekaart avaneb kuvab metaandmed poliitika jaoks väljastaja stringi kogumiseks.
1. Brauseri vahekaardil kuvataval metaandmete lehel kopeerige identiteedipakkuja väljastaja string (**väljastaja** väärtus, alustades väärtusega "https://" ja lõpetades väärtusega "/v2.0/"), mis sarnaneb järgmise näitega.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**VÕI**: sama metaandmete URL-i käsitsi loomiseks tehke järgmist.

1. Looge metaandmete aadressi URL järgmises vormingus, kasutades oma B2C rentnikku ja poliitikat: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Näide: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Sisestage metaandmete aadressi URL brauseri aadressiribale.
1. Kopeerige metaandmetest identiteedipakkuja väljaandja URL (väärtus **„väljaandja”**).
    - Näide: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>B2C rentniku konfigureerimine kaubanduse saidiehitajas

Kui teie Azure AD B2C rentniku häälestus on lõpule viidud, tuleb konfigureerida B2C rentnik kaubanduse saidiehitajas. Konfiguratsioonietapid hõlmavad B2C rakenduse teabe kogumist Azure'i portaalist, selle B2C rakenduse teabe sisestamist saidiehitajasse ja seejärel B2C rakenduse seostamist teie saidi ja kanaliga.

### <a name="collect-the-required-application-information"></a>Nõutava rakenduseteabe kogumine

Nõutava rakenduseteabe kogumiseks toimige järgmiselt.

1. Avage Azure'i portaalis **Home \>Azure AD B2C – rakenduse registreerimised**.
1. Valige oma rakendus ja seejärel valige vasakul navigeerimispaanil **Rakenduse** üksikasjade saamiseks Ülevaade.
1. Koguge **rakenduse (kliendi) ID viitest teie B2C rentnikus loodud B2C-rakenduse rakenduse ID**. See sisestatakse hiljem saidiehitajas väärtuseks **Kliendi GUID**.
1. Valige **ümbersuunamise URL-id** ja koguge oma saidi kohta kuvatud vastuse URL (häälestusel sisestatud vastuse URL).
1. Minge avalehele **\>Azure AD B2C – kasutajavood** ja koguge seejärel iga kasutajavoo poliitika täisnimed.

Järgmine pilt näitab näidet **Azure AD B2C - rakenduse registreerimiste ülevaatelehe** kohta.

![Azure AD B2C – rakenduse registreerimiste ülevaateleht, kus on esile tõstetud rakenduse (kliendi) ID](./media/ClientGUID_Application_AzurePortal.png)

Järgmisel pildil kuvatakse näide kasutajavoo poliitikatest lehel **Azure AD B2C – kasutajavood (poliitikad)**.

![Kõigi B2C poliitikavoo nimede kogumine.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Sisestage oma Azure AD B2C rentniku rakenduse teave rakendusse Commerce

Enne B2C rentniku seostamist oma saitidega, peate sisestama Azure AD B2C rentniku andmed kaubanduse saidiehitajasse.

Oma B2C Azure AD rentniku rakenduse teabe lisamiseks Commerce'ile järgige neid samme.

1. Logige sisse administraatorina oma keskkonna kaubanduse saidiehitajasse.
1. Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.
1. Valige jaotises **Rentniku** sätted saidi **autentimise häälestus**. 
1. Valige põhiaknas saidi autentimise **profiilide kõrval** suvand **Manage (Halda**). (Kui teie rentnik ilmub saidi autentimise profiilide loendisse, lisas administraator selle juba. Kontrollige, et alltoodud 6. sammus toodud kaubad ühtivad teie kavandatud B2C-seadistusega. Uusi profiile saab luua ka Azure AD sarnaste B2C rentnike või rakenduste abil, et arvestada väiksemate erinevustega, nagu erinevad kasutajapoliitika ID-d.
1. Valige **suvand Lisa saidi autentimise profiil**.
1. Sisestage järgmised nõutavad üksused kuvatud vormile, kasutades oma B2C rentniku ja rakenduse väärtusi. Väljad, mis ei ole kohustuslikud (ilma tärnita), võivad jääda tühjaks.

    - **Rakenduse nimi**: teie B2C rakenduse nimi, näiteks „Fabrikam B2C”.
    - **Rentniku nimi**: teie B2C rentniku nimi (nt „fabrikam“, kui domeen kuvatakse B2C rentnikule kui „fabrikam.onmicrosoft.com“). 
    - **Poliitika ID parooli unustamise korral**: kasutajavoo poliitika ID parooli unustamise korral, näiteks „B2C_1_PasswordReset”.
    - **Registreerumise poliitika ID**: registreerumise ja sisse logimise kasutajavoo poliitika ID, nt "B2C_1_signup_signin".
    - **Kliendi GUID**: B2C rakenduse ID, näiteks „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.
    - **Profiilipoliitika ID redigeerimine**: kasutajavoo poliitika ID profiili redigeerimiseks, näiteks „B2C_1A_ProfileEdit”.

1. Valige nupp **OK**. Nüüd peaks olema teie B2C rakenduse nimi loendis kuvatud.
1. Oma muudatuste salvestamiseks valige **Salvesta**.

Valikulist **kohandatud domeenivälja** tuleks kasutada ainult siis, kui seadistate Azure AD kohandatud domeeni B2C rentnikule. Täiendavate üksikasjade ja kaalutluste saamiseks kohandatud domeeni logimise **välja** kasutamise kohta vt [allpoololevat B2C-lisateavet](#additional-b2c-information).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C rakenduse seostamine teie saidi ja kanaliga

> [!WARNING]
> - Kui teie sait on juba seostatud B2C rakendusega, siis teise B2C rakendusse üleminekul eemaldatakse praegused juba sellesse keskkonda registreerunud kasutajatele loodud viited. Kui seda muudetakse, ei ole kasutajatele saadaval ükski praegu määratud B2C rakendusega seotud mandaat. 
> - Värskendage B2C-rakendust ainult siis, kui häälestate kanali B2C-rakendust esmakordselt või kui soovite, et kasutajad logiks uuesti sisse uue B2C-rakendusega kanali uute mandaatidega. Olge ettevaatlik kanalite seostamisel B2C rakendustega ja nimetage rakendusi selgelt. Kui kanal ei ole seostatud B2C rakendusega alljärgnevate etappidega, on sisestatakse kasutajad teie saidi kanalisse siselogimisel B2C rakendusse olekuga **vaikimisi** B2C rakenduste loendis **Rentniku sätted \> B2C sätted**.

B2C rakenduse seostamiseks teie saidi ja kanaliga toimige järgnevalt.

1. Liikuge oma saidile kaubanduse saidiehitajas.
1. Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.
1. Jaotises **Saidi sätted** valige **Kanalid**.
1. Valige oma kanal põhiakna jaotises **Kanalid**.
1. Valige paremal kanali atribuutide paanil oma B2C-rakenduse nimi **rippmenüüst Vali B2C-rakendus**.
1. Valige **Sule** ja seejärel valige **Salvesta ja avalda**.

## <a name="additional-b2c-information"></a>Lisateave B2C kohta

### <a name="customer-migration"></a>Kliendi migreerimine

Kui soovite migreerida kliendikirjeid eelmisest identiteedipakkuja platvormist, siis tehke koostööd Dynamics 365 Commerce meeskonnaga oma klientide migratsiooni vajaduste ülevaatamiseks.

Täiendava Azure AD B2C dokumentatsiooni hankimiseks klientide migratsiooni kohta vaadake teemat [Kasutajate migreerimine Azure Active Directory B2C-sse](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Kohandatud poliitikad

Täiendava teabe saamiseks Azure AD B2C suhtlus- ja poliitikavoogude kohandamise kohta, mis ei kuulu B2C standardpoliitikasse, vaadake teemat [Kohandatud poliitikad Azure Active Directory B2C-s](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Teisene administraator

Teie B2C rentnikku on valikuliselt võimalik lisada teisene administraatorikonto jaotises **Kasutajad**. See võib olla otsene või üldine konto. Kui teil on vaja jagada kontot meeskonnaressursside üleselt, saate luua ka ühise konto. Azure AD B2C-s talletatavate andmete tundlikkuse tõttu tuleb ühist kontot hoolikalt jälgida vastavalt teie ettevõtte turvalisuse tavadele.

### <a name="set-up-a-custom-sign-in-domain"></a>Kohandatud sisselogimisdomeeni loomine

Azure AD B2C võimaldab teil seadistada B2C rentniku jaoks kohandatud Azure AD sisselogimise domeeni. Juhiseid vt B2C [kohandatud domeenide Azure Active Directory lubamine](/azure/active-directory-b2c/custom-domain). 

Kui kasutate kohandatud sisselogimisdomeeni, tuleb domeen sisestada Commerce'i saidiloojasse.

Kohandatud sisselogimise domeeni sisestamiseks saidikonstruktoris järgige neid samme.

1. Saidikonstruktori ülemises parempoolses nurgas valige saidilüliti ja seejärel valige suvand Halda **saite**.
1. Valige vasakul navigeerimispaanil rentniku sätete **saidi autentimise \> häälestus**.
1. Valige jaotises **Saidi autentimise profiilid** suvand **Haldamine**.
1. Paremmenüüs väljaminek valige nupp Redigeeri **(sümbol), mis on seotud saidi autentimisprofiiliga,** mille jaoks soovite sisestada kohandatud domeeni.
1. Sisestage **kohandatud domeeni sisselogimisdomeeni** **väljale** Saidi autentimisprofiili redigeerimine (nt login.fabrikam.com).

> [!WARNING]
> Kui uuendate B2C rentniku Azure AD kohandatud domeeni, mõjutab muudatus loodud loa rentniku väljastaja üksikasju. Väljastaja üksikasjad kaasavad siis B2C-ga antud vaikedomeeni Azure AD asemel kohandatud domeeni. Erinev väljastaja **konfiguratsioon** Commerce headquartersis (**Retail ja Commerce \> Headquartersi \> häälestamise parameetrid Commerce shared parameters \>\> Identity Providers**) muudab süsteemi suhtlust saidi kasutajatega ja võib luua potentsiaalselt uue kliendikirje, kui kasutaja on autentinud uue väljastaja suhtes. Kohandatud domeenimuudatusi tuleb enne kohandatud domeeni lülitumist B2C keskkonnas põhjalikult Azure AD katsetada.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[URL-i ümbersuunamiste hulgiüleslaadimine](upload-bulk-redirects.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
