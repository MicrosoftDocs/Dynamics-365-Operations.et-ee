---
title: Klienditellimuste pealekorje töötlemine kassas
description: See teema kirjeldab funktsioone, mis on saadaval kassarakenduses klienditellimuse pealekorja töötlemiseks.
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e7df580557486c67fc82af19f742bc8002cb881
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231076"
---
# <a name="process-customer-order-pickups-in-pos"></a>Klienditellimuste pealekorje töötlemine kassas

[!include [banner](includes/banner.md)]

Kui [klienditellimus](customer-orders-overview.md) poest pealekorjeks luuakse, saab poe kasutaja kasutada kassarakendust varude korjamise alustamiseks. Kassa käivitab vajadusel lõpliku makse hõivamise. Samuti viib see lõpule pealekorjatud koguste laoseisu ja finantskanded.

Kui olete kaupluse kasutaja, saate sooritada pealevõtmist kasutades kassas toimingut **Tellimuse tagasikutsumine** või **Tellimuse täitmine**. Et teha toiming **Pealekorje** kättesaadavaks, peate kõigepealt järgima ühte järgmistest sammudest.

- Toimingu **Tellimuse tagasikutsumine** kasutamiseks otsige ja valige tellimus, millele järgi tullakse.
- Toimingu **Tellimuse täitmine** kasutamiseks otsige ja valige üks või rohkem tellimuse rida.

Kui valitud tellimus või tellimuse read ei ole selles kaupluses pealekorjeks konfigureeritud või kui tellimus on juba täies mahus peale korjatud, ei ole toiming **Pealekorje** enam saadaval.

![Pealekorje toiming](media/pickupoperation.png)

Rakenduse Microsoft Dynamics 365 Commerce versioonis 10.0.17 ja uuemates versioonides saab funktsiooni **Täiustatud kasutajakogemus pealekorje tellimuste töötlemiseks kassas** läbi Commerce'i peakontori funktsioonihalduse sisse lülitada. Kui funktsioon on välja lülitatud, ei saa kasutajad pealelaadimiskoguseid valida. Vaikimisi on reas tellitud täielik kogus see kogus, mis peale korjatakse. See kogemus võib olla problemaatiline, sest kasutajad võivad tellimuse täitmise kaudu pealekorje teostamisel unustada mõned kaubad pealekorjamiseks valimata.

Funktsioon **Täiustatud kasutajakogemus pealekorje tellimuste töötlemiseks kassas** annab kasutajatel suurema kontrolli pealekorjatavate toodete valimise üle ja nende toodete pealekorjatavate koguste üle. Kasutajad ei pea valima tellimuse täitmise lehel iga müügitellimuse rida enne, kui nad valivad **Pealekorje**. Kuvatakse kõik kaubad, mida saab peale võtta. Kasutajad saavad määrata pealekorje jaoks mitu rida, isegi kui valitakse ainult üks tooterida.

Kui funktsioon **Täiustatud kasutajakogemus pealekorje tellimuste töötlemiseks kassas** on sisse lülitatud ja valite toimingu **Pealekorje** kuvatakse dialoogiaken **Pealekorje**. Seal saate valida kaupu ja koguseid, mis peale võtta. Vaikimisi peetakse mis tahes tellitud kogust, millel laos on komplekteeritud või pakitud olekus varusid, pealekorjeks sobilikuks. Vaikimisi on see kogus seadistatud pealekorje koguseks. Saate muuta sisestatud kogust, eeldusel, et kogus ei ole 0 (null) ega ületa valitud rea avatud (st arveldamata) kogust.

![Pealekorje dialoogiboks](media/pickupselect.png)

Pärast pealekorjeks koguste valimist ja suvandi **Pealekorje** valimist kuvatakse tehingu leht. Kui funtksioon [omnikanali maksed](omni-channel-payments.md) on sees ja failis on eelautoriseeritud krediitkaardimakseid, tuleb makse rakendada.

Kandelehel arvutab süsteem summad, mille tähtaeg on käes, arvutades valitud kaupade lõpptähtaja ja lahutades seejärel kõik varem rakendatud deposiidid või autoriseeritud krediitkaardimaksed. Pealekorje lõpetamiseks peate makset töötlema. Kui kande lehe [ekraanipaigutus](pos-screen-layouts.md) on konfigureeritud sisaldama toimingut **Lõpeta kanne** ja maksmata summa puudub, saate kande ilmsa makseviisi valimata lõpuni viia. Kui toiming **Lõpeta kanne** ei ole saadaval, saate valida lingi **$0.00 maksmata** paanil **Kogusumma**, et viia tehing ilma makseviisi valimata lõpuni.

![Klienditellimuse pealekorje tehingu kandeleht](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Pealekorje ridade või koguste muutmine

Kui peate muutma pealekorje kogust peale seda, kui olete pealekorjatavad kaubad valinud, saate valida suvandi **Määra kogus**. Pealekorju koguseks ei saa valida **0** (null) ega tõsta seda väärtusele, mis ületab tellimuse reale jääva mittearveldamata koguse.. Pealekorje rea eemaldamiseks tehingu korvist valige suvand **Tühista kanne**. Praegune kanne peatatakse ja **Pealekorje** toimingu voog taaskäivitatakse.

Kui funktsioon **Pealekorjega tellimuste töötlemise kasutajakogemuse parandamine kassas** on sisse lülitatud, saavad organisatsioonid lisada kande lehe ekraanipaigutusele nupu toimingu **Pealekorje ridade muutmine** jaoks. Pärast seda, kui olete kassas pealekorje tehingu korvi loonud ja kauba valinud, saate valida käsu **Muuda pealekorje ridu**, kui peate pealekorjatavaid kaupu muutma aga ei taha tühistada kogu tehingut. Kuvatavas dialoogikastis **Muuda pealekorje ridu** saate muuta pealekroje kaupu ja koguseid. Seejärel uuendatakse tehingu korv, nii et see peegeldaks muudatusi.

![Pealekorje kaupade muutmise dialoogiaken](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]