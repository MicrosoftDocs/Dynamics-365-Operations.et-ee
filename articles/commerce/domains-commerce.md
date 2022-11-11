---
title: Domeenid Dynamics 365 Commerce'is
description: See artikkel kirjeldab, kuidas domeene käsitsetakse Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750676"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domeenid Dynamics 365 Commerce'is

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas domeene käsitsetakse Microsoft Dynamics 365 Commerce.

Domeenid on veebiaadressid, mida kasutatakse veebibrauseris teenuse Dynamics 365 Commerce saitidele navigeerimiseks. Saate juhtida oma domeeni haldamist valitud domeeni nimeserveri (DNS) pakkuja abil. Domeenidele viidatakse teenuse Dynamics 365 Commerce saidiehitajas, et koordineerida seda, kuidas saidile pärast avaldamist juurde pääseb. See artikkel vaatab üle, kuidas domeene ärisaidi arenduse ja käivitamise töötsükli jooksul käsitletakse ja viidatakse.

> [!NOTE]
> 6. mai 2022- 2022 Dynamics 365 Commerce`.dynamics365commerce.ms` . aasta mais asendatakse domeeniga kõik loodud keskkonnad, asendades varasema mustri `.commerce.dynamics.com`. Domeeniga ette ettevalmistamine olemasolevad `.commerce.dynamics.com` keskkonnad jätkavad tööd.

## <a name="provisioning-and-supported-host-names"></a>Hostinimede ettevalmistamine ja toetamine

E-kaubanduse keskkonna ettevalmistamisel teenuses [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) kasutatakse juurutatud Commerce'i keskkonnaga seotud domeenide sisestamiseks e-kaubanduse ettevalmistamise kuval välja **Toetatud hostinimed**. Need domeenid on kliendile suunatud domeeninimede serveri (DNS) nimed, kus majutatakse e-kaubanduse veebisaite. Domeeni sisestamine selles etapis ei käivita domeeni liikluse suunamist teiseks Dynamics 365 Commerce. Domeeni liiklus marsruuditakse Commerce'i lõpp-punkti alles siis, kui DNS-i kirjet CNAME värskendatakse Commerce'i lõpp-punkti kasutamiseks domeeniga.

> [!NOTE]
> Väljale **Toetatud hostinimed** saab sisestada mitu domeeni, eraldades need semikoolonitega.

Järgmisel joonisel on kujutatud LCS-i e-kaubanduse ettevalmistamise ekraan, kus on esile tõstetud väli **Toetatud hostinimed**. 

![LCS e-commerce ettevalmistamise ekraan koos esiletõstetud väljaga **Toetatud hostinimed**.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Kui ettevalmistamine on juba toimunud, saate luua hooldustaotluse lisadomeenide keskkonda lisamiseks. Teenusetaotluse loomiseks LCS-is tehke oma keskkonnas valikud **Tugi \> Toeprobleemid** ja valige **Edasta juhtum**.

## <a name="commerce-generated-urls"></a>Commerce'i loodud URL-id

Dynamics 365 Commerce'i e-kaubanduse keskkonna ettevalmistamisel loob Commerce URL-i, mis on keskkonna tööaadress. Sellele URL-ile viidatakse LCS-is kuvatavas e-kaubanduse saidi lingis pärast keskkonna ettevalmistamist. Commerce'i loodud URL on vormingus `https://<e-commerce tenant name>.dynamics365commerce.ms`, mille korral e-kaubanduse rentniku nimi on LCS-is Commerce'i keskkonna jaoks sisestatud nimi.

Tootmissaidi hostinimesid saate kasutada ka liivakastikeskkonnas. See valik on ideaaljuhul, kui kopeerite saidi sisendkausta keskkonnast tootmisse.

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

`https://xyz.dynamics365commerce.ms`

Kui olete sama saidi seadistamise ajal lisanud tee nimega „fabrikam”, pääsete veebibrauseri avaldatud saidi sisule juurde järgmise URL-i abil.

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Lehed ja URL-id

Pärast seda, kui teie sait on seadistatud teega, tuginevad kõik saidiehitaja lehtedega seotud URL-id saidi toimivale URL-ile (Commerce'i loodud URL või Commerce'i loodud URL koos teega). Uue URL-i loomine saidiehitajas (**URL-id /> +Uus**), valides lehe dialoogiboksi **Uus URL** loendist ja sisestades selle lehe URL-i tee, seostab selle URL-i valitud lehega. URL-i tee väärtus lisatakse saidi toimivale URL-ile lehele juurde pääsemiseks ja sel on silt `./<URL path>` saidiehitaja lehe **URL-id** URL-ide loendis.

Järgmisel joonisel on kujutatud saidiehitaja dialoogiboks **Uus URL**, milles on esile tõstetud näidis-URL-i tee. 

![Saidiehitaja dialoogiboks **Uus URL**.](./media/Domains_PageSetup2a.png)

Järgmisel joonisel on kujutatud saidiehitaja leht **URL-id**, mille loendis on esile tõstetud URL.

![Kasutajavoo suvandi käitamine poliitika voos.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Saidiehitaja domeenid

Toetatud hostinime väärtused on saadaval, et neid saaks saidi seadistamisel domeeniga seostada. Kui valite domeeniks toetatud hostinime väärtuse, näete valitud domeeni, mida viidatakse kogu saidiloojas. See domeen on ainult viide Commerce’i keskkonnas. Selle domeeni reaalajas liiklust ei edastata veel sellele domeenile Dynamics 365 Commerce.

Kui töötate saidiehitaja saitidega ja teil on seadistatud kaks saiti kahe erineva domeeniga, saate lisada oma toimivale URL-ile atribuudi **?domain=**, et pääseda brauseris juurde avaldatud saidi sisule.

Näiteks keskkond „xyz” on ette valmistatud ning saidiehitajas on loodud ja seostatud kaks saiti: üks domeeniga `www.fabrikam.com` ja teine domeeniga `www.constoso.com`. Iga sait seadistati tühja tee abil. Nendele kahele saidile pääseb veebibrauseri kaudu juurde järgmiselt, kasutades atribuuti **?domain=**.
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Kui domeenipäringu stringi ei ole esitatud keskkonnas, kus on antud mitu domeeni, kasutab Commerce esimest teie antud domeeni. Näiteks kui saidi seadistamisel esitati esmalt tee „fabrikam”, võidakse kasutada URL-i `https://xyz.dynamics365commerce.ms`, et pääseda juurde saidi `www.fabrikam.com` avaldatud sisule.

Saate lisada ka kohandatud domeene. Selleks valige projekti ärihalduse **lehel e-äri** **alapealkirjas + Lisa kohandatud domeen**. Slaider näitab olemasolevaid kohandatud domeene ja pakub võimalust lisada uus kohandatud domeen.

## <a name="update-which-commerce-scale-unit-is-used"></a>Värskendage, millist äriskaala üksust kasutatakse.

Commerce’i kasutatav Commerce Scale Unit (CSU) on tavaliselt valitud keskkonna algsel loomisel. Commerce võimaldab teil muuta seda, millist CSU eksemplari teie keskkonnas kasutatakse, võimaldades teil oma ülesehitust iseteenindusfunktsiooni kaudu paremini hooldada ja vähendada vajadust toega ühendust võtta. CSU eksemplari värskendamiseks minge projekti keskkonna Ärihalduse lehele ja valige seejärel värskendamisskaala **üksus**. Kasutage Uue **äriskaala üksuse** slaiderit uue CSU eksemplari valimiseks keskkonna jaoks saadaval csUs-ide loendist.

## <a name="traffic-forwarding-in-production"></a>Liikluse edastamine tootmisse

Mitme domeeni simuleerimiseks saate kasutada domeeni päringustringi parameetreid saidi commerce.dynamics.com lõpp-punktis. Kuid kui teil on vaja avaldada otse tootmisse, peate oma kohandatud domeeni liikluse edastama saidi `<e-commerce tenant name>.dynamics365commerce.ms` lõpp-punkti.

Lõpp-punkt `<e-commerce tenant name>.dynamics365commerce.ms` ei toeta kohandatud domeeni Secure Sockets Layers (SSL-id), seega peate häälestama kohandatud domeenid eesuste teenuse või sisu tarnevõrgu (CDN) abil. 

Kohandatud domeenide seadistamiseks sisenemispunkti teenuse või CDN-i abil on teil kaks võimalust.

- Seadistage eesuste teenus, nagu Azure Front Ukse, et käsitseda eesliidet liiklust ja ühendada oma Ärikeskkonnaga, mis võimaldab suuremat kontrolli domeeni- ja serdihalduse ning granulaarse turbepoliitika üle.

- Kasutage rakenduse Azure Front Ukse Dynamics 365 Commerce eksemplari, mis nõuab domeeni tõendamise ja tootmisdomeeni SSL-sertifikaatide hankimiseks meeskonnaga tegevuse kooskõlastamist.

> [!NOTE]
> Kui kasutate välist CDN-i või esikaaneteenust, veenduge, et taotlus on Äriportaalis äriportaali hostinimega, kuid X-Hosti (XFH) päisega \<custom-domain\>. Näiteks kui teie rakenduse Commerce lõpp-punkt `xyz.dynamics365commerce.ms``www.fabrikam.com` on ja kohandatud domeen on, `xyz.dynamics365commerce.ms` peaks edastatava nõude hostipäis olema ja olema XFH-päis `www.fabrikam.com`.

Lisateavet CDN-i teenuse otseseadistamise kohta leiate teemast [Sisu edastamise võrgu (CDN) toe lisamine](add-cdn-support.md).

Commerce'i esitatud Azure'i sisenemispunkti eksemplari kasutamiseks peate looma CDN-i seadistusabi teenusetaotluse Commerce'i töörühma abil. 

- Peate esitama oma ettevõtte nime, tootmise domeeni, keskkonna ID ja tootmise e-äri rentniku nime. 
- Peate kinnitama, kas see teenusetaotlus on olemasolevale domeenile (kasutatakse praegu aktiivse saidi puhul) või uue domeeni jaoks. 
- Uue domeeni korral saab kinnitada domeeni ja hankida SSL-serdi ühe etapi abil. 
- Domeenis, kus on olemasolev veebisait, on domeeni tõendamise ja SSL-i serdi loomiseks vajalik mitmetasandiline protsess. Sellel protsessil on seitsme tööpäeva teenusetaseme lepe (SLA) domeeni avaldamiseks, kuna see sisaldab mitut järjestikust etappi.

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

Äri esitatud Azure Front Ukse eksemplar ei toeta apex-domeene (juurdomeene, mis ei sisalda alamdomeene). Apex-domeenid vajavad lahendamiseks IP-aadressi ja Commerce Azure’i front ukse eksemplar on olemas ainult virtuaalsete lõpp-punktidega. Domeeni apex kasutamiseks on teil järgmised võimalused:

- **Võimalus 1** – Saate kasutada oma DNS-i pakkujat, et suunata tippdomeen ümber "www"-domeeni. Näiteks suunab fabrikam.com ümber saidile `www.fabrikam.com`, kus `www.fabrikam.com` on kirje CNAME, mis osutab Commerce'i hostitud Azure'i sisenemispunkti eksemplarile.

- **Valik 2** – kui teie DNS-i pakkuja toetab ALIAS-kirjeid, saate osutada domeenile Azure Front Ukse lõpp-punkt, mis tagab IP muudatuse lõpp-punkti kaudu. Teil tuleb hostida Azure Front Ukse eksemplari ise.
  
- **Valik 3** – kui teie DNS-i pakkuja ei toeta ALIAS-kirjeid, siis peate dns-i pakkuja muutma teenuse Azure DNS-iks ja hostima nii Azure DNS-i kui ka Azure Front Doori eksemplari ise.

> [!NOTE]
> Kui kasutate Azure'i sisenemispunkti, peate samas tellimuses seadistama ka Azure'i DNS-i. Azure'i DNS-is majutatud tippdomeen võib osutada teie Azure'i sisenemispunktile pseudonüümi kirjena. See on ainus võimalus, sest tippdomeenid peavad alati osutama IP-aadressile.
  
Kui teil on küsimusi apex-domeenide kohta, võtke ühendust Microsofti [toega](https://support.microsoft.com/).

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
