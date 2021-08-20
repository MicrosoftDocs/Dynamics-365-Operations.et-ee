---
title: SEPA otsedeebeti loa seadistamine
description: Ühtse euromaksete piirkonna (Single Euro Payment Area, SEPA) otsekorraldus võimaldab kreeditoril võtta vahendeid kliendi pangakontolt eeldusel, et klient on andnud kreeditorile allkirjastatud loa.
author: ShivamPandey-msft
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4f63f88daf65676104384a2d612aa415ae6533044ea52ce85947f75ad876ced
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758917"
---
# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA otsedeebeti loa seadistamine

[!include [banner](../includes/banner.md)]

Ühtse euromaksete piirkonna (Single Euro Payment Area, SEPA) otsekorraldus võimaldab kreeditoril võtta vahendeid kliendi pangakontolt eeldusel, et klient on andnud kreeditorile allkirjastatud loa. Kliendi allkirjastatud luba volitab kreeditori makset koguma ja annab kliendi pangale juhise see välja maksta. See teema on korraldatud nii, et näidata SEPA otsedeebeti mandaatide seadistamise protsessi.

## <a name="prerequisites"></a>Eeltingimused
Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

| Kategooria       | Eeltingimus                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Riik/regioon | Juriidilise isiku peamine aadress peab olema järgmistes riikides/regioonides: Austria, Belgia, Saksamaa, Hispaania, Prantsusmaa, Itaalia või Holland. |

1. Seadistage otsedeebeti lubade jaoks numbriseeria. Igal otsedeebeti loal peab olema unikaalne number. Looge lehel **Numbriseeriad** otsekorralduse lubade numbriseeria. Selle identifikaatoriga määrate numbriseeria otsekorralduse lubade süsteemile lehel **Müügireskontro parameetrid**.

2. Müügireskontro parameetrite seadistamine otsedeebeti mandaatidele Kasutage lehte **Müügireskontro parameetrid**, et otsedeebeti lubade jaoks parameetreid seadistada. Parameetrite seadistamiseks muutke vahekaardil **Otsedeebet** muutke vaikeparameetreid vastavalt vajadusele. Seejärel vahekaardil **Numbriseeriad** värskendage välja **Otsedeebeti loa ID** varasemalt seadistatud numbriseeriaga.

3. Otsedeebeti lubade makseviisi seadistamine Peate otsedeebeti lubade jaoks maksemeetodi seadistama. Selle makseviisiga saate teha päringuid arvete kohta, mille jaoks loote otsekorralduse makseid. Seadistage lehel **Makseviisid** makseviis. Otsekorralduse lubadele makseviisi seadistamiseks tuleb järgida makseviisi puhul neid lisajuhiseid.

-   Tehke väljal **Makse tüüp** valik **Elektrooniline makse**.
-   Valikuline: kui ootate, et igal kliendil on mitu luba, valige väljal **Periood** suvand **Arve**. Sel juhul luuakse iga arve kohta eraldi makse ja iga makse kasutab arve jaoks määratud luba.
-   Valige **Nõua luba** maksete loomiseks otsekorralduse lubadega. Valik **Nõua luba** on saadaval ainult juhul, kui teete valiku **Elektrooniline makse** väljal **Makse tüüp**.

Lisaressursid

[SEPA otsekorralduse ülevaade](sepa-direct-debit-overview.md) 

[Kliendi jaoks otsekorralduse loa loomine](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]