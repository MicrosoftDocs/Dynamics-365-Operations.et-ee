---
title: Töötlemise seadistamine ja käivitamine lihtsa ER-i eksporditava vormingu kutsumiseks, et luua Exceli aruanne
description: See teema toob näite, mis kirjeldab, kuidas seadistada ja kasutada elektroonilisi teateid.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a5fd466c98e0855f7a33929eeee42b9147d26ba19780b4ae7c8eb895ac27ea5e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737673"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Töötlemise seadistamine ja käivitamine lihtsa ER-i eksporditava vormingu kutsumiseks, et luua Exceli aruanne

[!include [banner](../includes/banner.md)]

Kui olete oma ER-i vormingu loonud, vastendanud selle andmeallikatega ja selle lõpule viinud, saate selle käivitada, kasutades tööruumi **Elektrooniline aruandlus**. Peale aruande loomist saate selle lokaalselt salvestada.

Aruandluse protsessi järgmiste aspektide kontrollimiseks peate seadistama elektroonilise sõnumi töötlemise:

- Logima teabe selle kohta, kes aruande lõi.
- Logima teabe selle kohta, millal aruanne loodi.
- Salvestama eelmiste perioodide jaoks loodud aruanded.

Järgnev näide näitab, kuidas saate seadistada elektroonilise sõnumside, et luua aruanne, mis põhineb eksporditaval ER-i vormingul Microsoft Excel jaoks. Kui soovite seda näidet järgida, peab ER-i Exceli ekspordivorming juba olema loodud, andmeallikatega vastendatud ja lõpule viidud. Samuti peab elektroonilise sõnumside jaoks numbriseeria juba seadistatud olema.

Kui koostate töötlemist, on kasulik, kui määratlete esmalt töötlemise tegevused ja olekud, mida hakatakse seadistama. Järgmisel joonisel on näidatud, kuidas töötlemine selle näite korral välja näeb.

![Töötlemise skeem](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Sõnumite olekute loomine

1. Avage **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumite olekud**.
2. Looge järgmised sõnumite olekud:

    - Uus
    - Ettevalmistatud
    - Loodud

    ![Sõnumite olekud](media/message-statuses.png)

3. Real oleku **Uus** jaoks valige märkeruut **Luba kustutamine**, et kasutajad saaksid selle olekuga sõnumid kustutada.

## <a name="create-additional-fields"></a>Lisaväljade loomine

1. Avage **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Lisaväljad**.
2. Lisage lisaväli ja selle väärtused.
3. Määrake suvandi **Kasutaja redigeerimine** väärtuseks **Jah**, et kasutajad saaksid seda välja redigeerida.

![Lisaväljad](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Sõnumi töötlemise tegevuste loomine

Selle näite jaoks loote järgmised sõnumi töötluse tegevused:

- **Loo sõnum**
- **Värskenda ettevalmistatuks**
- **Loo aruanne**
- **Värskenda esialgsele olekule** (valikuline)

Toimige rakendusega rakenduse loomiseks järgmiselt.

1. Avage **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumi töötlemise tegevused**.
2. Looge tegevus nimega **Loo sõnum**. Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Loo sõnum**.
3. Looge tegevus nimega **Värskenda ettevalmistatuks** ja määrake järgmised väljad:

    - Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Kasutaja töötlemine sõnumi tasemel**.
    - Kiirkaardil **Algolekud** väljal **Sõnumi olekud** valige **Uus**.
    - Kiirkaardil **Tulemi olekud** väljal **Sõnumi olekud** valige **Ettevalmistatud**. Väljal **Vastuse tüüp** sisestage **Edukalt täidetud**.

4. Looge tegevus nimega **Loo aruanne** ja määrake järgmised väljad:

    - Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Elektroonilise aruandluse eksportimine**. Väljal **Vormingu vastendamine** valige eksporditav ER-i vorming. Valikud on **Excel**, **XML**, **JSON**, **Tekst** ja **Muu**.
    - Kiirkaardil **Algolekud** väljal **Sõnumi olekud** valige **Ettevalmistatud**.
    - Kiirkaardil **Tulemi olekud** väljal **Sõnumi olekud** valige **Loodud**. Väljal **Vastuse tüüp** sisestage **Edukalt täidetud**.

    ![Aruande tegevuse loomine](media/generate-report-action.png)

5. Valikuline: et kasutajad saaksid aruannet mitu korda luua, saate luua tegevuse **Värskenda esialgsele olekule** ja määrata järgmised väljad:

    - Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Kasutaja töötlemine sõnumi tasemel**.
    - Kiirkaardil **Algolekud** väljal **Sõnumi olekud** valige **Loodud**.
    - Lisage kiirkaardil **Tulemolekud** eraldi rida kummagi sõnumioleku jaoks (**Ettevalmistatud** ja **Uus**). Valige mõlema rea puhul välja **Vastuse tüüp** sätteks **Edukalt käivitatud**.

## <a name="electronic-message-processing"></a>Elektronsõnumi töötlemine

Selles näites tuleb kõik tegevused seadistada nii, et need käivituks eraldi. Eeldatakse, et kasutaja käivitab iga toimingu.

1. Avage **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Elektronsõnumi töötlemine**.
2. Lisage oma töötlemisele kirje ning lisage kõik eelnevalt määratletud tegevused ja lisaväli.
3. Valikuline: määratlege kiirkaardil **Turberollid** oma töötlemise jaoks turberollid, et piirata juurdepääsu kindlale aruandlusele.
4. Avage **Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumid**.
5. Valige **Uus**, et luua uus sõnum. Selles punktis saate lisada kuupäevi ja kirjelduse. Saate vajaduse korral värskendada ka lisavälja väärtust.

    ![Elektronsõnumi loomine](media/create-electronic-message.png)

    Kiirkaardil **Tegevuste logi** olev ruudustik täidetakse automaatselt kõigi sõnumiga tehtud tegevuste logiga.

    Saate nüüd sõnumi oleku kas kustutada või seda värskendada. 

6. Sõnumi oleku värskendamiseks valige suvand **Värskenda olekut**. Valige väljal **Uus olek** suvand **Ettevalmistatud** ja seejärel valige **OK**.

    ![Sõnumi oleku värskendamine](media/update-status.png)

    Teate olek uuendatakse olekuks **Ettevalmistatud**.

7. Aruande loomiseks valige käsk **Loo aruanne**.

    Aruanne luuakse ning sõnumi olekut ja tegevuste logi värskendatakse.

8. Loodud aruande vaatamiseks valige lehe paremas ülanurgas nupp **Manus** (kirjaklambrisümbol).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
