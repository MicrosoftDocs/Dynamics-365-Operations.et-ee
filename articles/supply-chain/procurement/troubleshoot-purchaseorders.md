---
title: Ostutellimuste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada ostutellimustega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007487"
---
# <a name="troubleshoot-purchase-orders"></a>Ostutellimuste tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada ostutellimustega töötamisel tekkivaid probleeme.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Tegevuse saab lõpule viia alles pärast reanumbri täielikku ärajagamist.

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Kui ostutellimused imporditakse andmehalduse kaudu, ei järgita ostutellimuse reanumbrite puhul süsteemiparameetrites määratletud sammu.

### <a name="issue-description"></a>Probleemi kirjeldus

Vaikimisi ei kasutata andmeüksuse *Ostutellimuse read V2* kaudu imporditud ostutellimuse ridade jaoks automaatselt loodud reanumbrite puhul süsteemiparameetrites määratud süsteemi reanumbri sammu. Kui loote ostutellimuse käsitsi ja lisate ridu kasutajaliidese kaudu (UI), siis on reanumbrite samm õige. Kuid kui kasutate andmehaldusraamistikku (DMF), ei ole nende samm õige.

See probleem ilmneb seetõttu, et kui impordite ridu DMF-i kaudu ja reanumbrid ei ole imporditud üksuses juba määratud, kasutab süsteem nende määramiseks DMF-i meetodit. See meetod suurendab reanumbreid alati ühe võrra.

### <a name="issue-workaround"></a>Probleemi lahendus

Veenduge, et soovitud reanumbrid oleksid ostutellimuse ridade importimisel andmeüksuse reanumbrite väljades juba olemas. Sel juhul ei kirjuta DMF reanumbreid üle.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Vaikemaksugruppi ja vaikeskontot ei täideta arve konto põhjal.

Kui kasutate arve kontot, mis erineb kliendi kontost, siis ei täideta ostutellimuse loomisel arvekonto põhjal vaikemaksugruppi ja -skontot.

Selline käitumine on nii kavandatud. Maksugrupi ja skontode vaikeväärtused ning muu hinnateave põhineb kliendi kontol, mitte arve kontol.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Ostutellimuse kinnitamise ajal kuvatakse tõrge „Objekti viide ei ole seatud” või hankija arve sisestamisel ilmneb erand „Kutsumise sihtmärgi puhul ilmnes erand”.

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Üks või mitu arvestuse jaotust on kas üle- või alajaotatud.

### <a name="issue-description"></a>Probleemi kirjeldus

Kuvatakse järgmine tõrge: „Üks või mitu arvestuse jaotust on kas üle- või alajaotatud”.

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kas saan kuvada ainult minu loodud ostutellimusi?

See funktsioon pole praegu saadaval.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kas ma saan reserveerida varusid ja luua kandeid ostutellimusel registreeritud varude põhjal?

### <a name="issue-description"></a>Probleemi kirjeldus

Isegi kui kaupade olek on ostutellimusel *Registreeritud*, saate varusid siiski reserveerida. Teisisõnu saate luua kandeid registreeritud varude põhjal.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Looge ostutellimus.
2. Registreerige ostutellimuse rida.
3. Pange tähele, et saate luua reserveeringuid või kandeid registreeritud varude põhjal.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. Eeldatakse, et registreeritud kaubad on füüsiliselt lattu või varudesse saabunud ja seetõttu on need reserveerimiseks saadaval.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Ostutellimustel ei kajastate juriidilise isiku keelesätteid.

### <a name="issue-description"></a>Probleemi kirjeldus

Ostutellimusel kuvatakse toote nimi süsteemikeeles, mitte keeles, mis on määratud juriidilise isiku jaoks, kus ostutellimus loodi.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Seadke süsteemikeeleks *EN-US* (USA inglise keel).
1. Veenduge, et olemas oleks toode, mille nimi on tõlgitud keeltesse *EN-US* ja *DE* (saksa).
1. Muutke juriidilise isiku keeleks *DE*.
1. Looge toodet sisaldav ostutellimus juriidilises isikus, mille keeleks on määratud *DE*.
1. Pange tähele, et toote nimi kuvatakse ikka USA inglise keeles (süsteemikeeles).

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. Ostutellimuste puhul kuvatakse toode alati süsteemikeeles. Ostutellimuse keelt kasutatakse kinnitustöölehe loomisel.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Üksus „Kinnitatud hankijate loend toote põhjal” ei lase muuta jõustumiskuupäeva.

### <a name="issue-description"></a>Probleemi kirjeldus

Tootel on kinnitatud hankija, mille jõustumiskuupäev on näiteks 11. jaanuar 2018 (*01/11/2018*) ja aegumiskuupäev *Mitte kunagi*. Kui proovite muuta jõustumiskuupäevaks 10. jaanuari 2018 (*01/10/2018*) või 12. jaanuari 2018 (*01/12/2018*), kuvatakse järgmine tõrge.

> Kinnitatud tarnijate loendis (PdsApproveVendorList) ei saa kirjet luua. Väärtus „Aegumine” peab olema suurem kui väärtus „Jõustumine” või sellega võrdne.

### <a name="issue-resolution"></a>Probleemi lahendamine

Saate pikendada ainult perioodi, mille jooksul on hankija kinnitatud. Kehtivad järgnevad reeglid.

- Jõustumiskuupäeva muutmiseks nii, et see oleks varem kui ükskõik milline kauba hankija olemasolev kirje (periood), peab uue perioodi aegumiskuupäev olema enne kõiki olemasolevate kirjete aegumiskuupäevi.
- Aegumiskuupäeva muutmiseks nii, et see oleks hiljem kui mõni olemasolev periood, peab jõustumiskuupäev olema pärast mis tahes olemasoleva kirje hilisemat aegumiskuupäeva.
- Et vähendada tervet perioodi, mille jooksul on hankija kinnitatud, peate olemasolevad kirjed kustutama või neid muutma. Teise võimalusena saate kasutada importimise ajal **kärpimise** lülitit. See lüliti kustutab kõik tabelis „Kinnitatud hankijad kauba põhjal” olevad kirjed.

Probleemi kirjelduses kirjeldatud näidisstsenaariumi puhul, kus kirje jõustumiskuupäev on *01/11/2018* ja aegumiskuupäev *Mitte kunagi*, saate importida uue kirje, mille jõustumiskuupäev on *01/10/2018* ja aegumiskuupäev *Mitte kunagi*. Kuid te ei saa perioodi vähendada nii, et jõustumiskuupäev muudetaks andmehalduse kaudu kuupäevaks *01/12/2018*. Selle muudatuse peate tegema kasutajaliidese kaudu.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>Pärast tarneaadressi muutmist ostutellimuse päisel ei sünkroonita tarne nime.

### <a name="issue-description"></a>Probleemi kirjeldus

Ostutellimuse päises olev aadress muudetakse aadressiks, mis pole tarneaadress. Kuigi aadressi värskendatakse ostutellimusel, ei värskendata tarne nime värskendatud aadressi alusel.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. Valitud aadress tuleb märkida tarneaadressina. Muidu ei värskendata tarne nime valitud aadressi alusel.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kas ma saan otsida üles ostutellimuse tühistanud kasutaja?

Seda teavet jälgitakse ainult siis, kui ostutellimuse puhul kasutatakse muudatuste haldust. Kui kasutate muudatuste haldust, saate vaadata, kes esitas muudatuse (tühistamise) ja kes selle kinnitas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]