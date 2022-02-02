---
title: Funktsioonihalduse ülevaade
description: Selles teemas kirjeldatakse Funktsioonihaldust ja selle kasutamist.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 6605fe68576ce80726438b60c1f1fbf3782d0934
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984455"
---
# <a name="feature-management-overview"></a>Funktsioonihalduse ülevaade

[!include [banner](../../includes/banner.md)]

Igale väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduse kogemus pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Siis saate kasutada tööruumi funktsioonidokumentatsiooni vaatamiseks ning funktsioonide lubamiseks või keelamiseks.

## <a name="the-feature-management-workspace"></a>Funktsioonihalduse tööruum

Saate avada **Funktsioonihalduse** tööruumi, valides armatuurlaual vastava paani. Näete lehte, kus kuvatakse funktsioonide loend kõigi väljalasete jaoks, mida funktsioohalduse kogemus toetab. 

Funktsioonide loend sisaldab järgmist teavet.

- **Funktsiooni nimi** – lisatud funktsiooni kirjeldus.
- **Olek** – sümbol näitab, kas funktsioon on sisse lülitatud (märge), poel sisse lülitatud (tühi), on plaanitud sisse lülitamiseks (kell), on kohustuslikult sisse lülitatud (lukk), nõuab enne sisselülitamist tähelepanu (hoiatussümbol) või ei saa sisse lülitada (X). Siin kuvatavat sätet kasutatakse kõigi juriidiliste isikute puhul. Pidage meeles, et isegi kui funktsioon on sisse lülitatud, kontrollib seda ikkagi turve. Seetõttu on funktsioon saadaval ainult neile kasutajatele, kellel on sellele juurdepääs, põhinevalt nende turberollil. See on saadaval ainult juriidilistele isikutele, millele kasutajal on juurdepääs.
- **Luba kuupäeval** – kuupäev, millal funktsioon sisse lülitatud või on sisse lülitamiseks plaanitud.
- **Funktsioon lisatud** – kuupäev, mil funktsioon lisati teie keskkonda. See kuupäev sisestatakse automaatselt, kui värskendate oma keskkonda igakuiste väljaannete tsüklite ajal.
- **Funktsiooni olek** – funktsiooni praegune töötsükli olek: **eelvaade**, **vabastatud** (kuvatakse tühjana), **Sisselülitatud vaikimisi** ja **Kohustuslik**. Täpsemate üksikasjadega kaetud olekud on selles teemas hiljem kaetud. 
- **Moodul** – moodul, mida uus funktsioon mõjutab.

> [!NOTE]
> **Funktsiooni oleku** veerg kaasatakse versioonina 10.0.21.

Kui valite funktsiooni, kuvatakse lisateave üksikasjade paanil funktsioonide loendist paremal. Paani ülaosas näete funktsiooni nime, funktsiooni lisamise kuupäeva, funktsiooni poolt mõjutatud moodulit ja linki **Lisateave**. Valige see link funktsiooni dokumentatsiooni vaatamiseks. Kui dokumentatsioon ei ole saadaval, suunatakse teid ajutisele lehele. Üksikasjade paanil on ka väli **Kommentaarid**, kus saate lisada oma kommentaare funktsiooni kohta.

Tööruumis **Funktsioonihaldus** on ka mitu vahekaarti, mis igaüks kuvavad funktsioonide loendi.

- **Uus** – see vahekaart näitab kõiki funktsioone, mis on lisatud alates viimasest igakuisest uuendusest. Kui olete mõne igakuise uuenduse vahele jätnud, kuvab vahekaart kõik uued funktsioonid, mis on lisatud alates viimasest korrast, kui uuendasite. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Pole lubatud** – see vahekaart kuvab kõik funktsioonid, mida pole sisse lülitatud. Uusimad funktsioonid kuvatakse loendi ülaosas. Lisaks kuvatakse lehe ülaosas paanil väljas olevate funktsioonide koguarvu.
- **Plaanitud** – sellel vahekaardil kuvatakse kõik funktsioonid, mis on plaanitud tulevikus sisse lülitada. Kõige varasema plaanitud kuupäevaga funktsioonid kuvatakse loendi ülaosas. Lisaks näitab lehe ülaosas olev paan ajastatud funktsioonide koguarvu.
- **Kõik** – sellel vahekaardil kuvatakse kõik funktsioonid. Uusimad funktsioonid kuvatakse loendi ülaosas.

## <a name="feature-states"></a>Funktsiooni olekud
Funktsioonid võivad muutuda mitme oleku vahel, alustades funktsioonide haldamisest ja muutudes lõpuks tootes kohustuslikuks. See jaotis kirjeldab kehtivaid funktsiooni valikuid.

### <a name="preview-features-optional"></a>Eelvaade funktsioonidele (valikuline)

Tootemeeskonnad saavad otsustada uue funktsiooni algsel käivitamisel eelvaate funktsioonina. Eelvaate funktsioonid pole vaikimisi lubatud ja need on valikulised. Omaniku tootetiim värskendab pärast eduka eelvaateperioodi lõppu väljalasetavaid funktsioone.

> [!NOTE]
> Eelvaate funktsioonid alluvad kindlatele eelvaate [tingimustele](https://go.microsoft.com/fwlink/?linkid=2105274). 

### <a name="released-features-optional"></a>Väljastatud funktsioonid (valikuline)

Nende **funktsioonide oleku** veerg funktsioonina on tühi. Algselt väljastatuna lisatud funktsioone ei lülitata vaikimisi sisse ja nende lubamine on valikuline. Eelvaatest uuendatud funktsioonid säilitavad nende lubamise oleku.

### <a name="on-by-default-features-optional"></a>Vaikefunktsioonid (valikuline)

Funktsioonid, mida uuendatakse **vaikimisi**, on lülitatud vaikimisi sisse, kuid neid saab keelata. Pärast seda, kui funktsioonid, mida saab keelata, on olekus **Vabastatud** olnud vähemalt kuus kuud, eeldatakse, et nad liiguvad järgmise põhivabastuse ajal siia olekusse. Funktsioonid, mis **vaikimisi** lülituvad sissse eeldatava edastamise puhul [Mis on uut](../whats-new-changed.md) väljaandmise teemas. Värskenduse algatab toote omanik.

> [!NOTE]
> Kuna need funktsioonid lubatakse automaatselt, on oluline määrata, kas teie organisatsioon on valmis neid funktsioone uuendama või on vaja rohkem aega. Kui vaja on rohkem aega, võib olla vajalik need funktsioonid ajutiselt keelata. Pange tähele, et funktsiooni siirde vaikimisi valikule **Sees vaikimisi** tehakse tavaliselt põhivabastuses enne, kui see funktsioon on määratud **Kohustuslikuks**. Sel hetkel pole teil võimalust seda funktsiooni keelata. 

### <a name="mandatory"></a>Kohustuslik

**Kohustuslik on** funktsioonide eeldatav lõplik olek. See näitab, et funktsioonid on sisse lülitatud ja te ei saa neid keelata ilma Microsoft`iga kontakteerumata. Valikulised funktsioonid muutuvad kohustuslikuks pärast kahte põhivabastust. Kriitilisi funktsioone saab erandkorras kehtestada kohustuslikuna.

## <a name="example-of-expected-feature-lifecycles"></a>Eeldatava funktsiooni töötsüklite näide

Funktsioonid, mida saab keelata ja mis lisati avaldatuna ja valikulisena enne aprillikuist väljalaset või selle osana, lähevad järgmisel oktoobrikuisel väljaandel üle olekusse **Sees vaikimisi**. Siis muutuvad need **kohustuslikuks** järgmise aasta aprillis.

Funktsioon, mida ei saa keelata ja mis lisati avaldatuna ja valikulisena enne aprillikuist väljalaset või selle osana, läheb järgmise aasta aprillis üle olekusse **Kohustuslik**.

## <a name="enable-a-feature"></a>Funktsiooni lubamine

Kui funktsioon ei ole sisse lülitatud, kuvatakse üksikasjade paanil nupp **Luba kohe**. Selle nupu abil saate funktsiooni lubada.

Pärast funktsioonide lubamist ei saa mõnda neist enam keelata. Kui funktsiooni, mida proovite sisse lülitada, ei saa välja lülitada, kuvatakse hoiatus. Sel hetkel saate toimingu tühistamiseks ja funktsiooni keelamiseks valida **Tühista**. Siiski, kui valite **Luba** ja lubate selle funktsiooni, ei saa te seda hiljem keelata.

Mõned funktsioonid kuvavad enne nende lubamist sõnumi, mis annab lisateavet. Need omadused on tähistatud kollase hoiatussümboliga. Peaksite lisateavet hoolikalt lugema, et veenduda, et saate aru, mis juhtub, kui funktsioon on lubatud. Siiski saate endiselt valida suvandi **Luba**, et funktsioon sisse lülitada.

Mõni funktsioon kuvab sõnum, et funktsiooni ei saa enne toimingu tegemist lubada. Need omadused on tähistatud punane X hoiatussümboliga. Enne funktsiooni lubamist peate täitma kirjelduses kirjeldatud toimingud. Näiteks kui te ei saa kasutada funktsiooni kuni konfiguratsioonivõti on keelatud, siis peate esmalt keelama konfiguratsioonivõtme ja seejärel naasma funktsiooni haldusesse funktsiooni lubamiseks.

Pärast funktsiooni lubamist kuvatakse üksikasjade paanil lingi **Lisateave** all. See teade kas ütleb, et funktsioon lülitati sisse, või näitab kuupäeva, millal on funktsioon plaanitud sisse lülitada. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

Funktsioonid, mis on plaanitud tulevikus sisse lülitada, kuvatakse vahekaardil **Plaanitud**. Pakktöötlus lülitab need määratud kuupäeval keskööl sisse, lähtudes süsteemi kuupäevaga tähistatud ajavööndist.

## <a name="reschedule-a-feature"></a>Funktsiooni uuesti plaanimine

Kui funktsiooni ei ole plaanis tulevikus sisse lülitada, kuvatakse üksikasjade paanil nupp **Plaani**. Selle nupu abil saate muuta suvandi **Luba kuupäeval** väärtuse teiseks kuupäevaks.

1. Valige uuesti plaanimiseks plaanitud funktsioon ja seejärel valige üksikasjade paanil nupp **Plaani**.
2. Kuvatavas dialoogiboksis väljas **Luba kuupäeval** määrake uus kuupäev, millal tuleb funktsioon sisse lülitada.
3. Valige **Luba**, et funktsiooni uuesti plaanida, või **Keela** plaanimise tühistamiseks.

## <a name="disable-a-feature"></a>Funktsiooni keelamine

Kui funktsioon on juba lubatud, kuvatakse üksikasjade paanil nupp **Keela**. Selle nupu abil saate funktsiooni keelata. Nupp **Keela** ei ole saadaval, kui funktsiooni ei saa keelata pärast selle lubamist. 

Pärast funktsiooni keelamist kuvatakse üksikasjade paanil lingi **Lisateave** all teade. See teade ütleb, et funktsioon pole sisse lülitatud. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist. Funktsioonid, mis pole lubatud, kuvatakse vahekaardil **Pole lubatud**.

## <a name="features-that-must-be-enabled"></a>Funktsioonid, mis peavad olema lubatud

Mõnikord lisatakse kriitiline funktsioon, mis tuleb uuendamisel automaatselt sisse lülitada. Need funktsioonid lubatakse automaatselt väljas **Luba kuupäeval** määratud kuupäeval. Nende funktsioonide kohta kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade kinnitab, et funktsioon on lubatud, või näitab tulevast kuupäeva, millal funktsioon lubatakse. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

## <a name="enable-all-features"></a>Kõigi funktsioonide lubamine

Kõik funktsioonid saate lubada, kui valite nupu **Luba kõik**. 

Kui valite **Luba kõik**, kuvatakse suvand, kus peate esitama järgmise teabe:

- Kõigi funktsioonide loend, mis vajavad kinnitamist enne, kui neid saab lubada. Kui soovite funktsioone loendis lubada, valige väärtus **Jah** nupul **Luba funktsioonid, mis vajavad kinnitust**.
- Kõik funktsioonid, mida saab lubada, on lubatud. Neid funktsioone ei saa lubada.

Kõik funktsioonid, mida saab lubada, on lubatud. Kui funktsioon on juba plaanitud tulevikus lubatuks, siis ajakava ei muutu. 

## <a name="enable-all-features-automatically"></a>Luba kõik funktsioonid automaatselt

Kui soovite kõik uued funktsioonid automaatselt lubada, saate tööruumi pealkirja all oleva ripploendi abil muuta, mis juhtub uute funktsioonide lisamisel.

- Kõikide uute funktsioonide automaatseks lubamiseks keskkonda lisandumisel valige **Luba uued funktsioonid automaatselt**.
- Valige **Ärge lubage uusi funktsioone automaatselt** kui kõik rakendatavad uued funktsioonid peaksid teie keskkonda lisamisel olema vaikimisi välja lülitatud.

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

- Kui muudate välja **Lubatud** väärtuseks **Jah**, lülitatakse funktsioon sisse ja välja **Luba kuupäeval** väärtuseks määratakse praegune kuupäev.
- Kui muudate välja **Lubatud** väärtusele **Ei** või jätate välja **Luba kuupäeval** tühjaks, lülitatakse funktsiooni välja ja väli **Luba kuupäeval** tühjendatakse. Välja ei saa lülitada kohustuslikke funktsioone või funktsiooni, mida pole võimalik välja lülitada pärast selle sisse lülitamist.
- Kui muudate välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale.
- Kui muudate välja **Lubatud** väärtusele **Jah** ja muudate välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale. 
- Kui muudate välja **Lubatud** väärtusele **Ei**, aga muudate ka välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale.
- Kui funktsioon lülitatakse sisse ja lisate välja **Luba kuupäeval**, mis on määratud tulevasele kuupäevale, jääb funktsioon sisse lülitatuks. Funktsiooni uuesti plaanimiseks peate muutma välja **Lubatud** väärtuseks **Ei**.

## <a name="feature-management-and-flighting"></a>Funktsioonihaldus ja eelväljaanded

Funktsioonihaldusega saate juhtida igas väljaandes saadetud funktsioone. Eelväljaandega saab Microsoft Teams välja anda funktsioone piiratud arvule klientidele, et neid funktsioone saaks katsetada ja kontrollida kõiki kliente mõjutamata. Funktsioonihaldus ei reguleeri ühtegi eelväljaantud funktsiooni.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Funktsioonihalduse kasutamine ISV-funktsioonide või kohandatud funktsioonide sisselülitamiseks

Funktsioonihaldus pole praegu saadaval sõltumatute tarkvaramüüjate (ISV-d) funktsioonide ja kohandatud funktsioonide jaoks. Kuid Microsoft lisab rohkem funktsioone funktsioonihalduse parandamiseks. Kui need parandused on tehtud, muudab Microsoft funktsioonihalduse saadavaks kõikidele uutele funktsioonidele ja annab juhised funktsioonide uuendamiseks nii, et saaksite seda kasutada.

## <a name="frequently-asked-questions-faq"></a>Korduma kippuvad küsimused (KKK)

### <a name="when-are-features-added-removed-or-changed"></a>Millal funktsioone lisatakse, eemaldatakse või muudetakse? 
Omadused lisatakse, eemaldatakse ja neid muudetakse koodimuudatuste kaudu, mida omavad tootetiimid. Nende muudatuste vastuvõtmiseks tuleb keskkondi värskendada.

### <a name="does-a-feature-become-mandatory-automatically"></a>Kas funktsioon muutub automaatselt kohustuslikuks? 
Ei, funktsioon ei muutu automaatselt kohustuslikuks. Omaniku tootetiim peab koodi muutma.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Miks ei eksisteeri kindlat kohustuslikku lubamiskuupäeva? 
Värskenduste väljaandmissaeg on muutuv, keskkondade värskendamisaeg on muutuv ja kliendid saavad mõne värskenduse vahele jätta. Seetõttu on kindlaid kuupäevi raske määrata. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Kus asub dokumentatsioon kohustuslike funktsioonide kohta? 
Selle dokumentatsiooni koostavad Dynamics 365 rakendusemeeskonnad. Neid funktsioone mainitakse sageli jaotises [Värskendab kliendi funktsiooni olekuid](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) või [Eemaldatud või aegunud funktsioonid](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Kas on olemas tootesisene teatis või märguanne selle kohta, et funktsioon muutub kohustuslikuks? 
Praegu pole olemas teavitamismehhanismi, mis annaks teada, et funktsioon muutub kohustuslikuks.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Kas funktsioone lubatakse kunagi kliendi teadmata? 
Jah, funktsioone saab lubada kliendi teadmata järgmistes olukordades:
- Funktsioon viiakse **Sisse lülitatud vaikimisi**. Selles olekus saab funktsiooni siiski keelata. 
- Funktsiooni uuendatakse **kohustuslikuks**. See muudatus ilmneb ainult koos põhivabastusega. Kriitilisi funktsioone võib igal uuendamisel teisaldada **kohustuslikuks**.

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
