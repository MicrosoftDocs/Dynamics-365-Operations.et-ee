---
title: Teenuses Regulatory Configuration Services (RCS) elektroonilise arvelduse lisandmooduli konfigureerimine
description: See teema kirjeldab, kuidas konfigureerida elektroonilise arvelduse lisandmoodulit Dynamics 365 teenuses Regulatory Configuration Services (RCS).
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: bb4a426bb54ee21197f9954d946d60ea55f5eb76
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104371"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a>Teenuses Regulatory Configuration Services (RCS) elektroonilise arvelduse lisandmooduli konfigureerimine

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

Sellest teemast leiate teavet elektroonilise arvelduse lisandmooduli konfiguratsioonivõimaluste kohta Dynamics 365 teenuses Regulatory Configuration Services (RCS).

Elektroonilise arvelduse lisandmoodul aitab teil konfiguratsioonivõimaluste kaudu täita elektrooniliste arvete ärialaseid ja regulatiivseid nõudeid, ilma et peaksite midagi kodeerima. Olukordades, kus veebiteenused peavad elektroonilised arved elektrooniliselt kinnitama, aitavad konfiguratsioonivõimalused teil täita veebiteenustega sõnumite vahetamise nõudeid ilma midagi kodeerimata.

## <a name="electronic-reporting"></a>Elektrooniline aruandlus

Elektrooniline aruandlus (ER) toetab elektroonilise arvelduse lisandmoodulit.

Andmemudeli vastendamine ja vormingud on konfigureeritavad komponendid, mis luuakse ja mida hallatakse elektroonilise aruandluse kaudu ning mida kasutatakse elektroonilise arvelduse lisandmoodulis. ER-i vormingu kujundaja on tööriist failivormingute loomiseks ja haldamiseks. Seda kasutatakse elektroonilise arvelduse funktsioonide konfigureerimiseks.

Lisateavet vt teemast [Elektroonilise aruandluse (ER) ülevaade](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonid

Elektroonilise arvelduse funktsioonid vastutavad elektrooniliste arvete loomise eest elektroonilise arvelduse lisandmooduli kaudu. Need hõlmavad konfiguratsioonireegleid ja kasutavad neid andmete töötlemiseks, mida Microsofti teenused Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmoodulile ning elektroonilistele arvetele saadavad.

Funktsioonid toetavad ka olukordi, kus on nõutav vastavus failivormingu spetsifikatsioonidele ning kus väljund on eraldiseisev elektrooniline fail. Enamasti avaldab failivormingu spetsifikatsioonid maksuamet.

Lõpuks toetavad need funktsioonid sõnumite vahetust väliste veebiteenustega, mida majutab maksuamet või mõni volitatud osapool, ning autoriseerimistaotlusi või kinnitustemplit elektroonilisel arvel.

### <a name="availability-of-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide saadavus

Elektroonilise arvelduse funktsioonide saadavus oleneb riigist või regioonist. Kuigi mõned funktsioonid on üldiselt saadaval, on teised saadaval eelvaateversioonis.

#### <a name="preview-features"></a>Eelvaatefunktsioonid

Järgmises tabelis on toodud elektroonilise arvelduse funktsioonid, mis on praegu saadaval eelvaateversioonis.

| Riik/regioon | Funktsiooni nimi                         | Äridokument |
|----------------|--------------------------------------|-------------------|
| Austria        | Austria elektroonilised arved (AT)    | Müügi- ja projektiarved |
| Belgia        | Belgia elektrooniline arve (BE)      | Müügi- ja projektiarved |
| Brasiilia         | Brasiilia NF-e (BR)                  | Finantsdokumendi mudel 55, paranduskirjad, tühistamised ja tagasilükkamised |
| Brasiilia         | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuste finantsdokumendid |
| Brasiilia         | Brasiilia NFS-e São Paulo (BR)       | Teenuste finantsdokumendid |
| Taani        | Taani elektrooniline arve (DK)       | Müügi- ja projektiarved |
| Egiptus          | Egiptuse elektrooniline arve (EG) | Müügi- ja projektiarved |
| Eesti        | Eesti elektrooniline arve (EE)     | Müügi- ja projektiarved |
| Soome        | Soome elektrooniline arve (FI)      | Müügi- ja projektiarved |
| Prantsusmaa         | Prantsusmaa elektrooniline arve (FR)       | Müügi- ja projektiarved |
| Saksamaa        | Saksamaa elektrooniline arve (DE)       | Müügi- ja projektiarved |
| Itaalia          | FatturaPA (IT)                       | Müügi- ja projektiarved |
| Mehhiko         | Mehhiko CFDI (MX)                    | Müügiarved, saatelehed, varude üleviimised, maksetoetused ja tühistamised |
| Holland    | Hollandi elektrooniline arve (NL)        | Müügi- ja projektiarved |
| Norra         | Norra elektrooniline arve (NO)    | Müügi- ja projektiarved |
| Hispaania          | Hispaania elektrooniline arve (ES)      | Müügi- ja projektiarved |
| Euroopa         | PEPPOL-i elektrooniline arve            | PEPPOL-i müügi- ja projektiarved |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide konfigureeritavad komponendid

Elektroonilise arvelduse funktsioonid hõlmavad järgmisi konfigureeritavate komponentide gruppe.

- **Vormingud** – vormingud võimaldavad teil konfigureerida, mida elektroonilise arvelduse lisandmoodul peab genereerima, kui elektroonilisest dokumendist saab elektrooniline arve. Vormingud hõlmavad elektroonilise arve ning nende failide ja sõnumite vormingu konfiguratsiooni, mida kasutatakse taotluste esitamiseks ning vastuste saamiseks, kui nõutav on suhtlus välise veebiteenusega.
- **Tegevused** – tegevused võimaldavad teil konfigureerida, kuidas elektroonilise arvelduse lisandmoodul genereerib teenuste Finance ja Supply Chain Management esitatud elektroonilise dokumendi teisendamise elektrooniliseks arveks.
- **Kohaldatavusreeglid** – kohaldatavusreeglid võimaldavad teil konfigureerida konteksti, mida elektroonilise arvelduse lisandmoodul peab elektroonilise arvelduse funktsiooni töötlemiseks arvestama.
- **Muutujad** – muutujad võimaldavad teil konfigureerida konfiguratsiooniloogika koostamise tuge. Muutujaid saab kasutada väärtuste sisendina konkreetse tegevuse sooritamiseks. Teise võimalusena saab neid kasutada väärtuste vahetajana teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahel.
- **Elektroonilise dokumendi mudelivastendus** – elektroonilise dokumendi mudelivastendus võimaldab teil konfigureerida ER-i mudelivastendust. Mudelivastendus määratleb elektrooniliste dokumentide esitamise ajal elektroonilise arvelduse lisandmoodulisse integreeritava abstraktse arve andmevastenduse.
- **Arve kontekstimudel** – arve kontekstimudel võimaldab teil konfigureerida ER-i arve kontekstimudelit ja määratleda elektroonilise arvelduse funktsiooni konteksti.
- **Vastuse tüübid** – vastuse tüübid võimaldavad teil konfigureerida, mida elektroonilise arvelduse lisandmoodul peab teenustes Finance ja Supply Chain Management elektroonilise arve töötlemise tulemusena värskendama.

### <a name="formats"></a>Vormingud

Järgmistes loendites on toodud ER-i funktsioonide jaoks saadaolevad ER-i vormingu konfiguratsioonid.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Austria (AT) elektroonilised arved: Austria müügi- ja projektiarved

- OIOUBL-i müügiarve
- OIOUBL-i projektiarve
- OIOUBL-i müügi kreeditarve
- OIOUBL-i projekti kreeditarve

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgia (BE) elektroonilised arved: Belgia müügi- ja projektiarved

- UBL-i müügiarve BE
- UBL-i projektiarve BE
- UBL-i projekti kreeditarve BE
- UBL-i müügi kreeditarve BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brasiilia (BR) NF-e: NF-e Federal (Brasiilia)

- NF-e esitamise ekspordivorming (BR)
- NF-e paranduskirja ekspordivorming (BR)
- NF-e tühistamise ekspordivorming (BR)
- NF-e tagasilükkamise ekspordivorming (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brasiilia NFS-e (BR): NFS-e ABRASF Curitiba linn

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Inquire Curitiba (BR)

#### <a name="brazilian-br-nfs-e-nfs-e-so-paulo-city"></a>Brasiilia (BR) NFS-e: NFS-e São Paulo linn

- NFS-e Sao Paulo (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Taani (DK) elektroonilised arved: Taani müügi- ja projektiarved

- OIOUBL-i müügiarve
- OIOUBL-i projektiarve
- OIOUBL-i müügi kreeditarve
- OIOUBL-i projekti kreeditarve

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Hollandi (NL) elektroonilised arved: Hollandi müügi- ja projektiarved

- UBL-i müügiarve NL
- UBL-i projektiarve NL
- UBL-i projekti kreeditarve NL
- UBL-i müügi kreeditarve NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egiptuse (EG) elektroonilised arved: Egiptuse müügi- ja projektiarved

- Müügiarve (EG) (arveldus)
- Projektiarve (EG) (arveldus)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Eesti (EE) elektroonilised arved: Eesti müügi- ja projektiarved

- Müügiarve (EE)
- Projektiarve (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Soome (FI) elektroonilised arved: Soome müügi- ja projektiarved

- Müügiarve (FI)
- Projektiarve (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Prantsusmaa (FR) elektroonilised arved: Prantsusmaa müügi- ja projektiarved

- UBL-i müügiarve FR
- UBL-i projektiarve FR
- UBL-i projekti kreeditarve FR
- UBL-i müügi kreeditarve FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Saksamaa (DE) elektroonilised arved: Saksamaa müügi- ja projektiarved

- Müügiarve (DE)
- Projektiarve (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Itaalia (IT) elektroonilised arved: Itaalia müügi- ja projektiarved

- Müügiarve (IT)
- Projektiarve (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Mehhiko (MX) CFDI: CFDI Mehhiko jaoks

- CFDI arve vorming (MX)
- CFDI saateleht (MX)
- CFDI varude üleviimine (MX)
- CFDI makse vorming (MX)
- CFDI arve tühistamise vorming (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norra (NO) elektroonilised arved: Norra müügi- ja projektiarved

- OIOUBL-i müügiarve
- OIOUBL-i projektiarve
- OIOUBL-i müügi kreeditarve
- OIOUBL-i projekti kreeditarve

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL-i elektroonilised arved: PEPPOL-i müügi- ja projektiarved

- PEPPOL-i müügiarve
- PEPPOL-i projektiarve
- PEPPOL-i müügi kreeditarve
- PEPPOL-i projekti kreeditarve

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Hispaania (ES) elektroonilised arved: Hispaania müügi- ja projektiarved

- Müügiarve (ES)
- Projektiarve (ES)

### <a name="actions"></a>Actions

Järgmises tabelis on toodud saadaolevad tegevused ja see, kas need on praegu üldiselt saadaval või on ikka eelvaateversioonis.

| Tegevus                                        | Kirjeldus                                                                  | Kättesaadavus         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Teisenda dokument                            | Käivitage dokumendi teisendamiseks elektroonilise aruandluse vorming.                   | Üldiselt saadaval  |
| XML-dokumendi allkirjastamine                             | Digiallkirjastage XML-dokumente.                                   | Eelvaates           |
| Egiptuse maksuameti JSON-dokumendi allkirjastamine | Digiallkirjastage Egiptuse maksuameti jaoks JSON-dokumente.       | Üldiselt saadaval  |
| Egiptuse ETA teenusega integreerimine           | Suhelge Egiptuse maksuametiga.                                     | Üldiselt saadaval  |
| Brasiilia SEFAZ teenuse kutsumine                  | Integreerige finantsdokumendi edastamiseks Brasiilia SEFAZ teenusega.       | Eelvaates           |
| Mehhiko PAC teenuse kutsumine                      | Integreerige CFDI edastamiseks Mehhiko PAC teenusega.                      | Eelvaates           |
| Töötle vastust                              | Analüüsige veebiteenuse kutsumise kaudu saadud vastust.                     | Üldiselt saadaval  |
| MS-i teenuse Power Automate kasutamine                         | Integreerige Microsofti teenusesse Power Automate sisseehitatud vooga.                       | Eelvaates           |

## <a name="configuration-providers"></a>Konfiguratsiooni pakkujad

Konfiguratsioonipakkujad pakuvad elektroonilise arvelduse funktsioone ja nende ER-i komponente, nagu mudelivastendus, vormingu konfiguratsioon ja kontekstimudel. Nad avaldavad elektroonilise arvelduse funktsioonid ja ER-i komponendid seotud globaalses hoidlas. Sealt saavad teised organisatsioonid need alla laadida.

Enne RCS-i kaudu elektroonilise arvelduse funktsioonide konfigureerimist peate moodulis **Elektrooniline aruandlus** oma organisatsiooni konfiguratsiooniteenuse pakkujaks konfigureerima. Lisateavet konfiguratsioonipakkuja **aktiivseks** märkimise kohta leiate teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Globaalses hoidlas elektroonilise arvelduse funktsioonide vaatamine

Elektroonilise arvelduse funktsioonide sirvimiseks, mis on saadaval globaalses hoidlas konkreetse konfiguratsioonipakkuja jaoks, sünkroonige oma organisatsiooni RCS-i eksemplar. Kui sünkroonimine on lõpule jõudnud, värskendatakse saadaolevate elektroonilise arvelduse funktsioonide loendit.

## <a name="importing-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide importimine

Enne elektroonilise arvelduse funktsioonide kasutamist või konfigureerimist peate need oma organisatsiooni RCS-i eksemplari importima. Imporditoiming loob funktsioonidest lokaalse koopia ja kopeerib kõik funktsioonide kasutatavad ER-i parasiidid (nt vormingu konfiguratsioonid ja mudeli konfiguratsioonid) teie organisatsiooni RCS-i eksemplari.

Elektroonilise arvelduse funktsioone saate importida mis tahes konfiguratsioonipakkujalt.

## <a name="creating-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide loomine

Saate luua elektroonilise arvelduse funktsiooni nullist või tuletada selle mõnest teisest elektroonilise arvelduse funktsioonist.

Kui loote elektroonilise arvelduse funktsiooni nullist, peate ER-i komponendid (nt funktsiooni versiooni konfiguratsioonid ja muud konfiguratsioonid, nagu funktsiooni versiooni seadistus ja rakenduse seadistus) käsitsi lisama. Kui loote funktsiooni mõnest teisest funktsioonist tuletades, pärib uus funktsioon kõik algse funktsiooni konfiguratsioonid. 

## <a name="electronic-invoicing-feature-version"></a>Elektroonilise arvelduse funktsiooni versioon

Elektroonilise arvelduse funktsioonidel on versioonid. Uue versiooni loomisel lisatakse automaatselt suurem versiooninumber. Uuele versioonile saab määrata „kehtib alates“ kuupäeva.

Elektroonilise arvelduse funktsioonide versioonid järgivad elutsüklit, mis hõlmab kuni kolme olekut.

- **Mustand** – kui funktsiooni versioon on selles olekus, saate redigeerida selle konfiguratsiooni atribuute ja kõiki selle parasiite (nt failivormingu konfiguratsioone).
- **Valmis** – kui funktsiooni versioon on selles olekus, on see avaldatud teie organisatsiooniga seotud globaalses hoidlas. Funktsiooni versiooni ega ER-i komponente ei saa enam redigeerida.
- **Avaldatud** – kui funktsiooniversioon on selles olekus, on see avaldatud elektroonilise arvelduse lisandmoodulile. Funktsiooni versiooni ega ER-i komponente ei saa enam redigeerida.

### <a name="feature-configurations"></a>Funktsioonide konfiguratsioonid

Funktsioonide konfiguratsioonid hõlmavad kõiki elektroonilise arvelduse funktsioonide kasutatavaid ER-i vormingu konfiguratsioone. Kõik elektroonilised failid, mida elektroonilise arvelduse funktsioon töötlemise ajal kasutab, pärinevad selle funktsiooni konfiguratsioonidele lisatud vormingu konfiguratsioonidest.

Funktsiooni konfiguratsioonides pääsete juurde ER-i vormingu kujundajale, mis on vormingu konfiguratsioonide loomiseks kasutatav ER-i tööriist.

### <a name="feature-setup"></a>Funktsiooniseadistus

Funktsioonide seadistusi kasutatakse koos funktsioonide konfiguratsioonidega. Iga funktsiooni seadistus hõlmab tegevuste, kohaldatavusreeglite ja muutujate kogumeid, mis tagavad eeldatava käitumise, et elektroonilise arvelduse funktsioon saaks vastata elektroonilise arve konkreetsele nõudele.

### <a name="application-setup"></a>Rakenduse häälestus

Rakenduse seadistus peab olema seotud eelnevalt loodud ühendatud rakendusega.

Rakenduse seadistuse kaudu saate konfigureerida elektroonilise arvelduse funktsiooni osa, mida tuleb teha teenustes Finance ja Supply Chain Management. Olenemata elektroonilise arvelduse funktsioonist tuleb kasutada vähemalt kolme konfigureeritavat komponenti.

- **Tabeli nimi** – teenuste Finance ja Supply Chain Management üksus, mis hõlmab sisestatud arveid ja põhineb elektroonilise arvelduse funktsioonil.
- **Kontekst** – ER-i kaudu konfigureeritud arve kontekstimudeli nimi.
- **Äridokumentide vastendamine** – ER-i kaudu konfigureeritud arve vastendusmudeli nimi.

> [!IMPORTANT]
> Rakenduse seadistuses sisestatud konfiguratsiooni saab vaadata teenustes Finance ja Supply Chain Management. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**. Tehke vahekaardil **Elektrooniline dokument** valik **Juuruta** ja seejärel valige suvand **Ühendatud rakendus**.

### <a name="deploying-feature-versions"></a>Funktsioonide versioonide juurutamine

RCS-is kasutate elektroonilise arvelduse funktsiooni versiooni sihipäraseks avaldamiseks käsku **Juuruta**. Valige **Juuruta** ja seejärel valige juurutamise sihtmärgi määramiseks üks järgmistest suvanditest. 

- **Teenusekeskkond** – kui juurutamise sihtmärk on teenusekeskkond, avaldatakse elektroonilise arvelduse funktsiooni versioon teenusekeskkonnas. Elektroonilise arveldus lisandmoodul on seejärel valmis teenuste Finance ja Supply Chain Management saadetavaid elektroonilisi dokumente vastu võtma ja töötlema.
- **Ühendatud rakendus** – kui juurutuse sihtmärk on ühendatud rakendus, kirjutatakse rakenduse seadistusega määratud konfiguratsioon sellega varem seostatud teenuste Finance ja Supply Chain Management eksemplari.

Teenusekeskkonnas või ühendatud rakenduses saab juurutada ainult neid elektroonilise arvelduse funktsioonide versioone, mille olek on **Valmis**.

### <a name="removing-feature-versions"></a>Funktsioonide versioonide eemaldamine

RCS-is kasutate elektroonilise arvelduse lisandmooduli teenusekeskkonnast konkreetse elektroonilise arvelduse funktsiooni versiooni eemaldamiseks käsku **Tühista juurutus**.

> [!IMPORTANT]
> Käsk **Tühista juurutus** töötab ainult teenusekeskkondades. See ei eemalda elektroonilise arvelduse funktsioonide versioone ühendatud rakendustest.

### <a name="rebasing-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide aluse muutmine

Kui ühest elektroonilise arvelduse funktsioonist tuletatakse teine, värskendab käsk **Muuda alust** tuletatud funktsiooni algses funktsioonis tehtud muudatustega.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]