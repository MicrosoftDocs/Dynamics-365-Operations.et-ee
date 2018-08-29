---
title: Digitaalallkirjad
description: "Selles artiklis antakse ülevaade elektronallkirjadest ja kirjeldatakse nende kasutust Microsoft Dynamics 365 for Finance and Operationsis."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 374fd017a86fa7da6f78c287ba099d904cce64c4
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="electronic-signatures"></a>Digitaalallkirjad

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade elektronallkirjadest ja kirjeldatakse nende kasutust Microsoft Dynamics 365 for Finance and Operationsis.

<a name="what-is-an-electronic-signature"></a>Mis on elektronallkiri?
--------------------------------

Elektronallkiri kinnitab isiku, kes käivitab või kinnitab protsessi. Mõnes tööstuses on elektronallkiri juriidiliselt sama siduv kui käsitsi kirjutatud allkiri. 

Elektronallkirjad on määrustele vastavuse nõue mitmes reguleeritud tööstusharus, nt farmaatsia-, toiduainete- ja joogi-, ja lennundus ja kaitsetööstuses. Need on vajalikud ka vastavuse tagamiseks USA toiduainete ja -ravimiameti väljastatud määruste CFR-i 21. ptk osaga 11. 

**Märkus.** Elektrooniline allkiri pole sama mis digitaalallkiri. Elektrooniline allkiri asendab lihtsalt käsitsi kirjutatud allkirja, samal ajal, kui digitaalallkirjaga kaasnevad ka täiendavad turvameetmed. Digitaalallkirja abil saab tuvastada kas teine kasutaja või protsess on andmeid rikkunud. Digitaalallkirja saab ka kinnitada ja omanik, kellele andmete allkirjastamise sertifikaat kuulub, ei saa seda ümber lükata. Nagu allpool kirjeldatud, on Microsoft Dynamics 365 for Finance and Operationsi elektronallkirjadel sisseehitatud digitaalallkirja funktsioon.

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a>Elektronallkirjad Dynamics 365 for Finance and Operationsis
Finance and Operationsis saate kasutada tähtsateks äriprotsessideks elektronallkirju. Mõnedel protsessidel on sisseehitatud elektronallkirja võimalused. Igale andmebaasi tabelile või väljale saate luua ka allkirjanõuded. 

Elektronallkirjadel on sisseehitatud digitaalallkirja funktsioon. Iga dokumenti allkirjastav kasutaja peab hankima kehtiva krüptograafilise serdi. Dokumendi allkirjastamisel kinnitatakse sertifikaadiga seostuv privaatvõti. Finance and Operations salvestab elektronallkirja teabe kontrolljälje pakkumiseks logisse. Teavet elektrooniliste allkirjade seadistamise kohta vt teemast [Elektrooniliste allkirjade seadistamine (tegevuse juhis)](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Kasutajad, kes vajavad juurdepääsu elektronallkirjadele
Kolme tüüpi kasutajad vajavad tavaliselt turvapääsu digitaalallkirjadele: digitaalallkirja administraatorid, allkirjastajad ja digitaalallkirja audiitorid.

### <a name="electronic-signature-administrator"></a>Digitaalallkirja administraator

Elektroonilise allkirja administraator seadistab allkirjanõuded, üldised parameetrid ja kinnitajad ning saab allkirja kinnitamise nurjumisel märguandeid. Kasutajal, kes kuulub turberolli **Infotehnoloogiajuht**, on vaikimisi õigus elektronallkirju administreerida.

### <a name="signer"></a>Allkirjastaja

Allkirjastaja annab digitaalallkirjad nendele dokumentidele ja protsessidele, mis nõuavad allkirju. Kasutajal, kes kuulub turberolli **Süsteemi kasutaja**, on vaikimisi õigus dokumente elektrooniliselt allkirjastada. 

**Märkus.** Allkirjastaja võib vajada lisaõigusi, enne kui allkirjastatava dokumendi või protsessiga seotud andmetele antakse juurdepääs. Kasutaja, kes muudab andmeid ja peab seejärel need muudatused allkirjastama, peab omama andmete muutmise õigust. Kasutaja, kes allkirjastab teise kasutaja nimel, ei pruugi vajada andmetele juurdepääsu. Näiteks selline kasutaja on juhendaja, kes allkirjastab töötaja muudatusi.

### <a name="electronic-signature-auditor"></a>Digitaalallkirja audiitor

Elektronallkirja audiitor vaatab üle andmebaasilogi ja andmebaasis oleva allkirja ülevaatelogi. Kasutajal, kes kuulub turberolli **Infotehnoloogiajuht**, on vaikimisi õigus elektronallkirju kontrollida. 

Kui kasutate muud rolli kui **Infotehnoloogiajuht**, siis veenduge, et rollile oleksid määratud järgmised õigused.

-   Elektroonilise allkirja tõrgete kuvamine
-   Andmebaasilogi kuvamine

## <a name="signing-documents-electronically"></a>Dokumentide elektrooniline allkirjastamine
### <a name="get-a-certificate"></a>Sertifikaadi hankimine

Enne dokumentide elektroonilist allkirjastamist Finance and Operationsis peab taotlema serti. 

**Märkus.** Finance and Operations kasutab sertide loomiseks ja elektroonilise allkirjastamise võimaldamiseks Microsoft SQL Serveri funktsioone. Muid sertifikaate ega avaliku võtme infrastruktuure (PKI) pole vaja. 

Sertifikaadi taotlemisel luuakse teie jaoks rakenduse Finance and Operationsi andmebaasi avalik võti ja privaatvõti. Privaatvõti krüptitakse ainult teile teadaolevat parooli kasutades. Dokumendi elektroonsel allkirjastamisel kinnitatakse teie identiteet parooli sisestamisel. 

Serdi taotlemiseks klõpsake lehe **Suvandid** vahekaardil **Kontod** käsku **Hangi sert**. 

Peate sisestama ja kinnitama allkirjastamiseks kasutatava parooli. Parooli kasutatakse teie privaatvõtme kaitsmiseks ja sertifikaadi kasutamise volituseks. Parooli ei salvestata andmebaasis ja see ei ole teistele (isegi mitte Finance and Operationsi administraatorile) kättesaadav. 

Serdiga seotud parooli unustamisel peab serdi lähtestama. Serdi lähtestamine ei mõjuta dokumente, mille eelmise serdi abil allkirjastasite. Serdi lähtestamiseks klõpsake lehel **Suvandid** käsku **Lähtesta sert**.

### <a name="sign-a-document-electronically"></a>Dokumendi digitaalselt allkirjastamine

Vorm **Dokumendi allkirjastamine** kuvatakse siis, kui teete muudatuse, mis nõuab elektroonilist allkirja.

1.  Klõpsake lehel **Dokumendi allkirjastamine** vahekaarti **Dokument** dokumendi muudatuste ülevaatamiseks.
2.  Valige vahekaardilt **Allkiri** põhjusekood.
3.  Sisestage kommentaar, kui see on vajalik.
4.  Kui teie kasutaja ID-d väljal **Allkirjastaja** ei kuvata, siis valige see loendist.
5.  Sisestage oma asukoht, kui see teave on vajalik.
6.  Klõpsake nupul **OK**.

### <a name="sign-for-another-users-changes"></a>Teise kasutaja muudatuste allkirjastamine

Mõnikord on vaja kasutajal teise kasutaja muudatusi allkirjastada. Näiteks peab ülemus allkirjastama töötaja tehtud koosluse (BOM) muudatused. Kasutage seda protseduuri rakenduse Finance and Operations kasutaja määramiseks allkirjastajaks teise allkirjastaja asemel. 

**Märkus.** Kui üks kasutaja allkirjastab teise kasutaja muudatuse, peab muudatuse teinud kasutaja andma allkirja tööjaamas. Kasutaja ei saa muudatust salvestada enne, kui allkiri on antud. 

Kinnitajate määramiseks tehke järgmist.

1.  Klõpsake lehe **Suvandid** vahekaardil **Kontod** valikut **Määra kinnitaja**.
2.  Valige väljal **Kinnitaja kasutaja ID** selle kasutaja ID, kes peab teise kasutaja tehtud muudatuse allkirjastama.
3.  Valige väljal **Allkirjastatava kasutaja ID** selle kasutaja ID, kelle muudatustele peab alla kirjutama.





