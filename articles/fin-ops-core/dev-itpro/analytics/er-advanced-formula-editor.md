---
title: Elektroonilise aruandluse täiustatud valemiredaktor
description: See teema kirjeldab, kuidas täiustatud valemiredaktorit saab kasutada avaldiste konfigureerimiseks elektroonilise aruandluse (ER) mudeli vastendamise ja vormindamise komponentide jaoks.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: df402bc20753d2ba14295592f4b40e20f9fdc7bf
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138894"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Elektroonilise aruandluse täiustatud valemiredaktor

[!include [banner](../includes/banner.md)]

Lisaks [Elektroonilise aruandluse](general-electronic-reporting.md) [valemiredaktorile](general-electronic-reporting-formula-designer.md) saate täpsema elektroonilise aruandluse valemi redaktori abil parandada elektroonilise aruandluse (ER) avaldiste konfigureerimise kogemust. Täiustatud redaktor on brauseril põhinev ja seda kasutab [Monaco Editor](https://microsoft.github.io/monaco-editor). Selles teemas kirjeldatakse kõige sagedamini kasutatavaid täpsemaid redaktori funktsioone:

- [Koodi isevormindamine](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Koodi loomine](#CodeCompletion)
- [Koodis liikumine](#CodeNavigation)
- [Koodi struktureerimine](#CodeStructuring)
- [Otsi ja asenda](#FindAndReplace)
- [Andmete kleepimine](#DataPasting)
- [Süntaksi värving](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Täpsema valemiredaktori aktiveerimine</a>

Tehke järgmised sammud, et alustada oma Microsofti Dynamics 365 Finance eksemplaris täpsema valemiredaktori kasutamist.

1.  Avage **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2.  Valige lehe **Konfiguratsioonid**  vahekaardi **Konfiguratsioonid**  tegevuspaani rühma **Täpsemad sätted**  **Kasutaja parameetrid**.
3.  Seadke dialoogiboksi **Kasutaja parameetrid**  jaotise  **Käivitamise jälitus**  valiku **Luba täpsem valemiredaktor** parameetriks **Jah**.

[![ER-seadete leht](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Pange tähele, et see parameeter on kasutajakohane ja ettevõttekohane.

## <a name=""></a><a name="Autoformatting">Koodi isevormindamine</a>

Kui kirjutate mitut rida koodi sisaldava keeruka avaldise, on uue sisestatud rea taande aluseks eelmise rea taane. Saate valida read ja muuta nende taanet, vajutades klahvi **TAB** või klahvikombinatsiooni **SHIFT +TAB**.

[![ER valemiredaktor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Automaatvormindus võimaldab teil säilitada kogu avaldise hästi vormindatuna, et muuta edasine hooldus lihtsamaks ja lihtsustada konfigureerimise loogika mõistmist.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Redaktoris on sõnalõpetamise funtsioon, mis aitab teil avaldist kiiremini kirjutada ja vältida kirjavigu. Uue teksti lisamisel pakub redaktor automaatselt loendit funktsioonidest, mis esinevad teie sisestatud märkidega ER-funktsioonides. Saate käivitada IntelliSense'i ka konfigureeritud avaldise suvalises asukohas, vajutades **CTRL + tühik**.

[![ER valemiredaktor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Koodi lõpetamine</a>

Redaktor annab automaatselt koodi lõpetamise:

- lisades lõpusulu, kui sisestatakse algussulg, hoides kursorit sulgude sees.
- Teise ülakoma sisestamine, kui esimene on sisestatud, hoides kursorit ülakomade vahel.
- Teise jutumärgi sisestamine, kui esimene on sisestatud, hoides kursorit jutumärkide sees.

[![ER valemiredaktor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Kui osutate sisestatud sulule, tõstetakse selle paari teine sulg automaatselt esile, et näidata nende sees olevat vormelit.

## <a name=""></a><a name="CodeNavigation">Koodis liikumine</a>

Saate otsida oma avaldises sümboleid või ridu, tippides käsu **Mine** või kasutades käsupaletti või kontekstimenüüd.

Näiteks, et hüpata reale **8**, tehke järgmist:

- Vajutage **Ctrl + G** sisestage väärtus **8** ja vajutage seejärel sisestusklahvi **Enter**.

  - või -

- Vajutage klahvi **F1**, tippige **G**, valige **Mine reale** sisestage väärtus **8** vajutage sisestusklahvi (**Enter**).

[![ER valemiredaktor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Koodi struktureerimine</a>

Mõne funktsiooni, nt [IF](er-functions-logical-if.md) või [CASE](er-functions-logical-case.md) kood on automaatselt struktureeritud. Saate laiendada ja ahendada selle koodi kõiki ahendatavaid kohti, et vähendada avaldise redigeeritavat osa, et keskenduda ainult koodijupile, mis nõuab teie tähelepanu. Selle jaoks saab kasutada funktsiooni Lülita ahendamine/laiendamine käske.

Näiteks kõigi piirkondade ahendamiseks tehke järgmist:

- Vajutage **CTRL + K**

  - või -

- Vajutage klahvi **F1**, vajutage **FO**, valige **Ahenda kõik** ja seejärel vajutage sisestusklahvi **Enter**.

Kõigi piirkondade ahendamiseks tehke järgmist:

- Vajutage **CTRL + J**

  - või -
  
- Vajutage klahvi **F1**, tippige **UN**, valige **Laienda kõik** ja seejärel vajutage sisestusklahvi **Enter**.

[![ER valemiredaktor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Otsi ja asenda</a>

Teatud teksti otsimiseks valige oma avaldises tekst ja tehke järgmist:

- Vajutage **CTRL + F** ja vajutage seejärel **F3**, et leida valitud teksti järgmine esinemiskord või vajutage eelmise esinemiskorra leidmiseks klahvikombinatsiooni **SHIFT + F3**.

  - või -
  
- Vajutage klahvi **F1**, tippige **F** ja seejärel valige valitud teksti otsimiseks vajalik suvand.

Teatud teksti esinemiskordade asendamiseks valige oma avaldises tekst ja tehke järgmist:

- Vajutage **CTRL + H**. Sisestage asetekst ja valige asenduse suvand, et asendada valitud tekst või selle teksti kõik esinemisjuhud praeguses avaldises.

  - või -
  
- Vajutage klahvi **F1**, tippige **R** ja seejärel valige valitud teksti asendamiseks vajalik suvand. Sisestage asetekst ja valige asenduse suvand, et asendada valitud tekst või selle teksti kõik esinemisjuhud praeguses avaldises.

Teatud teksti kõigi esinemiskordade asendamiseks valige oma avaldises tekst ja tehke järgmist:

- Vajutage **CTRL + 2** ja sisestage seejärel alternatiivne tekst.

  - või -
  
- Vajutage klahvi **F1**, tippige **C** ja seejärel valige valitud teksti muutmiseks vajalik suvand. Sisestage alternatiivne tekst.

[![ER valemiredaktor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Andmeallikad ja funktsioonide kleepimine</a>

Saate valida **Lisa andmeallikas**, mis kleebib praegusele avaldisele andmeallika, mis on praegu valitud **Andmeallika** vasakul paanil. Samamoodi saate valida **Lisa funktsioon**, mis kleebib praegusele avaldisele funktsiooni, mis on praegu valitud **Funktsioonide** paremal paanil. Kui kasutate ER-i valemiredaktorit, kleebitakse valitud funktsioon või valitud andmeallikas alati konfigureeritud avaldise lõppu. Kui kasutate täiustatud ER-i valemiredaktorit, saab valitud funktsiooni või valitud andmeallika alati kleepida konfigureeritud avaldise mis tahes ossa. Peate kasutama kursorit, et määrata, kuhu soovite andmed kleepida.

[![ER valemiredaktor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Süntaksi värving</a>

Praegu kasutatakse erinevaid värve järgmiste avaldiste osade esiletõstmiseks:

- Kahekordsetes sulgudes olev tekst, mis võib tähistada teksti konstandi sildi ID-d.

[![ER valemiredaktor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)
- [Monaco redaktor](https://microsoft.github.io/monaco-editor)
