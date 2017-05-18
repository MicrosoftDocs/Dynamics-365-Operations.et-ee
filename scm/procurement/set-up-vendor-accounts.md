---
title: Hankijakontode seadistamine
description: "See teema kirjeldab teabetüüpe, mida peate määrama, kui loote uue hankijakonto."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2f0ddf0e4cff0d799a7baf6bdc9d5c2da0622f4d
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-vendor-accounts"></a>Hankijakontode seadistamine

[!include[banner](../includes/banner.md)]


See teema kirjeldab teabetüüpe, mida peate määrama, kui loote uue hankijakonto.

Hankijakonto loomisel sisestate teabe hankija kohta. Seda teavet kasutatakse andmete automaatselt dokumentidesse sisestamiseks ja hankijaga seotud tegevuse jälgimiseks. Näiteks saate hankija kohta järgmist teavet konfigureerida.

-   Määrake hankijagrupp. Iga hankija tuleb määrata hankijagrupile. Hankijagrupis olevatel hankijatel on parameetrid, mida nad jagavad. Näiteks võivad neil olla samad maksetingimused.
-   Konfigureerige kataloogi impordi jaoks hankija. Hankijad saavad esitada faili, mis sisaldab nende kaupade ja teenuste kataloogi. Seda faili saab üles laadida, et teie töötajad saaksid tellida hankijalt.
-   Määrake hankija hankekategooriatele.
-   Lubage olemasoleval hankijal teha äri teiste organisatsiooni juriidiliste isikutega.
-   Pange hankija teatud tüüpi kannete jaoks ootele.
-   Seadistage hankija pangateave nii, et saate makseid elektrooniliselt saata.
-   Seadistage hankija maksu-, tarne-, arve- ja makseteave. Vaikimisi kopeeritakse need sätteid uutesse dokumentidesse, mida loote hankija jaoks.
-   Seadistage vaikimisi finantsdimensioonid, mida kasutatakse hankijaga kannete automaatseks sisestamiseks finantsaruannetesse.

Hankijakontode loomise protsessi kiirendamiseks saate luua mallid. Malli loomiseks klõpsake lehe **Hankija** tegumiribal valikuid **Suvandid** &gt; **Kirje teave**. Seejärel klõpsake valikut **Ettevõttekontode mall**. Ettevõttekontode malle jagatakse teiste kasutajatega.  

Samuti saate luua kasutaja malli endale kasutamiseks. Te ei saa kustutada muude kirjetega (nt kontaktid või tooted) seotud hankijat.

## <a name="vendor-account-numbers"></a>Hankijakonto numbrid
Kontonumber on hankija kordumatu identifikaator. Saate seadistada kontonumbrid nii, et need luuakse hankija loomisel automaatselt. Samuti saate konfigureerida numbriseeria, et kontonumbrid sisestataks käsitsi. Näiteks võite identifikaatorina kasutada hankija telefoninumbrit.

## <a name="vendor-organizations-and-individual-vendors"></a>Hankija organisatsioonid ja üksikud hankijad
Uue hankijakonto loomisel peate valima, kas hankija on organisatsioon või isik. Teie valik mõjutab teavet, mida peate hankija jaoks sisestama. Isiku puhul hõlmab see teave eesnime, perekonnanime ja ametinimetust. Organisatsiooni puhul hõlmab see teave organisatsiooni numbrit ja töötajate arvu.

## <a name="addresses"></a>Aadressid
Iga hankija puhul saate määratleda mitu aadressi, millest igaüht kasutatakse erinevatel otstarvetel. Näiteks saate luua aadressi, millel on **Arve** otstarve. Või kui maksate hankijale tšekke kasutades, saate seadistada aadressi, millel on valiku **Ülekande adressaat** otstarve. Kui peate määrama aadressi, mida kasutada raha ülekandmisel välispankadesse, siis on otstarve **SWIFT**.

## <a name="vendor-contacts"></a>Hankija kontaktid
Saate talletada hankija kontaktid. Neid kontakte saab seejärel kasutada dokumentidel, nagu ostutellimused või pakkumiskutsed (RFQ-d).  

Hankija kontaktide lisamiseks klõpsake lehe **Kõik hankijad** vahekaardi **Grupis** grupis **Seadistus** klõpsake valikuid **Kontaktid** &gt; **Lisa kontaktid**.  

Hankija kontaktid saate luua nullist. Teise võimalusena saate kopeerida üksikasjad ühelt isikult, kes juba on registreeritud Microsoft Dynamics 365 for Operationsis, ja redigeerida teavet vastavalt nõudmisele.  

**Märkus.** Hankija kontakti lisamine pole sama mis sellele hankijale kontaktiteabe lisamine. Kuigi võite lisada hankijale üldise kontaktiteabe, võib teil olla ka mitu teatud inimest, kes on selles ettevõttes kontaktid ja kellel kõigil on oma kontaktiteave.  

Te ei saa kustutada kontaktiisiku kirjet, kui kontaktidel on dokumendis viidatud. Selle asemel saate kontakti inaktiveerida.  

Rakenduses Microsoft Office 365 saate isiklikele kontaktidele hankija kontakte lisada. Peate esmalt Microsoft Exchange Serveri sünkroonimise ja Microsoft Outlooki seadistuse viisardis seadistama sünkroonimise rakenduste Dynamics 365 for Operations ja Office 365 vahel.

## <a name="vendors-in-different-legal-entities"></a>Hankijad erinevates juriidilistes isikutes
Kui hankija on registreeritud teie organisatsioonis ainult ühele juriidilisele isikule ja teised juriidilised isikud peavad registreerima sama hankija, saate kasutada lehte **Lisa hankija teise juriidilisse isikusse**, et konfigureerida hankija tegema äri teise juriidilise isikuga. Peate valima hankija grupi, valuuta ja hoidma hankija olekut valitud juriidilises isikus.  

Kui mitu juriidilist isikut teie organisatsioonis on ärisuhetes sama hankijaga ja iga juriidiline isik peab selle hankija kohta eraldi hankija kontot, saate ühendada hankijakontode osapoole ID-d. Sellisel juhul saab jagada teavet, nagu aadress ja töötajate arv, et peaksite seda värskendama ainult ühes kohas.  

Osapoole ID-de ühendamiseks toimige järgmiselt.

1.  Lehel **Globaalne aadressiraamat** valige aadressiraamatu kirjed, mis tähistavad hankijat igas juriidilises isikus, kes tuleks kaasata vastendamisesse.
2.  Tegumiribal klõpsake valikut **Kirjete ühendamine**.

## <a name="agreements"></a>Lepped
Kui seadistate hankijakonto, saate soovi korral registreerida ka hankijaga sõlmitud lepingud. Saate seadistada hinna ja allahindluse lepingud, kasutades hankija kirje tegevusi. Samuti saate seadistada ostulepingu lehel **Ostulepingud**.

## <a name="putting-a-vendor-on-hold"></a>Hankija ootele panemine
Saate panna hankija ootele erinevate kandetüüpide puhul. Valikud on järgmised:

-   **Ei** – hankijat pole pandud ootele.
-   **Arve** – hankijale ei saa ühtki arvet sisestada.
-   **Kõik** – hankija on ootel kõikide kandetüüpide puhul. Need kandetüübid hõlmavad ostutaotlusi, arveid ja makseid.
-   **Makse** – hankijale ei saa ühtki makset luua.
-   **Taotlus** – luua saab ainult ostutaotlusi. Ühtki muud kannet ei saa luua.
-   **Mitte kunagi** – hankijat ei panda passiivsuse tõttu ootele.

Kui panete hankija ootele, saate määrata ka põhjuse ja kuupäeva, millal ootelolek lõppeb Kui te ei sisestada lõppkuupäeva, siis kestab hankija ootelolek määramata ajani.

## <a name="vendor-invoice-account"></a>Hankija arvekonto
Kui rohkem kui ühel hankijal on sama arveaadress või kui hankijaga arveldatakse muu osapoole kaudu, saate hankija kirjele määrata arvekonto. Arvekonto on konto, millele krediteeritakse arve summa, kui loote ostutellimuse põhjal hankijaarve. Kui te ei sisesta hankija kirjele arvekontot, kasutatakse arvekontona hankijakontot.

## <a name="vendor-bank-accounts"></a>Hankija pangakontod
Kui peate tegema makseid hankija pangakontole, saate sisestada teabe hankija panga ja pangakontode kohta lehele **Hankija pangakontod**. Samuti saate sisestada teabe pangakonto kinnitamise ja maksete teabe kohta. Näiteks saate hankija pangakontodele lisada eelpäringud. Neid eelpäringuid saab kasutada kontoandmete täpsuse kontrollimiseks, nagu protsessikoodid ja kontonumbrid. Peate hankijale maksete jaoks vaikekonto määrama. Siiski kui teete tegeliku makse, saate muuta selle konto mõneks teiseks hankija kontoks.

## <a name="ledger-accounts"></a>Pearaamatukontod
Saate määrata vaikekontod, mis ilmuvad automaatselt hankija arve töölehtedel määratud hankija puhul. See funktsioon võib olla kasulik, kui maksate tavaliselt aja jooksul samade hankijate sama tüüpi kaupade või teenuste eest. Kui määrate vaikekonto, saate kiirelt ja tõhusalt arve töölehele töölehe sisestused sisestada. Teie määratud vaikekontosid ei kasutata ostutellimuste ega hankijaarvete puhul, mis on sisestatud lehele **Hankija arve**.  

Valite vaikekontod lehel **Kontode vaikeseadistus**, mille saate avada hankija kirje vahekaardilt **Arve**. Siin valitud kontod ilmuvad hankija konto filtreeritud kontode loendis töölehe kirje sisestamisel. Saate seadistada ühe konto vaikekontona.




