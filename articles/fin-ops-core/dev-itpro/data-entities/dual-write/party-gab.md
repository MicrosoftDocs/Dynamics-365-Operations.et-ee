---
title: Osapool ja globaalne aadressiraamat
description: Selles teemas kirjeldatakse osapoole ja globaalse aadressiraamatu topeltkirjutuse funktsioone.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750784"
---
# <a name="party-and-global-address-book"></a>Osapool ja globaalne aadressiraamat

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

„Osapool” ja „Globaalne aadressiraamat” on põhimõtted Finance and Operationsi rakendustes. Osapooleks võib olla organisatsioon või isik. **Osapoole** atribuute on mugav globaalselt talletada ja hallata (nt nimi, keel, kontaktid ja aadressid). Kui atribuudi väärtus muutub ühes kohas, peegeldub see kõigis kohtades, kus **Osapool** on kasutusel.

## <a name="party"></a>Osapool

*Osapool* on ettevõttega seotud isik või organisatsioon. Osapoole kontseptsiooni kasutades saab inimene või organisatsioon ettevõttes täita rohkem kui ühte rolli (töötaja, klient, hankija või kontakt). Roll põhineb kontekstil ja eesmärgil. Siin on mõned näited kahest fiktiivstest ettevõtetest: Contoso ja Fabrikam.

+ **Töötaja**: töövõtja. Näiteks Contoso töövõtja
+ **Hankija**: tarnijaorganisatsioon või ainuomanik, kes tarnib ettevõttele kaupu või teenuseid. Näiteks kui Fabrikam müüb varusid Contosole, on Fabrikam hankija rollis.
+ **Kontakt**: kontaktisik. Näiteks kui Contoso ostab varusid Fabrikamilt, võtab Contoso töövõtja ühendust Fabrikami kontaktiga.
+ **Klient** : klient on isik või ettevõte, kes ostab ettevõttelt kaupu. Näiteks kui Contoso ostab varusid Fabrikamilt, on Contoso Fabrikami klient.

Osapoole mudelit kasutatakse sageli organisatsioonide ja inimeste vaheliste keerukate suhete meediumi kajastamiseks, eriti siis, kui osapool esitab rohkem kui ühte rolli. Järgmisena on toodud mõned levinumad näited.

+ Osapool võib olla nii klient kui ka hankija. Näiteks müüb Fabrikam Põhja-Ameerikas Contosole elektrijuhtmeid ja ostab Contosolt kokkupandud kõlareid. Euroopas müüb Fabrikam Contosole varuosi, kuid ei osta Contosolt midagi.
+ Osapool võib olla nii töövõtja kui ka klient. Näiteks ostab Contoso töövõtja Contosost elektroonikat isiklikuks kasutamiseks.
+ Isiku ja organisatsiooni vahel võib olla mitu-mitmele-seosed. Näiteks varustab Fabrikam teenusespetsialiste ja tööle on võetud paigutuse koordinaator. Koordinaator viib teenusespetsialistid vastavusse mitme Fabrikami kliendi töötaotlustega. Contoso on üks kliendikontodest. Kui Contoso vajab spetsialisti, võtab Contoso ühendust koordinaatoriga, kes seejärel vahendab taotlust. Koordinaator tegeleb kõigi klientide taotlustega, luues mitu-mitmele-seosed.

Järgmine pilt näitab Osapoole andmemudelit.

![Osapoole andmemudel](media/party-gab-image1.png)

> [!Tip]
> Kui proovite luua uut kontokirjet, kasutage välja "Osapool" kirje otsimiseks nime järgi. Kui leiate kirje, peate selle kirje vaid valima. Süsteem täidab automaatselt kõik osapoole andmed. Kõiki nõutavaid välju ei tule käsitsi täita. Selline käitumine võib ilmneda vormidel „Konto”, „Kontakt” ja „Hankija”, mis on tarnitud valmislahendusena.

Topeltkirjutus ei toeta kõiki Finance and Operationsi rakenduste osapoole rolle. Osapoolte rollide täieliku loendit vt [Globaalse aadressiraamatu ülevaade](../../../fin-ops/organization-administration/overview-global-address-book.md)ülevaatest.

### <a name="global-address-book"></a>Globaalne aadressiraamat

Globaalne aadressiraamat on ettevõttes osalevate organisatsioonide ja üksikisikute posti- ja elektronaadresside kataloog.

Globaalses aadressiraamatus talletatakse ja käsitletakse nii palju postiaadresse ja elektroonilisi aadresse, kui vaja. Oletame näiteks, et Fabrikamil on bensiinijaamad 50 asukohas. Igal asukohal on erinev postiaadress, meil ja telefoninumber. Kõigile äriostude arved lähevad põhibensiinijaama arvele, kuid ostud tarnitakse kindlasse bensiinijaama, mis ostu taotles. Globaalne aadressiraamat talletab Fabrikami põhibensiinijaama arveaadressina ja kõik bensiinijaamad tarneaadressina. Aadresse saab talletada üks kord ja neid saab tuua vastavalt pakkumis- ja tellimusvajadusele.

Inimene või organisatsioon saab ettevõtte kontekstil põhinevalt täita rohkem kui üht rolli. Kui seda tehakse, võivad inimeste posti- ja elektronaadressid olla samad. Sel juhul peab ühe rolli aadressimuutus kajastuma teises rollis ja vastupidi. Globaalne aadressiraamat talletab ja käsitleb aadresse globaalselt.

![Globaalse aadressiraamatu andmemudel](media/party-gab-image2.png)

## <a name="contacts"></a>Kontaktid

Kliendikogemuse rakenduses on *Kontakt* isik. Tabel **Kontakt** on ülekoormatud, et tähistada isikut, portaali kasutajat, B2C-klienti või hankijat. Esitus toimub vaikimisi ja erinevust pole võimlik teha seotud kandeid uurimata. Tabelil **Kontakt** on piiratud 1:1 seos tabeliga **Konto**. „Osapoole” ja globaalse aadressiraamatu mudeli osana tutvustatakse topeltkirjutuse klassifikatsiooni ning topeltkirjutus lubab atribuute, mis võimaldavad N:N-seoseid **Kontakt** isiku ja organisatsiooni vahel (konto üksus või hankija üksus).

Ridu **Kontakt** on kahte tüüpi.

+ Vöödiline kontakt – kontaktirida, millel on kohustuslik väärtus väljal **Ettevõte**.
+ Vöötideta kontakt – kontaktirida, kus väli **Ettevõte** on tühi.

Tabel **Kontakt** võib talletada järgmist tüüpi ridu:

Rea tüüp | Kirjeldus
---|---
Isik, kes on klient, nt müüdav kontakt või B2C-klient. | Vöödelise kontakti kirje, milles väli **Ettevõte** ei ole tühi ning väli **Klient** on seatud väärtuseks **Jah**.
Isik, kes on hankija, näiteks ainuomanik nagu hankija. | Vöödelise kontakti kirje, milles väli **Ettevõte** ei ole tühi ning väli **Hankija** on seatud väärtuseks **Jah**.
Isik on korraga nii klient kui ka hankija. | Vöödelise kontakti kirje, milles väli **Ettevõte** ei ole tühi ning väli **On klient** on seatud väärtuseks **Jah**, ja väli **On hankija** on seatud väärtuseks **Jah**. Isik võib olla nii ühe toote tootja kui ka teise toote tarbija. Seda Finance and Operationsi rakenduste suhet toetavad nii rakendused kui ka topeltkirjutus.
Isik, kes on organisatsiooni kontaktisik, kuid ei ole klient ega hankija. | Vöödita kontakti kirje, milles väli **Ettevõte** on tühi ning väli **On klient** on seatud väärtuseks **Ei**, ja väli **On hankija** on seatud väärtuseks **Ei**.

## <a name="contact-for-party"></a>Osapoole kontakt

**Osapoole kontakt** talletav ja käsitseb N:N-seoseid välja **Konto** ridade ja välja **Kontakt** ridade vahel. See võib välja filtreerida vöödilise **Kontakti** read vöötideta ridadest ja seostada ainult vöötideta **Kontakti** read **Konto** või **Hankija** ridadega.

Näiteks on Natasha Jones ja Miguel Reyes veterinaarid, kes oma piirkonnas asuvaid farme teenindavad. Natasha teenindab Seattle'i piirkonda ja Miguel Kenti piirkonda. Klienditeeninduse rakenduses on farmid esitatud klientidena ja veterinaarid on kontaktisikud. Üksikut **Kontakti** kirjet Natasha jaoks seostatakse kõigi farmidega, kus Natasha töötab. Samamoodi seostatakse ühte **Kontakti** kirjet Migueli jaoks kõigi farmidega, kus Miguel töötab.

Need seosed salvestatakse tabelisse **Kontakt osapoole jaoks**. Teabe leiate valmislahenduste vormidest.

+ Kui olete vormil **Konto**, leiate sealt vahekaardi nimega **Seotud kontaktid**. Kasutage seda vahekaarti, et seostada üks või mitu kontakti **Konto** reaga. Sellel vormil määrate organisatsiooni kontaktisiku. Pärast kontaktide määramist saate valida ühe kontakti konto esmaseks kontaktiks. Vormi **Kiirloomine** kasutamisel saate valida ainult kontaktisiku. Käitumine on sama, kui kasutate vormi **Hankija** ja kirje tüüp on **Organisatsioon**.
+ Kui olete vormil **Kontakt** ja rida on klient, hankija või mõlemad (vöödiga kontakt), siis seal on vahekaart nimega **Seotud kontaktid**. Kasutage seda vahekaarti, et seostada üks või mitu kontakti. Sellel vormil määrate organisatsiooni kontaktisiku B2C-kliendi või hankija jaoks. Pärast kontaktide määramist saate valida ühe esmaseks kontaktiks. Vormi **Kiirloomine** kasutamisel saate valida ainult kontaktisiku.
+ Kui olete vormil **Kontakt** ja rida on kontaktisik (vöödita kontakt), siis seal on vahekaart nimega **Seotud organisatsioonid**. Kasutage seda vahekaarti, et seostada üks või mitu klienti või hankijat. Sellel vormil määrate kliendi või hankija kontaktisiku jaoks. Klient või hankija võib olla organisatsioon, isik või mõlemad. Määratud aja jooksul saate neljalt väljalt valida ainult ühe väärtuse.

    ![Vahekaart „Seotud organisatsioonid”](media/party-gab-image3.png)

    + Kui valite **Osapoole ID**, siis määratakse aluseks olev kontakt kõikidele valitud osapoole rollidele.
    + Kui valite **Seostatud kontakti**, valite sellega vöödiga kontakti, mis on isiku tüüp.
    + Kui valite **Seostatud konto** või **Hankija**, siis valite organisatsiooni.

    Sõltumata teie valikust luuakse seos osapoole tasemel ja see on rakendatav kõigile osapoole rollidele ning talletatakse üksuses „Kontakt osapoole jaoks”.

> [!Note]
> Kliendikogemuse rakenduses tabeli **Kontakt osapoole jaoks** kuvanimi on **Kontakt kliendi/hankija jaoks**.

Kui avate **Kontakti** rea, kus **On klient** on **Ei** ja **On hankija** on **Ei**, näete vahekaarti **Seostatud organisatsioonid**. Kasutage seda vahekaarti, et seostada kontaktiga üks või mitu klienti või hankeorganisatsiooni.

Kui avate **Kontakti** rea, kus **On klient** on **Jah** või **On hankija** on **Jah**, näete vahekaarti **Seostatud kontaktid**. Kasutage seda vahekaarti, et seostada üks või mitu kontakti.

## <a name="postal-address"></a>Postiaadress

Uus vahekaart **Aadressid** on sisse viidud vormidele **Konto**, **Kontakt** ja **Hankija**. **Aadressid** toetavad N-aadresse ruudustiku abil, nagu näha sellel pildil.

![Ruudustik postiaadressi jaoks](media/party-gab-image4.png)

+ Veerus **Postiaadressi rollid** loetletakse aadressi eesmärgid.
+ Veerus **On esmane** loetletakse esmane aadress.
+ Veerus **Aadressi number** kuvatakse aadressijärjestus.
+ Nupp **+ Uus aadress** võimaldab teil luua uue aadressi. Saate luua soovitud arvu aadresse.

Väljad **Aadress 1** ja **Aadress 2** vahekaardil **Kokkuvõte** vormil **Konto** vastab vastavalt **Tarneaadressile** ja **Arveaadressile**.

![Postiaadressi kokkuvõtte vahekaart](media/party-gab-image5.png)

Väljad **Aadress 1**, **Aadress 2** ja **Aadress 3** vahekaardil **Kokkuvõte** vormil **Kontakt** vastab vastavalt **Ettevõtte asukoha aadressile**, **Tarneaadressile** ja **Arveaadressile**.

## <a name="electronic-address"></a>Elektrooniline aadress

Uus vahekaart **Elektronaadressid** on sisse viidud vormidele **Konto**, **Kontakt** ja **Hankija**. **Aadressid** toetavad N-aadresse ruudustiku abil, nagu näha sellel pildil.

![Ruudustik elektronaadressi jaoks](media/party-gab-image6.png)

+ Veerus **Tüüp** loetletakse aadressitüübid.
+ Veerus **On esmane** loetletakse esmane aadress.
+ Veerus **Eesmärk** loetletakse elektronaadressi eesmärgid.
+ **+ Uus elektronaadress** võimaldab teil luua uue aadressi. Saate luua soovitud arvu aadresse.

Elektron aadressid on saadaval ainult selles ruudustikus. Tulevastes väljalasetes eemaldatakse kõik elektron- ja postiaadressi väljad teistelt vahekaartidelt, näiteks vahekaartidelt **Kokkuvõte** ja **Üksikasjad**.

## <a name="setup-instructions"></a>Seadistusjuhised

Kui olete olemasoleva topeltkirjutusega klient, nõutakse järgmisi seadistusjuhiseid. Muul juhul võite selle jaotise vahele jätta.

1. Peatage järgmised kaardid, kuna need pole enam nõutavad. Selle asemel käivitage kaart Contacts V2 (msdyn_contactforparties).

    + CDS Contacts V2 ja Contacts (viitab kliendi kontaktidele)
    + CDS Contacts V2 ja Contacts (viitab hankija kontaktidele)

2. Järgmised üksuste vastendused värskendatakse osapoole funktsioonide jaoks, nii et nendele vastendustele tuleb rakendada uusimat versiooni.

Vastenda | Värskendage selle versioonini | Muutused
---|---|---
Kliendid V3 (kontod) | 1.0.0.5 |Eemaldatud PartyNumber ja teised osapoolega seotud väljad nagu nimi, isiklikud üksikasjad, postiaadressi väljad, elektroonilise kontaktiaadressi väljad jne.
Klient V3 (kontaktid) | 1.0.0.5 | Eemaldatud PartyNumber ja teised osapoolega seotud väljad nagu nimi, isiklikud üksikasjad, postiaadressi väljad, elektroonilise kontaktiaadressi väljad jne.
Hankijad V2 (msdyn_vendors) | 1.0.0.6 | Eemaldatud PartyNumber ja teised osapoolega seotud väljad nagu nimi, isiklikud üksikasjad, postiaadressi väljad, elektroonilise kontaktiaadressi väljad jne.
CDS müügipakkumise päised (pakkumised) | 1.0.0.6 | Asendas kontaktisiku viitega ContactforParty.
Müügiarve päised V2 (arved) | 1.0.0.4 | Asendas kontaktisiku viitega ContactforParty.
CDS müügitellimuste päised (salesorders) | 1.0.0.5 | Asendas kontaktisiku viitega ContactforParty.
Kontaktid V2 (msdyn_contactforparties) | 1.0.0.2 | See on uus kaart. Kui teil on osapoole lahenduse eelmine versioon, värskendage see kaart uusimale maintiud versioonile.
CDS-osapoole postiaadresside asukohad (msdyn_partypostaladdresses) | 1.0.0.1  | See on uus kaart, mis on lisatud osana eelmise osapoole eelvaate väljalaskest.
CDS-i postiaadresside ajalugu V2 (msdyn_postaladdresses) | | See on uus kaart, mis on lisatud osana eelmise osapoole eelvaate väljalaskest.
CDS-i postiaadresside asukohad (msdyn_postaladdresscollections) | | See on uus kaart, mis on lisatud osana eelmise osapoole eelvaate väljalaskest.
Osapoole kontaktid V3 (msdyn_partyelectronicaddresses) | | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.

## <a name="templates"></a>Mallid

Tabeli kaartide kogum toimib koos ning suhtluses osapoole ja globaalse aadressiraamatuga, nagu on näidatud järgmises tabelis.

Finance and Operations rakendus | Klientide kaasamise rakendus     | Kirjeldus
----------------------------|-----------------------------|------------
[Kontaktisiku tiitlid](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Kliendid V3](mapping-reference.md#101) | kontod |
[Kliendid V3](mapping-reference.md#116) | kontaktid |
[CDS osapooled](mapping-reference.md#220) | msdyn_parties |
[CDS-i osapoole postiaadressi asukohad](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS-i postiaadressi ajalugu V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS-i postiaadressi asukohad](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-i müügipakkumise päis](mapping-reference.md#215) | pakkumised |
[CDS-i müügitellimuse päised](mapping-reference.md#217) | müügitellimused |
[Viisakusväljendid](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Kontaktid V2](mapping-reference.md#221) | msdyn_contactforparties |
[Otsustamisrollid](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Tööhõive tööfunktsioonid](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Püsikliendi tasemed](mapping-reference.md#226) | msdyn_loyaltylevels |
[Osapoole kontaktid V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Isiklikud märgitüübid](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Müügiarve päised V2](mapping-reference.md#118) | arved |
[Tervitused](mapping-reference.md#228) | msdyn_salutations |
[Hankijad V2](mapping-reference.md#202) | msdyn_vendors |

Lisateavet vt [topeltkirjutuse vastendamise viitest](mapping-reference.md).
