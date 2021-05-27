---
title: VAT deklaratsioon Egiptuse jaoks
description: Käesolev teema kirjeldab, kuidas konfigureerida ja luua Egiptuse kinnipeetava maksu deklaratsioone.
author: sndray
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bd48ee96a26c59183981fae879e3659711e70ce3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021952"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>VAT deklaratsioon Egiptuse jaoks (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada ja luua käibemaksu tagastusvormi ning Egiptuse juriidiliste isikute müügi- ja osturaamatuid.

Egiptuse käibemaksutagastuse vorm on ametlik dokument, mis võtab kokku kogu tasutava käibemaksusumma, kogu sisendkäibemaksu summa tagasisaadav käibemaksu ja seotud käibemaksusumma kohustuse. Vormi kasutatakse kõigi maksumaksjate tüüpide puhul ning see tuleb maksuhalduri portaali kaudu käsitsi täita. KM-i tagastamise vormi nimetatakse tavaliselt KM-i tagastamise registreerimiseks.

Käibemaksu tagastusvorm hõlmab Dynamics 365 Finance järgmisi aruandeid:

- KM-i tagastusvorm nr 10, mis pakub vastavalt seadusandlusele summasid, korrigeerimisi ja KM-summasid rea kauba kohta.
- Müügikannete raamat
- Ostukannete raamat

## <a name="prerequisites"></a>Eeltingimused
Juriidilise isiku peamine aadress peab olema Egiptuses.
**Funktsioonide halduse** tööruumis, lülitage sisse järgmised funktsioonid:

   - (Egiptus) Müügi- ja ostumaksuaruande kategooriahierarhia.

Lisateavet funktsioonide lubamise kohta, vaata [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

**Elektroonilise aruandluse** tööruumis importige hoidlast järgmised elektroonilise aruandluse vormingud:

- VAT deklaratsioon Excel (EG)

> [!NOTE]
> Ülaltoodud vorming põhineb **maksudeklaratsiooni mudelil** ja kasutab **maksudeklaratsiooni mudeli vastendamist**. See lisakonfiguratsioon imporditakse automaatselt.

Lisateavet selle kohta, kuidas importida elektroonilise aruandluse konfiguratsioone, vaata [Elektrooniliste aruannete konfiguratsioonide allalaadimine Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine

Egiptuse deklaratsioonivormide rakendamine põhineb elektroonilise aruandluse (ER) konfiguratsioonil. Lisateavet konfigureeritava aruandluse võimaluste ja mõistete kohta vaata [Eektroonilisest aruandlusest](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Tootmise ja kasutaja aktsepteerimise testimiseks (UAT) keskkonnas, järgige [Laadige alla elektroonilise aruandluse konfiguratsioonid Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Käibemaksu tagastamise vormi ja seotud aruannete loomiseks Egiptuse juriidilises isikus laadige üles järgmised konfiguratsioonid:

- Maksudeklaratsiooni model.version.70.xml või uuem versioon
- Maksudeklaratsioon model.version.70.120.xml või uuem versioon
- VAT deklaratsioon Excel (EG).versioon.70.32 või hilisem versioon

Pärast ER-i konfiguratsioonide allalaadimist Lifecycle Services (LCS) või globaalsest hoidlast viige lõpule järgmised sammud.

1. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
1. Lehel **Konfiguratsioonid** valige tegevuspaanil **Vahetuskursi** > **laadimine XML-failist**.
1. Laadige üles failid, mis on loetletud ülaltoodud järjekorras. Pärast kõigi konfiguratsioonide üles laadimist peaks konfiguratsioonipuu olema finantsis.

## <a name="set-up-application-specific-parameters"></a>Seadistage rakenduspõhised parameetrid

Rakendusespetsiifilised parameetrid lasevad teil määrata kriteeriumid, kuidas maksukanded aruande loomisel igal real klassifitseeritakse ja arvutatakse. Määratlemine põhineb kauba käibemaksugrupi, käibemaksugrupi, käibemaksukoodi ja teiste otsingudefinitsioonis kehtestatud kriteeriumide konfiguratsioonil.

Egiptuse müügi- ja osturaamatute aruanded sisaldavad veerge, mis vastavad kindlatele kandeklassifikatsioonile kui operatsioonide, toodete ja egiptuse omastele dokumentidele. Selle asemel, et lisada need uued klassifikatsioonid kannete sisestamisel uuteks sisestusandmeteks, määratakse klassifikatsioonid konfiguratsioonides tehtud erinevate otsingute alusel, mida on tutvustatud **Konfiguratsioonid** > **Seadistage rakendusomased parameetrid** > **Seaded** nii, et need vastaksid Egiptuse kinnipeetavate aruannet nõuetele. 

![Rakendusekohaste parameetrite leht](media/egypt-vat-declaration-setup1.png)

Järgmisi otsingu konfiguratsioone kasutatakse kannete klassifitseerimiseks ostu- ja müügi käibemaksuraamatute aruannetes:

- **PurchaseItemTypeLookup** > Veerg O: kauba tüüp
- **KMMäärTüüpOtsing** > veerg B: maksu tüüp
- **KMMäärTüüpOtsing** > veerg C: tabeli kauba tüüp
- **PurchaseOperationTypeLookup** > Veerg A: dokumendi tüüp
- **SalesOperationTypeLookup** > veerg N: toimingu tüüp
- **SalesltemTypeLookup** > Veerg O: kauba tüüp

Viige lõpule järgmised sammud erinevate otsingute häälestamiseks, mida kasutatakse VAT deklaratsiooni ja seotud raamatute aruannete loomiseks. 

1. **Elektroonilise aruandluse** tööruumis valige **konfiguratsioonide** > **Häälestus**, et seadistada reeglid kannete klassifitseerimise tuvastamiseks VAT deklaratsiooni aruandes.
2. Valige praegune versioon ja valige **Otsingud** otsingunime kiirkaardil. Näiteks **SalesItemTypeLookup**. See otsing tuvastab klassifikatsioonide loendi käibemaksuraamatus, mida maksuamet on nõudnud.
3. Suvandis **Tingimused** valige kiirkaardil klassifikatsiooni veerus **Lisa** ja uuel real **Otsingu tulemused** veerus, valige klassifikatsiooniga **veerg O** seotud rida.
4. Veerus **Müügi maksu grupp** valige seotud kood, mida kasutatakse müügi klassifikatsiooni tuvastamiseks. Näiteks **kodumaine müügiarve**. Kui konfiguratsioon on muul viisil määratletud, saate kasutada ka kauba käibemaksugruppi, maksukoodi või puuatribuute kombinatsiooni. 
5. Veerus **Nimi** valige maksukande klassifikatsioon.
6. Korrake samme 3-5 kõigi saadaval otsingute puhul.
7. Lõppkirje rea kaasamiseks klõpsake uuesti nuppu **Lisa** ja valige **otsingutulemuse** veerus suvand **Pole rakendatav**. 
8. Ülejäänud veergudes valige **Mitte tühi**. 

> [!NOTE]
> Kui lisate viimase kirje **Pole kohaldatav**, määrate järgmise reegli: kui käibemaksugrupp, kauba käibemaksugrupp, maksukood ja argumendina edastatud nimi ei täida kõiki eelnevaid reegleid, ei kaasata kandeid müügi KM raamatusse. Kuigi seda reeglit aruande loomisel ei kasutata, aitab reegel puuduva reegli konfiguratsiooni korral vältida tõrkeid aruande loomisel.

Järgmised tabelid esindavad näidet kirjeldatud otsingukonfiguratsioonide soovitatava konfiguratsiooni kohta. 

**SalesItemTypeLookup**

| Otsingu tulemus         | Liin | Käibemaksugrupp    | Kauba käibemaksugrupp    | Maksukood (kood) | Nimi                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Kodumaine              | 1    | Kohalik_VAT          | *Mitte tühi*             | *Mitte tühi*     | Müük                 |
| Kodumaine              | 2    | Kohalik_VAT          | *Mitte tühi*             | *Mitte tühi*     | SalesCreditNote       |
| Kodumaine              | 3    | VAT_FINALC         | *Mitte tühi*             | *Mitte tühi*     | Müük                 |
| Kodumaine              | 4    | VAT_FINALC         | *Mitte tühi*             | *Mitte tühi*     | SalesCreditNote       |
| Kodumaine              | 5    | VAT_PUBLIO         | *Mitte tühi*             | *Mitte tühi*     | Müük                 |
| Kodumaine              | 6    | VAT_PUBLIO         | *Mitte tühi*             | *Mitte tühi*     | SalesCreditNote       |
| Eksport                | 7    | VAT_Eksport         | *Mitte tühi*             | *Mitte tühi*     | Müük                 |
| Eksport                | 8    | VAT_Eksport         | *Mitte tühi*             | *Mitte tühi*     | SalesCreditNote       |
| Masin ja seadmed | 9    | *Mitte tühi*        | VAT_M&E                 | *Mitte tühi*     | Müük                 |
| Masin ja seadmed | 10   | *Mitte tühi*        | VAT_M&E                 | *Mitte tühi*     | SalesCreditNote       |
| Masinate osad        | 11   | *Mitte tühi*        | VAT_Osad               | *Mitte tühi*     | Müük                 |
| Masinate osad        | 12   | *Mitte tühi*        | VAT_Osad               | *Mitte tühi*     | SalesCreditNote       |
| Vabastused            | 13   | VAT_EXE            | *Mitte tühi*           | *Mitte tühi*     | SaleExempt            |
| Vabastused            | 14   | VAT_EXE            | *Mitte tühi*           | *Mitte tühi*     | SalesExemptCreditNote |
| Pole kohaldatav        | 15   | *Tühi*            | *Tühi*                 | VAT_ADJ         | *Mitte tühi*           |
| Pole kohaldatav        | 16   | *Mitte tühi*        | *Mitte tühi*             | *Mitte tühi*     | *Mitte tühi*           |

 **SalesOperationTypeLookup**

| Otsingu tulemus  | Liin | Kauba käibemaksugrupp    | Maksukood    | Nimi                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Kaubad          | 1    | VAT_Kaubad               | *Mitte tühi* | Müük                 |
| Kaubad          | 2    | VAT_Kaubad               | *Mitte tühi* | SalesCreditNote       |
| Kaubad          | 3    | VAT_Kaubad               | *Mitte tühi* | SaleExempt            |
| Kaubad          | 4    | VAT_Kaubad               | *Mitte tühi* | SalesExemptCreditNote |
| Teenused       | 5    | VAT_SERV                | *Mitte tühi* | Müük                 |
| Teenused       | 6    | VAT_SERV                | *Mitte tühi* | SalesCreditNote       |
| Teenused       | 7    | VAT_SERV                | *Mitte tühi* | SaleExempt            |
| Teenused       | 8    | VAT_SERV                | *Mitte tühi* | SalesExemptCreditNote |
| Korrigeerimised    | 9    | *Tühi*                 | VAT_ADJ     | Müük                 |
| Korrigeerimised    | 10   | *Tühi*                 | VAT_ADJ     | Ost              |
| Pole kohaldatav | 11   | *Mitte tühi*             | *Mitte tühi* | *Mitte tühi*           |

**PurchaseItemTypeLookup**

| Otsingu tulemus          | Liin | Kauba käibemaksugrupp    | Maksukood    | Nimi                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Kaubad                  | 1    | VAT_Kaubad               | *Mitte tühi* | Ost                 |
| Kaubad                  | 2    | VAT_Kaubad               | *Mitte tühi* | PurhćhaseCreditNote       |
| Teenused               | 3    | VAT_SERV                | *Mitte tühi* | Ost                 |
| Teenused               | 4    | VAT_SERV                | *Mitte tühi*  | PurhchaseCreditNote       |
| Masin ja seadmed  | 5    | VAT_M&E                 | *Mitte tühi* | Ost                 |
| Masin ja seadmed  | 6    | VAT_M&E                 | *Mitte tühi* | PurhchaseCreditNote       |
| Masinate osad         | 7    | VAT_Osad               | *Mitte tühi* | Ost                 |
| Masinate osad         | 8    | VAT_Osad               | *Mitte tühi* | PurhchaseCreditNote       |
| Vabastused             | 9    | VAT_EXE                 | *Mitte pank*  | PurchaseExempt           |
| Vabastused             | 10   | VAT_EXE                 | *Mitte tühi* | PurchaseExemptCreditNote |
| Pole kohaldatav         | 11   | *Tühi*                 | VAT_ADJ     | *Mitte tühi*              |
| Pole kohaldatav         | 12   | *Mitte tühi*             | *Mitte tühi* | *Mitte tühi*              |
| Pole kohaldatav         | 13   | *Tühi*                 | *Mitte tühi* | *Mitte tühi*              |

**PurchaseOperationTypeLookup**

| Otsingu tulemus  | Liin | Käibemaksugrupp  | Maksukood    | Nimi                     |
|----------------|------|------------------|-------------|--------------------------|
| Kodumaine       | 1    | Kohalik_VAT        | *Mitte tühi* | Ost                 |
| Kodumaine       | 2    | Kohalik_VAT        | *Mitte tühi* | PurhchaseCreditNote       |
| Kodumaine       | 3    | Kohalik_VAT        | *Mitte tühi* | PurchaseExempt           |
| Kodumaine       | 4    | Kohalik_VAT        | *Mitte tühi* | PurchaseExemptCreditNote |
| Imporditud       | 5    | VAT_Import       | *Mitte tühi* | Ost                 |
| Imporditud       | 6    | VAT_Import       | *Mitte tühi* | PurhchaseCreditNote       |
| Imporditud       | 7    | VAT_Import       | *Mitte tühi* | PurchaseExempt           |
| Imporditud       | 8    | VAT_Import       | *Mitte tühi* | PurchaseExemptCreditNote |
| Korrigeerimised    | 9    | *Tühi*          | VAT_ADJ     | PurhchaseCreditNote       |
| Korrigeerimised    | 10   | *Tühi*          | VAT_ADJ     | Ost                 |
| Pole kohaldatav | 11   | *Mitte tühi*      | *Mitte tühi* | *Mitte tühi*              |

**KMMäärTüüpOtsing**

| Otsingu tulemus  | Liin | Maksukood (kood) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| Esimenetabel     | 3    | *Mitte tühi*     |
| Teinetabel    | 4    | *Mitte tühi*     |
| Pole kohaldatav | 5    | *Mitte tühi*     |


## <a name="set-up-general-ledger-parameters"></a>Seadistage pearaamatu parameetrid

VAT deklaratsioonivormi aruannete loomiseks Microsoft Excel määratlege ER formaat **pearaamatu parameetrite** lehel.

1. Minge **Maksu** > **Seadistamise** > **pearaamatu parameetritesse**.
2. Vahekaardil **Müügi maks** jaotises **Maksuvalikud** väljal **KM-aruande vormingu vastendamine** valige **käibemaksudeklaratsiooni Excel (EG)**. Kui jätate selle välja tühjaks, luuakse standardne käibemaksuaruanne SSRS-vormingus.
3. Valige **kategooriahierarhia**. See kategooria võimaldab kaubaartikli koodi väliskaubanduse vahekaardil kannetes, et lubada kasutajatel valida ja klassifitseerida kaupu ja teenuseid. Selle klassifikatsiooni kirjeldus on müügi- ja ostukannete aruannetes üksikasjalik. See konfiguratsioon on valikuline.

![Deklaratsiooni vorm](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>KM tagastuse aruande loomine
Perioodi käibemaksu tagastusaruande ettevalmistamine ja esitamine põhineb käibemaksu maksekannetel, mis sisestati käibemaksutöö tasakaalustamise ja sisestamise ajal. Lisateavet tasumisele kuuluva ja saadaoleva käibemaksu kohta leiate teemast [Müügi maksu ülevaade](../general-ledger/indirect-taxes-overview.md).

Maksudeklaratsiooni aruande loomiseks viige lõpule järgmised sammud.

1. Minge **Maks** > **Deklaratsioon** > **Käibemaks** > **Käibemaksu deklareerimine perioodil** või **sisestage ja saatke käibemaks**.
2. Saate valida **seadistatava perioodi**.
3. Valige alguskuupäev ja seejärel käibemaksu makseversioon.
5. Valige nupp **OK**. 
6. Sisestage eelmise perioodi kreeditsumma, kui see on rakendatav, või jätke summa nulliks.
7. Tehke väljal **Aruande detailid** üks järgmistest valikutest. 
   - **Ostude käibemaksuraamat**: ostumaksu kannete üksikasjade aruande loomine.
   - **Ostude käibemaksuraamat**: ostumaksu kannete üksikasjade aruande loomine.
   - **KM-i deklaratsioon**: looge ainult KM-i deklaratsiooni tagastusvorm.
8. Saate sisestada vormi määramiseks registreeritud isiku nime.
9. Keele valimine. Kõik aruanded tõlgitakse **en-us** ja **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


