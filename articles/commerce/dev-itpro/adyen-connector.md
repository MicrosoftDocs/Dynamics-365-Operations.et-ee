---
title: Dynamics 365 Payment Connector Adyeni jaoks – ülevaade
description: See artikkel annab Microsoft Dynamics Puhvri 365 Payment Connectori ülevaate Puhvrile.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 58d88e023b73ce19331bd6f54644a62d8f6f35af
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812082"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Dynamics 365 Payment Connector Adyeni jaoks – ülevaade

[!include [banner](../includes/banner.md)]

See artikkel annab Microsoft Dynamics Puhvri 365 Payment Connectori ülevaate Puhvrile ja sisaldab laias laastmikus toetatud funktsioonide ja funktsioonide loendit. Seotud artiklid katavad Puhvri liitumise, konnektori konfigureerimise, korduma kippuvate küsimuste ja mõne tavaprobleemide tõrkeotsingu juhise.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Makse ülekandmine | Laiend, mis hõlbustab sidet Microsoft Dynamics 365 Commerce  (ja seostatud komponente) ja makseteenuse vahel. Selles artiklis kirjeldatud ühendus rakendati standardse maksete tarkvara arenduskomplekti (SDK) abil. |
| Kaart on olemas | Viitab maksekannetele, kus esitatakse füüsiline kaart ja mida kasutatakse makseterminali ühenduse kaudu Dynamics 365 müügipunktiga. |
| Kaarti pole | Viitab maksekannetele, kus füüsiline kaart puudub, nt e-äri või kõnekeskuse stsenaariumid. Sellistes stsenaariumides sisestatakse maksega seotud teave käsitsi kas e-äri veebisaidile, Kõnekeskuse voole või müügi- või makseterminali. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Toetatud funktsioonid, funktsioonid, versioonid ja terminalid

Puhvrist Dynamics 365 Payment Connector for Puhvri kasutab standardseid makseid SDK. Seetõttu pole sellel spetsiaalseid võimalusi, mis ei ole saadaval ka muude makseühenduste jaoks.

### <a name="supported-versions"></a>Toetatud versioonid

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 toetatud versioonid
Esimese osapoole valmis rakendust Dynamics 365 Payment Connector for Puhvrit Puhvrile Microsoft Dynamics toetab 365 Finantsversioon 8.1.3 (jaanuar 2019) või uuem versioon ja Microsoft Dynamics 365 Retail versioonis 8.1.3 või uuemas versioonis. Kolmandad osapooled saavad siiski luua Puhvri 365 Microsoft Dynamics varasemate versioonide jaoks teisi makseühendusi.

#### <a name="supported-adyen-firmware-versions"></a>Toetatud Värskendamise versioonid

Allolevas loendis kirjeldatakse kassa iga versiooni jaoks toetatud minimaalseid ja maksimaalseid Omaadi Microsoft Dynamics 365 Retail versiooni versioone.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail Müügikoha versioon 10.0.25
| Min Omahinna Koosteversioon | Uuenduste maksimaalne versioon |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail Müügikoha versioon 10.0.26
| Min Omahinna Koosteversioon | Uuenduste maksimaalne versioon |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail Müügikoha versioon 10.0.27
| Min Omahinna Koosteversioon | Uuenduste maksimaalne versioon |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail Müügikoha versioon 10.0.28
| Min Omahinna Koosteversioon | Uuenduste maksimaalne versioon |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail Müügikoha versioon 10.0.29
| Min Omahinna Koosteversioon | Uuenduste maksimaalne versioon |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail Müügikoha versioon 10.0.30
| Min Omahinna Koosteversioon | Uuenduste maksimaalne versioon |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Rnen võib välja vabastuse versiooni uuendused pärast seda, kui Microsoft on põhiversiooni testinud. Kuni põhiversiooni toetatakse, on korras, kui samas põhiversioonis on väiksemaid versioonivärskendusi. Need uuendused on tavaliselt väga sihitud parandused ja ei vasta täieliku uuestitestimiseks ribale, kuni sama põhiversiooni on eelnevalt testitud. Uuendused ei tohiks ületada dokumentatsioonis loetletud Omayen lisaversiooni maksimaalset versiooni. 
>
> Versioonist 53 varasemast Graneni versioonist versiooni 53 migreerimiseks tuleb commerce’i igakuiste uuenduste jaoks kasutada kassa KB **4577957** versioone 10.0.11 kuni 10.0.14. Kui üks neist versioonidest on kasutuses ja ei sisalda kiirparandust, lubab makseterminali järeltäiendus makseid ainult NFC kaudu. Kiirparanduse rakendamine kassale lahendab selle probleemi. Kui kassaversioon on vanem kui versioon 10.0.11, siis esitatakse tugitaotlus, kus on esitatud nõue, et kb **4577957** jaoks on teenusest väljas MPOS vaja parandust.
> 
> Versioonide 59p7 kuni 62p9 puhul taotleb kinkekaardi sularaha väljaminek PIN-kirjet kaks korda stsenaariumides, **kus** kinkekaart sisestatakse käsitsi. Seda probleemi ei taaskuvata, kui kinkekaart on läbi tõmmake. Asendatakse välja. 

### <a name="supported-payment-terminals"></a>Toetatud makseterminalid
Dynamics 365 makse ülemine konnektor Puhvrile kasutab seadme-agnostilise [Puhvri makseterminali API-d](https://www.adyen.com/blog/introducing-the-terminal-api). See toetab kõiki makseterminale, mida rakendusliides (API) toetab. Toetatud makseterminalide täieliku loendi saamiseks külastage [Terminen POS-i terminalide](https://www.adyen.com/pos-payments/terminals) lehte.

Järgmises videos kirjeldatakse Terminen Miles SE1 makseterminali Android võimalusi.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>Toetatud maksevahendid

#### <a name="supported-debit-and-credit-cards"></a>Toetatud deebet- ja krediitkaardid

| Tootemark | Variant | Kaart on olemas | E-kaubandus | Kõnekeskus |
|---|---|:-:|:-:|:-:|
| MasterCard | Krediit | ✔ | ✔ | ✔ |
| MasterCard | Deebet | ✔ | ✔ | ✔ |
| MasterCard | Alpha Banki preemia | ✔ | ✔ | ✔ |
| MasterCard | Raha maks | ✔ |  |  |
| MasterCard | Õiguse tasu | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Deebeti tasu | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VIISA | Krediit | ✔ | ✔ | ✔ |
| VIISA | Deebet | ✔ | ✔ | ✔ |
| VIISA | Alpha Banki preemia | ✔ | ✔ | ✔ |
| VIISA | Android Maksma | ✔ |  |  |
| VIISA | Raha maks | ✔ |  |  |
| VIISA | Õiguse tasu | ✔ |  |  |
| VIISA | VISA väljaregistreerimine | ✔ | ✔ | ✔ |
| VIISA | VISAEttKort | ✔ | ✔ | ✔ |
| VIISA | VisaMäärabario | ✔ | ✔ | ✔ |
| VIISA | VISA Aravia kaart | ✔ | ✔ | ✔ |
| AMEX | Krediit | ✔ | ✔ | ✔ |
| AMEX | Deebet | ✔ | ✔ | ✔ |
| AMEX | Android Maksma | ✔ |  |  |
| AMEX | Raha maks | ✔ |  |  |
| AMEX | Õiguse tasu | ✔ |  |  |
| AMEX | AMEX-i kaubandus | ✔ | ✔ | ✔ |
| AMEX | AMEX-i tarbija | ✔ | ✔ | ✔ |
| AMEX | AMEX ettevõtte | ✔ | ✔ | ✔ |
| AMEX | AMEX väikeettevõttele | ✔ | ✔ | ✔ |
| Discover | Standardne | ✔ | ✔ | ✔ |
| Discover | Android Maksma | ✔ |  |  |
| Discover | Raha maks | ✔ |  |  |
| Discover | Õiguse tasu | ✔ |  |  |
| Diners   | Standardne | ✔ | ✔ | ✔ |
| Dinsseažmail | Standardne | ✔ | ✔ | ✔ |
| JCB | Standardne | ✔ | ✔ | ✔ |
| Ametiühingutasu\* | Standardne | ✔ |  |  |
| Ac deebet\* | Standardne | ✔ |  |  |

\* Naisele ei ole antud interac ja Union Pay korduvate kaarditõendeid, nii et neid ei saa toetada kaardi mitteesinetavate kannete puhul.

#### <a name="supported-gift-cards"></a>Toetatud kinkekaardid
| Kava | Kaart on olemas | Kaarti pole |
|---|:-:|---|
| Anna üle | ✔ | ✔ |
| SVS | ✔ | ✔ |

Nende väliste kinkekaardiskeemide toetamiseks läbi Dynamics 365 Payment Connectori Puhvri jaoks peate lõpulema täiendavad sammud. Lisateavet vt väliste kinkekaartide [toe kohta](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Toetatud ümbrised

| Kava | Kaart on olemas | Kaarti pole |
|---|---|---|
| Aliment | Tugi lisatakse tulevases väljalaskes. | Nr |
| WeTšat | Tugi lisatakse tulevases väljalaskes. | Nr |

#### <a name="supported-card-present-input-methods"></a>Toetatud kaart esitab sisendmeetodeid
| Sisestusmeetod | Toetatud | Märkmed |
|---|:-:|---|
| Dip | ✔ | |
| Kaarditõmme | ✔ | |
| Koputage | ✔ | |
| Kassa kasutajaliidese kaudu käsitsi sisestus. |  | Praegu ei toetata |
| Käsitsi sisestus makseterminali kaudu. | ✔ | Toetab krediit-, deebet- ja kinkekaartide käsitsi sisestamist pin-sisestusega. | 


#### <a name="supported-card-present-countries"></a>Toetatud kaart on praeguses riigis

Järgmistel riikidel on ärikomponendid saadaval ja kaardi toe andmine Komponentidelt. Äriteenuste praeguse rahvusvahelise kättesaadavuse korral külastage rahvusvaheliselt [saadavuslehekülge](/dynamics365/get-started/availability).

| Riik | Toetatud |
| --- | :-: |
| Austraalia | ✔ |
| Austria | ✔ |
| Belgia | ✔ |
| Kanada | ✔ |
| Tšehhi Vabariik | ✔ |
| Taani | ✔ |
| Eesti | ✔ |
| Soome | ✔ |
| Prantsusmaa | ✔ |
| Saksamaa | ✔ |
| Hongkongi EHP | ✔ |
| Ungari | ✔ |
| Island | ✔ |
| Iirimaa | ✔ |
| Itaalia | ✔ |
| Jaapan | Tulevane vabastamine |
| Läti | ✔ |
| Leedu | ✔ |
| Malaisia | ✔ |
| Holland | ✔ |
| Uus-Meremaa | ✔ |
| Norra | ✔ |
| Poola | ✔ |
| Singapur | ✔ |
| Šveits | ✔ |
| Hispaania | ✔ |
| Rootsi | ✔ |
| Šveits | ✔ |
| Ühendkuningriik | ✔ |
| Ameerika Ühendriigid | ✔ |
| Brasiilia | Tulevane vabastamine |

#### <a name="supported-card-not-present-countries"></a>Toetatavad kaart ei ole praeguses riigis

Oma kaardi mittekannete puhul toetab Sisestaja järgmisi riike. [Konkreetse riigi toe](https://www.adyen.com/contact/sales) üksikasjade saamiseks pöörduge Nende poole. Äriteenuste praeguse rahvusvahelise kättesaadavuse korral külastage rahvusvaheliselt [saadavuslehekülge](/dynamics365/get-started/availability).

| Riik | 
| --- |
| Argentina |
| Armeenia |
| Austraalia |
| Austria |
| Bahrein |
| Belgia |
| Brasiilia |
| Bulgaaria |
| Kanada |
| Tšiili |
| Hiina |
| Colombia |
| Horvaatia |
| Küpros |
| Tšehhi Vabariik  |
| Taani |
| Egiptus |
| Eesti |
| Soome |
| Prantsusmaa |
| Gruusia |
| Saksamaa |
| Gibraltar |
| Kreeka |
| Guernsey |
| Hongkongi EHP |
| Ungari |
| Island |
| India |
| Indoneesia |
| Iirimaa |
| Mani saar |
| Iisrael |
| Itaalia |
| Jaapan |
| Jersey |
| Lõuna-Korea |
| Kuveit |
| Läti |
| Leedu |
| Luksemburg |
| Malaisia |
| Malta |
| Mehhiko |
| Maroko |
| Holland |
| Uus-Meremaa |
| Norra |
| Peruu |
| Poola |
| Portugal |
| Katar |
| Rumeenia |
| Saudi Araabia |
| Serbia |
| Singapur |
| Slovakkia |
| Sloveenia |
| Lõuna-Aafrika Vabariik |
| Hispaania |
| Rootsi |
| Šveits |
| Taiwan |
| Tansaania |
| Tai |
| Selle välja id |
| Araabia Ühendemiraadid (AÜE) |
| Ühendkuningriik |
| Ameerika Ühendriigid, sh Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Toetatud Dynamics 365 maksefunktsioonid

Järgmine tabel näitab funktsioonide kogumeid, mida Dynamics 365 Payment Connector for Puhvri toetab. Need funktsioonid kasutavad täiustusi, mida tutvustati maksete SDK-le ja mõnedele komponentidele detsembris 2018. Need ei ole välistavad Dynamics 365 Payment Connectori Puhvri jaoks. Lisateavet selle kohta, kuidas neid täiustusi erineva makseühenduse jaoks kasutada, [vt makseterminali lõpp-lõpu maksete integreerimise loomine](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Kava | Kaart on olemas | Kaarti pole |
|---|:-:|:-:|
| [Kinkekaardi saldo väljaminek](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Maksete duplikaatkaitse](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Kanali lubamine  | ✔ | ✔ |
| Lingitud tagasimaksed | ✔<br>(Algab 10.0.1) | ✔<br>(Algab 10.0.1) |
| [Salvesta võrgumaksed](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Algab 10.0.2) | 
| [Välised kinkekaardid kõnekeskusele ja e-kaubandusele](./gift-card.md) | ✔<br>(Algab 10.0.10) | 
| [SCA makse ümbersuunamine](../adyen_redirect.md) | | ✔<br>(Algab 10.0.12) |
| [Sihtotstarbelised makseterminalid ning printeri ja sularahasahtli viibad](../pos-multi-hws.md) | ✔<br>(Algab 10.0.12) | |
| [SDK-taseme kaldlemise tugi Puhvri kaudu](tipping.md) | ✔<br>(Algab 10.0.14) | |
| [Tellimuse arveldamise astmeline hõivamine](incremental-capture.md) |  | ✔<br>(Algab 10.0.18) |
| [Väljaminekumaksed](../wallets.md) |  | ✔<br>(Algab 10.0.20) |
| [Omaste tasu koos Rnen-ga](google-pay-adyen.md) |  | ✔<br>(Algab 10.0.27) |

## <a name="next-steps"></a>Järgmised sammud

Teavet Dynamics 365 Makseühenduse seadistamiseks ja konfigureerimiseks Puhvri Puhvri jaoks vt [Dynamics 365 Makseühendust Puhvri seadistamiseks](adyen-connector-setup.md).

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Payment Connector Adyeni jaoks – häälestamine](adyen-connector-setup.md)

[Dynamics 365 Payment Connector Adyeni jaoks – KKK](adyen-connector-faq.md)

[Dynamics 365 Payment Connector Adyeni jaoks – tõrkeotsing](adyen-connector-troubleshoot.md)

[Maksete KKK](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
