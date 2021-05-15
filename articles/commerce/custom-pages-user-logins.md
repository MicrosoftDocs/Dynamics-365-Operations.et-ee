---
title: Kohandatud lehtede häälestus kasutajate sisselogimise jaoks
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce kohandatud lehti, mis käsitsevad Azure Active Directory (Azure AD) ettevõtte ja tarbija (B2C) rentnike kohandatud sisselogimisi.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d4a1c2f45d77c3ff9a7bb4dffaf12d877dc04e69
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936776"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Kohandatud lehtede häälestus kasutajate sisselogimise jaoks

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce kohandatud lehti, mis käsitsevad Azure Active Directory (Azure AD) ettevõtte ja tarbija (B2C) rentnike kohandatud sisselogimisi.

Kohandatud lehtede kasutamiseks, mis on rakenduses Dynamics 365 Commerce volitatud käsitsema kasutaja sisselogimise voogusid, peate seadistama Azure AD poliitikad, millele Commerce’i keskkonnas viidatakse. Saate konfigureerida Azure AD B2C poliitikaid „Registreerimine ja sisselogimine”, „Profiili redigeerimine” ja „Parooli lähtestamine”, kasutades Azure AD B2C rakendust. Azure AD B2C rentniku ja poliitika nimedele saab seejärel viidata ettevalmistamise protsessi käigus, mis on tehtud Commerce’i keskkonnas, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).

Kohandatud Commerce’i lehti saab luua, kasutades sisselogimist, registreerumist, konto profiili redigeerimist või üldiseid AAD mooduleid. Nendele kohandatud lehtede jaoks avaldatud lehe URL-idele tuleb seejärel viidata Azure AD B2C poliitika konfiguratsioonides Azure’i portaalis.

> [!WARNING] 
> Azure AD B2C kustutab vana (pärand) kasutajavood 1. augustiks 2021. Seetõttu peaksite plaanima oma kasutajavood migreerida uude soovitatud versiooni. Uus versioon pakub funktsioonide pariteeti ja uusi funktsioone. Lisateabe saamiseks vt [Azure Active Directory B2C kasutajavoog](/azure/active-directory-b2c/user-flow-overview).

>Commerce version 10.0.15 või uuema versiooni mooduliteeki tuleb kasutada soovitatud B2C kasutajavoogudega. Kasutada saab ka Azure AD B2C-s pakutavaid vaikimisi kasutajapoliitika lehti ja lubada lisatud taustapildi, logo ja taustavärvi muudatusi, mis on seotud ettevõtte kaubamärgiga. Kuigi kujunduse võimalused on piiratud, pakuvad kasutajapoliitika vaikelehed Azure AD B2C poliitika funktsioone ilma selleks mõeldud kohandatud lehekülgi loomata ja konfigureerimata. 

## <a name="set-up-b2c-policies"></a>B2C poliitikate seadistamine

Pärast Azure AD B2C rentniku seadistamist ja selle seostamist oma Commerce’i keskkonnaga, avage Azure’i portaalis leht **Azure AD B2C** ja seejärel valige menüüs jaotises **poliitikad** suvand **Kasutaja vood (poliitikad)**.

![Kasutajavoogude (poliitikate) käsk menüüs](./media/B2C_CustomPage_PoliciesMenu.png)

Nüüd saate konfigureerida kasutaja sisselogimise vood „Registreerimine ja sisselogimine”, „Profiili redigeerimine” ja „Parooli lähtestamine”.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Poliitika „Registreerimine ja sisselogimine” konfigureerimine

Poliitika „Registreerimine ja sisselogimine” konfigureerimiseks toimige järgmiselt.

1. Valige suvand **Uus kasutaja voog**, valige **Registreerimine ja sisselogimine** ja seejärel valige vahekaardil **Soovitatav** valik **Loo**.
1. Sisestage poliitika nimi (nt **B2C\_1\_SignInSignUp**).
1. Jaotises **Identiteedipakkujad** valige poliitika jaoks kasutatavad identiteedipakkujad. Minimaalselt peab olema valitud **Registreerimine meili teel**.
1. Veerus **Atribuudi kogumine** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi** ja **Perekonnanimi** juures.
1. Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Identiteedipakkuja**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.

    ![Valitud atribuudid ja nõuded](./media/B2C_SignInSignUp_Attributes.png)

1. Poliitika loomiseks valige **OK**.
1. Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**
1. Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.

    ![Uue poliitika atribuutide leht](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Poliitika nimi on Commerce’i keskkonnas täielikult viidatud. (Viitesse kaasatakse eesliide **B2C\_1\_**.) Poliitikaid ei saa pärast loomist ümber nimetada. Kui asendate oma Commerce’i keskkonna olemasoleva poliitika, saate kustutada algse poliitika ja luua uue poliitika, millel on sama nimi. Teise võimalusena, kui keskkond on juba ette valmistatud, saate teenusetaotluse kaudu esitada uue poliitika nime.

Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks. Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.

### <a name="configure-the-profile-editing-policy"></a>Poliitika „Profiili redigeerimine” konfigureerimine

Poliitika „Profiili redigeerimine” konfigureerimiseks järgige allolevaid etappe.

1. Valige suvand **Uus kasutaja voog**, valige **Profiili redigeerimine** ja seejärel valige vahekaardil **Soovitatav** valik **Loo**.
1. Sisestage poliitika nimi (nt **B2C\_1\_EditProfile**).
1. Jaotises **Identiteedipakkujad** valige poliitika jaoks kasutatavad identiteedipakkujad. Minimaalselt peab olema valitud **Kohaliku konto sisselogimine**.
1. Veerus **Atribuudi kogumine** märkige märkeruudud suvandite **Antud nimi** ja **Perekonnanimi** juures.
1. Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Identiteedipakkuja**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.
1. Poliitika loomiseks valige **OK**.
1. Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**
1. Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.

Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks. Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.

### <a name="configure-the-password-reset-policy"></a>Poliitika „Parooli lähtestamine” konfigureerimine

Poliitika „Parooli lähtestamine” konfigureerimiseks järgige allolevaid etappe.

1. Valige **Uus kasutajavoog** ja seejärel valige suvand **Parooli lähtestamine** ning valige vahekaart **Soovitatav** ja klõpsake nuppu **Loo**.
1. Sisestage poliitika nimi (nt **B2C\_1\_ForgetPassword**).
1. Jaotises **Identiteedipakkujad** valige suvand **Parooli lähtestamine meiliaadressi kasutades**.
1. Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.
1. Poliitika loomiseks valige **OK**.
1. Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**
1. Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.

Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks. Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.

## <a name="build-the-custom-pages"></a>Kohandatud lehtede koostamine

Commerce'is sisalduvad sihtotstarbelised Azure AD moodulid Azure AD B2C kasutajapoliitikate kohandatud lehtede loomiseks. Lehekülgi saab üles ehitada konkreetselt iga kasutajapoliitika lehekülje paigutuse jaoks, kasutades allpool kirjeldatud Azure AD B2C põhimooduleid. Teise võimalusena saab **AAD üldmoodulit** kasutada kõikide lehekülje kavandite ja poliitikate puhul Azure AD B2C-s (isegi lehe paigutuse valikute puhul alltoodud poliitikates). 

- Leheküljepõhised Azure AD moodulid on seotud Azure AD B2C-ga renderdatavate andmesisestusüksustega. Need moodulid annavad teile rohkem kontrolli elementide paigutamise üle oma lehekülgedel. Siiski võib allpool kirjeldatud vaikesätetest väljaspool hälvete arvestamiseks olla vaja üles ehitada rohkem lehti ja mooduli laiendeid.
- **AAD üldmoodulis** luuakse "div" element Azure AD B2C-le, et renderdada kasutajapoliitika lehekülje kavandi kõiki elemente, mis muudab paindlikumaks lehekülje B2C funktsioonid, kuid vähendab positsioonimise ja tööltemise kontrolli (ehkki CSS saab kasutada saidi väljailme ja stiili sobitamiseks).

Saate luua ühe lehe **AAD üldmooduliga** ja kasutada seda kõigi oma kasutajapoliitika lehtede puhul või saate koostada välja kindlad lehed, kasutades individuaalseid Azure AD mooduleid sisselogimiseks, registreerumiseks, profiili redigeerimiseks, parooli lähtestamiseks ja parooli lähtestamise kinnitamiseks. Saate kasutada ka mõlemat segamist, kasutades konkreetseid Azure AD lehekülgi allpool nimetatud lehekülje kavandite jaoks ja üldist AAD-mooduli lehekülge ülejäänud lehekülje kavandite jaoks nendel või muudel kasutaja poliitikalehtedel.

Lisateavet Azure AD mooduliteegiga lähetatud moodulite kohta saate lisateavet [identiteedihalduse lehtedelt ja moodulitest](identity-mgmt-modules.md).

Kasutaja sisselogimiste käsitsemiseks kohandatud ja identiteedimoodulitega lehtede koostamiseks toimige järgmiselt.

1. Liikuge kaubanduse saidiehitajas oma saidile.
1. Koostage järgmised viis malli ja lehekülge (kui teie saidil seda juba pole):
    - Mall **Sisselogimine** ja sisselogimise moodulit kasutav leht.
    - Mall **Registreerimine** ja registreerimise moodulit kasutav leht.
    - Mall **Parooli lähtestamine** ja parooli lähtestamise moodulit kasutav leht.
    - Mall **Parooli lähtestamise kinnitus** ja parooli lähtestamise kinnituse moodulit kasutav leht.
    - Mall **Profiili redigeerimine** ja konto profiili redigeerimise moodulit kasutav leht.

Lehtede loomisel järgige järgmisi juhiseid.

- Kasutage iga lehe või mooduli jaoks paigutust ja stiili, mis vastab kõige paremini teie ettevõtte vajadustele.
- Avaldage kõik lehed ja URL-id, mida tuleb Azure AD B2C seadistuses kasutada.
- Pärast lehtede ja URL-ide avaldamist koguge URL-id, mida tuleb kasutada Azure AD B2C poliitika konfiguratsioonideks. Igale URL-ile lisatakse selle kasutamisel järelliide **?preloadscripts=true**.

> [!IMPORTANT]
> Azure AD B2C-s viidatud leheküljed serveeritakse otse Azure AD B2C rentniku domeenist. Ärge korduvkasutage universaalseid päiseid ja jaluseid, millel on suhtelised lingid. Kuna need lehed majutatakse kasutamisel Azure AD B2C domeenis, tuleks kõikide linkide jaoks kasutada ainult absoluutseid URL-e. Soovitatav on luua kindel päis ja jalus koos kindlate URL-dega teie Azure AD-ga seotud kohandatud lehtede jaoks koos mis tahes ärispetsiifiliste moodulitega, mis nõuavad ühenduse eemaldamist jaemüügiserveriga. Näiteks ei tohi lemmikuid, otsinguriba, sisselogimislinki ja ostukorvi mooduleid kaasata ühtegi lehekülge, mida kasutatakse Azure AD B2C kasutajavoogudes.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C poliitikate konfigureerimine kohandatud lehe teabega 

Naaske Azure’i portaalis lehele **Azure AD B2C** ja valige menüüs jaotises **Poliitikad** suvand **Kasutajavood (poliitikad)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Poliitika „Registreerimine ja sisselogimine” kohandatud lehe teabega värskendamine

Poliitika „Registreerimine ja sisselogimine” kohandatud lehe teabega värskendamiseks tehke järgmist.

1. Valige varasemalt konfigureeritud poliitikas **Registreerimine ja sisselogimine** navigeerimispaanil suvand **Lehe paigutused**.
1. Valige paigutus **Ühendatud registreerimine või sisselogimise leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk sisselogimise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon** versioon **2.1.0** või uuem (nõuab Commerce'i versiooni 10.0.15 või uuema versiooni jaoks mooduliteeki).
1. Valige käsk **Salvesta**.
1. Valige paigutus **Kohaliku konto registreerimise leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk registreerimise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon** versioon **2.1.0** või uuem (nõuab Commerce'i versiooni 10.0.15 või uuema versiooni jaoks mooduliteeki).
1. Järgige jaotises **Kasutaja atribuudid** järgmisi samme.
    1. Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** tulbas **Vajab kinnitamist**.
    1. **E-posti aadressi** atribuudi puhul on soovitatav jätta veerus **Kontrollimist vajav** valitud vaikeväärtus **Jah** valimata. See valik tagab selle, et kasutajad registreeruksid antud meiliaadressiga sisse ja kontrolliksid, et neil on meiliaadress olemas.
    1. Atribuutide **Meiliaadressid**, **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** tulbas **Valikuline**.
1. Valige käsk **Salvesta**.

    ![Kohaliku konto lehe poliitika konfigureerimine](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Poliitika „Profiili redigeerimine” kohandatud lehe teabega värskendamine

Poliitika „Profiili redigeerimine” kohandatud lehe teabega värskendamiseks tehke järgmist.

1. Valige varasemalt konfigureeritud poliitikas **Profiili redigeerimine** navigeerimispaanil suvand **Lehe paigutused**.
1. Valige **Profiili redigeerimise lehekülje** paigutus (sõltuvalt teie ekraanist võib olla vaja kerida allapoole muid paigutuse valikuid).
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk profiili redigeerimise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Valige **Lehe paigutuse versioon** versioon **2.1.0** või uuem (nõuab Commerce'i versiooni 10.0.15 või uuema versiooni jaoks mooduliteeki).
1. Järgige jaotises **Kasutaja atribuudid** järgmisi samme.
    1. Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** tulbas **Valikuline**.
    1. Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** tulbas **Vajab kinnitamist**.
1. Valige käsk **Salvesta**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Poliitika „Parooli lähtestamine” kohandatud lehe teabega värskendamine

Poliitika „Parooli lähtestamine” kohandatud lehe teabega värskendamiseks tehke järgmist.

1. Valige varasemalt konfigureeritud poliitikas **Parooli lähtestamine** navigeerimispaanil suvand **Lehe paigutused**.
1. Valige paigutus **Unustasin parooli leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk parooli lähtestamise kinnitamise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon** versioon **2.1.0** või uuem (nõuab Commerce'i versiooni 10.0.15 või uuema versiooni jaoks mooduliteeki).
2. Valige käsk **Salvesta**.
3. Valige paigutus **Muuda parooli leht**.
4. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
5. Sisestage väljal **Kohandatud lehe URL** täispikk parooli lähtestamise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. Valige väljal **Lehe paigutuse versioon** versioon **2.1.0** või uuem (nõuab Commerce'i versiooni 10.0.15 või uuema versiooni jaoks mooduliteeki).
7. Valige käsk **Salvesta**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Siltide ja kirjelduste vaikimisi tekstistringide kohandamine

Mooduliteegis on sisselogimise moodulid eeltäidetud siltide ja kirjelduste vaiketekstistringidega. Stringe saate kohandada selle mooduli atribuutide paanil, millega töötate. Täiendavad stringid leheküljel (nt **Unustasid parooli?** lingitekst või **Konto loomise** kutse tegevuse tekstile) nõuavad Commerce'i tarkvara arenduskomplekti (SDK) kasutamist ja väärtuste uuendamist failis global.json sisselogimismooduli jaoks.

Näiteks unustatud parooli lingi vaiketekst on **Unustatud parool?**. Järgnevalt on näidatud see vaiketekst sisselogimise lehel.

![Sisselogimislehe ununenud parooli lingi vaiketekst](./media/B2C_SignUp_ModuleFace.png)

Siiski saate mooduliteegi sisselogimismooduli failis global.json muuta teksti väärtuseks **Kas unustasite parooli?**, nagu järgmises näites on näidatud.

![Värskendatud lingi tekst logisse mooduli Global. JSON failis](./media/B2C_CustomizingStringsForModule.png)

Pärast faili global.json värskendamist ja muudatuste avaldamist ilmub sisselogimise moodulil uus tekst nii Commerce'is kui ka raalajas sisselogimise lehel.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]