---
title: Funktsioonihalduse ülevaade
description: See teema kirjeldab funktsioonihaldust ja kuidas seda kasutada.
author: ChrisGarty
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 2164c07d1a179a0aa15611b742084d872f41bbfc
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270809"
---
# <a name="feature-management-overview"></a>Funktsioonihalduse ülevaade

[!include [banner](../../includes/banner.md)]

Igale väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduse kogemus pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

## <a name="the-feature-management-workspace"></a>Funktsioonihalduse tööruum

Saate avada **Funktsioonihalduse** tööruumi, valides armatuurlaual vastava paani. Näete lehte, kus kuvatakse funktsioonide loend kõigi väljalasete jaoks, mida funktsioohalduse kogemus toetab. Aja jooksul parandab Microsoft funktsioonihalduse kogemust, et see sisaldaks rohkem funktsioone funktsioonide haldamiseks.

Funktsioonide loend sisaldab järgmist teavet.

- **Funktsiooni nimi** – lisatud funktsiooni kirjeldus.
- **Lubatud olek** – sümbol näitab, kas funktsioon on sisse lülitatud (märge), poel sisse lülitatud (tühi), on plaanitud sisse lülitamiseks (kell) või on kohustuslikult sisse lülitatud (lukk). Siin kuvatavat sätet kasutatakse kõigi juriidiliste isikute puhul. Pidage meeles, et isegi kui funktsioon on sisse lülitatud, kontrollib seda ikkagi turve. Seetõttu on funktsioon saadaval ainult neile kasutajatele, kellel on sellele juurdepääs, mis põhineb nende turberollil. See on saadaval ainult juriidilistele isikutele, millele kasutajal on juurdepääs.
- **Luba kuupäeval** – kuupäev, millal funktsioon sisse lülitatud või on sisse lülitamiseks plaanitud.
- **Funktsioon lisatud** – kuupäev, mil funktsioon lisati teie keskkonda. See kuupäev sisestatakse automaatselt, kui värskendate oma keskkonda igakuiste väljaannete tsüklite ajal.
- **Moodul** – moodul, mida uus funktsioon mõjutab.

Kui valite funktsiooni, kuvatakse lisateave üksikasjade paanil funktsioonide loendist paremal. Paani ülaosas näete funktsiooni nime, funktsiooni lisamise kuupäeva, funktsiooni poolt mõjutatud moodulit ja linki **Lisateave**. Valige see link funktsiooni dokumentatsiooni vaatamiseks. Kui dokumentatsioon ei ole saadaval, suunatakse teid ajutisele lehele. Üksikasjade paanil on ka väli **Kommentaarid**, kus saate lisada oma kommentaare funktsiooni kohta.

Tööruumis **Funktsioonihaldus** on ka mitu vahekaarti, mis igaüks kuvavad funktsioonide loendi.

- **Uus** – see vahekaart näitab kõiki funktsioone, mis on lisatud alates viimasest igakuisest uuendusest. Kui olete mõne igakuise uuenduse vahele jätnud, kuvab vahekaart kõik uued funktsioonid, mis on lisatud alates viimasest korrast, kui uuendasite. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Pole lubatud** – see vahekaart kuvab kõik funktsioonid, mida pole sisse lülitatud. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute sisse lülitamata funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Plaanitud** – sellel vahekaardil kuvatakse kõik funktsioonid, mis on plaanitud tulevikus sisse lülitada. Kõige varasema plaanitud kuupäevaga funktsioonid kuvatakse loendi ülaosas. Uute graafikus olevate funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Kõik** – sellel vahekaardil kuvatakse kõik funktsioonid. Uusimad funktsioonid kuvatakse loendi ülaosas.

## <a name="turn-on-a-feature"></a>Funktsiooni sisselülitamine

Kui funktsioon ei ole sisse lülitatud, kuvatakse üksikasjade paanil nupp **Luba kohe**. Selle nupu abil saate funktsiooni sisse lülitada.

- Valige funktsioon, mida soovite sisse lülitada, ja seejärel valige üksikasjade paanil nupp **Luba kohe**. Funktsioon lülitatakse sisse.

Mõnda funktsiooni ei saa pärast sisse lülitamist välja lülitada. Kui funktsiooni, mida proovite sisse lülitada, ei saa välja lülitada, kuvatakse hoiatus. Saate valida nupu **Tühista** toimingu tühistamiseks ja jätta funktsiooni väljalülitatuks. Kui aga valite nupu **Luba** funktsiooni sisselülitamiseks, ei saa te seda hiljem välja lülitada.

Mõni funktsioon kuvab sõnumi, mis annab lisateavet enne nende sisselülitamist. Need omadused on tähistatud kollase hoiatussümboliga. Lugege lisateavet hoolikalt, et paremini mõista, mis juhtub, kui funktsioon on lubatud. Siiski saate endiselt valida suvandi **Luba**, et funktsioon sisse lülitada.

Mõni funktsioon kuvab sõnum, et funktsiooni ei saa enne toimingu tegemist lubada. Need omadused on tähistatud punane X hoiatussümboliga. Enne funktsiooni lubamist peate täitma kirjelduses kirjeldatud toimingud. Näiteks kui te ei saa kasutada funktsiooni kuni konfiguratsioonivõti on keelatud, siis peate esmalt keelama konfiguratsioonivõtme ja seejärel naasma funktsiooni haldusesse funktsiooni lubamiseks.

Kui funktsioon on sisse lülitatud, kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade kas ütleb, et funktsioon lülitati sisse, või näitab see kuupäeva tulevikus, millal funktsioon on plaanitud sisse lülitada. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

Funktsioonid, mis on plaanitud tulevikus sisse lülitada, kuvatakse vahekaardil **Plaanitud**. Pakktöötlus lülitab need määratud kuupäeval keskööl sisse, lähtudes süsteemi kuupäevaga tähistatud ajavööndist.

## <a name="reschedule-a-feature"></a>Funktsiooni uuesti plaanimine

Kui funktsiooni ei ole plaanis tulevikus sisse lülitada, kuvatakse üksikasjade paanil nupp **Plaani**. Selle nupu abil saate muuta suvandi **Luba kuupäeval** väärtuse teiseks kuupäevaks.

1. Valige uuesti plaanimiseks plaanitud funktsioon ja seejärel valige üksikasjade paanil nupp **Plaani**.
2. Kuvatavas dialoogiboksis väljas **Luba kuupäeval** määrake uus kuupäev, millal tuleb funktsioon sisse lülitada.
3. Valige **Luba**, et funktsiooni uuesti plaanida, või **Keela** plaanimise tühistamiseks.

## <a name="turn-off-a-feature"></a>Funktsiooni väljalülitamine

Kui funktsioon on juba sisse lülitatud, kuvatakse üksikasjade paanil nupp **Keela**. Selle nupu abil saate funktsiooni välja lülitada. Nupp **Keela** ei ole saadaval, kui funktsiooni ei saa välja lülitada pärast selle sisse lülitamist.

- Valige välja lülitamiseks funktsioon ja seejärel valige üksikasjade paanil nupp **Keela**. Funktsioon lülitatakse välja ja väli **Luba kuupäeval** tühjendatakse.

Kui funktsioon on välja lülitatud, kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade ütleb, et funktsioon pole veel sisse lülitatud. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist. Funktsioonid, mida pole sisse lülitatud, kuvatakse vahekaardil **Pole lubatud**.

## <a name="features-that-must-be-turned-on"></a>Funktsioonid, mis peavad olema sisse lülitatud

Mõnikord lisatakse kriitiline funktsioon, mis tuleb uuendamisel automaatselt sisse lülitada. Need funktsioonid lülitatakse sisse automaatselt väljas **Luba kuupäeval** määratud kuupäeval. Nende funktsioonide kohta kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade kas ütleb, et funktsioon lülitati sisse, või näitab kuupäeva, millal funktsioon sisse lülitatakse. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

## <a name="enable-all-features"></a>Kõigi funktsioonide lubamine

Vaikimisi lülitatakse kõik teie keskkonda lisatavad funktsioonid välja, kui need pole kohustuslikud funktsioonid. Kõik funktsioonid saate lubada, kui valite nupu **Luba kõik**. 

Kui valite **Luba kõik**, kuvatakse suvand, kus peate esitama järgmise teabe.
- Kõigi funktsioonide loend, mis vajavad kinnitamist enne, kui neid saab lubada. Kui soovite funktsioone loendis lubada, valige väärtus **Jah** nupul **Luba funktsioonid, mis vajavad kinnitust**.
- Kõik funktsioonid, mida saab lubada, on lubatud. Neid funktsioone ei saa lubada.

Kõik funktsioonid, mida saab lubada, on lubatud. Kui funktsioon on juba plaanitud tulevikus lubatuks, siis ajakava ei muutu. 

## <a name="turn-on-all-features-automatically"></a>Kõikide funktsioonide automaatselt sisselülitamine

Vaikimisi lülitatakse kõik teie keskkonda lisatavad funktsioonid välja, kui need pole kohustuslikud funktsioonid. Kuid kui soovite kõiki uusi funktsioone automaatselt sisse lülitada, saate kasutada ripploendit tööruumi nime all, et muuta, mis juhtub uute funktsioonide lisamisel.

- Kõikide uute funktsioonide automaatseks lubamiseks keskkonda lisandumisel valige `Enable new features automatically`.
- Kõikide uute funktsioonide automaatseks keelamiseks keskkonda lisandumisel valige `Do not enable new features automatically`.


Kui lubate kõik funktsioonid automaatselt, lubab see kõik funktsioonid, mis oleks lubatud, kui klõpsate nuppu **Luba kõik**. See ei luba kinnitamist nõudvaid funktsioone või funktsioone, mida ei saa enne toimingu tegemist lubada.

## <a name="check-for-updates"></a>Otsi värskendusi

Funktsioonid lisatakse teie keskkonda pärast iga värskendust. Siiski saate käsitsi värskendusi otsida, klõpsates nuppu **Otsi värskendusi**. Iga funktsioon, mis lisati süsteemi pärast värskendust, lisatakse funktsioonide loendisse. Näiteks kui kaasatud funktsioon on lubatud pärast väljaandmist, siis saate otsida värskendusi ja funktsioon lisatakse teie loendisse.

## <a name="assigning-roles"></a>Rollide määramine

Tööruumi **Funktsioonihaldus** saavad avada süsteemiadministraatorid ja ka kasutajad, kes on määratud funktsioonihalduri või funktsiooni vaataja rolli. Need kaks rolli loodi funktsioonihalduse kogemuse toetamiseks. Funktsioonihalduri rollis kasutajad saavad mis tahes funktsioone sisse või välja lülitada. Nad võivad ka värskendada funktsiooni välja **Kommentaarid**. Funktsiooni vaataja rollis kasutajad saavad ainult vaadata tööruumi **Funktsioonihaldus**. Nad ei saa funktsioone sisse või välja lülitada.

Funktsioonihalduri roll ja funktsiooni vaataja roll ei alista kasutaja kehtivat turvet. Nad kontrollivad lihtsalt seda, kas kasutaja saab funktsioone sisse ja välja lülitada. Need ei anna juurdepääsu funktsioonidele enestele.

## <a name="features-that-use-configuration-keys"></a>Konfiguratsioonivõtmeid kasutavad funktsioonid

Kui funktsioon kasutab konfiguratsioonivõtit, aga konfiguratsioonivõti ei ole sisse lülitatud, ei kuva tööruum **Funktsioonihaldus** funktsiooni saadaolevate funktsioonide loendis. Kui olete konfiguratsioonivõtme sisse lülitanud, peate uuendama funktsioonide loendit, kasutades menüü-üksust **Kontrolli uuendusi**. Funktsioon kuvatakse seejärel funktsioonide loendis.

Kui lülitate konfiguratsioonivõtme välja, ei eemaldata funktsiooni funktsioonide loendist.

## <a name="data-entities"></a>Andmeüksused

Andmeüksusega nimega **Funktsioonihaldus** saate eksportida funktsioonihalduse sätteid ühest keskkonnast ja importida need teise keskkonda. See üksus uuendab ainult olemasolevaid funktsioone. Üksuse äriloogika aitab ka tagada seda, et pärast importimist rakendatakse samad reeglid, mida kasutatakse tööruumis **Funktsioonihaldus**. Näiteks ei saa alistada kohustusliku funktsiooni sätet, eemaldades importimise ajal kuupäeva.

Järgmistest näidetes kirjeldatakse, mis juhtub, kui kasutate andmete importimiseks üksust **Funktsioonihaldus**.

- Kui muudate välja **Lubatud** väärtusele **Jah**, lülitatakse funktsioon sisse ja välja **Luba kuupäeval** väärtuseks määratakse praegune kuupäev.
- Kui muudate välja **Lubatud** väärtusele **Ei** või jätate välja **Luba kuupäeval** tühjaks, lülitatakse funktsioon välja ja väli **Luba kuupäeval** tühjendatakse. Välja ei saa lülitada kohustuslikke funktsioone või funktsiooni, mida pole võimalik välja lülitada pärast selle sisse lülitamist.
- Kui muudate välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale.
- Kui muudate välja **Lubatud** väärtusele **Jah** ja muudate välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale. 
- Kui muudate välja **Lubatud** väärtusele **Ei**, aga muudate ka välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale.
- Kui funktsioon lülitatakse sisse ja lisate välja **Luba kuupäeval**, mis on määratud tulevasele kuupäevale, jääb funktsioon sisse lülitatuks. Funktsiooni uuesti plaanimiseks peate muutma välja **Lubatud** väärtusele **Ei**.

## <a name="feature-management-and-flighting"></a>Funktsioonihaldus ja eelväljaanded

Funktsioonihaldusega saate juhtida igas väljaandes saadetud funktsioone. Eelväljaandega saab Microsoft Teams välja anda funktsioone piiratud arvule klientidele, et neid funktsioone saaks katsetada ja kontrollida kõiki kliente mõjutamata. Funktsioonihaldus ei reguleeri ühtegi eelväljaantud funktsiooni.

## <a name="new-features-are-optional-for-12-months"></a>Uued funktsioonid on valikulised 12 kuu jooksul

Uue mitte-kriitilise funktsiooni installimisel on see 12 kuu jooksul valikuline. See võimaldab planeerida teil ja teie organisatsioonil ette, millal funktsiooni kasutusele võtta ja testida seda koos teie igapäevaste toimingutega. Lisateavet vt teemast [Ühe versiooni teenuse värskenduste KKK](../one-version.md#what-about-new-features).

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Funktsioonihalduse kasutamine ISV-funktsioonide või kohandatud funktsioonide sisselülitamiseks

Funktsioonihaldus pole praegu saadaval sõltumatute tarkvaramüüjate (ISV-d) funktsioonide ja kohandatud funktsioonide jaoks. Kuid Microsoft lisab rohkem funktsioone funktsioonihalduse parandamiseks. Kui need parandused on tehtud, muudab Microsoft funktsioonihalduse saadavaks kõikidele uutele funktsioonidele ja annab juhised funktsioonide uuendamiseks nii, et saaksite seda kasutada.

## <a name="frequently-asked-questions-faq"></a>Korduma kippuvad küsimused (KKK)

### <a name="when-are-features-added-removed-or-changed"></a>Millal funktsioone lisatakse, eemaldatakse või muudetakse? 
Funktsioone lisatakse, eemaldatakse ja muudetakse koodimuudatuste kaudu. Nende muudatuste aktiveerimiseks tuleb keskkondasid värskendada.

### <a name="does-a-feature-become-mandatory-automatically"></a>Kas funktsioon muutub automaatselt kohustuslikuks? 
Ei, funktsiooni kohustuslikuks muutumine ei ole automaatne tegevus. Tootemeeskonnad peavad koodi muutma.

### <a name="when-do-features-become-mandatory"></a>Millal muutuvad funktsioonid kohustuslikuks? 
Reeglite järgi saab uute funktsioonidega nõustuda 12 kuu jooksul ning enne funktsiooni lubamist ei pea muudatusi haldama. Tootemeeskonnad saavad valida, kas muuta funktsioon pärast selle perioodi lõppu kohustuslikuks. 

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Miks ei eksisteeri kindlat kohustuslikku lubamiskuupäeva? 
Värskenduste väljaandmissaeg on muutuv, keskkondade värskendamisaeg on muutuv ja kliendid saavad mõne värskenduse vahele jätta. Seetõttu on kindlaid kuupäevi raske määrata. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Kus asub dokumentatsioon kohustuslike funktsioonide kohta? 
Selle dokumentatsiooni koostavad Dynamics 365 rakendusemeeskonnad. Neid funktsioone mainitakse sageli jaotises [Värskendab kliendi funktsiooni olekuid](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) või [Eemaldatud või aegunud funktsioonid](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Kas on olemas tootesisene teatis või märguanne selle kohta, et funktsioon muutub kohustuslikuks? 
Praegu pole olemas teavitamismehhanismi, mis annaks teada, et funktsioon muutub kohustuslikuks.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Kas funktsioone lubatakse kunagi kliendi teadmata? 
Jah, kui funktsioonidel ei ole funktsionaalset mõju, võidakse need vaikimisi lubada.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Mis on eelväljaanne ja kuidas on see seotud funktsioonihaldusega? 
Funktsiooni eelväljaanded on Microsofti kontrollitavad reaalajas sisse-väljalülitid. Need eristuvad kliendi kontrollitavatest suvanditest, mida pakub funktsioonihaldus. 
- Funktsioonide privaatseid eelversioone ei kuvata funktsioonihalduses enne, kui eelväljaanded on sisse lülitatud. Selle jaoks peab klient tootmiskeskkonnas andma nõusoleku spetsiaalse programmiga ühinemiseks.
- Kui eelväljaanded pole välja lülitatud, loetletakse funktsioonide avalikud eelversioonid ja väljastatud (üldiselt saadaolevad) funktsioonid funktsioonihalduses. Tootemeeskonnad lülitavad funktsiooni eelväljaande välja ainult viimases hädas kriitilise probleemi leidmise korral ning tavaliselt tehakse seda ühe kliendi kaupa.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Kas funktsioonide eelväljaandeid keelatakse kunagi kliendi teadmata? 
Jah, kui funktsioon mõjutab sellise keskkonna toimimist, millel ei ole funktsionaalset mõju, võidakse funktsioon lubada vaikimisi.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Kuidas saab funktsiooni lubamist koodis kontrollida?
Kasutage klassi **FeatureStateProvider** meetodit **isFeatureEnabled**, edastades sellele funktsiooniklassi eksemplari. Näide:

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Kuidas saab funktsiooni lubamist metaandmetes kontrollida?
Atribuuti **FeatureClass** saab kasutada näitamaks, et osa metaandmetest on seostatud funktsiooniga. Kasutada tuleb funktsiooni jaoks kasutatud klassinime, nt **BatchContentionPreventionFeature**. Need metaandmed on nähtavad ainult selles funktsioonis. Atribuut **FeatureClass** on saadaval menüüdes, menüükäskudes, loeteluväärtustes ja tabeli/vaate väljadel.

### <a name="what-is-a-feature-class"></a>Mis on funktsiooniklass?
Funktsioonihalduses nimetatakse funktsioone *funktsiooniklassideks*. Funktsiooniklass **rakendab klassi IFeatureMetadata** ja kasutab funktsiooniklassi atribuuti, et ennast funktsioonihalduse tööruumis tuvastada. Leidub paljusid näiteid saadaolevatest funktsiooniklassidest, mille lubamist saab koodis kontrollida API **FeatureStateProvider** abil ning metaandmetes atribuudi **FeatureClass** abil. Näide:

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Mis on IFeatureLifecycle, mida rakendavad mõned funktsiooniklassid?
IFeatureLifecycle on Microsofti-sisene mehhanism, mis näitab funktsiooni elutsükli etappi. Funktsioonid võivad olla järgmised.
- `PrivatePreview` – vajab eelväljaannet, et olla nähtav.
- `PublicPreview` – kuvatakse vaikimisi, kuid koos hoiatusega, et tegemist on funktsiooni eelversiooniga.
- `Released`– täielikult väljastatud.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
