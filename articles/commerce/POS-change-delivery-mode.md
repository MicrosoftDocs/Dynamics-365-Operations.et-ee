---
title: Tarnerežiimi muutmine kassas
description: Selles teemas kirjeldatakse, kuidas konfigureerida ja kasutada tarnerežiimi muutmise toimingut kassas.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965423"
---
# <a name="change-mode-of-delivery-in-pos"></a>Tarnerežiimi muutmine kassas

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas häälestada ja kasutada funktsiooni „tarnerežiimi muutmine” teie kassakeskkonnas. 

Dynamics 365 Commerce'i versioonis 10.0.10 ja uuemates versioonidess on saadaval toiming  **tarnerežiimi muutmine** (647) kassa ekraanipaigutustele lisamiseks.

Tarnerežiimi muutmise funktsioon võimaldab muuta ühe või mitme saadetise konfigureeritud müügiridade tarnerežiimi kassakandel. Commerce'i varasemates versioonides tuli läbida kogu **Saada kõik** ja **Saada valitud** konfiguratsioonivoog, kui sooviti muuta tarneviisi olemasoleval real, mis oli saatmiseks konfigureeritud. See protsess oli aeganõudev ja võis põhjustada juhuslikke muudatusi selle rea tarnepäritolus või tarnekuupäevades. Uus funktsioon pakub alternatiivset viisi nende müügiridade tarnerežiimi tõhusaks uuendamiseks.

Lisateavet selle kohta, kuidas lisada kassanuppude ruudustiku nupule toimingut, vaadake teemast [Kassa ekraanipaigutused](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

Kui see funktsioon on kassas konfigureeritud, valige **Muuda tarnerežiimi**, teile kuvatakse loendileht, mis võimaldab teil valida selle kande read, mille tarnerežiimi soovite muuta. Saate valida ainult osad või kõik read või väljuda muudatusi tegemata. Varem saadetiseks konfigureeritud müügiread on loendi ainsad read, mida saate muuta. Kui soovite muuta komplekteerimise või tarnimiseks järeletulemisena määratud rida saadetiseks, peate kasutama toimingut **Saada kõik** või **Saada valitud**. Seevastu kui soovite muuta saadetisena määratud rida komplekteerimiseks või tarnimiseks järeletulemiseks, peate kasutama toiminguid **Komplekteeri kõik**, **Komplekteeri valitud**, **Järeletulemine kõigile** või **Järeletulemine valitutele**.

Kui olete valinud muudetavad read, klõpsake valikul **Muuda tarnerežiimi**, et saaksite valida tarnerežiimi suvandeid. Kui valisite muutmiseks mitu rida, kuvab kassa ainult need tarnerežiimid, mis on konfigureeritud kõigi valitud toodete puhul lubatuks. Tarnerežiime saab konfigureerida nii, et need toetaksid kindlaid tooteid ja tarneaadresse. Kui on üks tarnerežiim on lubatud ühe toote ja aadressi kombinatsioonile, kuid ei ole lubatud teisele, ei ole see tarnerežiim saadaval. Kui soovite valida ühele tootele tarnerežiimi, mis ei ole toetatud teise toote puhul, peate tõenäolisel valima ned read ükshaaval ja muutma tarnerežiimi iga rea kohta eraldi.  

Pärast uue tarnerežiimi valimist kuvatakse kandeleht. Uute tarnerežiimi valikute ülevaatamiseks valige kannete loendist vahekaart **Tarne**.

## <a name="additional-resources"></a>Lisaressursid

[Kõnekeskuse tellimuste loomine](tasks/create-call-center-orders.md)

[Kandemeilide kohandamine tarneviisi järgi](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]