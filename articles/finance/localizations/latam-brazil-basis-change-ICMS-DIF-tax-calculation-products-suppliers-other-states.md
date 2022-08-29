---
title: ICMS-DIF-i maksuarvutuste aluse muutus teiste riikide hankijate toodete puhul
description: See artikkel kirjeldab konfiguratsiooni ICMS-DIF-i maksutüübi arvutusteks juhul, kui fiskaaldokument laekub Brasiilia osariigis Tomati do Sul (RS) või São Mossi (SP).
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218645"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>ICMS-DIF-i maksuarvutuste alusmuutus (topeltbaas) muude riikide hankijate toodete puhul

See artikkel **kirjeldab konfiguratsiooni ICMS-DIF-i** maksutüübi arvutusteks juhul, kui fiskaaldokument laekub Brasiilia osariigis Tomati do Sul (RS) või São Mossi (SP).

Vastavalt riikliku seaduse definitsioonile peab kogutav Imposto sobre Toolulação de Mercias e Serviços (ICMS) järgima järgmist reeglit:

*ICMS koguma* = ([(*Toimingu* summa – *ICMS* allikast) ÷ (1 – *ICMS % sisemine*)] × *ICMS % sisemine*) – *ICMS-i summa allikast*

## <a name="example"></a>Näide

Brasiilia ettevõte RS-i osariigis saab finantsdokumendi hankija ostuks SP osariigis. Ettevõte peab koguma ICMS-i protsendierinevuse RS-i osariigi (18 protsenti) ja SP osariigi (12 protsenti) vahel. Alus tuleb siiski arvutada vastavalt eelnevale reeglile.

- **Toimingu summa:** 1000,00 Brasiilia reaali (R$ 1000,00)
- **ICMS-i osariikides:** R$ 120,00
- **ICMS-i protsent RS-i osariigis:** 18 protsenti
- **ICMS-i kogumine RS-i osariigis:** (\[(1000 - 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Lahendus

ICMS-i (ICMS-DIF) arvutamiseks vastavalt RS-i osariigi reeglitele peate seadistama käibemaksukoodid ja käibemaksugrupi järgmisel viisil:

1. Looge käibemaksukood 12-protsendise ICMS-i saamiseks (teise osariigi puhul). Seda koodi kasutatakse hankijalt saadaoleva maksu summa registreerimiseks.
2. Looge käibemaksukood ICMS-DIF-i kogumiseks. Selle käibemaksukoodi protsent peab olema 18 protsenti (teie enda osariigi puhul), et määrata erinevus 18 protsendi ja 12 protsendi vahel. Saate maksutüübiks seada **ICMS-DIF**. See käibemaksukood tuleb arvutamisparameetrites määratleda järgmiselt:

    - Väljal Päritolu **valige** väärtus **Protsent brutosummast**.
    - **Valige marginaali alusväljal** netosumma **rea kohta**.
    - Määratlege maksustamiskood nii, et selle fiskaalväärtus oleks **3**. Sel viisil luuakse korrigeerimiskanne automaatselt, kui finantsraamatute **moodul** on lubatud.
    - Käibemaksugrupi konfiguratsioonis **valige** **ICMS-DIF-i** käibemaksukoodile valik Kasuta maksu.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Delta maksumäära kasutamine topeltbaasiga ICMS-DIF-i käibemaksukoodide konfigureerimisel

Eelnevalt kirjeldatud sätete kasutamisel arvutatakse **ICMS-DIF-i** käibemaksukood topeltbaasi reeglis. Siiski muutub nominaalmaksu määr 18 protsenti, mis erineb lihtbaasi reeglis 6-protsendisest määrast. See erinevus põhjustab vastuolud fiskaaldokumendis ja maksuaruandluses. Finantsversiooni Microsoft Dynamics 365 10.0.29 **puhul saate lubada (Brasiilia) deltamaksu määra ICMS-DIF-i** **maksukoodis** funktsioonihalduse topelt-alusjuhtumi funktsiooni jaoks vastuolu eemaldamiseks.

- Lisaks eelmise jaotise sammude lõpuleviimisele valige **käibemaksu väljal Käibemaks ICMS 12** **käibemaksukood**.
- Seadistage **ICMS-DIF-i** käibemaksukoodi maksumääraks 18 protsenti. Väli **Protsent/summa** näitab nominaalmaksu määra 6 protsendina.

> [!NOTE]
> ICMS-DIF-i **ja** **ICMS 12** käibemaksukoodid peavad olema määratud samas käibemaksugrupis.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Alusmuutus (topeltbaas) ICMS-DIF-i maksuarvutustes toodete puhul mittemaksustavatele tarbijatele (DI DUAL) teistes riikides

**Lubage (Brasiilia) ICMS-DI MÜÜGITELLIMUSE** **topeltbaas** funktsioonihalduse müügikannete funktsioonis, et toetada ICMS-DIF-i alusmuutust kaubanduses teise osariigi mittemaksusvatele tarbijatele. ICMS-DIF-i käibemaksu näidiskood jõustub müügitellimuse ja vabas vormis arve kannetes.

**Lubage (Brasiilia) ICMS-DITOOL-i topeltbaas IPI-i** **juhtumite** funktsiooni jaoks funktsioonihalduses, et toetada stsenaariume, kus kauplemine teise osariigi mittemaksvate maksumaksjatega on vastutav ka Imposto sobre Produtos Industrialprognoosi (IPI) eest. IPI käibemaksukoodi maksusumma tuvastatakse ja rakendatakse ICMS-DIPILOODI maksubaasis.

- Müügitellimuse või vabas vormis arve päise fiskaalteabe **kiirkaardil** **peab suvand Lõplik kasutaja** olema seatud väärtusele **Jah**.
- Ostutellimuse või hankija arve päise **finantsteabe** **kiirkaardil peab suvand Kasutus** ja tarbimine olema seatud väärtusele **Jah.**
