---
title: Import souborů v XML formátu s volitelnými atributy
description: Tento článek obsahuje informace o navrhování formátů elektronického výkaznictví, které určují atributy XML pro analýzu příchozích elektronických dokumentů ve formátu XML.
author: kfend
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: bd4e2d75a598dd36de8b2ce89e83789d87b3a72e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276619"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Import souborů v XML formátu s volitelnými atributy

[!include [banner](../includes/banner.md)]

Formáty elektronického výkaznictví můžete navrhovat pro analyzování příchozích dokumentů ve formátu XML. Některé atributy prvků XML lze zadat v navrženém formátu elektronického výkaznictví jako volitelné. To vám umožní zpracovat správně příchozí soubory s takovými atributy XML a bez nich. Poté můžete obsah z těchto souborů použít k aktualizaci dat aplikace.

Chcete-li získat další informace o této funkci, proveďte kroky v článku [(RCS) Import souborů v XML formátu s volitelnými atributy](tasks/import-files-xml-format-optional-attributes.md), které je součástí obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677). Tohoto průvodce záznamem úloh a přidružený vzorový soubor můžete stáhnout z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).


| Popis obsahu       | Soubor                                                         |
|---------------------------|--------------------------------------------------------------|
| Vzorový soubor ve formátu XML | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Průvodce úkolem                | RCS Import souborů v XML formátu s volitelnými atributy.axtr |


Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhovat konfiguraci elektronického výkaznictví pro import souborů v XML formátu obsahujícím volitelné atributy. K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md). Než začnete, stáhněte a uložte místně soubor IncomingDocumentToLearnHowToHandleOptionalAttributes.xml z Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684).

1. Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**.
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v článku [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Klikněte na **Konfigurace výkaznictví**.

## <a name="create-a-new-data-model-configuration"></a>Vytvoření nové konfigurace datového modelu
1. Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.
2. V poli **Název** zadejte Model pro import souboru xml.
3. Klepněte na možnost **Vytvořit konfiguraci**.
4. Klikněte na možnost **Návrhář**.
5. Kliknutím na možnost **Nový** otevřete dialogové okno.
6. Do pole **Název** zadejte Kořen.
7. Klikněte na tlačítko **Přidat**.
8. Kliknutím na možnost **Nový** otevřete dialogové okno.
9. Do pole **Název** zadejte Seznam.
10.    V poli **Typ položky** vyberte **Seznam záznamů**.
11.    Klikněte na tlačítko **Přidat**.
12.    Kliknutím na možnost **Nový** otevřete dialogové okno.
13.    Do pole **Název** zadejte Kód.
14.    V poli **Typ položky** vyberte **Řetězec**.
15.    Klikněte na tlačítko **Přidat**.
16.    Klikněte na možnost **Uložit**.
17.    Zavřete stránku.
18.    Klikněte na položku **Změnit stav**.
19.    Klikněte na **Dokončit**.
20.    Klikněte na tlačítko **OK**.

## <a name="create-a-format-for-data-import"></a>Vytvoření formátu pro import dat
1. Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.
2. V poli **Nový** zadejte Formát založený na datovém modelu Model pro import souboru xml.
3. V poli **Název** zadejte Formát pro import souboru xml. 
4. Vyberte možnost **Ano** v poli **Podporuje import dat**.
5. Klepněte na možnost **Vytvořit konfiguraci**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Návrh formátu pro analýzu příchozího souboru ve formátu XML
1. Klikněte na možnost **Návrhář**.
2. Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.
3. Ve stromovém zobrazení vyberte **XML\Element**.
4. Do pole **Název** zadejte kořen.
5. Klikněte na tlačítko **OK**.
6. Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.
7. Ve stromovém zobrazení vyberte **XML\Element**.
8. Do pole **Název** zadejte dokument.
9. V poli **Násobnost** vyberte **Jeden-n**.
10.    Klikněte na tlačítko **OK**.
11.    Ve stromovém zobrazení vyberte **root\document**.
12.    Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.
13.    Ve stromovém zobrazení vyberte **XML\Attribute**.
14.    Do pole **Název** zadejte id.
15.    Klikněte na tlačítko **OK**.
16.    Klikněte na možnost **Uložit**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Návrh mapování formátu pro uložení analyzovaných informací do datového modelu
1.    Klikněte na **Mapovat formát na model**.
2.    Klepněte na možnost **Nový**.
3.    V poli **Definice** zadejte nebo vyberte hodnotu.
4.    Do pole **Název** zadejte Mapování.
5.    Klikněte na možnost **Uložit**.
6.    Klikněte na možnost **Návrhář**.
7.    Ve stromové struktuře rozbalte **formát**.
8.    Ve stromovém zobrazení rozbalte **format\root: XML Element(root)**.
9.    Ve stromovém zobrazení vyberte **format\root: XML Element(root)\document: XML Element 1..* (document)**.
10.    Klikněte na **Vazba**.
11.    Ve stromovém zobrazení rozbalte **format\root: XML Element(root)\document: XML Element 1..* (document)**.
12.    Ve stromovém zobrazení vyberte **format\root: XML Element(root)\document: XML Element 1..* (document)\id**.
13.    Ve stromovém zobrazení rozbalte **List = format.root.document**.
14.    Ve stromovém zobrazení zvolte **List = format.root.document\Code**.
15.    Klikněte na **Vazba**.
16.    Klikněte na možnost **Uložit**.
17.    Zavřete stránku.

## <a name="run-format-mapping"></a>Spuštění mapování formátu
1. Klikněte na **Spustit**.
2. Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klikněte na tlačítko **OK**.

> [!NOTE]
> Vybraný soubor nebyl naimportován, protože návrh formátu předpokládá existenci atributu ID pro prvek ‘document’, ale importovaný soubor neobsahuje žádný takový atribut.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Upravení struktury formátu pro zpracování atributu XML jako volitelného
1. Zavřete stránku.
2. Ve stromovém zobrazení rozbalte **root\document**.
3. Ve stromovém zobrazení vyberte **root\document\id**.
4. V poli **Prázdný řetězec pro chybějící atribut** vyberte možnost **Ano**.
5. Klikněte na možnost **Uložit**.

## <a name="run-format-mapping-to-test-changes"></a>Spuštění mapování formátu pro testování změn
1. Klikněte na **Mapovat formát na model**.
2. Klikněte na **Spustit**.
3. Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klikněte na tlačítko **OK**.
5. Prohlédněte si vygenerovaný soubor. Všimněte si, že stejný soubor byl importován jako návrh formátu. V tomto okamžiku zvažte atribut ID pro prvek ‘document’ jako volitelný.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
