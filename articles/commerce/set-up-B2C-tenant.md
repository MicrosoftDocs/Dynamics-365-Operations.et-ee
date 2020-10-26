---
title: B2C rentniku seadistus Kaubanduses
description: Selles teemas kirjeldatakse kuidas seadistada Azure Active Directory (Azure AD) ettevõtja ja tarbija vahelisi (B2C) rentnikke kasutaja saidi autentimiseks rakenduses Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1910563865a21dab3345a82711ead9b9e57b92fa
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980960"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C rentniku seadistus Kaubanduses

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse kuidas seadistada Azure Active Directory (Azure AD) ettevõtja ja tarbija vahelisi (B2C) rentnikke kasutaja saidi autentimiseks rakenduses Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce kasutab Azure AD B2C'd kasutaja mandaadi ja autentimise voogude toetamiseks. Kasutaja saab nende voogude kaudu registreeruda, sisse logida ja lähtestada parooli. Azure AD B2C talletab kasutaja tundliku autentimisteabe, nt kasutajanime ja parooli. B2C rentniku kasutajakirje salvestab kas kohaliku B2C kontokirje või B2C sotsiaalse identiteedi pakkuja kirje. Need B2C kirjed lingitakse Commerce'i keskkonna kliendikirjetega.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Olemasoleva AAD B2C rentniku loomine või linkimine Azure'i portaalis

1. Logige sisse [Azure’i portaali](https://portal.azure.com/).
1. Valige Azure'i portaali menüüst käsk **Loo ressurss**. Veenduge, et kasutate tellimust ja kataloogi, mis on seotud teie Commerce'i keskkonnaga.

    ![Ressursi loomine Azure'i portaalis](./media/B2CImage_1.png)

1. Avage **Identiteedi \> Azure Active Directory B2C**.
1. Kui olete lehel **Uue B2C üürniku loomine või olemasoleva rentnikuga linkimine**, kasutage ühte valikutest, mis sobib kõige paremini teie ettevõtte vajadustega.

    - **Loo uus Azure AD B2C rentnik**: kasutage seda valikut uue AAD B2C rentniku loomiseks.
        1. Valige käsk **Loo uus Azure AD B2C rentnik**.
        1. Sisestage organisatsiooni nimi jaotises **Organisatsiooni nimi**.
        1. Sisestage algne domeeninimi jaotises **Algne domeeninimi**.
        1. Valige riik ja piirkond jaotises **Riik või piirkond**.
        1. Rentniku loomiseks valige **Loo**.

     ![Uue Azure AD rentniku loomine](./media/B2CImage_2.png)

     - **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**: kasutage seda suvandit, kui teil on Azure AD B2C rentnik, mida soovite linkida.
        1. Valige **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**.
        1. Jaotises **Azure AD B2C rentnik** valige sobiv B2C rentnik. Kui valikukastis kuvatakse teade „Ei leitud ühtegi sobilikku B2C rentnikku”, pole teil kehtivat sobilikku B2C rentnikku ja teil on vaja luua uus.
        1. Tehke jaotises **Ressursigrupp** valik **Loo uus**. Sisestage ressursirühmale **Nimi**, mis sisaldab rentnikku ja valige **Ressursigrupi asukoht** ning seejärel **Loo**.

    ![Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega](./media/B2CImage_3.png)

1. Kui uus Azure AD B2C kaust on loodud (see võib võtta mõne hetke), kuvatakse armatuurlaual link uuele kaustale. See link juhatab teid lehele „Tere tulemast Azure Active Directory B2C-sse”.

    ![Uue AAD kausta link](./media/B2CImage_4.png)

> [!NOTE]
> Kui teie Azure'i kontol on mitu tellimust või olete seadistanud B2C rentniku aktiivsele tellimusele linkimata, suunab ribareklaam **Tõrkeotsing** rentnikku tellimusega linkima. Valige tõrkeotsingu teade ja järgige tellimuse probleemi lahendamiseks juhiseid.

Järgmine pilt on Azure AD B2C ribareklaami **Tõrkeotsing** näide.

![Kuvatav hoiatus Kataloogist puudub aktiivne tellimus](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>B2C rakenduse loomine

Kui B2C rentnik on loodud, tuleb rentnikus luua B2C rakendus Commerce'i toimingutega suhtlemiseks.

B2C rakenduse loomiseks toimige järgmiselt.

1. Tehke Azure'i portaalis valik **Rakendused (pärand)** ja seejärel **Lisa**.
1. Jaotises **Nimi** sisestage soovitud AAD B2C rakenduse nimi.
1. Jaotises **Veebirakendus/veebi-API** valige parameetrile **Veebirakenduse/veebi-API kaasamine** väärtus **Jah**.
1. Määrake aarameetri **Varjatud voo lubamine** väärtuseks **Jah** (vaikeväärtus).
1. Jaotises **Vastuse URL** sisestage oma sihtotstarbelised vastuse URL-id. Vaadake allpool teemat [Vastuse URL-id](#reply-urls) vastuse URL-ide ja nende vormindamise kohta lisateabe saamiseks.
1. Määrake parameetri **Algse kliendi kaasamine** väärtuseks **Ei** (vaikeväärtus).
1. Valige **Loo**.

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

Saate valida, kas soovite kasutada Azure AD pakutavaid vaikimisi kasutajavooge, mis kuvavad AAD B2C poolt hallatavat lehekülge. Saate ka luua HTML-lehe, et juhtida nende kasutajavoo kogemuste välimust ja olemust. 

Kasutajapoliitika lehtede kohandamiseks Dynamics 365 Commerce'is vaadake teemat [Kohandatud lehtede häälestamine kasutaja sisselogimisteks](custom-pages-user-logins.md). Lisateavet leiate teemast [Azure Active Directory B2C kasutuskogemuse liidese kohandamine](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Registreerumise ja sisselogimise kasutajavoo poliitika loomine

Registreerimise ja sisselogimise kasutajavoo poliitika loomiseks toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Vahekaardil **Soovitatav** valige **Registreeru ja logi sisse**.
1. Sisestage poliitika nimi väljale **Nimi**. See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).
1. Märkige sobiv ruut jaotises **Identiteedipakkujad**.
1. Valige sobiv ettevõtte valik jaotises **Mitmikautentimine**. 
1. Jaotises **Kasutaja atribuudid ja nõuded** valige suvandid atribuutide kogumiseks või nõuete tagastamiseks vastavalt vajadusele. Commerce nõuab järgmisi vaikesätteid.

    | **Atribuudi kogumine** | **Nõude tagastamine** |
    | ---------------------- | ----------------- |
    | Meiliaadress          | Meiliaadressid   |
    | Eesnimi             | Eesnimi        |
    |                        | Identiteedipakkuja |
    | Perekonnanimi                | Perekonnanimi           |
    |                        | Kasutaja objekti ID  |

1. Valige **Loo**.

Järgmine pilt on Azure AD B2C registreerumise ja sisselogimise kasutajavoo näide.

![Registreerimise ja sisselogimise poliitika sätted](./media/B2CImage_11.png)

Järgmine pilt näitab valikut **Kasutajavoo käitamine** Azure AD B2C registreerumise ja sisselogimise kasutajavoos.

![Kasutajavoo suvandi käitamine poliitika voos](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profiili loomine kasutajavoo poliitika redigeerimisel

Profiili redigeerimise kasutajavoo poliitika loomiseks toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Vahekaardil **Soovitatav** valige **Profiili redigeerimine**.
1. Jaotises **Nimi** sisestage profiil kasutajavoogu redigeerides. See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).
1. Valige jaotises **Identiteedipakkujad** suvand **Kohaliku konto sisselogimine**.
1. Jaotises **Kasutaja atribuudid** märkige järgmised ruudud.
    - **Meiliaadress** (ainult **Tagastuse nõue**)
    - **Eesnimi** (**Atribuudi kogumine** ja **Tagastuse nõue**)
    - **Identiteedipakkuja** (ainult **Tagastuse nõue**)
    - **Perekonnanimi** (**Atribuudi kogumine** ja **Tagastuse nõue**)
    - **Kasutaja objekti ID** (ainult **Tagastuse nõue**)
1. Valige **Loo**.

Järgmine pilt on Azure AD B2C profiili redigeerimise kasutajavoo näide.

![Profiili redigeerimise kasutajavoo loomine](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Parooli lähtestamise kasutajavoo poliitika loomine

Parooli lähtestamiseks kasutajavoo poliitikas toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Vahekaardil **Soovitatav** valige **Parooli lähtestamine**.
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

- [Amazon](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Üksik rentnik)](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsofti konto](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Sotsiaalse identiteedipakkuja lisamine ja seadistamine

Sotsiaalse identiteedipakkuja lisamiseks ja seadistamiseks toimige järgmiselt.  

1. Azure'i portaalis liikuge jaotisesse **Identiteedipakkujad**.
1. Valige **Lisa**. Kuvatakse aken **Identiteedipakkuja lisamine**.
1. Jaotises **Nimi** sisestage kasutajatele kuvatav nimi teie sisselogimisaknas.
1. Valige jaotises **Identiteedipakkuja tüüp** loendist identiteedipakkuja.
1. Valige nupp **OK**.
1. Valige **Selle identiteedipakkuja häälestamine** aknale **Sotsiaalse identiteedipakkuja häälestamine** juurde pääsemiseks.
1. Jaotises **Kliendi ID** sisestage kliendi ID, mille saite identiteedipakkuja rakenduse häälestamisel.
1. Jaotises **Kliendi saladus** sisestage kliendi saladus, mille saite identiteedipakkuja rakenduse häälestamisel.
1. Kasutajavoo lisamine sisselogimise registreerumise poliitika jaoks.
1. Avage jaotis **Azure AD B2C – kasutajavood (poliitikad) \> {teie sisselogimise registreerumise poliitika} \> Identiteedipakkujad**.
1. Sisselogimise/registreerumise kasutajavoo poliitika manustamiseks valige kõik identiteedipakkujad, mille olete oma kontole seadistanud. Nende testimiseks valige käsk **Kasutajavoo käitamine** igale identiteedipakkujale. Uus vahekaart kuvab sisselogimisakna, kus kuvatakse uus identiteedipakkuja valikuväli.

Järgmisel pildil kuvatakse näited akende **Identiteedipakkuja lisamine** ja **Sotsiaalse identiteedipakkuja häälestamine** kohta Azure AD B2C-s.

![Sotsiaalse identiteedipakkuja lisamine rakendusse](./media/B2CImage_14.png)

Järgmisel pildil kuvatakse näide, kuidas valida identiteedipakkujaid Azure AD B2C lehel **Identiteedipakkujad**.

![Valige kõik enda poliitika jaoks lubatavad sotsiaalse identiteedipakkujad](./media/B2CImage_16.png)

Järgmisel pildil kuvatakse näide vaikimisi sisselogimisaken, millel on sotsiaalse identiteedipakkuja sisselogimisnupp.

![Näide vaikimisi sisselogimisaknast sotsiaalse identiteedipakkuja sisselogimisnupuga](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce'i peakontori värskendamine uue Azure AD B2C teabega

Kui eelpool loetletud Azure AD B2C ettevalmistavad etapid on lõpule viidud, peab Azure AD B2C rakendus olema registreeritud teie Dynamics 365 Commerce'i keskkonnas.

Peakontori väsrkendamiseks uue Azure AD B2C teabega toimige järgmiselt.

1. Avage Commerce'i jaotis **Commerce'i jagatud parameetrid** ja valige vasakpoolsest menüüst **Identiteedipakkujad**.
1. Jaotises **Identiteedipakkujad** toimige järgmiselt.
    1. Sisestage identiteedipakkuja väljaandja URL lahtrisse **Väljaandja**. Oma väljaandja URL-i saamiseks avage teema [Väljaandja URL-i hankimine](#obtain-issuer-url).
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

### <a name="obtain-issuer-url"></a>Väljaandja URL-i hankimine

Oma identiteedipakkuja väljaandja URL-i hankimiseks toimige järgmiselt.

1. Looge metaandmete aadressi URL järgmises vormingus, kasutades oma B2C rentnikku ja poliitikat: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Näide: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Sisestage metaandmete aadressi URL brauseri aadressiribale.
1. Kopeerige metaandmetest identiteedipakkuja väljaandja URL (väärtus **„väljaandja”**).
    - Näide: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>B2C rentniku konfigureerimine kaubanduse saidiehitajas

Kui teie Azure AD B2C rentniku häälestus on lõpule viidud, tuleb konfigureerida B2C rentnik kaubanduse saidiehitajas. Konfiguratsioonietapid hõlmavad B2C rakenduse teabe kogumist Azure'i portaalist, selle B2C rakenduse teabe sisestamist saidiehitajasse ja seejärel B2C rakenduse seostamist teie saidi ja kanaliga.

### <a name="collect-the-required-application-information"></a>Nõutava rakenduseteabe kogumine

Nõutava rakenduseteabe kogumiseks toimige järgmiselt.

1. Avage Azure'i portaalis jaotis **Avaleht \> Azure AD B2C - rakendused**.
1. Valige oma rakendus ja seejärel valige valige vasakpoolsel navigeerimispaanil **Atribuudid** rakenduse üksikasjade hankimiseks.
1. Väljalt **Rakenduse ID** hankige rakenduse ID oma B2C rentnikus loodud B2C rakendusest. See sisestatakse hiljem saidiehitajas väärtuseks **Kliendi GUID**.
1. Hankige vastuse URL jaotisest **Vastuse URL**.
1. Avage jaotis **Avaleht \> Azure AD B2C – kasutajavood (poliitikad)** ja seejärel hankige kõigi kasutajavoo poliitikate nimed.

Järgmisel pildil kuvatakse näide lehest **Azure AD B2C – rakendused**.

![Oma rentnikus B2C rakendusse liikumine](./media/B2CImage_19.png)

Järgmisel pildil kuvatakse näide rakenduse lehest **Atribuudid** Azure AD B2C-s. 

![Rakenduse ID kopeerimine B2C rakenduse atribuutidest](./media/B2CImage_21.png)

Järgmisel pildil kuvatakse näide kasutajavoo poliitikatest lehel **Azure AD B2C – kasutajavood (poliitikad)**.

![Kõigi B2C poliitikavoo nimede kogumine](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>Oma AAD B2C üürniku rakenduse teabe sisestamine Commerce'i

Enne B2C rentniku seostamist oma saitidega, peate sisestama Azure AD B2C rentniku andmed kaubanduse saidiehitajasse.

AAD B2C rentniku rakenduse teabe lisamiseks Commerce'i toimige järgmiselt.

1. Logige sisse administraatorina oma keskkonna kaubanduse saidiehitajasse.
1. Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.
1. Jaotises **Rentniku sätted** valige suvand **B2C sätted**. 
1. Valige põhiaknas **B2C rakendused** kõrvalt jaotis **Halda**. (Kui teie rentnik kuvatakse B2C rakenduste loendis, siis on administraator selle juba lisanud. Veenduge, et etapis 6 olevad üksused vastaksid teie B2C rakendusele.)
1. Valige **Lisa B2C rakendus**.
1. Sisestage järgmised nõutavad üksused kuvatud vormile, kasutades oma B2C rentniku ja rakenduse väärtusi. Väljad, mis ei ole kohustuslikud (ilma tärnita), võivad jääda tühjaks.

    - **Rakenduse nimi**: teie B2C rakenduse nimi, näiteks „Fabrikam B2C”.
    - **Rentniku nimi**: teie B2C rentniku nimi (nt „fabrikam“, kui domeen kuvatakse B2C rentnikule kui „fabrikam.onmicrosoft.com“). 
    - **Poliitika ID parooli unustamise korral**: kasutajavoo poliitika ID parooli unustamise korral, näiteks „B2C_1_PasswordReset”.
    - **Registreerumise sisselogimise poliitika ID**: kasutajavoo poliitika ID registreerumiseks ja sisselogimiseks, näiteks „B2C_1_signup_signin”.
    - **Kliendi GUID**: B2C rakenduse ID, näiteks „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.
    - **Profiilipoliitika ID redigeerimine**: kasutajavoo poliitika ID profiili redigeerimiseks, näiteks „B2C_1A_ProfileEdit”.

1. Valige nupp **OK**. Nüüd peaks olema teie B2C rakenduse nimi loendis kuvatud.
1. Oma muudatuste salvestamiseks valige **Salvesta**.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C rakenduse seostamine teie saidi ja kanaliga

> [!WARNING]
> Kui teie sait on juba seostatud B2C rakendusega, siis teise B2C rakendusse üleminekul eemaldatakse praegused juba sellesse keskkonda registreerunud kasutajatele loodud viited. Kui seda muudetakse, ei ole kasutajatele saadaval ükski praegu määratud B2C rakendusega seotud mandaat. 
> 
> Uuendage B2C rakendust ainult siis, kui seadistate kanali B2C rakendust esimest korda või kui soovite, et kasutajad registreeriksid selle kanali uue B2C rakendusega oma mandaadid uuesti. Olge ettevaatlik kanalite seostamisel B2C rakendustega ja nimetage rakendusi selgelt. Kui kanal ei ole seostatud B2C rakendusega alljärgnevate etappidega, on sisestatakse kasutajad teie saidi kanalisse siselogimisel B2C rakendusse olekuga **vaikimisi** B2C rakenduste loendis **Rentniku sätted \> B2C sätted**.

B2C rakenduse seostamiseks teie saidi ja kanaliga toimige järgnevalt.

1. Liikuge oma saidile kaubanduse saidiehitajas.
1. Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.
1. Jaotises **Saidi sätted**valige **Kanalid**.
1. Valige oma kanal põhiakna jaotises **Kanalid**.
1. Parempoolsel kanali atribuutide paanil valige oma B2C rakenduse nimi rippmenüüst **B2C rakenduse valimine**.
1. Valige **Sule** ja seejärel valige **Salvesta ja avalda**.

## <a name="additional-b2c-information"></a>Lisateave B2C kohta

### <a name="customer-migration"></a>Kliendi migreerimine

Kui soovite migreerida kliendikirjeid eelmisest identiteedipakkuja platvormist, siis tehke koostööd Dynamics 365 Commerce meeskonnaga oma klientide migratsiooni vajaduste ülevaatamiseks.

Täiendava Azure AD B2C dokumentatsiooni hankimiseks klientide migratsiooni kohta vaadake teemat [Kasutajate migreerimine Azure Active Directory B2C-sse](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Kohandatud poliitikad

Täiendava teabe saamiseks Azure AD B2C suhtlus- ja poliitikavoogude kohandamise kohta, mis ei kuulu B2C standardpoliitikasse, vaadake teemat [Kohandatud poliitikad Azure Active Directory B2C-s](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Teisene administraator

Teie B2C rentnikku on valikuliselt võimalik lisada teisene administraatorikonto jaotises **Kasutajad**. See võib olla otsene või üldine konto. Kui teil on vaja jagada kontot meeskonnaressursside üleselt, saate luua ka ühise konto. Azure AD B2C-s talletatavate andmete tundlikkuse tõttu tuleb ühist kontot hoolikalt jälgida vastavalt teie ettevõtte turvalisuse tavadele.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[URL-i hulgiümbersuunamiste üleslaadimine](upload-bulk-redirects.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
