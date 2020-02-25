---
title: ER-i sihtkoha tüübi e-post
description: Sellest teemast leiate teatevt, kuidas konfigureerida e-post sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019726"
---
# <a name="EmailDestinationType">Meili sihtkoht</a>

[!include [banner](../includes/banner.md)]

Saate konfigureerida faili sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks. Sihtkoha sätte põhjal tarnitakse loodud dokument e-kirja manusena.

Määrake valiku **Lubatud** väärtuseks **Jah** väljundfaili saatmiseks meiliga. Kui see valik on lubatud, saate määrata meili adressaadid ning redigeerida meilisõnumi teemat ja kehateksti. Saate seadistada meilide teema ja kehateksti jaoks püsiteksti või kasutada meilitekstide loomiseks elektroonilise aruandluse [valemeid](er-formula-language.md), et dünaamiliselt luua e-kirja tekste. 

Elektroonilise aruandluse meiliaadresside konfigureerimiseks on kaks võimalust. Konfiguratsiooni saab lõpule viia samamoodi, nagu prindihalduse funktsioon seda lõpule viib, või saate meiliaadressi lahendada, kasutades viitena ER konfiguratsioonile valemi kaudu.

[![Meili sihtkoha lubamine](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Meiliaadressi tüübid

Kui klõpsate valikut **Redigeeri** välja **Saaja** või **Koopia** puhul, kuvatakse dialoogiboks **Meili saaja**. Seejärel saate valida kasutatava meiliaadressi tüübi. **Konfiguratsiooni e-posti** ja **Prindihalduse** e-posti tüübid on praegu toetatud.

[![Meilitüübi valimine](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Prindihaldus

Kui valite meilitüübi **Prindihaldus**, saate sisestada väljale **Saaja** fikseeritud meiliaadressid. 

[![Fikseeritud e-posti aadresside konfigureerimine](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Fikseerimata meiliaadresside kasutamiseks tuleb valida failisihtkohaks meiliallika tüüp. Toetatakse järgmisi väärtusi: **Klient**, **Hankija**, **Potentsiaalne klient**, **Kontakt**, **Konkurent**, **Töötaja**, **Kandidaat**, **Potentsiaalne hankija** ja **Keelatud hankija**. Pärast meiliallika tüübi valimist avage välja **Meiliallika konto** kõrval oleva nupu abil vorm **Valemi kujundaja**. Saate kasutada seda vormi, et lisada valem, mis tagastab käitusaja, valitud allika tüübi **osapoole konto** töödeldud dokumendilt e-posti sihtkohta.

[![E-posti allika konto konfigureerimine](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Valemid on ER-i konfiguratsiooni põhised. Sisestage väljale **Valem** dokumendipõhine viide kliendi või hankija osapoole tüübile. Tippimise asemel võite otsida üles andmeallika sõlme, mis tähistab kliendi või hankija kontot, ja klõpsata siis valemi värskendamiseks nuppu **Lisa andmeallikas**. Näiteks kui kasutate **ISO 20022 kreeditülekande** konfiguratsiooni, tähistab hankija kontot sõlm `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Kui sisestate stringi väärtuse, näiteks `"DE-001"`ja salvestate valemi, saadetakse meilisõnum hankija kontaktisikule, **DE-001**.


[![Valemikoostaja leht](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![E-posti allika konto konfigureerimine](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigureerimismeil

Kasutage seda meilitüüpi, kui kasutataval konfiguratsioonil on andmeallikates sõlm, mis tagastab **meiliaadressi**. Õigesti vormindatud meiliaadressi saamiseks saate kasutada valemikujundajas sisalduvaid andmeallikaid ja funktsioone. Näiteks kui kasutate **ISO 20022 kreeditülekande** konfiguratsiooni, tähistab hankija konto kontaktisiku meiliaadressi sõlm `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![E-posti allika aadressi konfigureerimine](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Valemikoostaja elektroonilises aruandluses (ER)](general-electronic-reporting-formula-designer.md)
