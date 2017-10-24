---
title: "Klienditellimuste ülevaade"
description: "See teema annab teavet klienditellimuste kohta uudses jaemüügikassas (MPOS). Klienditellimused on teise nimega eritellimused. Teema hõlmab arutelu seotud parameetrite ja kandevoogude kohta."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f68f9dce544256a2b1a9927f019a676a6845f46d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="customer-orders-overview"></a>Klienditellimuste ülevaade

[!include[banner](includes/banner.md)]


See teema annab teavet klienditellimuste kohta uudses jaemüügikassas (MPOS). Klienditellimused on teise nimega eritellimused. Teema hõlmab arutelu seotud parameetrite ja kandevoogude kohta.

Mitmekanalilises jaemüügimaailmas pakuvad paljud jaemüüjad mitmesuguste toote- ja täitmisnõuete täitmiseks klienditellimuste ehk eritellimuste võimalust. Tüüpilised stsenaariumid on näiteks järgmised.

-   Klient soovib tooted kohale toimetada kindlal kuupäeval kindlale aadressile.
-   Klient soovib tooted kätte saada teisest poest või asukohast kui see, kust ta tooted ostis.
-   Klient soovib, et tema ostetud tooted saab kätte keegi teine.

Jaemüüjad kasutavad klienditellimusi ka kaotatud müügi minimeerimiseks, mida laoseisak võib põhjustada, kuna kauba saab tarnida või kätte saada teisel ajal või teises kohas.

## <a name="set-up-customer-orders"></a>Klienditellimuste seadistamine
Lehel **Jaemüügi parameetrid** saate määrata muu hulgas järgmisi parameetreid klienditellimuste täitmisviisi määratlemiseks.

-   **Deposiidi vaikeprotsent** – saate määrata summa, mille klient peab enne tellimuse kinnitamist deposiidina tasuma. Deposiidi vaikesumma arvutatakse protsendina tellimuse väärtusest. Olenevalt õigustest võib poemüüja summa alistada, kasutades valikut **Deposiidi alistamine**.
-   **Tühistamistasu protsent** – saate määrata klienditellimuse tühistamisel rakendatava tasu summa.
-   **Tühistamistasu kood** – kui klienditellimuse tühistamisel rakendatakse tasu, kajastub see müügitellimusel tasukoodi all. Kasutage seda parameetrit tühistamistasu koodi määratlemiseks.
-   **Saatekulude kood** – jaemüüjad saavad määrata lisatasu kauba saatmiseks kliendile. Saatekulude summa kajastub müügitellimusel tasukoodi all. Kasutage seda parameetrit saatekulude koodi vastendamiseks klienditellimuse saatekuludega.
-   **Saatekulude tagasimakse** – saate määrata, kas klienditellimusega seostatud saatekulud on tagasi makstavad.
-   **Maksimaalne kinnitamata summa** – saate määrata saatekulude tagasimakse maksimaalse summa tagastustellimustele, kui saatekulud on tagasi makstavad. Selle summa ületamisel peab tagasimakse jätkamiseks tegema haldur alistamistoimingu. Järgmiste stsenaariumide võimaldamiseks võib saatekulude tagasimakse ületada algselt makstud summat.
    -   Tasud rakendatakse müügitellimuse päise tasemel ja tooterea osalise koguse tagastamisel ei saa toodete ja koguse puhul lubatud saatekulude maksimaalset tagasimakset määrata viisil, mis toimiks kõigi jaeklientide puhul.
    -   Saatekulud lisatakse igale saatmisele. Kui klient tagastab tooteid mitu korda ja jaemüüja poliitika määrab, et jaemüüja kannab saatekulude tagastamiskulu, on tagastatavad saatekulud suuremad kui tegelikud saatekulud.

## <a name="transaction-flow-for-customer-orders"></a>Klienditellimuste kannetevoog
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Klienditellimuse loomine uudses jaemüügikassas

1.  Lisage kandesse klient.
2.  Lisage tooted ostukorvi.
3.  Klõpsake valikut **Loo klienditellimus** ja seejärel valige tellimuse tüüp. Tellimuse tüüp võib olla kas **Klienditellimus** või **Pakkumine**.
4.  Klõpsake valikut **Saada valitud** või **Saada kõik**, et saata tooted kliendi kontol olevale aadressile ning määrake nõutud saatmiskuupäev ja saatekulud.
5.  Klõpsake valikut **Komplekteeri valitud** või **Komplekteeri kõik**, et valida tooted, mis komplekteeritakse praegusest poest või teisest poest kindlal kuupäeval.
6.  Koguge deposiidisumma, kui deposiit on nõutav.

### <a name="edit-an-existing-customer-order"></a>Olemasoleva klienditellimuse redigeerimine

1.  Klõpsake avalehel valikut **Leia tellimus**.
2.  Otsige üles ja valige redigeeritav tellimus. Klõpsake lehe alaservas valikut **Redigeeri**.

### <a name="pick-up-an-order"></a>Tellimuse komplekteerimine

1.  Klõpsake avalehel valikut **Leia tellimus**.
2.  Valige komplekteeritav tellimus. Klõpsake lehe alaservas valikut **Komplekteerimine ja pakkimine**.
3.  Klõpsake valikut **Komplekteeri**

### <a name="cancel-an-order"></a>Tellimuse tühistamine

1.  Klõpsake avalehel valikut **Leia tellimus**.
2.  Valige tühistatav tellimus. Klõpsake lehe alaservas valikut **Tühista**.

#### <a name="create-a-return-order"></a>Tagastustellimuse loomine

1.  Klõpsake avalehel valikut **Leia tellimus**.
2.  Valige tagastatav tellimus, valige tellimuse arve ja seejärel valige tagastatava kauba tooterida.
3.  Klõpsake lehe alaservas valikut **Tagasta tellimus**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Klienditellimuste asünkroonne kannetevoog
Klienditellimus saab luua kassa klientrakendusest kas sünkroonses režiimis või asünkroonses režiimis.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Klienditellimuste asünkroonses režiimis loomise lubamine

1.  Klõpsake valikuid **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiil** &gt; **Funktsiooniprofiilid**.
2.  Määrake kiirkaardil **Üldine** valiku **Klienditellimuse loomine asünkroonses režiimis** sätteks **Jah**.

Kui valiku **Klienditellimuse loomine asünkroonses režiimis** sätteks on valitud **Jah**, luuakse klienditellimused alati asünkroonses režiimis, isegi kui Retail Transaction Service (RTS) on saadaval. Kui määrate valiku sätteks **Ei**, luuakse klienditellimused alati sünkroonses režiimis, kasutades RTS-i. Kui klienditellimused luuakse asünkroonses režiimis, tõmmatakse ja sisestatakse need Retaili tõmbamise (P) töödena. Vastavad müügitellimused luuakse Retailis, kui käsk **Sünkrooni tellimused** käivitatakse käsitsi või pakktöötluse kaudu.

<a name="see-also"></a>Vt ka
--------

[Hübriid-klienditellimused](hybrid-customer-orders.md)




