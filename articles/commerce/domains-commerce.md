---
title: Domeenid Dynamics 365 Commerce'is
description: Selles teemas kirjeldatakse, kuidas käsitsetakse domeene teenuses Microsoft Dynamics 365 Commerce.
author: BrShoo
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bf96c47b8f5e940ffdd9241c3bdda4162a3101c42004c58c431f135f11c39d14
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733987"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domeenid Dynamics 365 Commerce'is

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas käsitsetakse domeene teenuses Microsoft Dynamics 365 Commerce.

Domeenid on veebiaadressid, mida kasutatakse veebibrauseris teenuse Dynamics 365 Commerce saitidele navigeerimiseks. Saate juhtida oma domeeni haldamist valitud domeeni nimeserveri (DNS) pakkuja abil. Domeenidele viidatakse teenuse Dynamics 365 Commerce saidiehitajas, et koordineerida seda, kuidas saidile pärast avaldamist juurde pääseb. Selles teemas antakse ülevaade sellest, kuidas domeene käsitletakse ja viidatakse kogu kaubanduse saidi arendamise ja käivitamise töötsükli jooksul.

## <a name="provisioning-and-supported-host-names"></a>Hostinimede ettevalmistamine ja toetamine

E-kaubanduse keskkonna ettevalmistamisel teenuses [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) kasutatakse juurutatud Commerce'i keskkonnaga seotud domeenide sisestamiseks e-kaubanduse ettevalmistamise kuval välja **Toetatud hostinimed**. Need domeenid on kliendile suunatud domeeninimede serveri (DNS) nimed, kus majutatakse e-kaubanduse veebisaite. Domeeni sisestamine selles etapis ei hakka domeeni liiklust teenusesse Dynamics 365 Commerce suunama. Domeeni liiklus marsruuditakse Commerce'i lõpp-punkti alles siis, kui DNS-i kirjet CNAME värskendatakse Commerce'i lõpp-punkti kasutamiseks domeeniga.

> [!NOTE]
> Väljale **Toetatud hostinimed** saab sisestada mitu domeeni, eraldades need semikoolonitega.

Järgmisel joonisel on kujutatud LCS-i e-kaubanduse ettevalmistamise ekraan, kus on esile tõstetud väli **Toetatud hostinimed**. 

![LCS e-commerce ettevalmistamise ekraan koos esiletõstetud väljaga **Toetatud hostinimed**.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Kui ettevalmistamine on juba toimunud, saate luua hooldustaotluse lisadomeenide keskkonda lisamiseks. Teenusetaotluse loomiseks LCS-is tehke oma keskkonnas valikud **Tugi \> Toeprobleemid** ja valige **Edasta juhtum**.

## <a name="commerce-generated-urls"></a>Commerce'i loodud URL-id

Dynamics 365 Commerce'i e-kaubanduse keskkonna ettevalmistamisel loob Commerce URL-i, mis on keskkonna tööaadress. Sellele URL-ile viidatakse LCS-is kuvatavas e-kaubanduse saidi lingis pärast keskkonna ettevalmistamist. Commerce'i loodud URL on vormingus `https://<e-commerce tenant name>.commerce.dynamics.com`, mille korral e-kaubanduse rentniku nimi on LCS-is Commerce'i keskkonna jaoks sisestatud nimi.

Tootmissaidi hostinimesid saate kasutada ka liivakastikeskkonnas. See suvand on ideaalne kasutamiseks siis, kui kopeerite saidi liivakastikeskkonnast tootmisse.

## <a name="site-setup"></a>Saidi häälestus

Kui teie e-kaubanduse keskkond on ette valmistatud, peate seadistama oma saidi Commerce'i saidiehitajas saidi ja toimiva URL-i seostamiseks.

Saidi esmakordsel seadistamisel saidiehitajas kuvatakse dialoogiboks **Saidi seadistamine**.

Järgmisel illustratsioonil on kujutatud dialoogiboks **Saidi seadistamine** saidi „vaikimisi” jaoks, kui navigeerite saidile esmakordselt saidiehitaja kaudu.

![Dialoogiboks **Saidi seadistamine**.](./media/Domains_SetupyoursiteScreen.png)

Väli **Vali domeen** võimaldab teil saidiehitajas seostada oma saidiga ühe toetatud hostinimedest, mida pakutakse teie saidi jaoks LCS-is.

Välja **Tee** saab tühjaks jätta või lisada täiendava tee stringi, mis kajastub teie toimivas URL-is. Kui väli **Tee** on tühi, seostatakse saidiehitajas Commerce'i loodud URL seadistatava saidiga. Teed peavad olema kordumatud iga saidi/domeeni paari korral. Valitud saidil ja domeenis saab tühja teed kasutada ainult üks keskkonna sait või olla seostatud kordumatu tee stringiga. Saidi seadistamise ajal väljale **Tee** lisatud stringist saab Commerce'i loodud baas-URL-i alamtee, mida kasutatakse veebibrauseris saidile juurdepääsemiseks.

> [!NOTE]
> Tee on tuntud ka kui **Vastendatud tee**, kui lisada kanal saidiehitaja konfiguratsioonisektsiooni **Saidi sätted \> Kanalid**.

Näiteks kui teil on saidiehitaja sait „fabrikam“ e-kaubanduse rentnikus nimega „xyz“ ja kui seadistate saidi tühja teega, pääsete veebibrauseris juurde avaldatud saidi sisule, avades otse Commerce'i loodud baas-URL-i.

`https://xyz.commerce.dynamics.com`

Kui olete sama saidi seadistamise ajal lisanud tee nimega „fabrikam”, pääsete veebibrauseri avaldatud saidi sisule juurde järgmise URL-i abil.

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Lehed ja URL-id

Pärast seda, kui teie sait on seadistatud teega, tuginevad kõik saidiehitaja lehtedega seotud URL-id saidi toimivale URL-ile (Commerce'i loodud URL või Commerce'i loodud URL koos teega). Uue URL-i loomine saidiehitajas (**URL-id /> +Uus**), valides lehe dialoogiboksi **Uus URL** loendist ja sisestades selle lehe URL-i tee, seostab selle URL-i valitud lehega. URL-i tee väärtus lisatakse saidi toimivale URL-ile lehele juurde pääsemiseks ja sel on silt `./<URL path>` saidiehitaja lehe **URL-id** URL-ide loendis.

Järgmisel joonisel on kujutatud saidiehitaja dialoogiboks **Uus URL**, milles on esile tõstetud näidis-URL-i tee. 

![Saidiehitaja dialoogiboks **Uus URL**.](./media/Domains_PageSetup2a.png)

Järgmisel joonisel on kujutatud saidiehitaja leht **URL-id**, mille loendis on esile tõstetud URL.

![Kasutajavoo suvandi käitamine poliitika voos.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Saidiehitaja domeenid

Toetatud hostinime väärtused on saadaval, et neid saaks saidi seadistamisel domeeniga seostada. Toetatud hostinime väärtuse domeenina valimisel näete valitud domeeni, millele viidatakse saidiehitajas. See domeen on vaid viide Commerce'i keskkonnas ning selle domeeni reaalajas liiklust ei edastata veel teenusele Dynamics 365 Commerce.

Kui töötate saidiehitaja saitidega ja teil on seadistatud kaks saiti kahe erineva domeeniga, saate lisada oma toimivale URL-ile atribuudi **?domain=**, et pääseda brauseris juurde avaldatud saidi sisule.

Näiteks keskkond „xyz” on ette valmistatud ning saidiehitajas on loodud ja seostatud kaks saiti: üks domeeniga `www.fabrikam.com` ja teine domeeniga `www.constoso.com`. Iga sait seadistati tühja tee abil. Nendele kahele saidile pääseb veebibrauseri kaudu juurde järgmiselt, kasutades atribuuti **?domain=**.
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Kui domeeni päringustringi ei pakuta keskkonnas, kus on mitu domeeni, kasutab Commerce esimest teie pakutavat domeeni. Näiteks kui saidi seadistamisel esitati esmalt tee „fabrikam”, võidakse kasutada URL-i `https://xyz.commerce.dynamics.com`, et pääseda juurde saidi `www.fabrikam.com` avaldatud sisule.

## <a name="traffic-forwarding-in-production"></a>Liikluse edastamine tootmisse

Mitme domeeni simuleerimiseks saate kasutada domeeni päringustringi parameetreid saidi commerce.dynamics.com lõpp-punktis. Kuid kui teil on vaja avaldada otse tootmisse, peate oma kohandatud domeeni liikluse edastama saidi `<e-commerce tenant name>.commerce.dynamics.com` lõpp-punkti.

Saidi `<e-commerce tenant name>.commerce.dynamics.com` lõpp-punkt ei toeta kohandatud domeeni SSL-e, seega peate häälestama kohandatud domeenid, kasutades sisenemispunkti teenust või sisu edastamise võrku (CDN). 

Kohandatud domeenide seadistamiseks sisenemispunkti teenuse või CDN-i abil on teil kaks võimalust.

- Saate seadistada sisenemispunkti teenuse (nt Azure Front Door) eesserveri liikluse käsitlemiseks ja oma Commerce'i keskkonnaga ühenduse loomiseks. See tagab suurema kontrolli domeeni- ja serdihalduse ning täpsemate turbepoliitikate üle.
- Saate kasutada Commerce'i esitatud Azure'i sisenemispunkti eksemplari. Selleks on vaja koordineerida tegevust teenuse Dynamics 365 Commerce töörühmaga domeeni kinnitamiseks ja teie tootmise domeeni SSL-i sertide hankimiseks.

Lisateavet CDN-i teenuse otseseadistamise kohta leiate teemast [Sisu edastamise võrgu (CDN) toe lisamine](add-cdn-support.md).

Commerce'i esitatud Azure'i sisenemispunkti eksemplari kasutamiseks peate looma CDN-i seadistusabi teenusetaotluse Commerce'i töörühma abil. 

- Peate sisestama ettevõtte nime, tootmise domeeni, keskkonna ID ja tootmise e-kaubanduse rentniku nime. 
- Peate kinnitama, kas tegemist on olemasoleva domeeniga (mida kasutatakse praegu aktiivse saidi jaoks) või uue domeeniga. 
- Uue domeeni korral saab kinnitada domeeni ja hankida SSL-serdi ühe etapi abil. 
- Olemasolevat veebisaiti teenindava domeeni korral on domeeni kinnitamise ja SSL-serdi loomiseks nõutav mitmeetapiline protsess. Sellel protsessil on seitsme tööpäeva teenusetaseme lepe (SLA) domeeni avaldamiseks, kuna see sisaldab mitut järjestikust etappi.

Teenusetaotluse loomiseks LCS-is tehke oma keskkonnas valikud **Tugi \> Toeprobleemid** ja valige **Edasta juhtum**.

> [!NOTE]
> SSL-iga kohandatud domeene toetatakse ainult töökeskkondades. Mitte-töökeskkondade (nt liivakasti ja kasutaja nõusoleku testimise (UAT)) korral kasutage avaldatud sisule veebibrauseri kaudu juurdepääsemiseks Commerce'i loodud URL-i.

## <a name="ssl-certificate-process"></a>SSL-serdi protsess

Kui teenusetaotlus on esitatud, kooskõlastab Commerce'i töörühm teiega järgmised toimingud.

Uute domeenide korral.
- Commerce'i töörühm seadistab Azure'i sisenemispunkti teenuse eksemplari (Commerce'i hostitud).
- Seejärel esitab Commerce'i töörühm kirje CNAME, et osutada teie kohandatud domeenile.
- Pärast kirje CNAME värskendamist saab Commerce'i hostitud Azure'i sisenemispunkti eksemplar kinnitada domeeni omandiõigust ja hankida SSL-serti.

Olemasolevate/aktiivsete domeenide korral.
- Commerce'i töörühm palub teil lisada kirje `afdverify.<custom-domain>` CNAME oma domeeni pakkumiseks DNS-i pakkujale.
- Kui see on lõpule viidud, lisab Commerce'i töörühm domeeni Azure'i sisenemispunkti eksemplari ja pakub täiendavaid DNS-i TXT-kirjeid, mis lisatakse domeeni DNS-i.
- Pärast TXT-kirjete lõpule viimist viib Commerce'i töörühm lõpule SSL-serti häälestava domeeni Azure'i sisenemispunkti värskendused.

## <a name="apex-domains"></a>Tippdomeenid

Commerce'i esitatud Azure'i sisenemispunkti eksemplar ei toeta tippdomeene (juurdomeene, mis ei sisalda alamdomeene). Tippdomeenid vajavad probleemi lahendamiseks IP-aadressi ja Commerce'i Azure'i sisenemispunkti eksemplar on olemas ainult koos virtuaalsete lõpp-punktidega. Tippdomeeni kasutamiseks on teil kaks võimalust.

- **Võimalus 1** – Saate kasutada oma DNS-i pakkujat, et suunata tippdomeen ümber "www"-domeeni. Näiteks suunab fabrikam.com ümber saidile `www.fabrikam.com`, kus `www.fabrikam.com` on kirje CNAME, mis osutab Commerce'i hostitud Azure'i sisenemispunkti eksemplarile.

- **Võimalus 2** – tippdomeeni majutamiseks saate ise seadistada CDN-i/sisenemispunkti eksemplari.

> [!NOTE]
> Kui kasutate Azure'i sisenemispunkti, peate samas tellimuses seadistama ka Azure'i DNS-i. Azure'i DNS-is majutatud tippdomeen võib osutada teie Azure'i sisenemispunktile pseudonüümi kirjena. See on ainus võimalus, sest tippdomeenid peavad alati osutama IP-aadressile.

  ## <a name="additional-resources"></a>Lisaressursid

  [Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

  [Võrgupoe kanali häälestamine](./channel-setup-online.md)

  [E-kaubanduse saidi loomine](create-ecommerce-site.md)

  [Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

  [Robots.txt-failide haldamine](manage-robots-txt-files.md)

  [Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

  [B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

  [Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

  [Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

  [Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

  [Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]