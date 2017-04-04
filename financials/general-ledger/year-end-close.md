---
title: "Aastalõpu sulgemine"
description: "Teema käsitleb Häälestuste ja pearaamatu aastalõpu Sule protsess kulgeb järgmiselt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Aastalõpu sulgemine

Teema käsitleb Häälestuste ja pearaamatu aastalõpu Sule protsess kulgeb järgmiselt. 

Majandusaasta lõpus käivitate aastalõpu kohtuasi üle uus süsteem uusaasta. Enamikus organisatsioonides kestab aastalõpu Sulge protsessi mitu korda. Esimest korda oleks saada liikus uuel saldod. Aasta lõpu lähedal siis käivitamist uuesti, kui tarvis, liikuda saldod reguleerimine kanded uuel mitu korda. 

Aasta jooksul sulgeda protsessi, on kahte tüüpi võimalik loodud kanded. Avamise kanne luuakse alati ja saab luua uus süsteem uuel. Avamist tehingu ilmneb bilanssi pearaamatu konto saldode uuel ja saldod kasumiaruanne pearaamatu konto saldode jaotamata kasum pearaamatukontol uuel aastal. Sulgemise kanne luuakse soovi tuua alla null sulgeda rahandusaasta tulude ja kulude kontode jääke.

## <a name="prepare-to-run-the-year-end-close"></a>Valmistada, käivitada, aasta lõpus sulgeda
Enne aastalõpu kohtuasi, kontrollida järgmisi sätteid: 

**Põhikonto** lehel

-   Kinnitada ka **Main liik** iga peamine konto on õigesti määratletud. Kas peamine konto saldo viiakse edasi nagu algsaldo või suletud arvesse jaotamata kasum avamise toimingu määramiseks kasutatakse Main konto tüüp.
-   Selle **avate konto** ülekandmiseks uus peamine konto saldo, mille peamine ajal aasta lõpu lähedal saate kasutada välja. Peamine konto on kantud ka **avate konto** välja. Tavaliselt seda kasutatakse peamiste bilansikontod peamine konto on aktiivne ja peamiseks kasutajaks on uuel.

Kohta ning **pearaamatu parameetrid** alla lehekülg **Rahandusaasta sulgemine**:

-   Selle **Kustuta sulgeda aasta tehingute** suvandi abil saate määrata, kas süsteemi loodud avamist tehingu lähedal eelmise aasta lõpus kustutatakse aasta lõpu lähedal töötab jälle. Kui see suvand on seatud **Jah**, eelmise avamine kannet kustutada ja uue avamist tehingu on loodud põhineb tasakaalu. Kui see suvand on seatud **nr**, eelmise avamine tehing jääb ja täiendavad avamise kanne luuakse liikuda saldod edasi kohandada pärast eelmise aasta lõpu lähedal sisestatud kanded.
-   Selle **Loo sulgemiskanded ülekandmisel** võtmega saab Loo sulgemiskanded tulu ja kulu kontode jääke viia nullini sulgeda rahandusaasta. Kui see suvand on seatud **Jah**, avamine tehingu ja sulgemiskanne on loodud. Kui see suvand on seatud **nr**, vaid avamise kanne luuakse järgmise finantsaasta üle saldod. Tulu ja kulu konto saldode jäävad majandusaasta lõpus.
-   On **seatud rahandusaasta olek jäädavalt suletud** võtmega saab jäädavalt suletud olekuks aasta määratud. Kasutage seda sätet ettevaatlikult, sest kõigi perioodide jäädavalt suletud olek ei saa uuesti, vältida muudatusi alates majandusaasta lähetamine. See on seda määrata **nr**.
-   Selle **kande number peab olema täidetud** võtmega saab määrata, kas kande number peab võtma aasta lõpus kohtuasi sõites. See on parim lahendus tuleb numbri, et tehingut avamine kergesti identifitseerida.

Kohta ning **finantskalender** leht:

-   Järgmisel eelarveaastal peab olemas olema enne aasta lõpus sulgeda. Järgmise rahandusaasta on vajalik luua algusest kaalud avamise perioodil.

Kohta ning **pearaamatu kalender** leht:

-   Valikuline: Iga eelarveperioodi sulgeda rahandusaasta võib viia **ootel** kantud uute tehingute vältimiseks. Korrigeerimine kanded on märgistatud, On registreeritud perioodide saab uuesti avada korrigeerimine kannete, isegi siis, kui aasta lõpus kohtuasi on juba käitatud.

## <a name="define-year-end-close-templates"></a>Saate määratleda aastalõpu tihedas
Pärast süsteemi konfigureerimist aastalõpu Sulge protsessi käivitamist. Kohta ning **aasta lõpus sulgeda** lehel malli saab määratleda puhul käitatakse mille aasta lõpus sulgeda protsessi õigussubjektide rühm. Malli konfigureeritava iga majandusaasta lõpus lähedal, kuid seda saab muuta kui ettevõtte muutudes. 

Esiteks määratleda selle **nimi** malli ja valida Finantsaasta kalendri. Rühma nimi tuleks lisada juriidiliste isikute grupi kood.  Näiteks malle võib seadistada põhinevad geograafilisel jaotusel, Põhja-Ameerika, EMEA juriidilised isikud, ja APAC juriidiliste isikute loodud eraldi gruppidega. 

Seejärel saab juriidiliste isikute lisada malli. Juriidiliste isikute saab lisada valides organisatsiooni hierarhia või valides juriidilised isikud. Organisatsiooni hierarhia valimisel lisatakse malli ainult juriidiliste isikute järjestuses, mis kasutavad valitud Finantsaasta kalendri. Kui juriidiliste isikute abil saate lisada malli, saab lisada ainult juriidilistest isikutest sama finantskalender. Sama finantskalender on vajalik, sest aasta lõpus lähedal töötab valides majandusaasta, millega saab muuta kalendris kalender. 

Kui juriidilised isikud on lisatud, saate määratleda iga juriidilise isiku jaotamata kasum keskne raamatupidamine. Selle **mullu lõppkuupäev sulgeda** välja uuendatakse iga kord aasta lõpu lähedal töötab puhul. 

Selle **rahalise küljega** vahekaardil saab määratleda, millised finantsdimensioonide kasutatakse avamist tehingu. On määravad sätted on seotud ainult juriidilise isiku valitud selle **juriidiliste isikute** võrku. Igal juriidilisel isikul ruudustiku kordub setup. 

Selle **kanda bilansi mõõdud** abil määratletakse, kas finantsdimensioonide kohta bilansi kontodel sisestatud säilitamise tehingut avamine. Tavaks on, seadke selle suvandi väärtuseks on **Jah**. Ning **üle kanda tulu ja kulu mõõdud** võimaldab määratleda, millised finantsdimensioonide sisestatud tulu ja kulu konto kantakse jaotamata kasum põhikonto. Kõigepealt Tuvastage seotud valitud juriidilise finantsdimensioonide. See hõlmaks mis tahes aasta jooksul sisestada finantsdimensioonide, isegi kui rahalise küljega ei kuulu aktiivse konto struktuur. Määratleda, kas igale **lähedased ühe** või **sulgege kõik**.  Vaikimisi on **sulgeda kõik**, mis säilitab esialgse rahalise küljega konteeritud kannetega väärtustab ja kasutab neid loomine avamine saldod jaotamata kasumi kontole. Iga unikaalne kombinatsioon rahalisi väärtusi luuakse eraldi jaotamata kasum algusest kaalud. Kui **lähedal ühe** on valitud, kõik kanded sisestatakse selle rahalise küljega kokku võtta jaotamata kasumi algsaldo pärast väljale dimensiooniväärtuse **lähedal ühe**. Näiteks Oletame, et kõik majandusaasta sisestamise konto struktuur Main konto - osakond. Mall, dimensiooni osakond rahalise **lähedal ühe** on valitud ja 100 on sisestatud väärtus. Kui kõik edastada ka 200, 300 ja 400 sisestatud kanded kogutulu on $100,000, luuakse üks algsaldo jaotamata kasum - 100. Kui valite **lähedal ühe** ja rahalisi väärtusi tühjaks jätta, kõik tehingud konteerib jaotamata kasum selle dimensiooniväärtusega tühi. 

Aasta lõpus Sule protsess ei täida konto struktuure. Seda sellepärast, et konto struktuure saab muuta kogu majandusaasta ja see ei ole alati võimalik kindlaks määrata asjakohased kontoplaani struktuuris muutumise tõttu.  Avamiskannete loomisel saldod viiakse edasi koos finantsdimensioonide aasta lõpuks Sule Mall määratletud. Algusest kaalud kanded saime finantsdimensioonide enam sellega Jooksevkonto struktuur ja segmendi kombinatsioonid kehtivusaeg Jooksevkonto struktuur. Kui teie organisatsioon soovib välistada rahalise küljega jaotamata tulu algsaldo, seadke rahalise küljega olevat **lähedal ühe** ja dimensiooniväärtuse tühjaks jätta.

## <a name="run-the-year-end-close-process"></a>Aasta lõpus Sule protsess käivitada
Aasta lõpus tihedas Mallid on loodud, aastalõpu kohtuasi algatatakse valides **käivitage rahandusaasta** Updatehagi paani. Vali kõik või osa õigussubjektide malli käitamise aasta lõpu lähedal. Kui töötab aasta lõpus sulgeda rahandusaasta esimest korda, siis tõenäoliselt valida luua algusest kaalud kõigil juriidilised isikud. Kui teil on aasta lõpus Sule uuesti, võite käivitada protsess vaid juriidiliste isikutega, mille korrigeerimine kanded konteeriti. 

Saate valida rahandusaasta, mida soovite käivitada aasta lõpuks kohtuasi vastu. Kui rohkem kui üks on olemas viimase perioodi aasta, selle **nimi** välja muutuvad kättesaadavaks, nii et valige suletud perioodi sulgemise tehingu, kui seadistus on määratletud sulgemise kande loomisel. 

Sisestage kande number, mis või ei tohi nõuda, sõltuvalt seadistusest üldiselt pearaamatu parameetrid. Sama kandenumbrit kasutatakse valitud aasta lõpuks kohtuasi juriidilised isikud. Kande number on loodud, kasutades numbriseeria. Isegi kui see ei ole vajalik on tavaks on sisestada numbri. Sisestage kande number on hõlpsam leida tehingut avamine uuel. Kui ei ole kande number, kande avamine kande tühjaks. 

Kui soovite muuta vastupidiseks valitud rahandusaasta eelmise aasta lõpu lähedal, **Undo eelmise lähedale** et **Jah**. Aasta lõpu lähedal vastupidiseks, kuid protsessi saab alati uuesti. Aasta lõpu lähedal, tühistamisel on **mullu lõppkuupäev sulgeda** ei ole saadaval. 

Aasta lõpus kohtuasi vaikeväärtus sõidetud kogumitena. See on hea tava kogumitena võimaldab kasutajal pöörduda muude tegevuste protsessi käivitamiseks. Kui aasta lõpuks kohtuasi on lõppenud, on **mullu lõppkuupäev sulgeda** on uuendatud istungi kuupäeva.

Lisateabe saamiseks vaadake [pearaamatu perioodi lõpus sulgeda](close-general-ledger-at-period-end.md).


