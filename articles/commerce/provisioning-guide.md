---
title: E-kaubanduse hindamiskeskkonna konfigureerimine
description: Selles juhendis esitatakse üksikasjalikud juhised rakenduse Microsoft Dynamics 365 Commerce eelvaate keskkonna ettevalmistamiseks ja konfigureerimiseks.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771676"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>E-kaubanduse hindamiskeskkonna konfigureerimine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles juhendis esitatakse üksikasjalikud juhised rakenduse Microsoft Dynamics 365 Commerce eelvaate keskkonna ettevalmistamiseks ja konfigureerimiseks. Enne alustamist soovitame teil dokumendid vähemalt läbi sirvida, et saada aimu, mida protsess hõlmab ja mida juhend sisaldab.

*Märkused: kui teile ei ole veel antud juurdepääsu rakenduse Microsoft Dynamics 365 Commerce eelvaatele, saate taotleda eelvaate juurdepääsu [kaubanduse veebisaidilt](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Kokkuvõte
Keskkonna edukaks ettevalmistamiseks tuleb projekt luua kindla toote nime ja tüübiga. Keskkonnal ja teenusel Retail Cloud Scale Unit on samuti mõned konkreetsed parameetrid, mida peate kasutama, et hiljem alustada e-kaubanduse ettevalmistamist. Juhised selles juhendis sisaldavad kõiki vajalikke etappe, mida läbida ja milliseid parameetreid kasutada.

Pärast edukat ettevalmistamist on mõned hilisemad etapid, mida peate eelvaate keskkonna ettevalmistamiseks läbima. Mõned etapid on valikulised, sõltuvalt sellest, milliseid süsteemi aspekte soovite hinnata. Kui peaksite meelt muutma, saate alati hiljem valikulisi etappe käitada.

Kui teil on küsimusi ettevalmistamise etappide kohta või esineb probleeme, andke meile sellest teada [rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammer grupis](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Eeltingimused
Rakenduse Dynamics 365 eelvaate keskkonna ettevalmistamiseks on järgmised eeltingimused.
* Teil on juurdepääs portaalile **Lifecycle Services (LCS)**
* Teid on **rakenduse Dynamics 365 Commerce eelvaate programmi vastu võetud**
* Teil on vajalikud õigused, et luua projekt suvandite **Potentsiaalsed eelmüügid** või **Migreerimine, lahenduste loomine ja teave** jaoks
* Olete rolli **Keskkonnahaldur** või **Projekti omanik** liige projektis, kus te kavatsete keskkonna ette valmistada.
* Teil on administraatori juurdepääs oma Azure'i tellimusele või kontakt kordustellimusega administraatoriga, kes saab teie nimel teha kahte etappi, mis nõuavad administraatori õigusi
* Teie **AAD rentniku ID** on saadaval
* Olete loonud **AAD turberühma**, mida kasutatakse **e-kaubanduse süsteemi administraatorite grupina** ja mille ID on saadaval.
* Olete loonud **AAD turberühma**, mida kasutatakse **hinnangute ja arvustuste moderaatori grupina** ja mille ID on saadaval (võib olla sama, mis süsteemi administraatorite grupil eespool)
## <a name="provisioning-preview-environment"></a>Ettevalmistamise eelvaate keskkond
Need juhised hõlmavad rakenduse Microsoft Dynamics 365 Commerce eelvaate keskkonna ettevalmistamist. Pärast nende etappide edukat lõpetamist on teil eelvaate keskkond, mis on konfigureerimiseks valmis. Kõik siin kirjeldatud tegevused toimuvad LCS portaalis.

*Pidage meeles, et eelvaate juurdepääs on seotud LCS konto ja teie eelvaate rakenduses määratud organisatsiooniga. Peate kasutama sama kontot ettevalmistamiseks. Kui peate eelvaate keskkonna jaoks kasutama erinevat LCS kontot või rentnikku, peate need üksikasjad meile andma. Kontaktandmed leiate allpool jaotisest "täiendavad ressursid".*
### <a name="before-starting"></a>Enne alustamist
##### <a name="grant-access-to-e-commerce-applications"></a>Juurdepääsu andmine e-kaubanduse rakendustele

*Märkus: **isik, kes sisse logib, peab olema AAD rentniku administraator**. Kui seda etappi edukalt ei lõpetata, nurjuvad ülejäänud ettevalmistamise etapid.*

1. Selle etapi jaoks on teil vaja **AAD rentniku ID**-d. Peate autoriseerima e-kaubanduse rakendusi, et pääseda juurde oma Azure'i tellimusele. Lihtsaim viis selle saavutamiseks on sellise URL-i koostamine:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Ärge klõpsake otse URL-ile**, selle asemel kopeerige ja kleepige see oma brauserisse või tekstiredaktoris ja asendage **\{AAD_TENANT_ID\}** oma **AAD rentniku ID-ga** enne URL-i navigeerimist.
3. Teile esitatakse Microsoft AAD sisselogimise dialoog, kus te kinnitate, et soovite anda oma tellimusele juurdepääsu rakendusele "Dynamics 365 Commerce (eelvaade)".
4. Teid suunatakse lehele, mis kinnitab, kas operatsioon õnnestus.

##### <a name="log-in-to-the-lcs"></a>LCS portaali sisse logimine
1. Logige sisse LCS portaali: https://lcs.dynamics.com
1. Veenduge, et olete sisse logitud sama LCS kontoga, mida kasutasite eelvaatele juurdepääsu taotlemiseks.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Kinnitage, et eelvaate funktsioonid on saadaval ja lubatud
1. Kerige LCS esilehel paremale ja klõpsake paani **Eelvaate funktsiooni haldamine**.
1. Kerige jaotisesse "PRIVAATSED EELVAATE FUNKTSIOONID" ja veenduge, et järgmised funktsioonid on saadaval ja lubatud:
    1. **E-kaubanduse hindamine**
    1. **Kaubanduse eelvaate programmi keskkonnad**
1. Kui te ei näe neid funktsioone loendis, võtke meiega ühendust ja tagage järgmised andmed: töömeil, LCS konto ja rentniku üksikasjad. Vaadake jaotist **Lisaressursid** allpool, et saada teavet, kuidas meiega kontakteeruda.

![Eelvaate funktsiooni paan](./media/preview1.png)

![Eelvaatefunktsioonid](./media/preview2.png)
### <a name="create-project"></a>Projekti loomine
##### <a name="creating-new-project"></a>Uue projekti loomine
1. Klõpsake nuppu **+** uue projekti loomiseks.
1. Kui olete partner, valige suvand **Migreerimine, lahenduste loomine ja teave**.
1. Kui olete klient, valige suvand **Potentsiaalsed eelmüügid**.
1. Sisestage sobiv nimi, kirjeldus ja tööstus.
1. Suvandi **Toote nimi** väärtuseks valige **Dynamics 365 Retail**.
1. Suvandi **Toote versioon** väärtuseks valige **Dynamics 365 Retail**.
1. Suvandi **Metoodika** väärtuseks valige **Dynamics Retail juurutamise metoodika**.
1. Soovi korral võite importida rolle ja kasutajaid olemasolevast projektist.
1. Klõpsake käsku **Loo**.
1. Teid saadetakse projekti vaatesse.
##### <a name="add-azure-connector"></a>Azure'i konnektori lisamine
1. Kui olete partner, klõpsake suvandit **Projekti sätted** tööriista paanilt kõige parempoolsemal küljel.
1. Kui olete klient, valige suvand **Projekti sätted** ülemisest menüüst.
1. Valige suvand **Azure’i konnektorid**.
1. Azure'i konnektori lisamiseks klõpsake nuppu **+ lisa**.
1. Sisestage nimi.
1. Sisestage oma **Azure'i tellimuse ID**.
1. Lubage suvand **Azureʼi ressursihalduri (ARM) kasutamise konfigureerimine**.
1. Veenduge, et **Azure'i kordustellimuse AAD rentniku domeen (või ID)** on õige. Vajaduse korral konsulteerige oma Azure'i tellimuse administraatoriga.
1. Klõpsake käsku **Edasi**.
1. Järgige ekraanil kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele. Vajaduse korral konsulteerige oma Azure'i tellimuse administraatoriga.
    1. Logige sisse Azure'i portaali: https://portal.azure.com/
    1. Veenduge, et olete valinud õige kataloogi.
    1. Klõpsake suvandit **Tellimused** vasakul asuvast menüüst.
    1. Leidke loendist õige tellimus ja valige see. Vajaduse korral kasutage otsingut.
    1. Valige menüüst suvand **Juurdepääsu juhtelement (IAM)**.
    1. Klõpsake käsku **Lisa** jaotises **Lisa rollimäärang** paremal küljel. Avatakse paan **Lisa rollimäärang**.
    1. Suvandi **Roll** jaoks valige **Kaasautor**.
    1. Suvandi **Määra juurdepääs** väärtuseks jäta **Azure AD kasutaja, grupp või teenusesubjekt**.
    1. Jaotisesse **Vali** sisestage **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Valige loendist **Dynamicsi juurutamise teenused [wsfed-enabled]**.
    1. Klõpsake valikut **Salvesta**.
1. Klõpsake käsku **Edasi**.
1. Järgige ekraanil kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele. Vajaduse korral konsulteerige oma Azure'i tellimuse administraatoriga.
1. Klõpsake käsku **Edasi**.
1. Suvandi **Azure'i regioon** väärtuseks valige kas **Ida-USA**, **Ida-USA 2**, **Lääne-USA**, **Lääne-USA 2**.
1. Klõpsake käsku **Ühenda**.
1. Teie Azure'i konnektor peaks loendis ilmuma.
### <a name="import-extension"></a>Impordi laiend
1. Navigeerige tagasi oma projekti avalehele, klõpsates projekti nime ülaosas.
1. Kui olete partner, klõpsake suvandit **Varateek** tööriista paanilt kõige parempoolsemal küljel.
1. Kui olete klient, valige suvand **Varateek** ülemisest menüüst.
1. Valige suvand **Tarkvara juurutatav pakett** vasakul asuvast loendist.
1. Klõpsake toimingupaanil nuppu **IMPORDI**.
1. Valige suvand **Kaubanduse eelvaate demobaasi laiendus** varade loendist, mis on asukohas **JAGATUD VARATEEK**.
1. Klõpsake nuppu **Komplekteeri**.
1. Teid viiakse tagasi varateeki ja peaksite nägema laiendit loendis.

![Projekti loomine - versioonid](./media/import.png)
### <a name="deploy-environment"></a>Keskkonna juurutamine

*Pange tähele: on võimalik, et etappe 6, 7 ja/või 8 ei kuvata, kuna ühe suvandi ekraanid jäetakse vahele. Kui olete vaates **Keskkonna parameetrid**, kinnitage, et teil on tekst "Dynamics 365 Commerce (eelvaade) – demo (10.0.6 platvormi värskendus 30)" otse välja **Keskkonna nimi** kohal. Vt allolevat pilti.*

1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Klõpsake nuppu **+ lisa** keskkonna lisamiseks.
1. Suvandi **Rakenduse versioon** väärtuseks valige **10.0.6**.
1. Välja **Platvormi versioon** väärtuseks valige **Platvormi värskendus 30**.
1. Klõpsake käsku **Edasi**.
1. Keskkonna topoloogia puhul valige väärtuseks **DEMO**.
1. Keskkonna topoloogia puhul valige väärtus **Dynamics 365 Commerce (eelvaade) – demo**.
1. Kui olete varem konfigureerinud ühe Azure konnektori, kasutatakse seda selles keskkonnas. Mitme Azure'i konnektorite konfigureerimisel on teil võimalus valida, millist konnektorit soovite kasutada: **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2** (soovitatav parima lõppeesmärgi jõudluseks)
1. Sisestage **Keskkonna nimi**.
1. Kohandage vastavalt vajadusele VM-i suurust. (Soovitame kasutada VM SKU **D13 v2**.)
1. Jätke suvand **Täpsemad sätted**, nii nagu need on.
1. Pärast hinnakujunduse ja litsentsitingimuste läbivaatamist ekraanil märkige ruut, et näidata lepingut.
1. Klõpsake käsku **Edasi**.
1. Juurutamise kinnituse kuval, olles kontrollinud, et üksikasjad on õiged, klõpsake nuppu **Juuruta**.
1. Naasete vaatesse **Pilve majutatud keskkonnad** ja teie keskkond peaks ilmuma loendis.
1. Teie soovitud keskkond kuvatakse järjekorras ja seejärel juurutatakse. Kõigi keskkonna töövoogude lõpuleviimine võtab aega, nii et kontrollige mõne tunni pärast (umbes 6–9 tundi).
1. Enne jätkamist veenduge, et teie keskkonna olek on **Juurutatud**.

![Projekti loomine - versioonid](./media/project1.png)

![Projekti loomine – topoloogia 1](./media/project2.png)

![Projekti loomine – topoloogia 2](./media/project3.png)

![Projekti loomine – keskkonna parameetrid](./media/project4.png)
### <a name="initialize-rcsu"></a>RCSU lähtestamine
1. Vaates **Pilve hostitud keskkonnad** valige loendist oma keskkond.
1. Kuva paremas servas olevast keskkonna vaatest klõpsake valikut **Kõik üksikasjad**. Kuvatakse keskkonna üksikasjade vaade.
1. Jaotises **KESKKONNA FUNKTSIOONID** klõpsake käsku **Halda**.
1. Klõpsake vahekaardil **Jaemüük** nuppu **Lähtesta**. Kuvatakse RCSU lähtestamise parameetrite vaade.
1. Suvandi **REGIOON** väärtuseks valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA**, **Lääne-USA 2**.
1. Suvandi **VERSIOON** väärtuseks valige ripploendist variant **Täpsusta versioon** ja täpsustage allpool kuvatavas tekstiväljas **9.16.19262.5**. *Märkus: veenduge, et **täpsustate siin õiget versiooni**, et vältida RCSU hilisemat versiooni värskendamist.*
1. Lubage suvand **Rakenda laiend**.
1. Laiendite loendist valige suvand **Kaubanduse eelvaate demobaasi laiend**.
1. Klõpsake suvandit **Lähtesta**.
1. Juurutamise kinnituse kuval, olles kontrollinud, et üksikasjad on õiged, klõpsake nuppu **Jah**.
1. Olete naasnud vaatesse **Jaemüügi haldus**, mille vahekaart **Jaemüük** on aktiveeritud. Teie RCSU on ettevalmistamiseks ootele pandud.
1. Oodake, kuni teie RCSU olek **EDUKAS** enne jätkamist (kulub ligikaudu 2–5 tundi).
### <a name="initialize-e-commerce"></a>E-kaubanduse lähtestamine
1. Suunduge vahekaardile **e-kaubandus (eelvaade)**.
1. Pärast eelvaate nõusoleku läbivaatamist klõpsake nuppu **Häälestus**.
1. Sisestage nimi väljale **e-kaubanduse rentniku nimi**. Pidage siiski meeles, et see on nähtav mõnes URL-is, mis viitab teie e-kaubanduse eksemplarile.
1. Välja **Teenuse retail cloud scale unit nimi** jaoks valige loendist oma RCSU (loendis peaks olema ainult üks valik).
1. **e-kaubanduse geograafia** on automaatselt asustatud ja seda ei saa muuta.
1. Jätkamiseks klõpsake nuppu **Edasi**.
1. Väljale **Toetatud hostinimed** sisestage mis tahes kehtiv domeen (nt www.fabrikam.com).
1. Väljale **AAD süsteemi administraatori turberühm** sisestage AAD SG ID, mida soovite kasutada e-kaubanduse süsteemi administraatori grupina.
1. Väljale **AAD hinnangute ja arvustuse moderaatori turberühm**sisestage AAD SG ID, mida soovite kasutada hinnangute ja arvustuste moderaatori grupina.
1. Jätke välja **B2C** väärtused tühjaks (7 välja, mis algavad B2C-ga).
1. Jätke suvandi **Luba hinnangute ja arvustuste teenus** väärtuseks lubatud.
1. Klõpsake suvandit **Lähtesta**.
1. Olete naasnud vaatesse **Jaemüügi haldus**, mille vahekaart **E-kaubandus (eelvaade)** on aktiveeritud. Teie e-kaubanduse lähtestamine on käivitatud.
1. Enne jätkamist oodake, kuni teie e-kaubanduse lähtestamise olek on **LÄHTESTAMINE EDUKAS**.
1. Suvandi **LINGID** all, mis asuvad paremal all.
    * Märkige üles link **e-kaubanduse sait**. See on link teie C2-saidi juurele.
    * Märkige üles link **e-kaubanduse saidi halduse tööriist**. See on link saidi halduse tööriistale (C1 autorluse tööriist).
## <a name="post-provisioning-steps"></a>Ettevalmistusejärgsed etapid
Praeguses etapis on keskkond ette valmistatud lõpuni, kuid on veel konfiguratsiooni etappe, mille eest tuleb hoolitseda enne, kui saate alustada keskkonna hindamist.
### <a name="before-starting"></a>Enne alustamist
1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige loendist oma keskkond.
1. Klõpsake nuppu **Täielik teave** paremal olevast keskkonna teabest.
1. Klõpsake nuppu **Logi sisse**, et avada menüü ja valige suvand **Logi keskkonda**.

Veenduge, et **USRT** juriidiline isik on valitud (ülemises parempoolses nurgas).

### <a name="configure-pos"></a>Konfigureeri POS
##### <a name="associate-worker-with-your-identity"></a>Seosta töötaja oma identiteediga
1. Vasakul asuva menüü abil avage **Moodulid > Jaemüük > Töövõtjad > Töötajad**.
1. Otsige loendist ja valige kirje **000713 – Andrew Collette**.
1. Klõpsake tegevuspaneelil valikut **Jaemüük**.
1. Klõpsake valikut **Seosta olemasolev identiteet**.
1. Väljale **Meil** (paremal pool välja **Otsi meili abil**) sisestage oma meiliaadress.
1. Klõpsake nuppu **Otsing**.
1. Valige oma nimega kirje.
1. Klõpsake valikut **OK**.
1. Klõpsake valikut **Salvesta**.
##### <a name="activate-cloud-pos"></a>Pilve kassa aktiveerimist
1. Logige sisse LCS portaali.
1. Liikuge oma projekti juurde.
1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige loendist oma keskkond.
1. Klõpsake nuppu **Täielik teave** paremal olevast keskkonna teabest.
1. Klõpsake nuppu **Logi sisse**, et avada menüü, valige **Logi sisse pilve müügikohta**, POS peaks üles laadima.
1. Klõpsake käsku **Edasi**.
1. Logige sisse oma AAD kontoga.
1. Välja **Kaupluse nimi** väärtuseks valige **San Francisco**.
1. Klõpsake käsku **Edasi**.
1. Jaotise **Register ja seade** väärtuseks valige **SANFRAN-1**.
1. Klõpsake käsku **Aktiveeri**.
1. Peaksite olema välja logitud ja jõudma kassa sisselogimise aknasse.
1. Nüüd saate pilve kassa kogemusse sisse logida, kasutades operaatori ID-d **000713** ja parooli **123**.
### <a name="site-setup"></a>Saidi häälestus
1. Logige sisse **saidi halduse tööriista**, kasutades URL-i, mille varem märkisite.
1. Klõpsake saidil **Fabrikam**, et avada saidi häälestuse dialoog.
1. Domeeni jaoks valige eelnevalt sisestatud domeen e-kaubanduse lähtestamisel.
1. Vaikimisi kanali jaoks valige **Fabrikami laiendatud e-pood**. *Märkus: veenduge, et valite **laiendatud** e-poe*.
1. Vaikekeeleks valige **en-us**.
1. Jäta suvand **Tee** nii nagu see on.
1. Klõpsake valikut **OK**.
1. Teid saadetakse saidi lehtede loendisse.
### <a name="enable-jobs"></a>Tööde lubamine
1. Logige sisse keskkonda (HQ).
1. Kasutades menüüd vasakul, avage **Jaemüük > Päringud ja aruanded > Pakett-tööd**.
1. Teostage järgmised etapid iga listis toodud töö jaoks.
    * **Jaemüügitellimuse meiliteavituse töötlemine**.
    * **Toote saadavus**.
    * **P-0001**.
    * **Tellimuste töö sünkroonimine**.
1. Kasutage kiirfiltrit, et otsida tööd, kasutades selle nime (eespool loetletud).
1. Kui töö olek on **Kinnipeetud**, tehke järgmist.
    1. Vali kirje.
    1. Tegevuspaanil avage **Pakett-töö**-lint ja klõpsake nuppu **Muuda olekut**.
    1. Valige olek **Ootel** ja klõpsake nuppu **OK**.
### <a name="run-full-data-sync"></a>Käivita andmete täielik sünkroonimine
1. Vasakul asuva menüü abil avage **Moodulid> Jaemüük > Peakontori häälestus > Jaemüügi planeerija > Kanali andmebaas**.
1. Kanal **Vaikimisi** valitakse vasakul olevast loendist. *Valige muu saadaolev kanal (nimega **scXXXXXXXXX**)*.
1. Klõpsake toimingupaanil valikut **Andmete täielik sünkroonimine**.
1. Sisestage jaotugraafikuna väärtus **9999**.
1. Klõpsake valikut **OK**.
1. Klõpsake valikut **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Pärast neid etappe olete valmis alustama oma eelvaate keskkonna hindamist!
Kasutage URL-i **e-kaubanduse saidi halduse tööriist**, et navigeerida C1 autorluse kogemuse juurde ja URL-i **e-kaubanduse sait**, et navigeerida C2-saidi kogemuse juurde.

## <a name="additional-resources"></a>Lisaressursid
### <a name="how-to-find-your-aad-tenant-id"></a>Kuidas leida oma AAD rentniku ID
AAD rentniku ID on GUID ja näeb välja nagu see näide: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Azure'i portaalist
1. Logige sisse Azure'i portaali: https://portal.azure.com/
1. Veenduge, et olete valinud õige kataloogi.
1. Klõpsake suvandit **Azure Active Directory** vasakul asuvast menüüst.
1. Valige suvand **Atribuudid** jaotises **Haldus**.
1. AAD rentniku ID kuvatakse jaotises **Kataloogi ID**.
##### <a name="from-openid-connect-metadata"></a>OpenID ühenduse metaandmed
Looge **OpenID URL**, asendades **\{YOUR_DOMAIN\}** oma domeeniga, nt microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration muutub https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Navigeerige valiku **OpenID URL** juurde, nii et teie domeen on selle sees.
1. AAD rentniku ID-d saab vaadelda mitme atribuudi väärtuses.
1. Otsige valik **authorization_endpoint** ja ekstraktige GUID otse pärast **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Kuidas leida oma AAD turberühma ID-d
AAD turberühma ID on GUID ja näeb välja nagu see näide: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

See etapp eeldab, et kasutaja on grupi liige, kes püüab leida ID-d.
1. Navigeerige Graph Explorerisse: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Klõpsake valikut **Logi sisse Microsoftiga** ja logige sisse oma identimisteabega.
1. Pärast sisselogimist klõpsake vasakul valikut **Kuva rohkem näiteid**.
1. Lubage valik **Grupid** parempoolsel paanil.
1. Sulgege õige paan.
1. Klõpsake valikut **kõik grupid, kuhu kuulun**.
1. Leidke oma grupp tekstiväljalt **Vastuse eelvaade**.
1. Turberühma ID märgitakse atribuudi **id** all.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Testige krediitkaardi teavet, et sooritada testoste.
Selleks, et sooritada testi kandeid saidil, saate kasutada järgmist testi krediitkaardi teavet.

Kaardi number: 4111-1111-1111-1111, aegumine: 10/20, CVV: 737

*Märkus: te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul!*
### <a name="useful-links"></a>Kasulikud lingid
* [LCS (Lifecycle services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure'i portaal](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)
* [Abiressursid rakenduse Dynamics 365 Retail jaoks](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Rakenduse Microsoft Dynamics 365 Commerce eelvaate tugi
Kui teil tekib ettevalmistuse tegemisel probleeme, vaadake abi saamiseks jaotist [Rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammer grupp](https://aka.ms/Dynamics365CommercePreviewYammer). 

Kui teil on grupile Yammer ligipääsuks probleeme, saate meiega ühendust võtta ka meili teel aadressil **Dynamics365Commerce@microsoft.com**. Seda meiliaadressi ei jälgita aktiivselt, nii et vastuse saamine võib viibida.
***
## <a name="prerequisites-for-optional-features"></a>Valikuliste funktsioonide eeltingimused
Kui soovite hinnata ülekande meilifunktsioone, peavad olema täidetud järgmised eeltingimused.
* Teil on meili server saadaval (SMTP-server), mida saab kasutada Azure'i tellimusel, kus te eelvaate keskkonda ette valmistate.
* Teil on serveri FQDN/IP, SMTP pordi number ja autentimise üksikasjad saadaval.

Kui soovite hinnata digitaalse varahalduse funktsioone, täpsemalt sisse tuua uusi omnikanali pilte, peavad olema täidetud järgmised eeltingimused.
* Teie **CMS rentniku nimi** peab olema saadaval. Selle nime leidmise juhised on allpool.
### <a name="configure-image-backend-optional"></a>Pildi tagaserveri konfigureerimine (valikuline)
##### <a name="finding-your-media-base-url"></a>Oma meediumi aluse URL-i leidmine
*Märkus: enne selle etapi lõpuleviimist peate lõpuni viima **saidi häälestuse** lõpuni viima*.
1. Logige sisse saidi halduse tööriista, kasutades URL-i, mille varem märkisite.
1. Avage sait **Fabrikam**.
1. Valige suvand **Varad** vasakul asuvast menüüst.
1. Valige mis tahes üks pildi vara.
1. Otsige suvand **Avalik URL** paremal asuvast vara inspektorist. Selle sees on URL.
    * Näidis-URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Asendage viimane identifikaator URL-is (MA1nQC ülaltoodud URL-is) järgmise stringiga: **search?fileName=**
    * Näidis-URL pärast asendamist: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * See on teie **Meedia baas-URL** – märkige see üles.
##### <a name="updating-the-media-base-url"></a>Meedia baas-URL-i värskendamine
1. Logige sisse keskkonda (HQ).
1. Vasakul asuva menüü abil avage **Moodulid> Jaemüük > Kanali häälestus > Kanali profiilid**.
1. Klõpsake valikut **Redigeeri**.
1. Suvandis **Profiili atribuudid** asendage atribuudi väärtus **Meedia serveri baas-URL**  väärtusega **Meedia baas-URL**, mille enne lõite.
1. Valige vasakult loendist teine kanal, mis on kanali **Vaikimisi** all.
1. Suvandil **Profiili atribuudid** klõpsake nuppu **+ lisa**.
1. Lisatud atribuudi jaoks valige atribuudivõtmena **Meedia serveri baas-URL** ja atribuudi väärtuseks sisestage **Meedia baas-URL**, mille enne lõite.
1. Klõpsake valikut **Salvesta**.

### <a name="configure-email-server-optional"></a>Meiliserveri konfigureerimine (valikuline)
Palun võtke arvesse, et siin sisestatud SMTP-serveri või meiliteenus peab olema juurdepääsetav Azure'i kordustellimusest, mida kasutate keskkonnas.
1. Logige sisse keskkonda (HQ).
1. Vasakul oleva menüü abil avage **Moodulid > Jaemüük > Peakontori häälestus > Parameetrid > Meili parameetrid**.
1. Klõpsake vahekaarti **SMTP sätted**.
1. Väljale **Väljamineva meiliserver** tippige oma SMTP-serveri või meiliteenuse FQDN või IP-aadress.
1. Väljale **SMTP-pordi number** sisestage pordi number (vaikimisi on see 25, kui te ei kasuta SSL-i).
1. Väljale **Kasutajanimi** tippige väärtus (kui on nõutav autentimine).
1. Väljale **Parool** tippige väärtus (kui on nõutav autentimine).
1. Klõpsake valikut **Salvesta**.
1. Klõpsake käsku **Värskenda**.
1. Klõpsake vahekaarti **Testmeil**.
1. Valige välja meiliteenuse pakkuja väärtuseks **SMTP**.
1. Väljale **Saada** sisestage meiliaadress, millele soovite testmeili saata.
1. Klõpsake käsku **Saada testmeil**.
### <a name="configure-email-templates-optional"></a>Meilimallide konfigureerimine (valikuline)
Meilimall iga kandelise sündmuse jaoks, mille jaoks soovide meile saata, tuleb uuendada kehtiva saatja meiliaadressiga.
1. Vasakul asuva menüü abil avage **Moodulid> Organisatsiooni haldus > Häälestus > Organisatsiooni meilimallid**.
1. Klõpsake valikut **Kuva loend**.
1. Iga malli jaoks loendis tehke järgmist.
    1. Väljale **Saatja meil** tippige saatja meiliaadress selle meilimalli jaoks.
    1. (Valikuline) väljale **Saatja nimi** tippige nimi, mida kasutatakse selle meilimalli saatjana.
1. Klõpsake valikut **Salvesta**.
### <a name="customizing-email-templates-optional"></a>Meilimallide kohandamine (valikuline)
Võite soovida kohandada meilimalle, et kasutada erinevaid pilte või värskendada malli linke, et naasta oma eelvaate keskkonda. Järgmised etapid selgitavad, kuidas vaikimisi malle alla laadida, neid kohandada ja süsteemi malle värskendada.
1. Brauseri abil laadige kohalikku arvutisse [Microsoft Dynamics 365 Commerce eelvaate vaikimisi meilimallide .zip-fail](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), mis sisaldab järgmisi HTML-dokumente.
    1. Tellimuse kinnituse mall
    1. Kinkekaardi väljastamise mall
    1. Uue tellimuse mall
    1. Pakketellimuse mall
    1. Tellimuse malli valimine
1. Kohandage malle teksti või HTML-redaktori abil. Palun vaadake allpool toetatud märkide loendit.
1. Logige sisse keskkonda (HQ).
1. Vasakul asuva menüü abil avage **Moodulid> Jaemüük > Peakontori häälestus > Parameetrid > Organisatsiooni meilimallid**.
1. Kõigi mallide nägemiseks laiendage loendit vasakul.
1. Iga malli puhul, mida soovite kohandada, tehke järgmist.
    1. Valige loendist mall.
    1. Jaotises **Meilisõnumi sisu** valige sobiv keele versioon loendist (vaikimisi **en-US**).
    1. Jaotises **Meilisõnumi sisu** klõpsake valikut **Redigeeri**, peaksite nägema paani **Laadi üles meilimall**.
    1. Klõpsake valikut **Sirvi** ja leidke HTML-fail kohandatud sisuga.
    1. Klõpsake nuppu **Laadi üles**, teie mall laaditakse süsteemi ja kuvatakse eelvaade.
    1. Klõpsake valikut **OK**.
    1. (Valikuline) kohandage malli atribuuti **Teema**.
    1. Klõpsake valikut **Salvesta**.

#### <a name="supported-tokens-in-the-email-template"></a>Toetatud märgid meilimallis
Need märgid asendatakse meili renderdamise ajal tegelike väärtustega, mis rakenduvad kliendile ja nende tellimusele.

**Müügitellimus** – järgmised load rakenduvad üldisele müügitellimusele.

|Märgi nimi|Luba|
|---|---|
|Tellimuse kood|%salesid%|
|Kliendi nimi|%customername%|
|Tarneaadress|%deliveryaddress%|
|Arveaadress|%customeraddress%|
|Tellimuse kuupäev|%shipdate%|
|Tarneviis|%modeofdelivery%|
|Allahindlus|%discount%|
|Käibemaks|%tax%|
|Tellimuse kogusumma|%total%|

**Müügirida** - järgmised load on täidetud iga toote puhul tellimuses.

*Märkus: asetage valikute **Toote loend – algus** ja **Toote loend – lõpp** märgid HTML-ploki algusesse ja lõppu, mis kordub iga toote puhul.*

|Märgi nimi|Luba|
|---|---|
|Tooteloend - algus|\<!--%tablebegin.salesline% -->|
|Tooteloend - lõpp|\<!--%tableend.salesline%-->|
|Toote nimi|%lineproductname%|
|Kirjeldus|%lineproductdescription%|
|Kogus|%linequantity%|
|Reaühiku hind|%lineprice% (kontrollige)|
|reaüksuse kogusumma|%linenetamount%|
|rea allahindlus|%linediscount%|
|Lähetuskuupäev|%lineshipdate%|
|Hanke meetod|%linedeliverymode%|
|tarneaadress|%linedeliveryaddress%|
|Rea müügiüksus|%lineunit%|

