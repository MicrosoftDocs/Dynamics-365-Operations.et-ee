---
title: Elektroonilise arvelduse konfigureerimine Regulatory Configuration Services -is (RCS)
description: See teema kirjeldab, kuidas konfigureerida elektroonilist arveldust Dynamics 365 teenuses Regulatory Configuration Services (RCS)-is.
author: gionoder
ms.date: 11/08/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 640244612a2a553ec09661635787cb7f8694283b
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779666"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Elektroonilise arvelduse konfigureerimine Regulatory Configuration Services -is (RCS)

[!include [banner](../includes/banner.md)]

Sellest teemast leiate teavet elektroonilise arvelduse konfiguratsioonivõimaluste kohta Dynamics 365 teenuses Regulatory Configuration Services (RCS).

Elektroonilise arvelduse lisandmoodul aitab teil konfiguratsioonivõimaluste kaudu täita elektrooniliste arvete ärialaseid ja regulatiivseid nõudeid, ilma et peaksite midagi kodeerima. Stsenaariumides, kus elektroonilised arved peab veebiteenus elektrooniliselt kinnitanud, aitavad konfiguratsioonivõimalused täita ka veebiteenusega sõnumite vahetamise nõudeid ilma koodita.

## <a name="electronic-reporting"></a>Elektrooniline aruandlus

Elektrooniline aruandlus (ER) toetab elektroonilist arveldust.

Andmemudeli kaardistamine ja vormingud on konfigureeritavad komponendid, mis luuakse ja mida hallatakse läbi ER-i ja kasutades Elektroonilist aruandlust. ER-i vormingu kujundaja on tööriist failivormingute loomiseks ja haldamiseks. Seda kasutatakse elektroonilise arvelduse funktsioonide konfigureerimiseks.

Lisateavet vt teemast [Elektroonilise aruandluse (ER) ülevaade](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonid

Elektroonilise arvelduse funktsioonid vastutavad elektrooniliste arvete loomise eest elektroonilise arvelduse lisandmooduli kaudu. Need hõlmavad konfiguratsioonireegleid ja kasutavad neid andmete töötlemiseks, mida Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmoodulile ning elektroonilistele arvetele saadavad.

Funktsioonid toetavad ka olukordi, kus on nõutav vastavus failivormingu spetsifikatsioonidele ning kus väljund on eraldiseisev elektrooniline fail. Enamasti avaldab failivormingu spetsifikatsioonid maksuamet.

Lõpuks toetavad need funktsioonid sõnumite vahetust väliste veebiteenustega, mida majutab maksuamet või mõni volitatud osapool, ning autoriseerimistaotlusi või kinnitustemplit elektroonilisel arvel.

## <a name="availability-of-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide saadavus

Elektroonilise arvelduse funktsioonide saadavus oleneb riigist või regioonist. Kuigi mõned funktsioonid on üldiselt saadaval, on teised saadaval eelvaateversioonis.

### <a name="generally-available-features"></a>Saadaolevad üldfunktsioonid

Järgmises tabelis on toodud elektroonilise arvelduse funktsioonid, mis on üldiselt saadaval.

| Riik/regioon | Funktsiooni nimi                         | Äridokument |
|----------------|--------------------------------------|-------------------|
| Austria        | Austria elektroonilised arved (AT)    | Müügi- ja projektiarved |
| Belgia        | Belgia elektrooniline arve (BE)      | Müügi- ja projektiarved |
| Brasiilia         | Brasiilia NF-e (BR)                  | Finantsdokumendi mudel 55, paranduskirjad, tühistamised ja tagasilükkamised |
| Brasiilia         | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuste finantsdokumendid |
| Brasiilia         | Brasiilia NF-e import meilist (BR) | Rahandusdokumentide 55. mudel |
| Taani        | Taani elektrooniline arve (DK)       | Müügi- ja projektiarved |
| Egiptus          | Egiptuse elektrooniline arve (EG)     | Müügi- ja projektiarved |
| Eesti        | Eesti elektrooniline arve (EE)     | Müügi- ja projektiarved |
| Soome        | Soome elektrooniline arve (FI)      | Müügi- ja projektiarved |
| Prantsusmaa         | Prantsusmaa elektrooniline arve (FR)       | Müügi- ja projektiarved |
| Saksamaa        | Saksamaa elektrooniline arve (DE)       | Müügi- ja projektiarved |
| Itaalia          | FatturaPA (IT)                       | Müügi- ja projektiarved |
| Holland    | Hollandi elektrooniline arve (NL)        | Müügi- ja projektiarved |
| Norra         | Norra elektrooniline arve (NO)    | Müügi- ja projektiarved |
| Hispaania          | Hispaania elektrooniline arve (ES)      | Müügi- ja projektiarved |
| Euroopa         | PEPPOL-i elektrooniline arve            | PEPPOL-i müügi- ja projektiarved |
| Euroopa         | PEPPOL hankija arve                | PEPPOL impordi hankijaarved |
| Saudi Araabia   | Elektroonilised arved Saudi Araabias (SA)| Müügi- ja projektiarved |

### <a name="preview-features"></a>Eelvaatefunktsioonid

Järgmises tabelis on toodud elektroonilise arvelduse funktsioonid, mis on praegu saadaval eelvaateversioonis.

| Riik/regioon | Funktsiooni nimi                         | Äridokument |
|----------------|--------------------------------------|-------------------|
| Mehhiko         | Mehhiko CFDI (MX)                    | Müügiarved, saatelehed, varude üleviimised, maksetoetused ja tühistamised |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Elektroonilise arvelduse funktsioonide konfigureeritavad komponendid

Elektroonilise arvelduse funktsioonid hõlmavad järgmisi konfigureeritavate komponentide gruppe.

- **Vormingud**: vormingud võimaldavad teil konfigureerida, mida elektroonilise arvelduse lisandmoodul peab genereerima, kui elektroonilisest dokumendist saab elektrooniline arve. Vormingud hõlmavad elektroonilise arve ning nende failide ja sõnumite vormingu konfiguratsiooni, mida kasutatakse taotluste esitamiseks ning vastuste saamiseks, kui nõutav on suhtlus välise veebiteenusega.
- **Tegevused**: tegevused võimaldavad teil konfigureerida, kuidas elektroonilise arvelduse lisandmoodul genereerib teenuste Finance ja Supply Chain Management esitatud elektroonilise dokumendi teisendamise elektrooniliseks arveks.
- **Kohaldatavusreeglid**: kohaldatavusreeglid võimaldavad teil konfigureerida konteksti, mida elektroonilise arvelduse lisandmoodul peab elektroonilise arvelduse funktsiooni töötlemiseks arvestama.
- **Muutujad**: muutujad võimaldavad teil konfigureerida konfiguratsiooniloogika koostamise tuge. Muutujaid saab kasutada väärtuste sisendina konkreetse tegevuse sooritamiseks. Teise võimalusena saab neid kasutada väärtuste vahetajana teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahel.
- **Elektroonilise dokumendi mudelivastendus**: elektroonilise dokumendi mudelivastendus võimaldab teil konfigureerida ER-i mudelivastendust. Mudelivastendus määratleb elektrooniliste dokumentide esitamise ajal elektroonilise arvelduse lisandmoodulisse integreeritava abstraktse arve andmevastenduse.
- **Arve kontekstimudel**: arve kontekstimudel võimaldab teil konfigureerida ER-i arve kontekstimudelit ja määratleda elektroonilise arvelduse funktsiooni konteksti.
- **Vastuse tüübid**: vastuse tüübid võimaldavad teil konfigureerida, mida elektroonilise arvelduse lisandmoodul peab teenustes Finance ja Supply Chain Management elektroonilise arve töötlemise tulemusena värskendama.

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

#### <a name="saudi-arabian-sa-electronic-invoice-sales-and-project-invoices-for-saudi-arabia"></a>Saudi Araabia (SA) elektrooniline arve: Saudi Araabia müügi- ja projektiarved

- Müügi e-arve (SA)
- Projekti e-arve (SA)

Lisaks ER-vormingu konfiguratsioonidele, mis on saadaval e-arveldamise teenusega kasutamiseks, saate luua ka oma ER-vormingu konfiguratsioone. E-arveldamise funktsioonidega kasutamiseks loodud vormingukonfiguratsioonid ei toeta siiski otsest viidet Finance või Supply Chain Management halduse tabelitele ega ühelegi vastavale metaandmele. Toetatakse ainult viiteid ER-mudeli vastendusele.

### <a name="actions"></a>Actions

Järgmises tabelis on toodud saadaolevad tegevused ja see, kas need on praegu üldiselt saadaval või on ikka eelvaateversioonis.

| Tegevus                                        | Kirjeldus                                                                  | Kättesaadavus         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Teisenda dokument                            | Käivitage dokumendi teisendamiseks elektroonilise aruandluse vorming.                   | Üldiselt saadaval  |
| XML-dokumendi allkirjastamine                             | Digiallkirjastage XML-dokumente.                                   | Üldiselt saadaval  |
| Egiptuse maksuameti JSON-dokumendi allkirjastamine | Digiallkirjastage Egiptuse maksuameti jaoks JSON-dokumente.       | Üldiselt saadaval  |
| Egiptuse ETA teenusega integreerimine           | Suhelge Egiptuse maksuametiga.                                     | Üldiselt saadaval  |
| Brasiilia SEFAZ teenuse kutsumine                  | Integreerige finantsdokumendi edastamiseks Brasiilia SEFAZ teenusega.       | Üldiselt saadaval  |
| Mehhiko PAC teenuse kutsumine                      | Integreerige CFDI edastamiseks Mehhiko PAC teenusega.                      | Eelvaates           |
| Töötle vastust                              | Analüüsige veebiteenuse kutsumise kaudu saadud vastust.                     | Üldiselt saadaval  |
| MS-i teenuse Power Automate kasutamine                         | Integreeri vooga sisseehitatud Microsoft Power Automate.                       | Eelvaates           |

### <a name="applicability-rules"></a>Kohaldatavusreeglid

Kohaldatavuse reeglid on konfigureeritavad klauslid, mis on määratletud e-arveldamise funktsiooni tasemel. Reeglid on konfigureeritud pakkuma e-arveldamise funktsioonide täitmise konteksti e-arveldamise võimaluse komplekti kaudu.

Kui Finance- või Supply Chain Management äridokument esitatakse e-arveldamiseks, ei sisalda äridokument selgesõnalist viidet, mis võimaldaks e-arveldamise võimalusel kutsuda konkreetset e-arveldamise funktsiooni esitamise töötlemiseks.

Kui äridokument on õigesti konfigureeritud, sisaldab see siiski vajalikke elemente, mis võimaldavad e-arveldamisel lahendada, milline e-arveldamise funktsioon tuleb valida, ja seejärel luua e-arve.

Kohaldatavuse reeglid võimaldavad e-arveldamise võimaluse komplektil leida täpsed e-arveldamise funktsioonid, mida tuleb kasutada edastuse töötlemiseks. Selleks viiakse esitatud äridokumendi sisu vastavusse kohaldatavuse reeglite klauslitega.

Näiteks võetakse e-arveldamise funktsioonide komplekti kasutusele kaks e-arveldamise funktsiooni koos seostuvate kohaldatavusreeglitega.

| E-arveldamise funktsioon | Kohaldatavusreeglid        |
|------------------------------|--------------------------- |
| A                            | <p>Riik = BR</p><p>ja</p><p>Juriidiline isik = BRMF</p>  |
| B                            | <p>Riik = MX</p><p>ja</p><p>Juriidiline isik = MXMF</p>  |

Kui Finance või Supply Chain Management äridokument esitatakse e-arveldamise võimaluse komplekti, sisaldab äridokument atribuute, mis on täidetud järgmiselt.

- Riik = BR
- Juriidiline isik = BRMF

E-arveldamise võimaluse komplekt valib e-arveldamise funktsiooni **A**, et töödelda edastust ja luua e-arve.

Sarnaselt, kui äridokument sisaldab järgmist.

- Riik = MX
- Juriidiline isik = MXMF

E-arve loomiseks on valitud e-arveldamise funktsioon **B**.

Kohaldatavuse reeglite konfiguratsioon ei saa olla mitmetähenduslik. See tähendab, et kahel või enamal e-arveldamise funktsioonil ei saa olla samu klausleid, vastasel juhul ei too see kaasa valikut. Kui e-arveldamise funktsioonid on dubleeritud, kasutage ebaselguse vältimiseks täiendavaid klausleid, et võimaldada e-arveldamise võimalusel eristada kahte e-arveldamise funktsiooni.

Näiteks kaaluge e-arveldamise funktsiooni **C** . See funktsioon on e-arveldamise funktsiooni **A** koopia.

| E-arveldamise funktsioon | Kohaldatavusreeglid        |
|------------------------------|--------------------------- |
| A                            | <p>Riik = BR</p><p>ja</p><p>Juriidiline isik = BRMF</p>  |
| C                            | <p>Riik = BR</p><p>ja</p><p>Juriidiline isik = BRMF</p>  |

Selles näites on funktsioon **C** äridokumendi esitamise ees sisaldades järgmist.

- Riik = BR
- Juriidiline isik = BRMF

E-arveldamise funktsioon ei suuda eristada, millist e-arveldamise funktsiooni tuleb edastuse töötlemiseks kasutada, kuna esildised sisaldavad täpselt samu klausleid.

Nende kahe funktsiooni eristamiseks kohaldatavuse reeglite kaudu tuleb ühele funktsioonile lisada uus klausel, mis võimaldab e-arveldamise võimalusel valida õige e-arveldamise funktsiooni.

| E-arveldamise funktsioon | Kohaldatavusreeglid        |
|------------------------------|--------------------------- |
| A                            | <p>Riik = BR</p><p>ja</p><p>Juriidiline isik = BRMF</p>  |
| C                            | <p>Riik = BR</p><p>ja</p><p>Juriidiline isik = BRMF</p><p>ja</p><p>Mudel=55</p>  |

Keerukamate klauslite loomise toetamiseks on saadaval järgmised ressursid.

Loogikatehtemärgid:
- ja
- Või

Operaatoritüübid:
- Equal
- Not equal
- Greater than
- Less than
- Suurem kui või võrdne
- Väiksem kui või võrdne
- Contains
- Algab järgmisega

Andmetüübid:
- String
- Arv
- Loogiline
- Kuupäev
- UUID

Võimalus rühmitada ja tühistada klauslite rühmitamine.
Näidis näeb välja järgmine.

| E-arveldamise funktsioon | Kohaldatavusreeglid        |
|------------------------------|--------------------------- |
| C                            | <p>Riik = BR</p><p>ja</p><p>( Juriidiline isik = BRMF</p><p>või</p><p>Mudel=55)</p>  |


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

- **Teenusekeskkond** – kui juurutamise sihtmärk on teenusekeskkond, avaldatakse elektroonilise arvelduse funktsiooni versioon teenusekeskkonnas. Elektroonilise arvelduse lisandmoodul on seejärel valmis teenuste Finance ja Supply Chain Management saadetavaid elektroonilisi dokumente vastu võtma ja töötlema.
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
