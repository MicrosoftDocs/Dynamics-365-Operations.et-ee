---
title: Maksmiseks valmis
description: See teema näitab, kuidas märkida töötaja maksmiseks valmis rakenduses Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732413"
---
# <a name="ready-to-pay"></a>Maksmiseks valmis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Kui soovite märkida töötaja maksmiseks valmis olevaks, peate esmalt lubama funktsioonihalduses **(Eelvaate) palgaarvestuse integratsiooni** funktsiooni. Lisateavet funktsioonide eelversioonide lubamise kohta vt [Funktsioonide haldamine](hr-admin-manage-features.md).

See funktsioon võimaldab personalispetsialistidel mõista, millised töötajad on palgaarvestuseks valmis ja mis nõuavad tegevust enne, kui kolmandast osapoolest palgapakkuja seda tarbib.

## <a name="mark-employee-as-ready-to-pay"></a>Märgi töötaja maksmiseks valmis

Töötaja teabe kogumine ja kontroll võib olla aeganõudev ja täis rohkeid tõrkeid. Pakkudes inimressursside spetsialistidele võimalust töötajate teabe ülevaatamiseks ja selle lihtsaks uuendamiseks, aitab Dynamics 365 Human Resources vähendada palga töötlemise lõpetamiseks kulunud aega.

Töötaja staatuse muutmiseks kui "valmis makseks" tehke järgmist.

1. Avage **Tasuhaldus**. Tööruumis on kaks paani 
    - **Töötajad on maksmiseks valmis**
    - **Töötajad, kes pole maksmiseks valmis**
    ![Tasuhalduse tööruum.](./media/hr-ready-to-pay-1-workspace.png)

2. Valige paani **Töötajad, kes pole maksmiseks valmis**.

3. Valige valideeritavad töötajad. **Palgaarvestuse vahekaardil** grupis **Maksmiseks valmis** valige **Kontrolli**.
    ![Kontrolli töötajaid.](./media/hr-ready-to-pay-2-validate.png)

4. Tulemuste ülevaatamiseks valige grupis **Maksmiseks valmis** **Palgaarvestus vahekaardil** valik **Tulemused**.

## <a name="validation"></a>Valideerimine

Enne töötaja märkimist maksmiseks valmis olevaks teeb süsteem profiili täielikkuse põhikontrolli.

![Kinnita tulemused.](./media/hr-ready-to-pay-3-results.png)

Järgmine tabel sisaldab teavet iga teostatud valideerimise kohta. 

| Valideerimine | Details |
| --- | --- |
| Aadressi eesmärgi parameeter | Kontrollib, kas parameeter **Kasuta palgaarvestuse aadresse** on sees. |
| Palgaarvestuse aadress | Kinnitatakse, kui töötaja profiilil on vähemalt üks aadress, mille eesmärk on „Palgaarvestuse elukoht” või „Palgaarvestuse töökoht”, ja iga eesmärgi jaoks on ainult üks aadress. |
| Töösuhe | Kontrollige, kas töötajal on vähemalt üks tööleping (praegune, eelmine või tulevane). |
| ID-number | Kinnitab, kas parameeter "Kasuta palgatöötluses identifitseerimistüüpe" on jah ja kas parameetris näidatud identifitseerimistüüp on täidetud töötajaprofiilis. |
| Ees- ja perekonnanimi | Kinnitab, kas töötaja profiil on kehtiv, kontrollige, kas väljad **Nimi** ja **Perekonnanimi** on täidetud.|
| Asend | Kontrollige, kas töötajale on määratud ametikoht. |
| Sünnikuupäev | Kinnitab, kas töötaja profiil on kehtiv, kontrollides, kas väli **Sünnipäev** on täidetud. |
| Hüvitus | Kontrollige, kas töötaja on registreeritud fikseeritud hüvituskavasse. |

Kui üks neist kinnitustest ebaõnnestub, ei saa te töötajat maksevalmis märkida.

Kui väli **Maksmiseks valmis** on **Ei**, näitab see, et peate töötaja profiili lõpuleviimiseks midagi tegema. See ei peata andmete avatud saatmist üheski andmeüksuses. 

## <a name="known-issues"></a>Teadaolevad probleemid

- Funktsiooni **Sujuv töötajate sisenemine** tuleb funktsioonihalduses keelata. Selle funktsiooni kasutamisel ei tööta hüvitise haldamise tööruumi paanid korralikult.
- Töötaja vormil **Palgaarvestuse vahekaart** on grupp **Maksmiseks valmis** on saadaval igale kasutajarollile. 

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
