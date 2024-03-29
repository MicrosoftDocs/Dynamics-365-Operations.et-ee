---
title: Osapool ja globaalne aadressiraamat
description: See artikkel kirjeldab topeltkirjutuse osapoole ja globaalse aadressiraamatu funktsioone.
author: RamaKrishnamoorthy
ms.date: 08/02/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 7f06b6e69b76bf12092fdceca5b45a6750b52233
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228986"
---
# <a name="party-and-global-address-book"></a>Osapool ja globaalne aadressiraamat

[!include [banner](../../includes/banner.md)]



*Osapool* ja *globaalne aadressiraamat* on finantside ja toimingute rakenduste mõisted. Osapooleks võib olla organisatsioon või isik. Osapoole atribuute on mugav globaalselt talletada ja hallata (nt nimi, keel, kontaktid ja aadressid). Kui atribuudi väärtus muutub ühes kohas, peegeldub see kõigis kohtades, kuhu osapool on kaasatud.

## <a name="party"></a>Osapool

Osapool on ettevõttega seotud isik või organisatsioon. Osapoole kontseptsiooni kasutades saab inimene või organisatsioon ettevõttes täita rohkem kui ühte rolli (nagu töötaja, klient, hankija või kontakt). Roll põhineb kontekstil ja eesmärgil. Siin on mõned näited rollidest kahest fiktiivstest ettevõtetest: Contoso ja Fabrikam:

+ **Töötaja** – Töövõtja. Näide on Contoso töötaja.
+ **Hankija** – Tarnijaorganisatsioon või ainuomanik, kes tarnib ettevõttele kaupu või teenuseid. Näiteks kui Fabrikam müüb tarneid Contosole, on Fabrikam Contoso hankija.
+ **Kontakt** – Kontaktisik. Näiteks kui Contoso ostab varusid Fabrikamilt, võtab Contoso töötajad ühendust Fabrikami kontaktiga.
+ **Klient** : Isik või ettevõte, kes ostab ettevõttelt kaupu. Näiteks kui Contoso ostab varusid Fabrikamilt, on Contoso Fabrikami klient.

Osapoole mudelit kasutatakse sageli organisatsioonide ja inimeste vaheliste keerukate suhete meediumi kajastamiseks, eriti siis, kui osapoolel on rohkem kui üks roll. Järgmisena on toodud mõned levinumad näited.

+ Osapool võib olla nii klient kui ka hankija. Näiteks Põhja-Ameerikas müüb Fabrikam Contosole elektrit ja ostab Contosost monteeritud riike. Euroopas müüb Fabrikam osaSid Contosole, kuid see ei osta Contosost midagi.
+ Osapool võib olla nii töövõtja kui ka klient. Näiteks ostab Contoso töövõtja Contosost elektroonikat isiklikuks kasutamiseks.
+ Isiku ja organisatsiooni vahel võib olla mitu-mitmele (N:N) – seosed. Näiteks varustab Fabrikam teenusespetsialiste ja võtab tööle paigutuse koordinaator. Paigutuse koordinaator viib teenusespetsialistid vastavusse mitme Fabrikami kliendi töötaotlustega. Contoso on üks Fabrikami klientidest. Kui Contoso nõuab teenusespetsialisti, võtab see ühendust paigutuse koordinaatoriga, kes seejärel lihtsustab taotlust. Kuna paigutuse koordinaator tegeleb kõikide klientide taotlustega, kaasatakse N:N-seos.

Järgmine pilt näitab osapoole andmemudelit.

![Osapoole andmemudel.](media/party-gab-image1.png)

> [!TIP]
> Kui proovite luua uut kontokirjet, kasutage välja **Osapool** kirje otsimiseks nime järgi. Sel viisil, kui te kirje leiate, peate selle lihtsalt valima. Süsteem täidab automaatselt kõik osapoole andmed. Kõiki nõutavaid välju ei tule käsitsi täita. Selline käitumine võib ilmneda valmislahendusega lehtedel **Konto**, **Kontakt** ja **Hankija** .

Topeltkirjutus ei toeta kõiki finantside ja toimingute rakenduste osapoole rolle. Osapoolte rollide täieliku loendit vt [Globaalse aadressiraamatu ülevaade](../../../fin-ops/organization-administration/overview-global-address-book.md)ülevaatest.

### <a name="global-address-book"></a>Globaalne aadressiraamat

Globaalne aadressiraamat on ettevõttes osalevate organisatsioonide ja üksikisikute posti- ja elektronaadresside kataloog.

Globaalses aadressiraamatus talletatakse ja käsitletakse nii palju postiaadresse ja elektroonilisi aadresse kui vaja. Oletame näiteks, et Fabrikamil on bensiinijaamad 50 asukohas. Igal asukohal on erinev postiaadress, meiliaadress ja telefoninumber. Kõigile äriostude arved lähevad põhibensiinijaama arvele, kuid ostud tarnitakse kindlasse bensiinijaama, mis ostu taotles. Globaalne aadressiraamat talletab Fabrikami põhibensiinijaama arveaadressina ja kõik bensiinijaamad tarneaadressina. Aadresse saab talletada üks kord ja neid saab leida vastavalt pakkumis- ja tellimusvajadusele.

Sõltuvalt ärikontekstist võib inimene või organisatsioon täita rohkem kui ühte rolli ja sama postiaadressi ja elektroonilist aadressi võidakse kasutada kõigi rollide puhul. Sel juhul peab ühe rolli aadressimuutus kajastuma teistes rollides ja vastupidi. Globaalne aadressiraamat talletab ja käsitleb aadresse globaalselt.

Järgmisel joonisel on näidatud globaalse aadressiraamatu andmemudel.

![Globaalse aadressiraamatu andmemudel.](media/party-gab-image2.png)

## <a name="contact"></a>Kontakt

Kliendikogemuse rakenduses on kontakt isik. Tabel **Kontakt** on ülekoormatud, et tähistada isikut, portaali kasutajat, B2C-klienti või hankijat. Esindatus on peidetud ja seda ei ole võimalik ilma seotud kannete uurimiseta tuvastada. Tabelil **Kontakt** on piiratud 1:1 seos tabeliga **Konto** . Osapoole ja globaalse aadressiraamatu mudeli osana tutvustatakse topeltkirjutuse klassifikatsiooni ning topeltkirjutus lubab atribuute, mis võimaldavad N:N-seoseid kontaktisiku ja organisatsiooni vahel (**Konto** või **Hankija** üksus).

Ridu **Kontakt** on kahte tüüpi.

+ **Vöödiline kontakt** – **Kontakti** rida kus **Ettevõtte** väljal on kohustuslik väärtus.
+ **Vöötideta kontakt** – **Kontakti** rida, kus väli **Ettevõte** on tühi.

Tabel **Kontakt** võib talletada järgmist tüüpi ridu.

| Rea tüüp | Kirjeldus |
|----------|-------------|
| Isik, kes on klient, nt müüdav kontakt või B2C-klient | Vöödilise kontakti kirje, milles väli **Ettevõte** ei ole tühi ning välja **Klient** väärtuseks on seatud **Jah**. |
| Isik, kes on hankija, näiteks ainuomanik nagu hankija | Vöödilise kontakti kirje, milles väli **Ettevõte** ei ole tühi ning väljal **Hankija** on seatud väärtuseks **Jah**. |
| Isik, kes on korraga nii klient kui ka hankija | Vöödilise kontakti kirje, milles väli **Ettevõte** ei ole tühi ning väljal **On kKlient** on seatud väärtuseks **Jah** ja välja **On Hankija** on seatud väärtuseks **Jah**. Isik võib olla nii ühe toote tootja kui ka teise toote tarbija. Seda suhet toetavad nii finantside ja toimingute rakendused kui ka topeltkirjutus. |
| Isik, kes on organisatsiooni kontaktisik, kuid ei ole klient ega hankija | Vöödita kontakti kirje, milles väli **Ettevõte** on tühi ning väljal **On Klient** on seatud väärtuseks **Ei**, ja väljal **On Hankija** on seatud väärtuseks **Ei**. |

## <a name="contact-for-party-table"></a>Osapoole tabeli kontakt

Tabel **Osapoole kontakt** talletab ja käsitseb N:N-seoseid välja **Konto** ridade ja välja **Kontakt** ridade vahel. See võib välja filtreerida vöödilise **Kontakti** read vöötideta ridadest ja seostada ainult vöötideta **Kontakti** read **Konto** või **Hankija** ridadega.

Näiteks on Natasha Jones ja Miguel Reyes veterinaarid, kes oma piirkonnas asuvaid farme teenindavad. Natasha teenindab Seattle'i piirkonda ja Miguel Kenti piirkonda. Klienditeeninduse rakenduses on farmid esitatud klientidena ja veterinaarid on kontaktisikud. Üksikut **Kontakti** kirjet Natasha jaoks seostatakse kõigi farmidega, kus Natasha töötab. Samamoodi seostatakse ühe **Kontakti** kirjet Migueli jaoks kõigi farmidega, kus Miguel töötab.

Need seosed salvestatakse tabelisse **Kontakt osapoole jaoks**. Teavet leiate valmislahendusega lehtedel **Konto**, **Kontakt** ja **Hankija** :

+ **Konto** lehel saate kasutada vahekaarti **Seotud Kontaktid** , et seostada üks või mitu kontakti **Konto** reaga. Sel viisil määrate organisatsiooni kontaktisiku. Siis saate valida konto esmaseks kontaktiks ühe kontakti. Kui kasutate lehte **Kiirloomine** , saate valida ainult kontaktisiku. Käitumine on sama, kui kasutate lehte **Hankija** ja kirje tüüp on **Organisatsioon**.
+ **Kontakti** lehel, kui rida on klient, hankija või mõlemad (riba kontakt), saate kasutada vahekaarti **Seotud Kontaktid** et siduda üks või mitu kontakti. Sel viisil määrate kontaktisiku B2C-kliendi või hankija jaoks. Siis saate valida ühe kontakti esmaseks kontaktiks. Kui kasutate lehte **Kiirloomine** , saate valida ainult kontaktisiku.
+ **Kontakti** lehel, kui rida on kontaktisik (vöötideta kontakt), saate kasutada vahekaarti **Seotud Kontaktid** et siduda üks või mitu klienti või hankijat. Sel viisil määrate kliendid või hankijad põhi kontaktisikuteks. Klient või hankija võib olla organisatsioon, isik või mõlemad. Korraga saate valida väärtuse ainult ühel neljast väljast:

    + Kui valite määra väärtus **Osapoole ID** väljale, siis määratakse aluseks olev kontakt kõikidele valitud osapoole rollidele.
    + Kui valite **Seostatud Kontakti** välja, valite sellega vöödiga kontakti, mis on **Isiku** tüüp.
    + Kui valite väärtuse väljal **Seotud konto** või **Seotud Hankija** , valite organisatsiooni.

    ![Associated Organizations vahekaart Kontaktilehel.](media/party-gab-image3.png)

    Sõltumata teie valikust luuakse seos osapoole tasemel ja see on rakendatav kõigile osapoole rollidele ning talletatakse üksuses **Kontakt osapoole jaoks** .

> [!NOTE]
> Kliendikogemuse rakenduses tabeli **Kontakt osapoole jaoks** kuvanimi on **Kontakt kliendi/hankija jaoks**.

Kui avate **Kontakti** rea, kus nii väli **On Klient** kui ka **On Hankija** on seatud väärtusele **Ei**, kuvatakse vahekaart **Seostatud Organisatsioonid**. Kasutage seda vahekaarti, et seostada kontaktiga üks või mitu kliendi- või hankija organisatsiooni.

Kui avate **Kontakti** rea, kus nii väli **On Klient** kui ka **On Hankija** on seatud väärtusele **Jah**, kuvatakse vahekaart **Seostatud Organisatsioonid** . Kasutage seda vahekaarti, et seostada üks või mitu kontakti.

## <a name="postal-addresses"></a>Postiaadress

Uus vahekaart **Aadressid** on sisse viidud lehtedele **Konto**, **Kontakt** ja **Hankija**. See vahekaart toetab mitut postiaadressi ruudustiku abil, nagu näha järgmises illustratsioonis.

![Ruudustik postiaadresside jaoks.](media/party-gab-image4.png)

Ruudustik sisaldab järgmisi veerge.

+ **Postiaadressi rollid** -- Postiaadresside eesmärk.
+ **On esmane** – Väärtus, mis näitab, kas aadress on esmane aadress.
+ **Aadressi number** – Aadressi järjekord.

Ruudustiku kohal saate kasutada nuppu **Uus Aadress**, et luua nii palju sihtaadresse, kui soovite.

Kliendi kaasamise **rakendustes** **·**, kui kasutaja sisestab aadressid vahekaardi Kontod vahekaardil Kokkuvõte, **vastavad väljad Aadress 1** **ja Aadress 2** **·** **vastavalt** tarne- ja arveaadressidele. Kui kasutaja loob postiaadressi finantside ja toimingute rakendustes, **ilmuvad kliendikirje kaks esimest aadressi väljadel Address1** **ja Address2** **ning** kasutaja saab aadressi eesmärgi muuta valikuks Tarne ja **Arve.**

![Postiaadresside kokkuvõtte vahekaart.](media/party-gab-image5.png)

Samamoodi vastavad vahekaardi Kontakt väljad Aadress **1**, **Aadress** 2 **ja Aadress 3** **·** **·** **vastavalt** ettevõtte- **·** **ja** tarneaadressidele ning arveaadressidele.

## <a name="electronic-addresses"></a>Elektroonilised aadressid

Uus vahekaart **Elektroonilised Aadressid** on sisse viidud lehtedele **Konto**, **Kontakt** ja **Hankija**. See vahekaart toetab mitut elektroonilist aadressi ruudustiku abil, nagu näha järgmises illustratsioonis.

![Ruudustik elektronaadressi jaoks.](media/party-gab-image6.png)

Ruudustik sisaldab järgmisi veerge.

+ **Tüüp** – elektroonilise aadressi tüüp.
+ **On Esmane** – Väärtus, mis näitab, kas aadress on esmane aadress.
+ **Eesmärk** – Elektronaadresside eesmärgid.

Ruudustiku kohal saate kasutada nuppu **Uus Elektrooniline Aadress**, et luua nii palju sihtaadresse, kui soovite.

Müügivihje kvalifikatsiooniprotsessi käigus saate sisestada nii ettevõtte telefoninumbri kui ka mobiiltelefoni numbri. Ettevõtte telefoninumber on esmane **telefoninumber, kui IsMobile=Ei** ja mobiiltelefoni numbrit peetakse teisene telefoninumber, **kui IsMobile=Yes**.

> [!TIP]
> Kasutage vahekaarte **Aadressid** ja **Elektroonilised aadressid** vormidel **Konto** ja **Kontakt** posti- ja elektrooniliste aadresside haldamiseks. See tagab, et aadressiandmed sünkroonitakse finantside ja toimingute rakendustega.

## <a name="setup"></a>Seadistus

1. Avage oma Customer Engagement rakenduse keskkond.

2. Installige kõik eeltingimuse lahendused, nagu on kirjeldatud topeltkirjutusega [rakenduse orkestratsioonipaketis](separated-solutions.md).

3. Installige [Topeltkirjutuse osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab).

4. Avage Finance and Operations rakendus. Liikuge andmehalduse moodulisse ja valige Topeltkirjutus vahekaart. Avaneb topeltkirjutuse haldusleht.

5. Rakendage mõlemad sammudes 2 ja 3 installitud lahendused kasutades [Teosta lahendus](link-your-environment.md) funktsiooni.

6. Peatage järgmised kaardid, kuna need pole enam nõutavad. Selle asemel käivitage `Contacts V2 (msdyn_contactforparties)` kaart.

    + CDS Contacts V2 ja Contacts (viitab kliendi kontaktidele)
    + CDS Contacts V2 ja Contacts (viitab hankija kontaktidele)

7. Järgmised üksuste vastendused värskendatakse osapoole funktsioonide jaoks, nii et nendele vastendustele tuleb rakendada uusimat versiooni.

    Vastenda | Värskendage selle versioonini | Muutused
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.2 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.6 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Customers V3 (accounts)` | 1.0.0.5 |Eemaldatud `PartyNumber` ja teised osapoolega seotud väljad nagu nimi, isiklikud üksikasjad, postiaadressi väljad ja elektroonilise kontaktiaadressi väljad.
    `Customer V3 (contacts)` | 1.0.0.5 | Eemaldatud `PartyNumber` ja teised osapoolega seotud väljad nagu nimi, isiklikud üksikasjad, postiaadressi väljad ja elektroonilise kontaktiaadressi väljad.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Eemaldatud `PartyNumber` ja teised osapoolega seotud väljad nagu nimi, isiklikud üksikasjad, postiaadressi väljad ja elektroonilise kontaktiaadressi väljad.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Asendas kontaktisiku `ContactforParty` viitega.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Asendas kontaktisiku `ContactforParty` viitega.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Asendas kontaktisiku `ContactforParty` viitega.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.2 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Complimentary Closings (msdyn_compliemntaryclosings)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.
    `CDS Address roles (msdyn_addressroles)` | 1.0.0.0 | See on uus kaart, mis on osaliselt lisatud sellele väljalaskele.

8. Enne ülalolevate kaartide käitamist, peate käsitsi värskendama integratsioonivõtmeid, nagu on kirjeldatud järgnevates sammudes. Seejärel valige nupp **Salvesta**.

    | Vastenda | Võtmed |
    |-----|------|
    | Konto |  kontonumber [Konto Number]<br>msdyn_company.cdm_companycode [Ettevõte (Ettevõtte Kood)] |
    | Kontakt | msdyn_contactpersonid [Konto Number / Kontaktisiku ID]<br>msdyn_company.cdm_companycode [Ettevõte (Ettevõtte Kood)] |
    | Kliendi/Hankija kontakt | msdyn_contactforpartynumber [Osapoole Numbri Kontakt]<br>msdyn_company.cdm_companycode [Seotud Ettevõte (Ettevõtte Kood)] |
    | Tarnija | msdyn_vendoraccountnumber [Hankija Kontonumber]<br>msdyn_company.cdm_companycode [Ettevõte (Ettevõtte Kood)]|

9. Dataverse’is duplikaadituvastusreeglite märgipiirid on suurendatud 450 märgilt 700-le. See piirang võimaldab teil lisada duplikaattuvastusreeglitele ühe või mitu võtit. Laiendage tabeli **Kontod** duplikaadituvastusreeglit, määrates järgmised väljad.

    | Field | Väärtus |
    |-------|-------|
    | Nimi | Sama kontonimega kontod. |
    | Kirjeldus | Tuvastab kontokirjed, mille konto nime atribuudis on sama väärtus. |
    | Põhikirje tüüp | Konto |
    | Vastav kirjetüüp | Konto |
    | Konto Nimi (väli) | Täpne Vaste |
    | Ettevõte (väli) | Täpne Vaste |
    | Seosetüüp (väli) | Täpne Vaste |
    | Osapoole id (väli) | Täpne Vaste |
    | Valige (väli) | (tühi) |

    ![Kontode duplikaatreegel.](media/duplicate-rule-1.PNG)

10. Laiendage tabeli **Kontod** duplikaadituvastusreeglit, määrates järgmised väljad.

    | Field | Väärtus |
    |-------|-------|
    | Nimi | Sama eesnime ja perekonnanimega kontaktid. |
    | Kirjeldus | Tuvastab kontaktikirjed, mis on samade väärtustega väljadel Eesnimi ja Perekonnanimi. |
    | Põhikirje Tüüp | Kontakt |
    | Vastav Kirjetüüp | Kontakt |
    | Eesnimi (väli) | Täpne Vaste |
    | Perekonnanimi (väli) | Täpne Vaste |
    | Ettevõte (väli) | Täpne Vaste |
    | Osapoole Id (väli) | Täpne Vaste |
    | Valige (väli) | (tühi) |

    ![Kontaktide duplikaatreegel.](media/duplicate-rule-2.PNG)

11. Kui olete olemasolev topeltkirjutusega kasutaja, järgige juhiseid [Täiendage osapoole ja globaalse aadressiraamatu mudelit](upgrade-party-gab.md) ning täiendage oma andmeid. **Ärge jätkake etapiga 12 ilma seda sammu lõpule viimata.** Kui te olete uus topeltkirjutusega kasutaja, jätkake sammuga 12.

12. Kui te olete olemasolev topeltkirjutusega kasutaja, läbige etapp 11 ja seejärel käivitage kaardid järgmises järjekorras. Kui te olete uus topeltkirjutusega klient, saate otse edasi minna. Kui kuvatakse tõrketeade, mis näitab, et projekti kinnitamine nurjus. Puudub sihtväli...", avage kaart ja valige **suvand Värskenda tabeleid** ning käivitage seejärel kaart.

    Finantside ja toimingute rakendus | Klientide kaasamise rakendus  
    ----------------------------|------------------------
    [CDS osapooled](mapping-reference.md#220) | msdyn_parties
    [CDS-i postiaadressi asukohad](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS-i postiaadressi ajalugu V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS-i osapoole postiaadressi asukohad](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Osapoole kontaktid V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Kliendid V3](mapping-reference.md#101) | kontod
    [Kliendid V3](mapping-reference.md#116) | kontaktid
    [Hankijad V2](mapping-reference.md#202) | msdyn_vendors
    [Kontaktisiku tiitlid](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Viisakusväljendid](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Tervitused](mapping-reference.md#228) | msdyn_salutations
    [Otsustamisrollid](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Tööhõive tööfunktsioonid](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Püsikliendi tasemed](mapping-reference.md#226) | msdyn_loyaltylevels
    [Isiklikud märgitüübid](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Kontaktid V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-i müügipakkumise päis](mapping-reference.md#215) | pakkumised
    [CDS-i müügitellimuse päised](mapping-reference.md#217) | müügitellimused
    [Müügiarve päised V2](mapping-reference.md#118) | arved
    [CDS-aadressi rollid](mapping-reference.md#301) | msdyn_addressroles

> [!NOTE]
> Kaart `CDS Contacts V2 (contacts)` on kaart, mille peatusite sammus 1. Kui proovite käitada teisi kaarte, võivad need 2 vastekaarti ilmuda ülalpeetavate loendis. Ära käita neid kaarte.
>
> Kui osapool ja globaalse aadressiraamatu lahendus on installitud, peate kataloogi keelama.`Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead` Kui desinstallid osapoole ja globaalse aadressiraamatu lahenduse siis peate ühenduse keelama.
>
> `msdyn_*partynumber` välja (ühe rea tekstivälja), mis on kaasatud tabelitesse **Konto**, **Kontakt** ja **Hankija** ei tohiks kasutada edasiminekuks. Sildinimel on eesliide **Iganenud** selguse jaoks. Selle asemel kasutage **msdyn_partyid** välja. See väli on tabeli **msdyn_party** otsing.
>
> Tabeli nimi | Vana väli | Uus väli
> --------|-------|--------
> Konto | `msdyn_partynumber` | `msdyn_partyid`
> Kontakt | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Mallid

Tabeli kaartide kogum toimib koos ning suhtluses osapoole ja globaalse aadressiraamatuga, nagu on näidatud järgmises tabelis.

| Finantside ja toimingute rakendus | Klientide kaasamise rakendus | Kirjeldus |
|----------------------------|-------------------------|-------------|
| [Kontaktisiku tiitlid](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Kliendid V3](mapping-reference.md#101) | kontod |
| [Kliendid V3](mapping-reference.md#116) | kontaktid |
| [CDS osapooled](mapping-reference.md#220) | msdyn\_parties |
| [CDS-i osapoole postiaadressi asukohad](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS-i postiaadressi ajalugu V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS-i postiaadressi asukohad](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-i müügipakkumise päis](mapping-reference.md#215) | pakkumised |
| [CDS-i müügitellimuse päised](mapping-reference.md#217) | müügitellimused |
| [Viisakusväljendid](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Kontaktid V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Otsustamisrollid](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Tööhõive tööfunktsioonid](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Püsikliendi tasemed](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Osapoole kontaktid V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Isiklikud märgitüübid](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Müügiarve päised V2](mapping-reference.md#118) | arved |
| [Tervitused](mapping-reference.md#228) | msdyn\_salutations |
| [Hankijad V2](mapping-reference.md#202) | Msdyn\_hankijad |
| [CDS-aadressi rollid](mapping-reference.md#301) |msdraamat\_ addressroles|

Lisateavet vt [topeltkirjutuse vastendamise viitest](mapping-reference.md).

## <a name="address-roles-as-a-multi-select-drop-down-list"></a>Aadressirollid mitmetasandilise ripploendina
Postiaadress või elektrooniline aadress võivad teenida rohkem kui üht eesmärki. Näiteks võib postiaadress olla nii arveaadressi kui ka tarneaadressina. Sellisel juhul saab kasutaja ripploendist **valida** nii **Arve** kui ka Tarne, nagu järgmisel joonisel näha. 

![Eesmärgi/rolli ripploend.](media/purpose.png)

## <a name="known-issues-and-limitations"></a>Teadaolevad probleemid ja piirangud

+ Kui loote finantside ja toimingute rakendustes kliendi aadressiga ja salvestate selle, ei pruugi aadress aadressitabeliga **sünkroonida**. Põhjus on platvormi topeltkirjutuse järjestuse probleemis. Lahendusena looge kõigepealt klient ja salvestage see. Seejärel lisage aadress.
+ Finantside ja toimingute rakendustes, kui kliendikirjel on esmane aadress ja te loote sellele kliendile uue kontakti, pärib kontaktkirje esmase aadressi seotud kliendikirjest. See juhtub ka hankija kontakti korral. Dataverse ei toeta praegu seda käitumist. Kui topeltkirjutus on lubatud, sünkroonitakse finantside ja toimingute rakendusest esmase aadressiga päritud kliendikontaktid Dataverse koos aadressiga.
+ Finantside ja toimingute rakendustes saate luua kontaktikirje vormilt **Lisa kontakt**. Kui proovite luua uut kontakti vormilt **Kuva Kontakt** tegevus nurjub. See on teadaolev probleem.

    ![Teadaolev probleem Kontakti Lisamisega.](media/party-gab-contact-issue.png)

+ **Esialgne sünkroonimine** ei toeta **Saadaval Alates** ja **Saadaval Kuni** väljasid **OsapooleKontakt** , kuna DIXF teisendab väärtuse täisarvu asemel stringiks. Teisendus käivitab tõrke `Cannot convert the literal '<say 08:00:00>' to the expected type edm.int32`.
+ Te ei saa sisestada edasisuunas postiaadressi, kasutades finantside ja operatsioonide rakendust topeltkirjutusega, Dataverse sest ei toeta kuupäeva mõju. Kui sisestate finantside ja toimingute rakenduse abil tulevikku ajastatud postiaadressi, Dataverse sünkroonitakse see täielikult ja aadressi näete kohe kasutajaliideses. Selle kirje mis tahes uuendused tulemuseks on viga, kuna see on tulevikku ajastatud ja mitte ajastatud finantside ja toimingute rakenduses.
