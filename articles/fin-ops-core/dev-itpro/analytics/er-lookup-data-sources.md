---
title: Konfigurace zdrojů dat vyhledávání pro použití parametrů specifických pro aplikace elektronického výkaznictví
description: V tomto tématu je vysvětleno, jak lze konfigurovat zdroje dat vyhledávání ve formátech elektronického vykazování (ER) pro použití parametrů specifických pro aplikaci ER.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 2849df85c37c4ed00754be91b9a9708db1bb16b7d0eb49d3a61d169037687196
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723182"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Konfigurace zdrojů dat vyhledávání pro použití parametrů specifických pro aplikace elektronického výkaznictví 

[!include[banner](../includes/banner.md)]

Funkce pro specifické parametry aplikace [elektronické výkaznictví (ER)](general-electronic-reporting.md) vám umožňují konfigurovat filtrování dat ve formátu ER tak, aby bylo založeno na sadě abstraktních pravidel. Tuto sadu pravidel lze nakonfigurovat tak, aby používala zdroje dat typu **Vyhledávání**, které jsou k dispozici ve formátu ER. Můžete pak specifikovat skutečná pravidla nad rámec návrhářů komponent ER pomocí uživatelského rozhraní (UI), které je generováno automaticky na základě nastavení zdroje dat **Vyhledávání** odpovídajícího formátu ER a aktuálních dat právnické osoby. Nakonec k zadaným pravidlům bude mít přístup zdroj dat **Vyhledávání** formátu ER při spuštění tohoto formátu ER.

> [!NOTE]
> Pomocí nakonfigurovaných zdrojů dat upravitelného formátu ER můžete určit, jaká data aplikace se použijí ke konfiguraci skutečných pravidel.

Použijte [Návrhář operací ER](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) k přenesení zdroje dat **Vyhledávání** do svého formátu ER. Zdroj dat musí být nakonfigurován tak, aby popisoval, jak vypadají vaše abstraktní pravidla, včetně následujících:

   - Sada parametrů určitého datového typu, jehož hodnota je poskytována k určení jediného pravidla.
   - Typ hodnoty určitého datového typu, který je vrácen jedním pravidlem, když je toto pravidlo považováno za nejvhodnější mezi jinými.

Můžete nakonfigurovat následující typy zdrojů dat **Vyhledávání** v závislosti na typu hodnoty, která je vrácena libovolným nakonfigurovaným pravidlem:

   - Použijte typ **Datový model\Vyhledávání**, když musí být vrácena hodnota výčtu modelu.
   - Použijte typ **Dynamics 365 Operations\vyhledávání**, když musí být vrácen hodnota výčtu aplikace nebo hodnota [rozšířeného datového typu](../extensibility/extensible-edts.md) aplikace.
   - Použijte typ **Výčet formátu\Vyhledávání**, když musí být vrácena hodnota výčtu formátu.

Následující obrázek ukazuje, jak lze konfigurovat výčet formátu ve vzorovém formátu ER.

   ![Zobrazení výčtu formátu jako základu pro nakonfigurovaný zdroj dat vyhledávání.](./media/er-lookup-data-sources-img1.gif)

Následující obrázek ukazuje komponenty formátu, které byly nakonfigurovány tak, aby vykazovaly různé typy daní v jiné části generované sestavy.

   ![Zobrazení sekcí formátu pro samostatné hlášení různých typů daní.](./media/er-lookup-data-sources-img2.png)

Následující obrázek ukazuje, jak návrhář operací ER umožňuje přidání zdroje dat typu **Výčet formátu\Vyhledávání**.  Přidaný zdroj dat je nakonfigurován jako vracející hodnotu výčtu formátu `List of taxation levels`.

   ![Přidání zdroje dat ER typu Výčet formátu\Vyhledávání.](./media/er-lookup-data-sources-img3.gif)

Následující obrázek ukazuje, jak je přidaný zdroj dat nakonfigurován pro použití pole **Kód** seznamu záznamů **Model.Data.Tax** zdroje dat **Model** jako parametru, který musí být zadán pro každé nakonfigurované pravidlo.

![Konfigurace parametrů přidaného zdroje dat typu Výčet formátu\Vyhledávání.](./media/er-lookup-data-sources-img4.gif)

Přidaný zdroj dat `Model.Data.Tax` je nakonfigurován tak, aby určoval daňový kód pro každé nakonfigurované pravidlo přístupem k záznamům tabulky aplikace **TaxTable**.

   ![Kontrola zdroje dat vyhledávání jedné firmy typu Výčet formátu\Vyhledávání.](./media/er-lookup-data-sources-img5.gif)

Pravidla vyhledávání pro vybraný formát ER můžete nastavit pomocí uživatelského rozhraní, které je automaticky v souladu se strukturou nakonfigurovaného zdroje dat. V současné době toto uživatelské rozhraní vyžaduje, abyste pro každé pravidlo zadali vrácenou hodnotu jako hodnotu výčtu formátu `List of taxation levels` a daňový kód jako parametr.

   ![Nastavte pravidla pro nakonfigurovaný zdroj dat.](./media/er-lookup-data-sources-img6.gif)

Následující obrázek ukazuje, jak lze zdroj dat `Model.Data.Summary.LevelByLookup` typu **Vypočítané pole** nakonfigurovat tak, aby volal nakonfigurovaný zdroj dat **Vyhledávání** poskytující požadované parametry. Ke zpracování tohoto volání za běhu, ER prochází seznam nakonfigurovaných pravidel v definované sekvenci a vyhledá první pravidlo, které splňuje zadané podmínky. V tomto příkladu je to pravidlo, které obsahuje daňový kód, který odpovídá uvedenému. Výsledkem je nalezení nejvhodnějšího pravidla a tento zdroj dat vrátí hodnotu výčtu, která je nakonfigurována pro nalezené pravidlo.

> [!NOTE]
> Pokud není nalezeno žádné použitelné pravidlo, je vyvolána výjimka. Chcete-li těmto výjimkám zabránit, nakonfigurujte na konci seznamu pravidel další pravidla pro zpracování případů, kdy je zadána nekonfigurovaná hodnota nebo žádná hodnota. Podle potřeby použijte možnosti **\*Není prázdné\*** a **\*Prázdné\***.  
>
> ![Přidejte zdroj dat pro volání nakonfigurovaného zdroje dat vyhledávání.](./media/er-lookup-data-sources-img7.png)

Když nastavíte možnost **Mezi firmami** na **Ano** pro upravitelný zdroj dat vyhledávání, přidáte nový požadovaný parametr **Firma** k sadě parametrů tohoto zdroje dat. Hodnota parametru **Společnost** musí být zadána za běhu, když je volán zdroj dat vyhledávání. Když je za běhu zadán kód společnosti, použijí se pravidla nakonfigurovaná pro tuto společnost k nalezení nejvhodnějšího pravidla a vrátí se odpovídající hodnota. Následující ilustrace ukazuje, jak to můžete udělat a jak se změní sada parametrů upravitelného zdroje dat.

   ![Kontrola zdroje dat vyhledávání mezi firmami typu Výčet formátu\Vyhledávání.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Vyberte každou společnost zvlášť a nakonfigurujte sadu pravidel pro tento zdroj dat vyhledávání upravitelného formátu ER. Výjimka je vyvolána za běhu, když je voláno vyhledávání mezi společnostmi s kódem společnosti, pro kterou nebylo nastavení vyhledávání dokončeno.
>
> Ujistěte se, že udělujete oprávnění uživateli, který spouští formát ER s mezipodnikovým zdrojem dat **Vyhledávání** pro přístup k datům každé společnosti, která je v rozsahu tohoto zdroje dat. Jinak je v době běhu vyvolána výjimka.

Od verze 10.0.19 jsou k dispozici rozšířené možnosti zdrojů dat **Vyhledávání**. Když nastavíte možnost **Rozšířené** na **Ano** pro upravitelný zdroj dat vyhledávání, je nakonfigurovaný zdroj dat vyhledávání transformován na strukturovaný zdroj dat, který nabízí další funkce pro analýzu nakonfigurované sady pravidel. Následující obrázek znázorňuje tuto transformaci.

   ![Kontrola strukturovaného zdroje dat vyhledávání typu Výčet formátu\Vyhledávání.](./media/er-lookup-data-sources-img9.gif)

- Podpoložka **Vyhledávání** je navržena jako funkce k nalezení nejvhodnějšího pravidla ze sady konfigurovatelných pravidel na základě poskytnuté sady parametrů.
- Podpoložka **IsLookupResultSet** je navržena jako funkce, která přijímá zadanou hodnotu základního výčtového zdroje dat a vrací *logickou* hodnotu **True**, když sada pravidel obsahuje alespoň jedno pravidlo, pro které byla zadaná hodnota výčtu nakonfigurována jako vrácená hodnota. Tato funkce vrací *logickou* hodnotu **False**, když nejsou nakonfigurována žádná pravidla pro vrácení poskytnuté hodnoty výčtu.
- Podpoložka **Nastavení** je navržena jako funkce, která vrací sadu nakonfigurovaných pravidel jako záznamy seznamu záznamů. Vrácené hodnoty a sada parametrů nakonfigurovaných pravidel jsou prezentovány v každém vráceném záznamu jako pole příslušných datových typů:

    - Vrácená hodnota je uvedena jako pole **Výsledek vyhledávání**.
    - Konfigurované parametry jsou prezentovány jako pole s názvy parametrů (pole **Kód** v tomto příkladu).

Další informace o tom, jak konfigurovat zdroj dat **Vyhledávání**, viz [Konfigurace formátů ER tak, aby používaly parametry, které jsou specifikovány pro každou právnickou osobu](er-app-specific-parameters-configure-format.md). Informace o tom, jak nastavit pravidla vyhledávání, najdete v části [Nastavení parametrů formátu ER na právnickou osobu](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Další prostředky

[Konfigurace formátů elektronického výkaznictví pro použití parametrů zadaných pro právnickou osobu](er-app-specific-parameters-configure-format.md)

[Nastavení parametrů formátu elektronického výkaznictví podle právnické osoby](er-app-specific-parameters-set-up.md)
