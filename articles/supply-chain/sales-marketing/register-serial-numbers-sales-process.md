---
title: Järjestatud kaupadega töötamine
description: See teema selgitab, kui registreerida müügiprotsessi ajal seerianumbreid saatelehtedel või arvetel. See funktsioon on abiks, kui ettevõte soovib hõivata seerianumbreid teenindus‑ ja garantiieesmärkidel, kuid ei pea seerianumbreid varude sissetulekust väljaminekuni alles hoidma.
author: omulvad
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e4f5a04e85d3cc34111b7421fbff6cbde413b7c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001520"
---
# <a name="working-with-serialized-items"></a>Järjestatud kaupadega töötamine

[!include [banner](../includes/banner.md)]

See teema selgitab, kui registreerida müügiprotsessi ajal seerianumbreid saatelehtedel või arvetel. See funktsioon on abiks, kui ettevõte soovib hõivata seerianumbreid teenindus‑ ja garantiieesmärkidel, kuid ei pea seerianumbreid varude sissetulekust väljaminekuni alles hoidma.

Paljud ettevõtted soovivad seerianumbreid hõivata teenindus‑ ja garantiieesmärkidel ega pea seerianumbreid varude sissetulekust väljaminekuni alles hoidma. Selliste stsenaariumide puhul saate seerianumbrid toodete müümisel saatelehtedele või arvetele registreerida. Kui tooted hiljem tagastatakse, saate iga toote arvega siduda, et näha, kas toode on müüdud, ja kas teenindus- või garantiikohustused on kehtivad.

Müügiprotsessi seerianumbrite lubamiseks valige leheküljel **Jälgimisdimensiooni grupid** suvand **Aktiivne müügiprotsessis**. Järgmised sündmused toimuvad Supply Chain Managementis:
-   Kiirkaardil **Seerianumbrid** valitakse suvand **Seerianumbri juhtimine**. Kui see suvand on valitud, tuleb saatelehel või arvel iga kauba kohta üks seerianumber registreerida.
-   Kõik seerianumbri jälgimisdimensiooni grupi valikud eemaldatakse, välja arvatud suvand **Määramata väljaminekud lubatud**. Saate valida suvandi **Määramata väljaminekud lubatud** seerianumbri kontrollimise tühistamiseks ning toodete pakkimise ja arvete esitamise lubamiseks seerianumbreid registreerimata.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Millal tuleb müügiprotsessi ajal seerianumbrid registreerida?
Seerianumbrid saate registreerida kas müügitellimuse saatelehel või arvel. Kui koostate arve järjestatud kaubale, mis lähetati koos saatelehega, saate valida, millised saatelehe seerianumbrid arvele lisada. Registreeritud seerianumbrite arv ei tohi ületada lähetatud kaupade kogust. Osalise arve loomisel saate valida väiksema arvu järjestatud üksusi, kui saatelehel registreeriti. Saatelehe või arve printimisel kaasatakse registreeritud seerianumbrid.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Kas saan seerianumbreid sisestada skannides või pean need tippima?
Seerianumbreid saate sisestada nii skannides kui ka tippides. Skanneri kasutamisel määrab skannimisrežiim, kas seerianumbrid lisatakse saatelehel olevasse seerianumbrite loendisse või eemaldatakse sealt. Kui soovite skannida seerianumbreid näiteks käeshoitava vöötkoodiskanneriga, seadistage skanner pärast seerianumbrit saatma käsku Sisesta või TAB. See käsk näitab andmevoo lõppu. Vastasel juhul tuleb iga seerianumbri skannimise järel klaviatuuril sisestusklahvi Enter või TAB vajutada.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Kui luban müügiprotsessi seerianumbrid, kas pean registreerima kõik seerianumbrid kõigile kaupadele?
Seerianumbrite registreerimine kõigi saatelehel või arvel olevate kaupade puhul sõltub tootele määratud jälgimisdimensiooni grupi seadistusest. Kui lubate müügiprotsessi seerianumbrid, valitakse automaatselt suvand **Seerianumbri juhtimine**. Seejärel peate registreerima ühe seerianumbri või loetamatu numbri puhul tühja väärtuse iga saatelehel või arvel oleva kauba kohta. Kui te ei soovi iga kauba seerianumbrit nõuda, valige kaubale määratud jälgimisdimensiooni grupis suvand **Määramata väljaminekud lubatud**. Seejärel saate registreerida lähetatava kauba kogusest vähem seerianumbreid. Kui registreerite lähetatavate kaupade kogust ületava arvu seerianumbreid, ei saa saatelehte või arvet sisestada.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Kas saan registreerida seerianumbrid osaliste arvete ja osaliste saadetiste jaoks?
Saate luua müügitellimustele osalisi arveid ja saatelehti ning registreerida ainult nendel arvetel ja saatelehtedel sisalduvate kaupade seerianumbrid. Kui soovite luua osalise arve ja müügitellimusel on rohkem kui üks saateleht, saate lisada rohkem kui ühe saatelehe seerianumbrid. Kuid saatelehti, millele pole lisatud kõiki seerianumbreid, võib olla ainult üks. Näiteks kui teil on kolm saatelehte ja igal saatelehel on kaks järjestatud kaupa, ei saa luua osalist arvet iga saatelehe ühele kaubale.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Mida teha siis, kui seerianumber pole loetav?
Kui seerianumbrit ei saa lugeda ega skannida, saate luua kaubale tühja rea, klõpsates leheküljel **Seerianumbrid** valikut **Pole loetav**. Kui seerianumber muutub hiljem kättesaadavaks, saate arvet või saatelehte uuendada. Lisateavet vt järgmisest jaotistest „Kas saan müügitellimusele registreeritud seerianumbreid parandada või muuta?”

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Kas saan müügitellimusele registreeritud seerianumbreid parandada või muuta?
Jah, saate seerianumbreid parandada, kui täidetud on järgmised tingimused.
-   **Arved** – saate muuta seerianumbreid kaupade puhul, mille eest te pole veel arvet esitanud. Sellega uuendatakse ka saatelehte. Kui müügitellimuse rida on parandatud negatiivse koguse registreerimisega, ei saa müügitellimuse rea seerianumbreid muuta.
-   **Saatelehed** – te ei saa osaliselt parandada järjestatud kaupu sisaldavat saatelehe rida. Peate tühistama terve rea koguse. Kui saateleht on tühistatud või parandatud, ei pea te samade järjestatud kaupade jaoks uut saatelehte luues tühistatud seerianumbreid uuesti registreerima. Kasutatakse registreeritud numbreid.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Kas saan vaadata kindla saatelehega koos lähetatud või teatud arvel olevaid seerianumbreid?
Jah, saate käivitada päringu saatelehe töölehe rea või arve töölehe rea kohta, et vaadata kõiki dokumendis sisalduvaid seerianumbreid.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Kas saan vaadata laos olevaid järjestatud kaupu?
Ei, te ei saa laos olevaid järjestatud kaupu vaadata, kuna seerianumbrid registreeritakse kaupadele alles siis, kui need on müüdud.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Kas saan registreerida tegeliku kaaluga kaupade seerianumbrid?
Ei, müügiprotsessi ajal ei saa te tegeliku kaaluga kaupade seerianumbreid registreerida. Peale selle ei saa määrata toodet, mis on seadistatud tegeliku kaaluga kaubana, ainult müügiprotsessi ajal seerianumbreid kasutavasse jälgimisdimensiooni gruppi.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Kas saan seerianumbreid jaemüügikohas registreerida?

Jah, kassas (POS) palutakse kasutajal seerianumber sisestada, kui kasutaja müüb kauba, mis on määratud ainult müügiprotsessi ajal seerianumbreid kasutavasse jälgimisdimensiooni gruppi.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Millised turberollid on müügiprotsessi ajal seerianumbrite registreerimisel nõutavad?
See funktsioon on saadaval kõigile rollidele, kes saavad hallata müügi saatelehti ja arveid. Järgmised ülesanded lasevad töötajatel seerianumbreid parandada ja loetamatuid või skannimatuid seerianumbreid tühjade kirjetena registreerida.
-   Seerianumbrite paranduse haldamine
-   Loetamatute seerianumbrite registreerimise haldamine







[!INCLUDE[footer-include](../../includes/footer-banner.md)]