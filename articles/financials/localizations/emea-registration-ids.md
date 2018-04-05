---
title: Registreerimise ID-d
description: See teema annab teavet registreerimise ID-de seadistamise ja kasutamise kohta.
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 978c6c6f2a3de803f252e93040d2d7eb2bc4a793
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="registration-ids"></a>Registreerimise ID-d

[!include[banner](../includes/banner.md)]


See teema annab teavet registreerimise ID-de seadistamise ja kasutamise kohta.

Paljudes riikides ja regioonides on erinevad määrused ja nõuded maksu registreerimisnumbrite ehk ID-de salvestamiseks. See teema annab ülevaate nõutud sätetest ja toetatud registreerimistüüpide töötlemisest erinevates Euroopa riikides/piirkondadeds asuvate osapoolte puhul. Kõigis riikides/regioonides kehtivad oma nõuded mitmesuguste erinevate ametiasutuste registreerimisnumbritega seotud riigikohaste funktsioonide toetamiseks. Registreerimisnumbrid on näiteks isikukood (SSN), maksu ID-kood (TIN) ja Euroopa käibemaksukood (EL-i KMKR). See funktsioon pakub ühtset raamisitikku kõigi piirkondade kõigile riikidele, võttes arvesse mõne Euroopa riigi riigikohaseid nõudeid. Järgmised jaotised kirjeldavad üldist teabevoogu, mida kasutatakse registreerimise ID-de seadistamiseks ja töötlemiseks.

## <a name="registration-type-creation"></a>Registreerimistüübi loomine
Enne registreerimise ID sisestamist peate seadistama erinevat tüüpi registreerimisnumbrite jaoks registreerimistüübid, mis igale osapoolele kehtivad. Erinevates riikides/regioonides asuvate hankijate, klientide, töötajate ja juriidiliste isikute jaoks registreerimistüüpide loomiseks ning haldamiseks minge lehele **Organisatsiooni haldus** &gt; **Globaalne aadressiraamat** &gt; **Registreerimistüübid** &gt; **Registreerimistüübid**.

|Väli                 |Kirjeldus      |
|------------------------------|----------------------------|                                                                           
| Nimi                | Registreerimistüübi nimi. |                                                                           
| Kirjeldus         | Registreerimistüübi kirjeldus. |
| Riik/regioon      | Riigi/regiooni kordumatu identifikaator.|
| Maksuhaldur       | Registreerimistüübiga seostatud maksuamet.|
| Kitsendatud       | Maksu registreerimistüübile kohalduva piirangu laad: Pole, Isik, Organisatsioon.|
| Vorming              | Registreerimistüübi kinnitusvorming.|
| Saab uuendada      | Määratleb, kas registreerimistüübi registreerimisnumbrit saab pärast sisestamist värskendada.|
| Kordumatu              | Määratleb, kas registreerimistüübi registreerimisnumber on kordumatu. |
| Riigi puhul esmane | Kui mõni osapool on seostatud kindlas riigis ühe või mitme aadressiga ja registreerimise ID kehtib kõigi nende aadresside puhul, peate määrama ühe neist aadressidest selle riigi puhul peamise aadressina. Peamisena saab registreerida ainult ühe ID. Määratleb, kas registreerimisnumbri saab sisestada ainult riigi primaarse aadressi puhul. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Määrake registreerimistüüp registreerimiskategooriale
Registreerimiskategooria on riigi/regiooni registreerimise identifikaator, mis on heaks kiidetud kasutamiseks kindlas riigis/regioonis maksu-, tolli- ja muul otstarbel. See kategooria määratleb kõnealuse registreerimise ID kinnitusreeglid (nt kontrollnmbrid jne) ja registreerimise ID kaasamise erinevates aruannetes. Kindla riigi registreerimistüübi määramiseks toetatud registreerimiskategooriasse kasutage lehte **Organisatsiooni haldus** &gt; **Globaalne aadressiraamat** &gt; **Registreerimistüübid** &gt; **Registreerimiskategooriad**.

| Väli            | Kirjeldus|
|-----------------------|----------------|
| Registreerimise tüüp     | Registreerimistüüp kõnealuses riigis/regioonis.|
| Kitsendatud         | Maksu registreerimistüübile kohaldub piirangu laad: Pole, Isik, Organisatsioon.|
| Registreerimiskategooria | Riigis kasutamiseks heakskiidetud kordumatu registreerimise identifikaator. Microsoft Dynamics 365 for Finance and Operationsi toetatud kategooriate tervikloend on allpool. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Sisestage registreerimise ID-d globaalse aadressiraamatu kirjete puhul

Rakenduse Microsoft Finance and Operations globaalne aadressiraamat (GAB) sisaldab konsolideeritud aadressiteavet klientide, hankijate, kontaktide, ärisuhete ja juriidiliste isikute kohta. Lisateavet vt teemast [Globaalse aadressiraamatu ülevaade](../../fin-and-ops/organization-administration/overview-global-address-book.md). Osapoole kirjed, mis on salvestatud globaalsesse aadressiraamatusse, võivad sisaldada üht või mitut aadressikirjet. Neid aadresse kasutatakse erinevatel eesmärkidel, näiteks arvete või tarnimise jaoks. Saate määrata aadressiteabe jaoks registreerimise ID-d klientidele, hankijatele, töötajatele ja juriidilistele isikutele. Leidke osapoole (juriidiline isik, hankija, klient, töötaja) kirje, mille jaoks soovite registreerimise ID-d sisestada, ja klõpsake osapoole, juriidilise isiku, hankija, kliendi või töötajaga seotud vormidel valikut **Registreerimise ID-d**, et avada leht **Aadresside haldamine**. Klõpsake vahekaardil **Maksu registreerimine** nuppu **Lisa** ja sisestage registreerimise ID kohta järgmine teave.


|Väli                |Kirjeldus                                                |
|---------------------|-----------------------------------------------------------|
| Registreerimise tüüp   | Registreerimistüüp valitud riigis/regioonis.     |
| Registreerimiskood | Osapoole registreerimise ID.                                |
| Kirjeldus         | Registreerimisnumbri kirjeldus.               |
| Lõik             | Lisateave registreerimisnumbri kohta. |
| Väljaandev asutus      | Registreerimisnumbri väljastanud asutus.        |
| Väljastamise kuupäev         | Registreerimisnumbri väljastamiskuupäev.              |
| Jõustunud           | Registreerimisnumbri kehtivuskuupäev.           |
| Aegumine          | Registreerimisnumbri aegumiskuupäev.          |

> [!NOTE]
> Juriidilise isiku, hankija või kliendi maksukohuslase koodi saab valida KMKR-iga seotud registreerimise ID-de seast ja osapoole jaoks sisestada.

## <a name="search-for-records-by-registration-id"></a>Kirjete otsing registreerimise ID alusel
Osapoolte kirjete otsimine registreerimise ID alusel on võimalik osapoole, juriidilise isiku, hankija, kliendi ja töötajaga seotud vormidel. Klõpsake valikut **Registreerimise ID otsing**, et avada leht **Registreerimise ID otsingukriteeriumid**. Määrake otsingukriteeriumid ja klõpsake nuppu **Leia**. Süsteem kuvab valitud kirjed globaalsest aadressiraamatust ja seostatud tüüpi osapoole kirjed.

## <a name="supported-registration-categories"></a>Toetatud registreerimiskategooriad
Järgmises tabelis on toodud Finance and Operationsis toetatud registreerimistüübid. Kui olete Microsoft Dynamics AX 2012 registreerimise ID väljadega tuttav, leiate sellest tabelist ka nende väljade vasted Finance and Operationsi registreerimiskategooriatele.

| Finance and Operationsi registreerimiskategooria         |Riik/regioon  | Dynamics AX 2012 mõiste/väli|
|---------------------------------------------------------------|---------------------|---------------------------------|
| KM-i ID                                                        | Kõik Euroopa Liidu (EL) riigid|  Maksukohustuslase kood (seadusjärgset tüüpi TAX ID rakenduses AX 2012 R3)|
| Ettevõtte ID (COID)                                          | Belgia, Tšehhi Vabariik, Eesti, Ungari, Läti, Leedu, Poola, Šveits | Ettevõtte number (EnterpriseNumber) Registreerimisnumber (RegNum\_W) Registreerimisnumber (RegNum\_W) Registreerimisnumber (RegNum\_W) Registreerimisnumber (RegNum\_W) Ettevõtet kood (EnterpriseCode) Registreerimisnumber (RegNum\_W) UID (Seadusjärgset tüüpi UID rakenduses AX 2012 R3) |
| Haru ID                                                     | Belgia            | Filiaali kood (BranchNumber)|
| Spisová značka (registreerimisnumber, väljaandev asutus, sektsioon) | Tšehhi Vabariik     | Sisestatud number (CommercialRegisterInsetNumber) Säilitatud äriregistris (CommercialRegister) Äriregistri sektsioon (CommercialRegisterSection)|
| Tollikliendi ID                                           | Soome | Tollikliendi number (CustomsCustomerNumber\_FI)|
| INN                                                           | Venemaa Föderatsioon| INN (seadusjärgset tüüpi INN rakenduses AX 2012 R3)|
| RRC                                                           | Venemaa Föderatsioon| RRC (seadusjärgset tüüpi RRC rakenduses AX 2012 R3)|
| OKDP                                                          | Venemaa Föderatsioon| OKDP (seadusjärgset tüüpi OKDP rakenduses AX 2012 R3)|
| OKPO                                                          | Venemaa Föderatsioon| OKPO (seadusjärgset tüüpi OKPO rakenduses AX 2012 R3)|
| RCOAD                                                         | Venemaa Föderatsioon| RCOAD (seadusjärgset tüüpi RCOAD rakenduses AX 2012 R3)|
| OGRN                                                          | Venemaa Föderatsioon| OGRN (seadusjärgset tüüpi OGRN rakenduses AX 2012 R3) |
| SNILS                                                         | Venemaa Föderatsioon| SNILS (seadusjärgset tüüpi SNILS rakenduses AX 2012 R3)|
| CIFTS                                                         | Venemaa Föderatsioon| CIFTS (seadusjärgset tüüpi CIFTS rakenduses AX 2012 R3)|
| Pass                                                      | Hispaania             | Pass|
| Ametlik identifitseerimisdokument                              | Hispaania             | Ametlik identifitseerimisdokument|
| Elukohatõend                                         | Hispaania             | Elukohatõend|
| Muu identifitseerimisdokument                                 | Hispaania             | Muu identifitseerimisdokument|
| Pole loendatud                                                  | Hispaania             | Pole lahenduses AX 2012 R3 saadaval|


Lisateavet registreerimise ID-de töötlemise kohta, sealhulgas nõutavad eeltingimused, leiate järgmistest elutsükliteenuste (LCS) KMKR-i tegevuste salvestistest.

-   KM ID seadistamine
-   Hankija KMKR-i registreerimine
-    Osapoole otsing KM ID abil





