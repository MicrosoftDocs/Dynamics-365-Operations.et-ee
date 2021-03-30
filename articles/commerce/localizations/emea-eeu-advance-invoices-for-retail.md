---
title: Commerce'i ettemaksuarved Ida-Euroopa puhul
description: Selles teemas selgitatakse, kuidas seadistada Ida-Euroopa ettemaksu teavitusi.
author: epopov
manager: annbe
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5199d745eea467408eed32c5cd5ba8f964fec497
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225722"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a>Commerce'i ettemaksuarved Ida-Euroopa puhul

[!include [banner](../includes/banner.md)]

Selles teemas sisalduv teave kehtib Ida-Euroopa asukohale ja puudutab konkreetselt kaubandust.

Poola, Ungari ja Tšehhi Vabariigi korral tuleb peale kliendilt müügipunktis saadud ettemakset see ettemakse maksude eesmärgil registreerida ning vajalik on luua ja trükkida ettemaksuarve, mis sisaldab ettemaksu summat. Lisaks tuleb Poola korral ettemaksearvete tehingud kanda pearaamatusse.

Kui müügitellimuse arve lõpuks sisestatakse, peaks lõppdokument sisaldama ettemaksuarvet ning näidatud peaksid olema mistahes ettemaksed.

Kui loote müügireskontost müügitellimusi, peate looma ettemaksuarved käsitsi, kasutades jaotise [Ida-Euroopa ettemaksuarved](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice) protseduure. Kui loote müügitellimusi kassa kaudu, loob ja sisestab teile ettemaksearved süsteem.

## <a name="supported-scenarios"></a>Toetatud stsenaariumid

Toetatud on järgmised stsenaariumid.

- Ettemaksuarve loomine ja sisestamine.
- Deposiidisumma muutmine. Kui klient otsustab sissemakse summat suurendada, väljastatakse lisandub ettemaksuarve. Kõigi teiste deposiidisumma muudatuste korral (näiteks, kui kliendi tellimust muudetakse), luuakse eelnevalt loodud ettemaksuarvele kreeditarve ning luuakse ja sisestatakse uus ettemaksuarve parandatud summaga.
- Seotud ettemaksuarvetega müügitellimuse tühistamine. Sellisel juhul luuakse ettemaksuarvele kreeditarve.
- Ettemaksuarvetega seotud müügitellimuse arve sisestamine. Müügiarve tühistatakse müügitellimusega seotud ettemaksuarve summas. Esialgse ettemaksuarve kanded tasakaalustatakse ettemaksuarve tühistamise kannetega.

## <a name="set-up-advance-invoices"></a>Ettemaksuarvete seadistamine

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a>Ettemaksuarvete loomise funktsionaalsuse sisselülitamine

1. Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**.
2. Seadistage **Tellimus** kiirkaardi **Klienditellimused** vahekaardi suvand **Deposiidi ettemaksuarve koostamine** **Jah** peale.

### <a name="define-the-parameters-for-posting-advance-invoices"></a>Ettemaksuarvete sisestamise parameetrite määramine.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
2. Seadistage **Ettemaksuarve** kiirkaardi **Uuendused** vahekaardil **Sisestusreeglid**, **Käibemaksugrupp**, ja **Kauba käibemaksugrupp** väljad. Kui need väljad on õigesti seadistatud, sisestatakse ettemaksuarve. Kui need väljad ei ole seadistatud, ettemaksuarveid ei sisestata.

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a>Lülitage välja käibemaksu sisestamine ettemaksu töölehekandele

Ettemaksu töölehekande käibemaksu ei sisestata, kui ettemaksuarve sisestamine on sisse lülitatud. Selle nõude täitmise kontrollimiseks toimige järgmiselt.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
2. Veenduge, et **Makse** kiirkaardi **Pearaamat ja käibemaks** vahekaardil on järgmised väljad kas tühjad või seadistatud **Ei** peale:

    - Ettemaksu töölehekande käibemaks
    - Sisestusreeglid ettemaksu töölehekandega
    - Ettemakse maksugrupp
    - Kauba käibemaksugrupp

## <a name="print-advance-invoices"></a>Ettemaksuarvete printimine

Ettemaksuarveid saate printida kassast Microsoft Windowsi printeriga, mis on riistvarajaamaga ühendatud. Kassast ettemaksuarvete printimiseks on kaks võimalust:

- **Printige ettemaksuarve pärast kassas kande lõpetamist.** See suvand kuvatakse automaatselt, kui ettemaksuarve on loodud ja Windowsi printer on õigesti seadistatud. Sel juhul prinditakse ainult viimane klienditellimusega seotud ettemaksuarve.
- **Ettemaksuarve töölehelt uuesti printimine.** Valige töölehtede avamiseks **Näita töölehte**, leidke klienditellimus ja seejärel valige **Prindi ettemaksuarve**. Sel juhul prinditakse kõik kliendi tellimusega seotud ettemaksuarved.

### <a name="set-up-a-windows-printer"></a>Windowsi printeri seadistamine

Riistvarajaamaga ühendatud Windowsi printeriga dokumentide kassast printimise võimaldamiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**.
2. Valige riistvaraprofiil, mis on seotud selle kauplusega, kus printerit kasutatakse.
3. Uuendage seaded kas jaotises **Printer** või jaotises **Printer 2**:

    - Väljal **Printer** valige **Windowsi draiver**.
    - Sisestage printeri nimi väljale **Seadme nimi**.

4. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
5. Valige töö **1090** ja seejärel **Käivita kohe**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]