---
title: Klientuuri ülevaade
description: Selles teemas antakse ülevaade kaupluse rakenduses saadaolevast uuest klientuurist.
author: bebeale
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 8f3135d0a34086b67c6e5ce11a5af47a51479c92
ms.sourcegitcommit: 8a14eac1c27f10c2b1b02ac9ad82339f5e127602
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2021
ms.locfileid: "5554990"
---
# <a name="clienteling-overview"></a>Kliendisuhtluse ülevaade

[!include [banner](includes/banner.md)]


Paljud jaemüüjad, eriti tipptasemel erialased jaemüüjad, soovivad, et nende müügi kaastöötajad moodustavad pikaajalisi suhteid oma põhiklientidega. Kaastöötajad peaksid teadma, mis nende klientidele meeldib ja ei meeldi, ostuajalugu, toote-eelistusi ja olulisi kuupäevi, nagu tähtpäevad ja sünnipäevad. Kaastöötajad vajavad kohta, kus nad saavad seda teavet jäädvustada ja seda vajaduse korral lihtsalt leida. Kui see teave on saadaval ühes vaates, saavad kaastöötajad kergesti suunata kliente, kes vastavad kindlatele kriteeriumitele. Näiteks võivad nad leida kõik kliendid, kes eelistavad osta käekotte, või kliendid, kellel on oluline sündmus lähenemas, nagu sünnipäev või aastapäev.

## <a name="client-book"></a>Kliendiraamat

Rakenduses Microsoft Dynamics 365 Commerce saavad jaemüüjad kasutada kliendi raamatu funktsioone, et aidata talletada partneritele pikaajalisi suhteid peamiste klientidega.

Kliendi raamat hõlmab kliendikaarte, mis näitavad iga kliendi kontaktandmeid koos kolme täiendava atribuudiga, mis on määratud jaemüüja poolt ja mis on konfigureeritud rakenduses Headquarters. Jaemüüjad saavad otsustada kolm kõige olulisemat asja, mida müügi kaastöötajad peaksid klientide kohta teadma. Näiteks ehete jaemüüja võib soovida kaasata olulisi kuupäevi, nagu tähtpäevad või sünnipäevad, sest need kuupäevad on juhud, kui inimesed võivad osta rohkem ehteid. Samuti võib moe-jaemüüja soovida kaasata kliendi eelistatud kaubanduskeskuste huvid ja kaubamärgid.

Kliendiraamat laseb ka müüdavatel sidusettevõtetel loendit filtreerida, nii et see näitab ainult kliente, kes vastavad kindlatele kriteeriumidele. Näiteks on poodi jõudnud uus kingade kollektsioon ning partner soovib teavitada kliente, kellele meeldib kingi osta. Sel juhul võib sidusettevõte kliendi raamatut filtreerida, et leida vastavaid kliente ja seejärel võtta täiendavaid meetmeid.

Kui mis tahes kliente ei peeta enam põhiklientideks mingil põhjusel ja seetõttu ei tohiks neid tähelepanelikult hallata, saavad müügipartnerid need oma kliendi raamatust eemaldada.

Mõned jaemüüjad ei soovi kliente hallata müügi sidusettevõtte tasemel. Selle asemel soovivad nad hallata kaupluse tasemel peamiste klientide loendit. Need jaemüüjad saavad vaadata kliente kaupluse kliendi raamatutest. Seda valikut kasutades saavad jaemüüjad vaadata kliendi raamatuid kõigi nende müügiesindajate kohta, mille aadressiraamat vastab praeguse kaupluse aadressiraamatule. Sel viisil, kui sidusettevõte töötab mitme juriidilise isiku kaupluses, näitab kliendi raamat kliente kõigist nende kauplustest. See funktsioon toetab lisafunktsioone. Näiteks saab kliente ühelt sidusettevõttelt teisele seostada. See võimalus on kasulik, kui kaastöötajad on üle kantud või ettevõttest lahkunud.

Igal müügiesindajal võib olla üks kliendi raamat juriidilise isiku kohta ja sidusettevõtted saavad lisada ühe või mitu klienti oma kliendi raamatusse. Commerce'is saab iga klienti praegu lisada ainult ühte kliendi raamatusse. Microsoft plaanib siiski lisada funktsioone, mis võimaldab ühe kliendi lisamist mitmesse kliendi raamatusse.

> [!NOTE]
> Erinevalt kliendi otsingust ei filtreeri kliendi raamat poe aadressiraamatute alusel kliendi kirjeid.

## <a name="activities-and-notes"></a>Tegevused ja märkused

Võrgus olevad kanalid annavad jaemüüjatele võimaluse saada teavet kliendi eelistuste kohta, nõudmata klientide selgesõnaliselt selle teabe esitamist. Seevastu, kui kliendid suhtlevad kaupluse sidusettevõtetega, jagavad nad selgesõnaliselt teavet oma eelistuste kohta. Kahjuks võib see teave kaotsi minna pärast müügi lõppu. Kuid kui see teave on salvestatud, võib see aidata jaemüüjatel paremini mõista kliente ja seeläbi aidata neil pakkuda paremaid soovitusi ja paremat üldist ostude kogemust.

Selleks et jäädvustada kriitilist teavet, mida kliendid jagavad, saavad müügiesindajad kasutada mitte ainult kliendi raamatu atribuute, vaid ka funktsiooni tegevusi ja märkmeid. Jaemüüjad saavad konfigureerida tegevuste tüüpe, nt teavet kaupluse külastuse, meiliaadressi, telefoninumbri ja kohtumiste kohta. Tegevusi, mida seostatakse loomisega, saab vaadata kassas (POS) ajaskaala vormingus. Neid saab vaadata ka vahekaardil **Tegevused** lehel **Kõik kliendid \> Üldine** rakenduses Headquarters.

Müügiesindajad saavad kasutada ka märkmeid, et jäädvustada üldise kliendi teavet, millele saab enne iga suhtlust viidata. Need märkmed salvestatakse rakendusse Headquarters ja neid saab vaadata kliendi profiilis või kõnekeskuse kliendi üksikasjade lehel.

> [!NOTE]
> Praegu saab kõiki märkmeid ja tegevusi vaadata mis tahes selle juriidilise isiku jaoks töötav müügiesindaja, kes saab vaadata kliendi üksikasjade lehti. Märkmed ja tegevused ei piirdu sidusettevõttega, kes lisas kliendi raamatusse.

## <a name="integration-with-dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights-iga integreerimine

Rakenduse Dynamics 365 Customer Insights abil saavad jaemüüjad koondada andmeid erinevatest süsteemidest, mida kliendid kasutavad jaemüüja kaubamärgiga suhtlemiseks. Seejärel saavad nad neid andmeid kasutada kliendi ühe vaate loomiseks ja nendest arusaamise tuletamiseks. Customer Insightsi integreerimine Commerce'iga laseb jaemüüjatel valida ühe või mitu meedet, mis tuleks kliendi kaardil kuvada kliendi raamatus. Näiteks saavad jaemüüjad kasutada Customer Insightsi andmeid, et arvutada kliendile „kloppimise tõenäosus” ja määratleda „järgmine parim tegevus”. Kui need väärtused on määratletud kui meetmed, saab neid kuvada kliendi kaardil ja see võib pakkuda olulist teavet müügiesindajate jaoks. Lisateavet Customer Insightsi kohta vt rakenduse [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview) dokumentatsioonist. Lisateavet meetmete kohta vt [Meetmed](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Seadista klientuur

Klientuuri funktsioonide sisselülitamiseks oma keskkonnas toimige järgmiselt.

1. **Funktsioonide halduse** tööruumis filtreerige funktsioone rakenduse **Retail and Commerce** moodulis.

    ![Klientuur Commerce'i mooduli funktsioonide loendis](./media/Enable_clienteling.png "Klientuur Retail and Commerce'i mooduli funktsioonide loendis")

2. Lülitage sisse **Klientuuri** funktsioon, valides **Luba kohe.**
3. Lehe **Commerce'i parameetrid** vahekaardil **Numbriseeria** valige rida **Kliendi raamatu ID**. Seejärel sisestage numbriseeria kood väljale **Numbriseeria kood**. Süsteem kasutab seda numbriseeriat, et määrata kliendi raamatutele ID.
4. Valige käsk **Salvesta**.
5. Looge uus atribuudirühm, mis sisaldab atribuute, mida soovite hõivata klientide jaoks, keda hallatakse kliendi raamatutes. Vaadake juhiseid jaotises [Atribuudid ja atribuudirühmad](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle).

    - Määratlege nõutavad atribuudid, **mida saab täpsustada**. Seejärel saavad müügiesindajad kasutada neid atribuute oma kliendi raamatu filtreerimiseks.
    - Seadistage nende atribuutide jaoks kuvatav tellimus. See kuvatav tellimus määratleb, millised atribuudid tuleb kliendi kaardil kuvada kliendi raamatus. 1. kuvatav tellimus on suurem kui 2. kuvatav tellimus. Seetõttu kuvatakse atribuut, millel on kuvatav tellimus 1, enne atribuuti, millel on kuvatud tellimus 2.

    > [!NOTE]
    > Saate teha Customer Insightsi kättesaadavaks samalt lehelt. Siiski tuleb luua Azure'i rakenduse ID ja saladus autentimise eesmärgil. (Lisateavet nõuete kohta leiate teema [Customer Insightsi integreerimine Commerce'iga](#turn-on-the-integration-of-customer-insights-with-commerce) hilisemast jaotisest.) Kui Customer Insights on sisse lülitatud ja te valite ühe või mitu meedet, mis tuleks kuvada kliendi kaardil, kuvatakse need meetmed esimesena. Seejärel kuvatakse kliendi raamatu atribuudi grupid, mis põhineb kuvatud tellimusel. Näiteks, kui valite Customer Insightsist kaks meedet, kuvatakse kliendi kaardil need kaks meedet ja üks kliendi raamatu atribuut. (Näidatud on kliendi raamatu atribuut, millel on kõrgeim kuvatav tellimus.)

6. Valige lehe **Commerce'i parameetrid** vahekaardi **Klientuur** väljal **Kliendi raamatu atribuudirühm** äsjaloodud atribuudirühm.

    ![Valitud kliendi raamatu atribuudirühm](./media/Client%20book%20attributes.png "Valitud kliendi raamatu atribuudirühm")

7. POS-is toimuvate tegevuste hõivamiseks määratlege tegevuse tüübid lehel **Tegevuse tüübid** (**Jaemüük ja kaubandus \> Kliendid \> Tegevuse tüübid**).

    > [!NOTE]
    > Tegevuste tüübid tõmmatakse Commerce Scale Uniti poolt, kui see teeb esimest korda reaalajas kõne. Pärast tegevuste tõmbamist salvestatakse need mõneks tunniks vahemällu. Kui muudate tegevuse tüüpe, oodake, kuni vahemälu enam ei kehti. Teise võimalusena, mitte-tootmiste keskkondades, taaskäivitage Commerce Scale Uniti teenus.

8. Lisage kaks nuppu vastavale POS-i ekraani paigutusele, et müügiesindajad saaksid vaadata oma kliendi raamatut ja kaupluse kliendi raamatut. (Kaupluse kliendi raamatute hulka kuuluvad kliendid kõigist kliendi raamatutest kõigi partneritega, kes jagavad aadressiraamatut kauplusega.) Vastavatele toimingutele on pandud nimeks **Klientide kuvamine kliendi raamatus** ja **Klientide kuvamine kaupluse kliendi raamatutest**. Saadaval on kolm lisatoimingut, mis on seotud kliendi raamatutega. Need toimingud määravad, millised kaastöötajad saavad kliendi raamatust kliente lisada, eemaldada ja uuesti määrata. Need on vastavalt nimega **Lisa klient kliendi raamatusse**, **Eemalda klient kliendi raamatust** ja **Määra kliendid teise kliendi raamatusse.**
9. Käivitage järgmised jaotuse graafiku tööd: 1040, 1150, 1110 ja 1090.

Kui olete selle protseduuri lõpetanud, saavad sidusettevõtted avada kliendi üksikasjade lehe kassas ja lisada kliendid oma kliendi raamatusse, vaadata ja jäädvustada klientide tegevusi ja märkmeid ning suunata kliente, kasutades kliendi ja kliendiraamatu atribuute, et filtreerida kliendiraamatut. Järgmisel joonisel on toodud kliendi raamatu näide.

![Kliendi raamatu näide](./media/client_book.png "Kliendi raamatu näide")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Customer Insightsi integreerimise sisselülitamine Commerce'iga

Customer Insightsi Commerce'iga integreerimise sisselülitamiseks peate veenduma, et teil on aktiivne Customer Insightsi eksemplar rentnikult, kus Commerce on ette valmistatud. Teil peab olema ka Azure Active Directory (Azure AD) kasutajakonto, millel on Azure'i tellimus.

Integratsiooni seadistamiseks läbige need etapid.

1. Registreerige Azure'i portaalis uus rakendus ja märkige rakenduse nimi, rakenduse ID ja saladus üles. Seda teavet kasutatakse teenusest teenusesse autentimiseks Commerce'i ja Customer Insightsi vahel. Märkige saladus kindlasti üles, kuna see tuleb võtmehoidlasse salvestada. Järgmise näite puhul kasutage rakenduse nime, rakenduse ID ja saladuse jaoks vastavalt parameetreid CI_Access_name, CI_Access_AppID, CI_Access_Secret. Lisateavet vaadake teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteedi platvormiga](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

    > [!IMPORTANT]
    > Tehke nii, et mäletaksite saladuse muutmist enne selle aegumist. Vastasel juhul peatub integratsioon ootamatult.

2. Avage oma Customer Insightsi eksemplar ja otsige üleval loodud rakenduse nime (selles näites CI_Access_name).
3. Looge Azure'i võtmehoidla ning märkige üles nimi ja URL (selles näites KeyVaultName, KeyVaultURL). Juhised leiate teemast [Lühijuhend: saate seada ja tuua saladuse Azure'i võtmehoidlast Azure'i portaali abil](https://docs.microsoft.com/azure/key-vault/quick-create-portal).
4. Salvestage saladus (selles näites CI_Access_Secret) hoidlasse. Kui saladus on hoidlasse salvestatud, määratakse saladusele nimi. Märkige saladuse nimi (selles näites SecretName) üles.
5. Azure'i võtmehoidla kaudu saladusele juurdepääsuks peate looma teise rakenduse ning määrama rakenduse ID ja saladuse (selles näites KeyVault_Access_AppID ja KeyVault_Access_Secret). Märkige saladus kindlasti üles, kuna seda ei kuvata enam.
6. Seejärel peate andma rakendusele load Commerce'i kaudu API-de abil võtmehoidlale juurdepääsuks. Avage Azure'i portaalis rakenduse leht. Tehke jaotises **Haldamine** valik **API load**. Andke juurdepääsuluba **Azure'i võtmehoidlale**. Selle loa jaoks valige **Juurdepääsupoliitika**. Valige mall **Saladuse haldus** ning valige suvandid **Hangi**, **Loend**, **Dekrüpti** ja **Krüpti**. 
5. Avage Commerce'i peakontoris **Süsteemihaldus \> Seadistus \> Võtmehoidla parameetrid** ja sisestage võtmehoidlale vajalik teave. Seejärel sisestage väljal **Võtmehoidla klient** rakenduse ID, mida kasutasite sammus 4, nii et Commerce pääseks ligi saladustele võtmehoidlas.
6. 1. etapis loodud rakenduse lisamiseks turvaliste rakenduste loendisse (nimetatakse mõnikord ka turvaliseks loendiks) avage Customer Insights ja valige rakenduse jaoks **kuvamisõigus**. Vaadake juhiseid jaotisest [Load](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions).
7. Värskendage Commerce'i peakontori (HQ) lehel jaotises **Süsteemihaldus > Seadistus > Võtmehoidla parameetrid** välju, nagu allpool kirjeldatud. 

- **Võtmehoidla URL**: KeyVaultURL (vt üleval 3. etappi).
- **Võtmehoidla klient**: KeyVault_Access_AppID (vt üleval 5. etappi).
- **Võtmehoidla saladuse võti**: KeyVault_Access_Secret (vt üleval 5. etappi).
- Tehke jaotises **Saladused** järgmised valikud.
    - **Nimi**: mis tahes nimi, nt CISecret.
    - **Kirjeldus**: mis tahes väärtus.
    - **Saladus**: **hoidla**://<Name of key vault>/<name of secret>> Selles näites on see vault://KeyVaultName/SecretName.

Pärast väljade värskendamist valige **Kinnita** ja veenduge, et rakendus Commerce pääseks saladusele juurde.

8. Määrake Commerce'i lehe **Commerce'i parameetrid** vahekaardi **Klientuur** kiirkaardil **Dynamics 365 Customer Insights** parameetri **Rakenduse ID** väärtuseks CI_Access_AppID (vt üleval 1. etappi). Valige väljal **Saladuse nimi** selle saladuse nimi, mis sisestati üleval 7. etapis (CISecret). Määrake suvand **Luba Customer Insights** valikule **Jah**. Kui seadistus mingil põhjusel ei õnnestu, kuvatakse tõrketeade ja selle suvandi väärtuseks määratakse **Ei**. 

Customer Insightsis võib olla mitu keskkonda, nagu katse- ja tootmisprotsess. Väljale **Keskkonna eksemplari ID** sisestage sobiv keskkond. Väljale **Alternatiivne kliendi ID** sisestage atribuut Customer Insightsis, mis on vastendatud kliendi konto numbriga. (Commerce'is on kliendi ID kliendi kontonumber.) Ülejäänud kolm atribuuti on meetmed, mis kuvatakse kliendi raamatus kliendikaardil. Kliendikaardi kuvamiseks saate valida kuni kolm meedet. Te ei pea siiski mingeid meetmeid valima. Nagu eelnevalt mainitud, näitab süsteem esmalt neid väärtusi ja seejärel kliendi raamatu atribuudigrupi väärtusi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
