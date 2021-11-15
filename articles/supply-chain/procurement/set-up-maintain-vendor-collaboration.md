---
title: Hankija koostöö seadistamine ja haldamine
description: Selles teemas selgitatakse, kuidas seadistada hankija koostööd rakenduses Dynamics 365 Supply Chain Management. Samuti selgitatakse, kuidas varustada uusi tarnijate koostöökasutajaid ja hallata nende kasutajate turberolle.
author: Henrikan
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b635255fffa6fd3c6612cd248dc692df204aa76d
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651978"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Hankija koostöö seadistamine ja haldamine

[!include [banner](../includes/banner.md)]

Tarnija koostööliides pakub välistele hankija kasutajatele piiratud hulga teavet ostutellimuste, arvete ja saadetise laoseisu kohta. Selle liidese kaudu saab müüja vastata ka pakkumise päringutele (RFQ) ning vaadata ja muuta ettevõtte põhiteavet.

Selles teemas selgitatakse, kuidas seadistada hankija koostööd rakenduses Dynamics 365 Supply Chain Management. Samuti selgitatakse, kuidas seadistada töövoogu uute tarnijate koostöökasutajate loomiseks ja kuidas hallata nende kasutajate turberolle.

> [!NOTE]
> Teave turberollide seadistamise kohta tarnija koostöö jaoks kehtib ainult Finance and Operationsi praeguse versiooni kohta. Microsoft Dynamics AX 7.0 (veebruar 2016) ja rakenduse Microsoft Dynamics AX versiooni 7.0.1 (mai 2016) puhul saate hankijatega koostööd teha, kasutades moodulit **Hankija portaal**. Lisateavet Microsoft Dynamics AX-i hankija portaali kasutajaõiguste kohta leiate artiklist [Hankija portaali kasaja turvalisus](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Seadistage hankija koostöö turberollid

Hankespetsialist või hankija, kellel on piisavad õigused, saab taotleda kontaktisiku määramist kasutajaks, lubades kontaktisiku kirjes **Luba hankijast kasutaja**. Ettevalmistusprotsessi käigus valitakse uuele väliskasutajale kasutajaõigused ja esitatakse uue tarnija kasutaja taotlus. On oluline, et seadistaksite õigesti tarnija kasutaja päringus valimiseks saadaval olevad kasutajaõigused. Vastasel juhul võidakse hankijatele anda juurdepääs teabele, millele neil ei peaks olema juurdepääsu Supply Chain Management tarneahela halduses.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Seadistage turberollid, mida saab valida, kui kontaktisiku jaoks kasutatakse uut kasutajapäringut

1. Valige **Süsteemi haldus** &gt; **Turvalisus** &gt; **Välised rollid**.
2. Valige **Uus** ja seejärel turberoll ja **Hankija** osapoole roll.

Võib-olla soovite lisada suvandis Supply Chain Management pakutavad rollid **Hankija administraator (väline)** ja **Hankija (väline)**. Teise võimalusena saate kasutada teie ettevõtte loodud turberolle.

Peaksite tegema rolli **Hankija administraator (väline)** kättesaadavaks ainult siis, kui müüjad peaksid saama luua uusi kontakte, esitada tarnija koostöö kasutajataotlusi uute kasutajate kohta ja kasutajateabe muudatusi ning käsitleda neid taotlusi töövoo kaudu.

Kui kavatsete hankija kontaktid ja kasutajad käsitsi seadistada, saate teha kättesaadavaks ainult **Hankija (väline) rolli**. See roll on siis ainus roll, mida saab hankija kasutaja päringu kaudu taotleda.

> [!NOTE]
> Roll **SystemUser** antakse automaatselt, kui loote uue kasutajakonto käsitsi. Seetõttu peate selle rolli eemaldama ja määrama rolli **SystemExternalUser**. Kui uusi kasutajakontosid luuakse töövoo kaudu, mille algatas hankija kasutaja taotlus uue kasutaja loomiseks, määratakse üks või mitu rolli, mille olete seadistanud hankija koostööks, ja roll **SystemExternalUser**.

#### <a name="vendor-admin-external-security-role"></a>Hankija administraatori (väline) turberoll

Rolli **Hankija eadministraator (väline)** saab kasutada väliste hankijate jaoks, kes haldavad hankija kontaktteavet ja esitavad taotlusi uute hankijate koostöökasutajate loomiseks. Selle turberolliga väliskasutajad saavad täita järgmisi ülesandeid.

- Saate vaadata ja muuta kontaktisiku teavet, nagu isiku ametinimetus, e-posti aadress ja telefoninumber.
- Lisage uus või olemasolev kontaktisik hankija kontodele, mille kontaktiks nad on.
- Kustutage kõik nende loodud kontaktisikud.
- Aktiveerige või inaktiveerige seos kontaktisiku ja hankija konto vahel. Pärast kontaktisiku ja hankija konto vahelise seose inaktiveerimist ei saa kontaktisikule uutel ostutellimustel ega muudel dokumentidel viidata.
- Keelake või lubage kontaktisiku juurdepääs hankija koostööliidese dokumentidele, mis on seotud hankija kontoga. Pärast kontaktisiku ja hankija konto vahelise seose inaktiveerimist keelatakse alati juurdepääs hankija kontoga seotud dokumentidele.
- Taotlege kontaktisikule uut kasutajakontot, kasutades toimingut **Luba kasutaja**.
- Taotlege kontaktisiku kasutajakonto inaktiveerimist.
- Turberollide lisamiseks või eemaldamiseks taotleda kontaktisiku kasutajakonto muutmist.
- Kuva RFQ-d.

#### <a name="vendor-external-security-role"></a>Hankija (väline) turberoll

**Hankija (väline) rolli** saab kasutada väliste hankijate jaoks, kes töötavad ostutellimustega. Selle turberolliga väliskasutajad saavad täita järgmisi ülesandeid.

- Ostutellimustele vastamine ja nende kohta teabe vaatamine.
- Säilitage hankijate koostööarveid.
- Vaata saadetiste laoseisu.
- Kuva ja vasta RFQ-dele.
- Kuva hankija teave.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Seadistage turberollid, mida kasutatakse potentsiaalsete hankijate liitumisel

Võimalike hankijate registreerimistaotluse kaudu algatatud hankijate jaoks peate seadistama välise turberolli. See roll määratakse uutele kasutajatele ettevalmistamise käigus, mida juhib **Kasutaja päringu töövoog (platvorm)** tüüpi töövoog. Lisateavet leiate selle teema hilisemast jaotisest [Seadistage töövood hankija koostöö kasutajate taotluste töötlemiseks](#set-up-workflows-to-process-vendor-collaboration-user-requests).

Lisateavet potentsiaalsete tarnijate kaasamise kohta leiate jaotisest [Kaasatud hankijad](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Seadistage turberoll, mida kasutatakse uue potentsiaalse hankija kasutaja taotluse esitamisel

1. Valige **Süsteemi haldus** > **Turvalisus** > **Välised rollid**.
2. Valige **Uus** ja seejärel turberoll ja **Potentsiaalne hankija** osapoole roll.

Peaksite lisama Supply Chain Management tarneahela halduses pakutava rolli **Hankija (väline)**.

Turvaroll annab juurdepääsu ainult uue hankija registreerimisviisardi jaoks.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Seadistage töövood hankjia koostöö kasutajate taotluste töötlemiseks

Kõigi asjakohaste ülesannete lõpuleviimise ja asjakohaste kinnituste andmise tagamiseks peate seadistama hankija koostöö kasutajataotluste käsitlemiseks töövood.

Hankija koostöö kasutajataotlused esitavad kas välised hankijad, kellel on **Hankija adminsitraator (väline)** turberoll või sarnased õigused, või teie ettevõtte hankespetsialistid. Neid saab genereerida ka tulevaste hankijate registreerimistaotlustest hankija liitumisprotsessi ajal.

Taotlusi on kolme tüüpi.

- Taotleb uue kasutaja loomist
- Taotleb olemasoleva kasutaja inaktiveerimist
- Taotleb olemasoleva kasutaja turberollide muutmist

Lisateabe saamiseks hankija koostöö kasutajataotluste kohta vaata teemast [Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md).

Peate looma kaks või enam töövoogu, et töödelda kõiki kolme tüüpi hankija koostöö kasutajataotlusi. Uued töövood luuakse lehel **Kasutaja töövood**.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Näide töövoost uute kasutajate loomiseks ja turberollide muutmiseks

Hankija kasutajate taotluste käsitlemiseks uute kasutajate loomiseks ja turberollide muutmiseks saate töövoo algusesse panna hargnemise tingimuse. Sel viisil kasutatakse erinevat töövoo haru olenevalt sellest, kas taotlus on luua uus kasutaja või muuta olemasolevat kasutajat.

Selle hargnemise seadistamiseks looge uus **Kasutajapäringu töövoog (platvorm)** tüüpi töövoog. Selle töövoo harud võivad sisaldada järgmisi elemente.

#### <a name="branch-to-provision-new-users"></a>Haru uute kasutajate loomiseks

1. Määrake heakskiitmisülesanne isikule, kes vastutab selle kinnitamise eest, et uutele kasutajatele tuleks anda juurdepääs hankijate koostööteabele.
2. Määrake ülesanne inimesele, kes vastutab Azure'i portaalis uute Microsoft Azure Active Directory (Azure AD) kasutajakontode taotlemise eest. Kasutage selle sammu jaoks eelmääratletud ülesannet **Saada Azure B2B kasutaja kutse**. B2B kasutajaid saab automaatselt Azure AD-sse eksportida. Kasutage eelmääratletud **Määrake Azure AD B2B kasutaja**. Lisateavet leiate teemast [B2B kasutajate eksportimine Azure AD-sse](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Määrake kinnitamisülesanne inimesele, kes laadib Azure'i üles. Kui konto loomine ebaõnnestub, lükkab see inimene ülesande tagasi ja lõpetab töövoo. Selle kinnitamisülesande saab vahele jätta, kui olete lisanud sammu, mis ekspordib B2B rakendusliidese (API) kaudu automaatselt Azure'i uued kasutajakontod.
4. Lisage automaatne ülesanne, mis loob uue kasutaja. Kasutage selle sammu jaoks eelmääratletud ülesannet **Kasutaja automaatne määramine**.
5. Lisage ülesanne, mis teavitab uut kasutajat. Võib-olla soovite saata uuele kasutajale tervitusmeili, mis sisaldab Supply Chain Management URL-i. See meil võib kasutada malli, mille loote lehel **E-kirjad** ja seejärel valite lehel **Kasutaja töövoo parameetrid**. Mall võib sisaldada märgendit **%portalURL%**. Kui tervitusmeil luuakse, asendatakse see silt Supply Chain Management rentniku URL-iga.

    > [!NOTE]
    > Seda töövoogu saab kasutada mitme stsenaariumi korral, mis hõlmavad kasutaja kaasamist. Näiteks saab seda kasutada siis, kui potentsiaalsed müüjad või kontaktisikud nõuavad hankija koostöökontot. Seetõttu peaksite e-kirja sõnastama üldise väitena, mida saab kasutada mitmel otstarbel.

#### <a name="branch-to-modify-security-roles"></a>Haru turberollide muutmiseks

1. Määrake kinnitusülesanne isikule, kes vastutab turberollide muudatuste kinnitamise eest.
2. Lisage automaatne ülesanne, mis lisab või eemaldab asjakohased turberollid. Kasutage selle sammu jaoks ülesannet **Kasutaja automaatne määramine**.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Kasutaja inaktiveerimise töövoo näide

Looge **Inaktiveeri kasutajapäringu töövooplatvorm** töövoog ja lisage seejärel järgmised toimingud.

1. Määrake kinnitamissülesanne isikule, kes vastutab kasutajate inaktiveerimise taotluste vastuvõtmise eest. Selle kinnitusetapi automatiseerimiseks saate lisada tingimusi.
2. Lisage automaatne ülesanne, mis inaktiveerib kasutaja. Kasutage selle sammu jaoks ülesannet **Kasutaja automaatne inaktiveerimine**.
3. Lisage kõik vajalikud puhastustööd. Näiteks saate lisada ülesande, mis eemaldab konto Azure'i portaali kataloogist.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Lubage hankija koostöö konkreetse hankija jaoks

Enne kasutajakonto loomist kellelegi, kes kasutab hankija koostööd, peate seadistama hankija nii, et see saaks kasutada hankija koostööd. Seadistage väli **Koostöö aktiveerimine** lehe **Hankijad** vahekaardil **Üldine**. Valikud on järgmised:

- **Aktiivne (ostutellimus kinnitatakse automaatselt)** – ostutellimused kinnitatakse automaatselt, kui hankija kinnitab need ilma muudatuste taotluseta.
- **Aktiivne (ostutellimust ei kinnitata automaatselt)** – teie organisatsioon peab ostutellimused käsitsi kinnitama pärast seda, kui hankija on need kinnitanud.

> [!NOTE]
> Selle ülesande saavad täita ka teie ettevõtte hankespetsialistid.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Uute hankijate koostöö kasutajate varustamise tõrkeotsing

Uued hankija koostöökasutajad on ette nähtud töövoo kaudu, mille seadistate hankijate koostöö kasutajate taotluste töötlemiseks **Hankijast kasutaja määramine** tüüpi.

Kui uue hankija koostöökasutaja meiliaadress kuulub domeeni, mis on Azure'is rentnikuna registreeritud (st kui see on hallatava domeeni konto), peab meiliaadress olema olemasolev Azure AD konto. Vastasel juhul ei saa ettevalmistusprotsessi lõpule viia.

Lisateavet protsessi kohta, mida kasutatakse Azure AD kontohalduse töövoo ülesandes **Saada Azure B2B kasutaja kutse**, vt teemat [Azure Active Directory B2B koostöö](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Lisaressursid

[Hankija koostöö väliste hankijatega](vendor-collaboration-work-external-vendors.md)

Vaadake lühikest videot hankija liitumisprotsessi kohta: [Uue hankija kaasamine](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]