---
title: Maksmiseks valmis
description: See teema näitab, kuidas märkida töötaja maksmiseks valmis rakenduses Dynamics 365 Human Resources.
author: marcelbf
ms.date: 08/25/2021
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
ms.openlocfilehash: 825aa327cc1530675fad57be6fc1b4313f0cf998
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068966"
---
# <a name="ready-to-pay"></a>Maksmiseks valmis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Kui soovite märkida töötaja maksmiseks valmis olevaks, peate esmalt lubama funktsioonihalduses **(Eelvaate) palgaarvestuse integratsiooni** funktsiooni. Lisateavet funktsioonide eelversioonide lubamise kohta vt [Funktsioonide haldamine](hr-admin-manage-features.md).

See funktsioon võimaldab personalispetsialistidel mõista, millised töötajad on palgaarvestuseks valmis ja mis nõuavad tegevust enne, kui kolmandast osapoolest palgapakkuja seda tarbib.

## <a name="mark-employee-as-ready-to-pay"></a>Märgi töötaja maksmiseks valmis

Töötaja teabe kogumine ja kontroll võib olla aeganõudev ja täis rohkeid tõrkeid. Pakkudes inimressursside spetsialistidele võimalust töötajate teabe ülevaatamiseks ja selle lihtsaks uuendamiseks, aitab Dynamics 365 Human Resources vähendada palga töötlemise lõpetamiseks kulunud aega.

Töötaja staatuse muutmiseks kui "valmis makseks" tehke järgmist.

1. Avage **Tasuhaldus**. Tööruumis on kaks paani: 
    - **Töötajad on maksmiseks valmis**
    - **Töötajad, kes pole maksmiseks valmis**
    ![Tasuhalduse tööruum.](./media/hr-ready-to-pay-1-workspace.png)

2. Valige paani **Töötajad, kes pole maksmiseks valmis**.

3. Valige valideeritavad töötajad. **Palgaarvestuse vahekaardil** grupis **Maksmiseks valmis** valige **Kontrolli**.
    ![Kontrolli töötajaid.](./media/hr-ready-to-pay-2-validate.png)

4. Tulemuste ülevaatamiseks valige grupis **Maksmiseks valmis** **Palgaarvestus vahekaardil** valik **Tulemused**.

## <a name="validation"></a>Valideerimine

Enne töötaja maksevalmiduse märkimist kinnitatakse töötaja profiili täielikkus.

![Kinnita tulemused.](./media/hr-ready-to-pay-3-results.png)

| Valideerimine | Details |
| --- | --- |
| **Aadressi eesmärgi parameeter** | Kinnitab, et parameeter **Kasuta palgaarvestuse aadresse** oleks valitud. |
| **Palgaarvestuse aadress** | Kinnitab, et töötaja profiilil on vähemalt üks aadress, mille eesmärk on **Palgaarvestuse elukoht** või **Palgaarvestuse töökoht**, ja iga eesmärgi jaoks on ainult üks aadress. |
| **Töösuhe** | Kinnitab, et töötajal oleks vähemalt üks tööleping (praegune, eelmine või tulevane). |
| **ID-number** | Kinnitab, et parameeter **Kasuta palgatöötluses identifitseerimistüüpe** oleks **Jah** lehel **Inimressursid** ja kas parameetris näidatud identifitseerimistüüp on täidetud töötaja profiilis. |
| **Ees- ja perekonnanimi** | Kinnitab, et väljad **Nimi** ja **Perekonnanimi** on täidetud.|
| **Asend** | Kinnitab, et töötajale oleks määratud ametikoht. |
| **Sünnikuupäev** | Kinnitab, et **Sünnipäeva** väli oleks täidetud |
| **Hüvitus** | Kinnitab, et töötaja oleks registreeritud fikseeritud kompensatsioonikavasse. |

Kui üks neist kinnitustest ebaõnnestub, ei saa te töötajat maksevalmis märkida.

Kui väli **Maksmiseks valmis** on **Ei**, näitab see, et peate töötaja profiili lõpuleviimiseks midagi tegema. See ei peata andmete avatud saatmist üheski andmeüksuses. 

## <a name="process-automation"></a>Protsesside automatiseerimine

Saate automatiseerida kõikide töötajate kinnitamise [Protsessi automatiseerimise](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation)abil. **Kompensatsiooni halduse** tööruumis minge **Lingid** \> **Parameetrid** \> **Prostsessi automatiseerimine**.

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
