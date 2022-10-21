---
title: Arvehõive lahenduse vastendamise reeglid
description: See artikkel annab teavet arve hõivamise lahenduse vastendamisreeglite häälestuse kohta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690981"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Arvehõive lahenduse vastendamise reeglid

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Vastendamisreeglid toovad põhiandmed Microsoft Dynamics 365 Finantside või ettevõtte ressursiplaanimise (ERP) süsteemist. Pärast vastendamisreeglite seadistamist tuletatakse finantside hankijaarvete loomiseks vajalik teave. Vastendamisreeglite kasutamisel kontrollib ostureskontro (AP) ametnik olekut, selle asemel et täita käsitsi kõik puuduvad väljaväärtused.

Vastendamisreegli tüüpe on nelja tüüpi:

- Juriidiline isik
- Hankija konto
- Kaup
- Kulutüüp

## <a name="manage-mapping-rules-by-using-the-app"></a>Vastendamisreeglite haldamine rakenduse abil

Vastendamisreeglite haldamiseks rakenduse abil valige **häälestus**. Vastendamisreegli **häälestuse** vahekaardil on neli valikut:

- Juriidiline isik 
- Hankija konto 
- Kauba vastendamine 
- Kulutüüp

Näiteks valite suvandi Juriidilise **isiku vastendamisreeglid**. Juriidilise isiku kood tuvastatakse ettevõtte nime, aadressi ja maksu registreerimisnumbri abil. Reegli puhul, mille nimi on **LE-USPM**, kui ettevõtte nimi sisaldab teksti "Contoso Contoso Contosocs USA," **on juriidilise isiku kood USPM**.

Lehel kuvatakse kõik aktiivsed vastendamisreeglid. Passiivsete vastendamisreeglite vaatamiseks valige **juriidilise isiku aktiivse vastendamise reeglid** **ja seejärel valige juriidilise isiku passiivse vastendamise reeglid**.

Järgmised tegevused on saadaval reeglite vastendamiseks.

### <a name="create-a-mapping-rule"></a>Vastendusreegli loomine

Vastendamisreegli loomiseks saate kasutada kahte meetodit:

- Valige **uue** vastendamisreegli loomiseks uus. Seejärel sisestage vastendamisreegli teave. Reeglinime **väärtus** peab olema iga vastendamisreegli tüübi puhul kordumatu.
- Kui valite olemasoleva vastendusreegli, **muutub nupp** Kopeeri kättesaadavaks. Valige see ja seejärel valige **kuvatavas dialoogiboksis OK**. Vastendamisreegel luuakse valitud reegli dubleerimisel.

### <a name="edit-a-mapping-rule"></a>Vastendamisreegli redigeerimine

Vastendusreegli redigeerimiseks valige väli ja muutke väärtust.

### <a name="activatedeactivate-mapping-rules"></a>Vastendamisreeglite aktiveerimine/inaktiveerimine

Ühe või mitme vastendamisreegli desaktiveerimiseks valige need leheküljel **Aktiivsed vastendamise** reeglid ja seejärel valige desaktiveeri **.** Reeglid teisaldatakse aktiivsete vastendusreeglite **lehelt passiivsete** vastendamisreeglite **lehele**.

Vastendusreeglite aktiveerimiseks valige need leheküljel Passiivsed **vastendamisreeglid** ja seejärel valige **aktiveeri**.

### <a name="remove-mapping-rules"></a>Vastendamisreeglite eemaldamine

Vastendamisreeglite eemaldamiseks valige need ja seejärel kustuta **.**

### <a name="check-for-conflicts"></a>Kontrolli konfliktide tegemist

Kui kahel **vastendamisreeglil** **on** sama juriidiline isik ja hankija konto väärtused, **kuid** erineva kauba nime väärtused, tuvastati konflikt ja vastendamisreeglit ei looda ega värskendata.

## <a name="importexport-mapping-rules-from-excel"></a>Vastendamisreeglite importimine/eksportimine Excelist

Exceli lisandmoodulit saab kasutada partii reeglite haldamiseks. Valikud on järgmised:

- Laadige alla Exceli mall.
- Ekspordi Excelisse.
- Importige Excelist.

### <a name="download-an-excel-template"></a>Exceli malli allalaadimine

Exceli malli allalaadimiseks valige laadi **mall alla**. Seejärel valige malli kaasamiseks väljad.

### <a name="export-to-excel"></a>Excelisse eksportimine

Saate eksportida kahel viisil:

- Valige **Ava Excelis Online,** et avada fail Excelis. Seejärel saate faili võrgus redigeerida. Kui olete lõpetanud, valige **Salvesta**. Kõik teie muudatused salvestatakse vastendamise **reeglilehel**.
- Valige **vastendamisreegliid** sisaldava Exceli faili allalaadimiseks allalaadimise tööleht. Seejärel saate faili redigeerida. Kui olete lõpetanud, valige uuendatud **töölehe üleslaadimiseks** suvand Impordi Excelist.

### <a name="import-from-excel"></a>Impordi Excelist

1. Valige **suvand Impordi Excelist**, et importida andmeid XLSX-failist. Saate importida ka komaga eraldatud väärtustest (CSV) või XML-failidest. Enne importimist peaksite otsustama, kas duplikaadid on lubatud.
2. Valige **vastendus** ülevaate vastendamine, et vaadata üle atribuutide vastendamine ja otsustada, kas see on õige. Vastendamissuhet saate muuta.
3. Kui olete importimise lõpetanud, valige **importimise käivitamiseks** suvand Lõpeta import.
4. Saate valida **Jälita protsessi** impordiprotsessi edenemise jälgimiseks.

    Impordi olek uuendatakse olekust **Lõpeta** sõelumine **·**, seejärel **teisenduseni** ja lõpuks lõpetatud **olekuks**.

Kui impordiprotsess on lõpule viidud, kuvatakse edumiste, osaliste tõrgete, vigade ja kogu töödeldud statistika.
